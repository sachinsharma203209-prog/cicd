cicd refers continue integration and continue delivery and continue deployment it is automate the software deployment 
=> ci automate the build and testing and validate the code quality

=> cd refers to application ready to production deployment

 =>production deployment require the manual deployment
 => cdp automate the deployment the validate the deployment the changed
 In continue deployment without manaual approval cdp 
 and cd is automatically delivery the application is production ready in dev stage test 
 cdp is continue delivery in production require the approval


 advantage

 standardized the build test and deplploy the application workflow

 reduce the repettive enjinnering and opeation activity

 improved the scalibilty 


 stage of ci and cd

 1 fetch source code
   tools -github ,gitlab
   triggerd the code when dev to push and pr

2 build the application
  tools maven ,gradle
  compile java application artifact
  execute maven lifecycle

3 executed the automated the testing
  tools junit, testng
  Run unit test and integration testing
  stop the pipleline if failure

4 Run security and quality assurace
   tools sonarscanner , trivy
   execute the SAST  and the dependecy scanning
   enforce the quality gates

5 Build the continer image
  tools - docker
  package the application to image
   and tag the image for upload the registry

6  publish arifact and  container image
    tools - docker hub registry and ecr


7 deploy the application
  tools - k8s argocd, helm
  deploy the workload  onk8

8 execute the post deployment validation
   execute the heal


What is github action
github action is event driven  automation and orechestration platform for modern software delivery platform workflow 
 maintained by
 it is manged service by github provider

=========================================================================================

     Core  construct of github action
  

1 -   Workflow 
      Top level workflow define inside the github action\
      workflow triggered using githubaction event like push ,pull
      container one or more job and job have step
      stored under  .github/workflow  inside the repo

2 - job
     logical execution stages inside the workflow
     each job execute on independ runner(machine)
     job execute on paralled by default
     job execute also on sequential by need keyword
     inside the job have step execute the sequentially
  
3 - step
    small execution unit inside the github action
    execute the same runner env in sequential manner
    common used the run and use keyword


   ====================================================================
  

Type of runner


  Github hosted runner
  fresh tempory and disposable machine provided by each job
  no patching and maintaining the infra
  limited infra and network capability  will be customized
  example -ubuntu latest, window latest and macis latest


  Selfhost runner
  it managed by orgainisation and execute the job support privated network customization and env update example aws and k8







