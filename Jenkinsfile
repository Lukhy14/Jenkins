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
        httpRequest(url: 'httpRequest acceptType: \'APPLICATION_JSON\', contentType: \'APPLICATION_JSON\', customHeaders: [[maskValue: false, name: \'oauth-token\', value: \'926139f5-13da-42ba-a069-f743060d2fb2\']], httpMode: \'POST\', responseHandle: \'NONE\', url: \'https://testeqdepot.sugarondemand.com/rest/v10/Contacts?max_num=1\', wrapAsMultipart: false', contentType: 'APPLICATION_JSON', httpMode: 'GET', acceptType: 'APPLICATION_FORM', responseHandle: 'STRING')
      }
    }

  }
}