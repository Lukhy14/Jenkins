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
        
        def response= httpRequest(url: 'https://testeqdepot.sugarondemand.com/rest/v10/Contacts?max_num=1', contentType: 'APPLICATION_JSON', httpMode: 'GET', customHeaders :'oauth-token:926139f5-13da-42ba-a069-f743060d2fb2',acceptType: 'APPLICATION_FORM', responseHandle: 'STRING')
        println("Status: "+response)
        
      }
    }

  }
}
