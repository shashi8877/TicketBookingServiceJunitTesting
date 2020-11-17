pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
            //  bat "rmdir  /s /q TicketBookingServiceJunitTesting"
                sh "rm -f TicketBookingServiceJunitTesting"
                
               // bat "git clone https://github.com/kishancs2020/TicketBookingServiceJunitTesting.git"
                
             //  bat "git clone https://github.com/shashi8877/TicketBookingServiceJunitTesting.git"
                sh "git clone https://github.com/shashi8877/TicketBookingServiceJunitTesting.git"
            
              //  bat "mvn clean -f TicketBookingServiceJunitTesting"
                sh "mvn clean -f TicketBookingServiceJunitTesting"
            }
        }
        stage('install') {
            steps {
                //bat "mvn install -f TicketBookingServiceJunitTesting"
                sh "mvn install -f TicketBookingServiceJunitTesting"
            }
        }
        stage('test') {
            steps {
              ///  bat "mvn test -f TicketBookingServiceJunitTesting"
                 sh "mvn test -f TicketBookingServiceJunitTesting"
            }
        }
        stage('package') {
            steps {
             //   bat "mvn package -f TicketBookingServiceJunitTesting"
                sh "mvn package -f TicketBookingServiceJunitTesting"
            }
        }
    }
}
