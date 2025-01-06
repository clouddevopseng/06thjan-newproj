node {
stage('Download') {
        git branch: 'test', url: 'https://github.com/clouddevopseng/06thjan-newproj.git'
                  {
stage('Artifacts') {
        sh 'mvn package'
                   }
stage('Deployment') {
    deploy adapters: [tomcat9(credentialsId: '38c4c625-1cd6-4925-9c7e-c677d4d0b324', path: '', url: 'http://13.201.57.145:8080')], contextPath: '/test-apps', war: '**/*.war'
                    }
     }
