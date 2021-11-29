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
        sh '''   def get = new URL("https://rheem.sugarondemand.com/rest/v11_12/Emails/f7fc5448-4a72-11ec-9181-0682bc097fac").openConnection();
get.setRequestHeader("oauth-token","40d0cccd-6079-4b38-a390-ea4924dbaf3e")
def getRC = get.getResponseCode();
println(getRC);
if(getRC.equals(200)) {
    println(get.getInputStream().getText());
}
'''
      }
    }

  }
}