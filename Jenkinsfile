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
      def response =   httpRequest(url: 'https://testeqdepot.sugarondemand.com/rest/v10/Contacts?max_num=1', customHeaders: [[maskValue: false, name: 'oauth-token', value: 'b25eb700-4de4-4cf1-9aa7-8185a7e37e4f']], contentType: 'APPLICATION_JSON', httpMode: 'GET', acceptType: 'APPLICATION_FORM', responseHandle: 'STRING', authentication: 'CRMTOKEN')
         println("Status: "+response)
        
      }
    }

  }
}
