# Node Dependency Management

**TLDR:**

- In existing projects, only update packages if you encounter security issues/bugs or if you can expect a significant performance boost from more recent versions.
- Integrate audits in your build pipeline to get informed about security issues early.
- Optionally include automated solutions like Renovate Bot to get informed about new versions automatically
- Before you blindly update: check the contents of released packages and evaluate the changes.
- **As always:** a good code coverage with unit/integration tests will save you **a lot of time and headaches** when updating your dependencies.

## When to update?

There are three reasons why you would want to update a dependency on existing projects:

1.  security issues
2.  significant performance improvements
3.  bugfixes

If you currently don't experience any problems with your dependencies, save yourself the hassle, and **don't blindly update**.

You can automate the process of checking for problems with your dependencies by using Tools like Dependabot or Greenkeeper.

At Avenga projects can easily integrate a preinstalled version of Renovate Bot with gitlab.

### Security Issues

**How do I know if I might have vulnerable dependencies in my project?**

Both npm and yarn offer an easy way to check your application for known security issues:

[npm audit](https://docs.npmjs.com/cli/audit)
[yarn audit](https://legacy.yarnpkg.com/en/docs/cli/audit/)

Checking for vulnerabilities should be an automated part of your ci pipeline.

If you are building an application where security is a crucial concern, there are also some paid solutions like [snyk](https://snyk.io/plans/) or [probely](https://probely.com/pricing/) that offer more in-depth analysis, integrations and automated solutions.

### Significant performance improvements

If you update for performance reasons: **always measure!**

**Do not update blindly based on suggested performance increases you read on a blog or elsewhere! Always measure the impact on _your specific_ setup.**

## After installing new versions

**Verify that the new version didn't break anything!**

- run your tests locally
- do a quick manual test with your local dev-setup
- build/deploy the application to your staging environment and test manually. Deploy the changes in a separate branch to your staging environment if you can do so
- run end2end-tests if you have any

## Summary

- Does everything work as expected? Were no vulnerabilities found? Don't update anything. Do you have some spare time left? Better add some more tests or work on strategies to remove technical debt to increase the stability of your app.
- Did you find a problem with any of your dependencies? Check which version will resolve your issue with the least effort on your side and with a low probability of breaking anything. Be conscious about included changes and don't blindly update to the latest version available.
- After updating, test manually and run your test suites against your bundle to make sure everything works as expected.
- Use automated audits to get notified about vulnerable dependencies as early as possible.
