1. Microservices [architecture patterns]
2. Move [to K8s]
3. Microservices and [API Gateways]

### What is an API Gateway
Here is a list of common concerns handled by API gateways:

- Authentication
- Transport security
- Load-balancing
- Request dispatching (including fault tolerance and service discovery)
- Dependency resolution
- Transport transformations
- Data aggregation

4. Netflix [Zuul and JWT integration]
5. Netflix Zull with [Rate Limit]
6. Using [spring boot containers]


## Kubernets
- Horizontal [Auto Scaling]
- Kong [on kubernetes]

## All About kong

Create a Rate limiting pluggin for Kong ingress:
```
apiVersion: configuration.konghq.com/v1
kind: KongPlugin
metadata:
  name: global-rate-limit
  labels:
    global: \"true\"
config:
  minute: 5
  policy: local
plugin: rate-limiting
```
[on Kubernetes]:<https://github.com/Kong/kubernetes-ingress-controller/blob/master/docs/guides/getting-started.md>

[Auto Scaling]:<https://www.youtube.com/watch?v=y9CYnjlWKok&t=370s>
[Rate Limit]:<https://www.baeldung.com/spring-cloud-zuul-rate-limit>
[Zuul and JWT integration]:<https://www.baeldung.com/spring-security-zuul-oauth-jwt>
[API Gateways]:<https://auth0.com/blog/an-introduction-to-microservices-part-2-API-gateway/>
[to K8s]:<https://www.appdynamics.com/blog/product/migrating-from-docker-compose-to-kubernetes/>
[architecture patterns]:<https://docs.microsoft.com/en-us/azure/architecture/patterns/>
[spring boot containers]:<https://spring.io/blog/2018/11/08/spring-boot-in-a-container>
