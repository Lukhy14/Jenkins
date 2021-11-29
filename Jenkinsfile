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
        httpRequest(url: 'https://testeqdepot.sugarondemand.com/rest/v10/Contacts?max_num=1', customHeaders: [[maskValue: false, name: 'oauth-token', value: 'cae7bf76-f87c-4fa3-9b22-acf4833f1cf1']], contentType: 'APPLICATION_JSON', httpMode: 'GET', acceptType: 'APPLICATION_FORM', responseHandle: 'NONE', outputFile: 'outputCRMResponse', validResponseCodes: '200')
     
      }
    }

  }
}
