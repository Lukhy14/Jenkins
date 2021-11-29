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

    stage('CRMTOKEN') {
      steps {
        httpRequest(url: 'https://testeqdepot.sugarondemand.com/rest/v11/oauth2/token?username=dm1&grant_type=password&client_id=sugar&password=Suavis*123&platform=apiCRM')
      }
    }
    
    stage('CRM') {
      steps {
        httpRequest(url: 'https://testeqdepot.sugarondemand.com/rest/v10/Contacts?max_num=1', contentType: 'APPLICATION_JSON', httpMode: 'GET', consoleLogResponseBody: true, acceptType: 'APPLICATION_JSON', responseHandle: 'STRING', authentication: 'CRMTOKEN')
      }
    }

    

  }
}
