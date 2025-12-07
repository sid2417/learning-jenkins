## Jenkins Notes::


### disableConcurrentBuilds()

- Prevents multiple builds of the same job from running at the same time.
- Jenkins will not start a new build if the previous one is still running.
- New builds remain queued until the running build completes.


### ansiColor('xterm') 
- is a Jenkins Pipeline step used to enable colored console output in the      Jenkins job logs.