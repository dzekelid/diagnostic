---
swagger: "2.0"
x-collection-name: Google Beacons
x-complete: 0
info:
  title: Google Proximity Beacon API Get Diagnostics
  description: |-
    List the diagnostics for a single beacon. You can also list diagnostics for
    all the beacons owned by your Google Developers Console project by using
    the beacon name `beacons/-`.

    Authenticate using an [OAuth access token](https://developers.google.com/identity/protocols/OAuth2)
    from a signed-in user with **viewer**, **Is owner** or **Can edit**
    permissions in the Google Developers Console project.
  contact:
    name: Google
    url: https://google.com
  version: v1beta1
host: proximitybeacon.googleapis.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1beta1/{beaconName}/diagnostics:
    get:
      summary: Get Diagnostics
      description: |-
        List the diagnostics for a single beacon. You can also list diagnostics for
        all the beacons owned by your Google Developers Console project by using
        the beacon name `beacons/-`.

        Authenticate using an [OAuth access token](https://developers.google.com/identity/protocols/OAuth2)
        from a signed-in user with **viewer**, **Is owner** or **Can edit**
        permissions in the Google Developers Console project.
      operationId: proximitybeacon.beacons.diagnostics.list
      x-api-path-slug: v1beta1beaconnamediagnostics-get
      parameters:
      - in: query
        name: alertFilter
        description: Requests only beacons that have the given alert
      - in: path
        name: beaconName
        description: Beacon that the diagnostics are for
      - in: query
        name: pageSize
        description: Specifies the maximum number of results to return
      - in: query
        name: pageToken
        description: Requests results that occur after the `page_token`, obtained
          from theresponse to a previous request
      - in: query
        name: projectId
        description: Requests only diagnostic records for the given project id
      responses:
        200:
          description: OK
      tags:
      - Diagnostic
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