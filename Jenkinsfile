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
      def response =   httpRequest(url: 'https://testeqdepot.sugarondemand.com/rest/v10/Contacts?max_num=1', customHeaders: [[maskValue: false, name: 'oauth-token', value: '9195eb91-5025-40ac-afe5-832d65895cc3']], contentType: 'APPLICATION_JSON', httpMode: 'GET', acceptType: 'APPLICATION_FORM', responseHandle: 'STRING', authentication: 'CRMTOKEN')
         println("Status: "+response)
        
      }
    }

  }
}
