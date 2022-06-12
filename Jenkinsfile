pipeline{
    agent any
    stages{
        stage('Maven Compile')
        {
            steps
            {
                withMaven(maven:'Maven_Local')
                sh 'mvn clean compile'
            }
        }
        stage('Maven test')
        {
            steps{
                withMaven(maven:'Maven_Local')
                sh 'mvn test'
            }
        }
        stage('Maven Deploy')
        {
          steps{
              withMaven(maven:'Maven_Local')
              sh 'mvn deploy'
          }
        }
    }
}
