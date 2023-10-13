pipeline{
    agent {label 'slave'}
    stages{
        stage('clone'){
            steps{
                git url:'https://github.com/kirtan8/new-java-prj-oct3.git',branch:'main'
            }
        }
    stage('build'){
            steps{
                sh 'mvn clean install'
            }
        }
    stage('diploy'){
            steps{
                sh 'cd target ; sudo cp *.war /home/ec2-user/apache-tomcat-10.1.14/webapps'
            }
        }
    }
}
