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

    stage('Call CRM') {
      steps {
        sh '''$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => \'https://rheem.sugarondemand.com/rest/v11_12/Emails/f7fc5448-4a72-11ec-9181-0682bc097fac\',
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => \'\',
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 0,
  CURLOPT_FOLLOWLOCATION => true,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => \'GET\',
  CURLOPT_HTTPHEADER => array(
    \'oauth-token: 91bc11e9-6ec1-4bfd-be9c-2024b371286e\'
  ),
));

$response = curl_exec($curl);

curl_close($curl);
echo $response;'''
      }
    }

  }
}