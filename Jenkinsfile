properties(
  [
    disableConcurrentBuilds(),
    [
      $class: 'ParametersDefinitionProperty',
      parameterDefinitions: [
        [
          name: 'CLUSTER_ID',
          description: 'OpenShift Dedicated Cluster Id',
          $class: 'hudson.model.StringParameterDefinition',
          defaultValue: ''
        ],
        [
          name: 'SKIP_STATUSPAGE',
          description: 'Do not create or complete statuspage banners during the course of this job',
          $class: 'hudson.model.BooleanParameterDefinition',
          defaultValue: false
        ],
        [
          name: 'SKIP_ZABBIX_ALERT_ON_FAILURE',
          description: 'Do not send failure metrics to zabbix to avoid creating PD alerts.' +
                      'You may use this when you are testing and do not wish to bother primary on-call with pages' +
                      ' related to this job failing.',
          $class: 'hudson.model.BooleanParameterDefinition',
          defaultValue: false
        ],
        [
          name: 'SKIP_RENEW',
          description: 'Do not renew certificate from Lets encrypt. This can be used if new certs already' +
                        ' exists in private repo and you only need to apply it to the cluster',
          $class: 'hudson.model.BooleanParameterDefinition',
          defaultValue: false
        ],
        [
          name: 'MOCK',
          description: 'Mock run to pickup new Jenkins parameters?',
          $class: 'hudson.model.BooleanParameterDefinition',
          defaultValue: false
        ],
      ]
    ],
  ]
)


timestamps {
 node('master') {
    checkout scm
    stage('Build') {
            cluster_name = params.CLUSTER_ID
            sh "echo hello ${CLUSTER_ID}"
    }
 }
}
