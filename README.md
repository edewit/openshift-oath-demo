## Openshift login
As a system user invoke:

```
  oc create -f <(echo '
  kind: OAuthClient      
  apiVersion: oauth.openshift.io/v1
  metadata:
    name: demo
  secret: demo
  redirectURIs:
    - "http://nodejs-rest-http-launcher.192.168.42.21.nip.io/"
  grantMethod: prompt
  ')     
```
