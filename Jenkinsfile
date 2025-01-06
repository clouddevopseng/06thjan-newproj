node {
stage('Download') {
        git branch: 'dev', url: 'https://github.com/clouddevopseng/06thjan-newproj.git'
                  {
stage('Artifacts') {
        sh 'mvn package'
                   }
stage('Deployment') {
    deploy adapters: [tomcat9(credentialsId: '9f59547d-51d9-44b4-8f82-a9f74112209d', path: '', url: 'http://13.201.115.67:8080')], contextPath: '/dev-apps', war: '**/*.war'
                    }
     }
