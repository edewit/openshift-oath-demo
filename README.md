##Openshift login
As a system user invoke:

```
  oc create -f <(echo '
  kind: OAuthClient      
  apiVersion: oauth.openshift.io/v1
  metadata:
    name: demo
  secret: demo
  redirectURIs:
    - "http://nodejs-rest-http-launcher.192.168.42.21.nip.io/#access_token=VlU8rotZULYiVpAgZ7I6Et_A4WtuBciJm7NOGtGLWz8&expires_in=86400&scope=user%3Afull&token_type=Bearer"
  grantMethod: prompt
  ')     
```
