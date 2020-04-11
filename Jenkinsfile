pipeline {
   agent any

   stages {
      stage('build') {
         steps {
            echo 'build'
         }
      }
   }

   post {
   	always {
   		mail to: 'liruirui1992@126.com',
   			subject: "Status of pipeline: ${currentBuild.fullDisplayName}",
   			body: "${env.BUILD_URL} has result ${currentBuild.result}"
   	}
   }
}
