timestamps {
    node('master') {
        checkout scm
        stage('Build') {
            result = sh(returnStdout: true, script: """
                echo "line1"
                echo "line2"
                echo "line3"
                """)

        //  for (int i = 0; i < 4; i++) {
        //  	sh "echo hello ${i}"
        //  }
            strs = result.split('\n')
            for ( String str : strs ) {
                echo "a new line\n"
                echo str
            }
        }
    }
}
