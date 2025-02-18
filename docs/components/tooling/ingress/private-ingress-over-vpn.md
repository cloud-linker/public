# Private Ingress Over VPN

By default, and for security measures, nobody is able to access a private domain, even over VPN.

To allow your team (and you) to visit internal services, you need to configure access permission in your VPN Provider.

You need to so this manually, so you are able to precisely give access to peoples or groups later depending on the service. You can expose privately parts of your product also, like an admin backoffice, only for employee that does Technical Support.

### Twingate

* Go to the Admin Console
* Go to the "Remote Network" tab
* Select the Remote Network where your Cluster is
* Add a new Resource with either :&#x20;
  * a static URL, for example : monitoring.internal.domain.com
  * or a wildcard, for example : \*.internal.domain.com
*
