pipeline {
  agent any
  stages {
    stage('Initialize') {
      steps {
        timestamps() {
          echo 'Hello'
        }

      }
    }

    stage('CRM') {
      steps {
        httpRequest(url: 'https://rheem.sugarondemand.com/rest/v11_12/Emails/f7fc5448-4a72-11ec-9181-0682bc097fac', contentType: 'application/json', httpMode: 'GET', consoleLogResponseBody: true, acceptType: 'application/json', responseHandle: 'application/json')
      }
    }

  }
}