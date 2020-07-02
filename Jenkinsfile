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
            try {
                build job: 'stdout', parameters: [[$class: 'StringParameterValue', name: 'NUMBER_TO_RENEW', value: "20"]]
            } catch (err) {
                echo "got error from build job"
            }
        }
    }
}
