pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
            bat 'rmdir walmart-delivery-proc'
	    bat 'git clone -b master https://github.com/kumar-b-baibhav/walmart-delivery-proc.git walmart-delivery-proc'
      }
    }
    stage('Build') {
      steps {
            dir('.\\walmart-delivery-proc') {
                bat 'mvn clean package deploy -DskipMunitTests -DmuleDeploy -DmuleVersion=4.4.0 -DgrantType="client_credentials" -DclientId=5fe6d27bef4b440bb7472991e4546574 -DclientSecret=ad896cb0490a4c4296D5A5426A7A49E7 -DapplicationName=walmart-delivery-proc-api -Denvironment=Sandbox -DbusinessGroup="Apisero Inc" -DworkerType=MICRO '
			}
      }
    }
  }

}
