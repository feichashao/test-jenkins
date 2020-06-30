properties(
  [
    disableConcurrentBuilds(),
    [
      $class: 'ParametersDefinitionProperty',
      parameterDefinitions: [
        [
          name: 'NUMBER_TO_RENEW',
          description: 'How many clusters to renew in this batch',
          $class: 'hudson.model.StringParameterDefinition',
          defaultValue: '20'
        ]
      ]
    ]
  ]
)


timestamps {
    node('master') {
        checkout scm
        stage('Build') {
            sh(script: """
                echo "line1" >> output
                echo "line2" >> output
                echo "line3" >> output
                echo "line4" >> output
                echo "line5" >> output
                echo "line6" >> output
                echo "line7" >> output
                echo "line8" >> output
                echo "line9" >> output
                echo "line10" >> output
                echo "line12" >> output
                echo "line13" >> output
                echo "line14" >> output
                echo "line15" >> output
                echo "line16" >> output
                echo "line17" >> output
                echo "line18" >> output
                echo "line19" >> output
                echo "line20" >> output
                echo "line21" >> output
                echo "line22" >> output
                echo "line23" >> output
                echo "line24" >> output
                echo "line25" >> output
                echo "line26" >> output
                echo "line27" >> output
                echo "line28" >> output
                echo "line29" >> output
                """)

            result = sh(returnStdout: true, script: """
                head -n ${params.NUMBER_TO_RENEW} output
            """)

            strs = result.split('\n')
            for ( String str : strs ) {
                echo "-- a new line --\n"
                echo str
            }
        }
    }
}
