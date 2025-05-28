pipeline
{
agent any
stages
  {
     stage("cont_downld")
     {
      steps
      {
       git branch: 'dev2', url: 'https://github.com/Akhilprakashm/newproject'
      }
     }
    stage("cont_build")
    {
     steps
    {
    sh 'mvn package'
    }
    }
    stage("cont_test")
    {
    steps
    {
      deploy adapters: [tomcat9(alternativeDeploymentContext: '', credentialsId: '8e450dea-8be1-4f3b-a969-b7116c4db32b', path: '', url: 'http://172.31.47.14:8080')], contextPath: 'multi2', war: '**/*.war'
    }
    }
  }
}
