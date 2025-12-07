## Jenkins Notes::


### disableConcurrentBuilds()

- Prevents multiple builds of the same job from running at the same time.
- Jenkins will not start a new build if the previous one is still running.
- New builds remain queued until the running build completes.


### ansiColor('xterm') 
- is a Jenkins Pipeline step used to enable colored console output in the      Jenkins job logs.

### webhook setting
- These setting in github repo
- Payload URL : https://3.239.1.2:8080/github-webhook/  
- ( / ending slash is mandatory)
- if you select Enable SSL verification : https://3.239.1.2:8080/github-webhook/
- if you Disable SSL verification : http://3.239.1.2:8080/github-webhook/
- Content type * : application/json
- Which events would you like to trigger this webhook? : Pushes