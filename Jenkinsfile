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
        httpRequest(url: 'https://testeqdepot.sugarondemand.com/rest/v10/Contacts?max_num=1', contentType: 'APPLICATION_JSON', httpMode: 'GET', consoleLogResponseBody: true, acceptType: 'APPLICATION_JSON', responseHandle: 'STRING', authentication: '0c8f5480-1bb7-47c2-b183-5089a0ae581f')
      }
    }

  }
}