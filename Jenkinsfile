podTemplate(yaml: '''
              apiVersion: v1
              kind: Pod
              spec:
                containers:
                - name: shell
                  image: ubuntu:latest
                  command:
                  - sleep
                  args:
                  - 99d
'''
  ) {

  node(POD_LABEL) {
    stage('Echo a message') {
      container('shell') {
        sh '''
          echo hello Jenkins!
        '''
      }
    }
  }
}
