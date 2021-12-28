pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
            dir('C:\\Users\\rasikananjikhane\\AnypointStudio\\studio-workspace\\walmart-delivery-partner1') {
                bat 'mvn clean package deploy -DskipMunitTests -DmuleDeploy -DmuleVersion=4.4.0 -DgrantType="client_credentials" -DclientId=5fe6d27bef4b440bb7472991e4546574 -DclientSecret=ad896cb0490a4c4296D5A5426A7A49E7 -DapplicationName=walmart-delivery-proc-api -Denvironment=Sandbox -DbusinessGroup="Apisero Inc" -DworkerType=MICRO '
			}
      }
    }
  }

}
