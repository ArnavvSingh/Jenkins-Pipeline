pipeline{
    agent any
    stages{
        stage("Stage 1"){
            steps{
                echo "Build the code using Maven to compile and package the code"
            }
        }
        stage("Stage 2"){
            steps{
                echo "Run unit tests with JUnit to ensure the code functions as expected and run integration tests using Citrus to ensure the different components of the application work together as expected"
            }
            post{
                success{
                    mail to: "arnavvsingh05@gmail.com",
                    subject: "Unit and Integration testing status email",
                    body: "Unit and Integration testing was sucessfull"
                }
                failure{
                    mail to: "arnavvsingh05@gmail.com",
                    subject: "Unit and Integration testing status email",
                    body: "Unit and Integration testing failed"
                }
            }
        }
        stage("Stage 3"){
            steps{
                echo "Use SonarQube to analyse code to make sure it meets industry standards"
            }
        }
        stage("Stage 4"){
            steps{
                echo "Perform a security scan using Nessus to identify any vulnerabilities"
            }
            post{
                success{
                    mail to: "arnavvsingh05@gmail.com",
                    subject: "Security scan status email",
                    body: "Unit and Integration testing was sucessfull"
                }
                failure{
                    mail to: "arnavvsingh05@gmail.com",
                    subject: "Security scan status email",
                    body: "Unit and Integration testing failed"
                }
            }
        }
        stage("Stage 5"){
            steps{
                echo "Deploy the application to staging server AWS EC2 instance"
            }
        }
        stage("Stage 6"){
            steps{
                echo "run integration tests on the staging environment to ensure the application functions as expected in a production-like environment"
            }
            post{
                success{
                    mail to: "arnavvsingh05@gmail.com",
                    subject: "Unit and Integration testing in production environment status",
                    body: "Unit and Integration testing was sucessfull"
                }
                failure{
                    mail to: "arnavvsingh05@gmail.com",
                     subject: "Unit and Integration testing in production environment status",
                    body: "Unit and Integration testing failed"
                }
            }
        }
        stage("Stage 7"){
            steps{
                echo "Deploy the application to production server AWS EC2 instance"
            }
        }
        
            
    }
}              
    



