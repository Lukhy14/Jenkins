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
        
       httpRequest(url: 'https://testeqdepot.sugarondemand.com/rest/v10/Contacts?max_num=1', contentType: 'APPLICATION_JSON', httpMode: 'GET',acceptType: 'APPLICATION_FORM', responseHandle: 'STRING')
       
        
      }
    }

  }
}
