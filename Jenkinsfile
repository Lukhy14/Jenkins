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
        httpRequest(url: 'https://testeqdepot.sugarondemand.com/rest/v10/Accounts/07bf2308-8cc6-11eb-b01c-02857c81fa36?fields=id,name,date_modified,account_type,industry,annual_revenue,phone_fax,billing_address_street,billing_address_street_2,billing_address_street_3,billing_address_street_4,billing_address_city,billing_address_state,billing_address_postalcode,billing_address_country,phone_office,phone_alternate,parent_id,sic_code,parent_name,assigned_user_id,assigned_user_name,email1,website,acc_status_c,acc_address_type_c,acc_naics_c,acc_opco_c,assigned_user_sales_code_c,acc_ship_to_code_c,acc_customer_id_c', contentType: 'APPLICATION_JSON', httpMode: 'GET', consoleLogResponseBody: true, acceptType: 'APPLICATION_JSON', responseHandle: 'STRING', authentication: '926139f5-13da-42ba-a069-f743060d2fb2')
      }
    }

  }
}