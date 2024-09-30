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
- - in our pipeline, we can check if certain files were changed, and use it as a condition to trigger or skip the stage or a job.

### CI/CD Artifact storage optimization

Artifacts are very useful to keep files available after a pipeline reaches its end.

pipelines are run in a "fresh" enviroment each time, either in a shell executor or in a newly created container. This is very good to avoid a previous run changinh the state for the next run.

This also means that any file we want to have access to after the pipeline's runtime needs to be saved as an artifact.

It's important to only keep relevant artifacts, as to not use storage needlessly

It's also important to keep all the relevant artifact, as to not lose access to artifacts we still need.

### CI/CD Registry storage optimizations

GitLab CI gives us access to a custom container registry for each project, group and repository. This allows us to push and pull images, both manually and from our CI/CD pipelines.

This means we can use the registry to:

- host custom images needed during CI/CD.
- host custom images for release.
- host copies of official DockerHub images, but with custom tags.

out custom registry has limited storage, and to optimize it we should:

- use the smallest image possible (alpine ans slim tags are your friends)
- - use the smallest image possible as a base
- - use multi-stage builds to keep build tools and dependencies out of the final image.
- only keep relevant images and tags, clean up old uneeded ones (sheduled cleanup?)
