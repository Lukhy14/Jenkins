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
      def response =   httpRequest(url: 'https://testeqdepot.sugarondemand.com/rest/v10/Contacts?max_num=1', customHeaders: [[maskValue: false, name: 'oauth-token', value: 'e2a4f7d2-35b6-4848-b744-1e97f8a879a1']], contentType: 'APPLICATION_JSON', httpMode: 'GET', acceptType: 'APPLICATION_FORM', responseHandle: 'STRING', authentication: 'CRMTOKEN')
         println("Status: "+response)
        
      }
    }

  }
}
