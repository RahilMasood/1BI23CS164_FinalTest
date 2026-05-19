pipeline 
{
    agent any

    tools 
    {
        gradle 'Gradle'
        jdk 'jdk'
    }
    
    stages 
    {
        stage('Checkout') 
        {
            steps 
            {
                git branch: 'master', url: 'https://github.com/RahilMasood/1BI23CS164_FinalTest.git'
            }
        }

        stage('Build') 
        {
            steps 
            {
                sh 'gradle build'
            }
        }

        stage('Test') 
        {
            steps 
            {
                sh 'gradle test'
            }
        }

        stage('Run Application') 
        {
            steps 
            {
                sh 'gradle run'
            }
        }
    }

    post 
    {
        success 
        {
            echo 'Successful!'
        }
        
        failure 
        {
            echo 'Failed!'
        }
    }
}
