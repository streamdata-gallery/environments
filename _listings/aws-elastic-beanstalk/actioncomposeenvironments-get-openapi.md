---
swagger: "2.0"
x-collection-name: AWS Elastic Beanstalk
x-complete: 0
info:
  title: AWS Elastic Beanstalk API Compose Environments
  version: 1.0.0
  description: |-
    Create or update a group of environments that each run a separate component of a single
          application.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AbortEnvironmentUpdate:
    get:
      summary: Abort Environment Update
      description: |-
        Cancels in-progress environment configuration update or application version
              deployment.
      operationId: abortEnvironmentUpdate
      x-api-path-slug: actionabortenvironmentupdate-get
      parameters:
      - in: query
        name: EnvironmentId
        description: This specifies the ID of the environment with the in-progress
          update that you want to      cancel
        type: string
      - in: query
        name: EnvironmentName
        description: This specifies the name of the environment with the in-progress
          update that you want to      cancel
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments
  /?Action=ApplyEnvironmentManagedAction:
    get:
      summary: Apply Environment Managed Action
      description: Applies a scheduled managed action immediately.
      operationId: applyEnvironmentManagedAction
      x-api-path-slug: actionapplyenvironmentmanagedaction-get
      parameters:
      - in: query
        name: ActionId
        description: The action ID of the scheduled managed action to execute
        type: string
      - in: query
        name: EnvironmentId
        description: The environment ID of the target environment
        type: string
      - in: query
        name: EnvironmentName
        description: The name of the target environment
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments
  /?Action=ComposeEnvironments:
    get:
      summary: Compose Environments
      description: |-
        Create or update a group of environments that each run a separate component of a single
              application.
      operationId: composeEnvironments
      x-api-path-slug: actioncomposeenvironments-get
      parameters:
      - in: query
        name: ApplicationName
        description: The name of the application to which the specified source bundles
          belong
        type: string
      - in: query
        name: GroupName
        description: The name of the group to which the target environments belong
        type: string
      - in: query
        name: VersionLabels.member.N
        description: A list of version labels, specifying one or more application
          source bundles that belong      to the target application
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---