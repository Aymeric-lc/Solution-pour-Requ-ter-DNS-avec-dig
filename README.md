# Solution-pour-Requ-ter-DNS-avec-dig


La commande utilisée :  **dig A** www.wildcodeschool.com

;; ANSWER SECTION:
www.wildcodeschool.com.	72	IN	CNAME	2902314.group14.sites._hubspot.net._
2902314.group14.sites.hubspot.net. 72 IN CNAME	group14.sites._hscoscdn10.net._
group14.sites.hscoscdn10.net. 295 IN	A	_199.60.103.225_
group14.sites.hscoscdn10.net. 295 IN	A	_199.60.103.31_

**199.60.103.225** et **199.60.103.31** sont les **adresses Ipv4** du site de la **Wild Code Shool**
**Schoolhubspot.net** et **hscoscdn10.net** semblent être les **hébergeurs** du site de la **Wild Code School**

-----------------------------------------------------------------------

La commande utilisée : **dig AAAA odyssey.wildcodeschool.com**
;; QUESTION SECTION:
;odyssey.wildcodeschool.com.	IN	AAAA

;; ANSWER SECTION:
odyssey.wildcodeschool.com. 300	IN	CNAME	ghs._googlehosted.com._
ghs.googlehosted.com.	218	IN	AAAA	_2a00:1450:400c:c02::79_

**2a00:1450:400c:c02::79** est **l'adresse Ipv6** du site **odyssey.wildcodeschool.com**

**googlehosted.com** semble être l'**hébergeur** du site **odyssey.wildcodeschool.com**

-------------------------------

La commande utilisée : **dig NS wildcodeschool.com**
;; QUESTION SECTION:
;wildcodeschool.com.		IN	NS

;; ANSWER SECTION:
wildcodeschool.com.	86400	IN	NS	_kim.ns.cloudflare.com._
wildcodeschool.com.	86400	IN	NS	_cash.ns.cloudflare.com._

Les noms des **serveurs faisant autorité** sur le domaine wildcodeschool.com sont donc : **kim.ns.cloudflare.com et cash.ns.cloudflare.com**

----------------------------------------------

La commande utilisée : **dig SOA wildcodeschool.com**
;; QUESTION SECTION:
;wildcodeschool.com.		IN	SOA

;; ANSWER SECTION:
wildcodeschool.com.	1800	IN	SOA	_cash.ns.cloudflare.com_. dns.cloudflare.com. 2400969826 10000 2400 604800 1800

Le **serveur primaire** sur le domaine wildcodeschool.com est : **cash.ns.cloudflare.com.**

------------------------------------------------------------------

Pour finir j'ai fais le 2e bonus avec la cmd : **dig @9.9.9.9 A** www.wildcodeschool.com
Et je n'ai pas noté de grosse différence avec la cmd : **dig A** www.wildcodeschool.com
En dehors du server qui changeait d'identification de 127.0.0.53#53(127.0.0.53) à 9.9.9.9#53(9.9.9.9)
