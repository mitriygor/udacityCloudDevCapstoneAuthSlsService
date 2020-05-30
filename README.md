## Auth0 Service
The service has been implemented in the scope of the https://github.com/mitriygor/udacityCloudDevCapstoneAuctionSlsApp

The service uses Auth0 and provides authorization functionality and could be used for cross-stack authorization

#### Example:

```yaml
functions:
  someFunction:
    handler: src/handlers/someFunction.handler
    events:
      - http:
          method: POST
          path: /something
          authorizer: arn:aws:lambda:#{AWS::Region}:#{AWS::AccountId}:function:sls-auth-service-draft-dev-auth
```
