# CI CD

## Continous Integretion

is the automation of tasks preparing our codebase for a code review or release. Some examples of tasks we might see in a CI pipeline:

- running automated unit tests.
- running automated integration tests.
- scanning our code/image for vulnerabilites.
- linting our code.
- validating our IaC.
- produce a report of planned changes on our IaC.

## Continous Delivery

is the automation of tasks delivering our next release. Some example of tasks we might see in a CD pipeline:

- compiling our code (possibly cross-compiling to different OSes and architectures).
- building a container image and pushing it to a registry.
- compiling other artifact needed for release.
- migrating database (update).

## Continous Deployment

is the automation of our deployments, where our newest release lands in production (or any other enviroment we might have set up, such as a staging env for a side branch[merge]).


# CI/CD Optimization

### runtime optimization

- identyfy the steps that take long time, and are potentially repeated accross stages/jobs.
- We'll then need to "cache" these stages somehow, so that we can save some time.
- Or run jobs in a custom image that already has all dependencies installed.

- Another way save runtime on our CI is to not run stages and jobs when they're not needed.

