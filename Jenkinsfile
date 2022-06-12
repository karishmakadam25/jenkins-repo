pipeline{
    agent any
    stages{
        stage('Compile stage')
        {
            steps
            {
                withMaven(maven:'Maven_Local')
                sh 'mvn clean compile'
            }
        }
        stage('Testing Stage')
        {
            steps{
                withMaven(maven:'Maven_Local')
                sh 'mvn test'
            }
        }
        stage('Deployment Stage')
        {
          steps{
              withMaven(maven:'Maven_Local')
              sh 'mvn deploy'
          }
        }
    }
}
