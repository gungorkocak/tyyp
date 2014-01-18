# tyyp://

![A demonstrator shows love and support for TYYP during one of the recent protests in Istanbul](http://i.imgur.com/E38iED0.jpg) ![Analytics](https://ga-beacon.appspot.com/UA-46881978-1/tyyp?pixel) ![TYYP in the making...](http://i.imgur.com/vN6U1MG.jpg)

TYYP is an application level networking protocol for government controlled information systems, named after the notable 21st century villian Recep Tayyip Erdogan. TYYP was not started or is being coordinated by an open standards concorcium, because openness and freedom are oxymorons of the dictatorial values we commonly share and some of our design goals.

## Features and design goals

* Acts as a proxy between users and HTTP/HTTPs resources.
* Removes the bad side effects of HTTPs.
* Removes anonymity permanently. You can match any request with a subscriber. Good news is that your subsribers don't need to remember passwords anymore, your ISPs can automatically log your users into any website.
* Provides full functional parity with HTTP/HTTPs on the client level. It's perfectly backwards compatible, browsers don't need to support TYYP. Your users can keep continue to use fully open sourced browsers -- which is also a good selling point.
* All requests are logged and persisted at least for 2 years, you don't need to be in a hurry investigate the dirty laundry of your subscribers.
* Makes it possible to censor or block a certain path under a domain. It is such a huge improvement over blocking the entire host or the entire IP block. DNS block is so 2000s...
* Retrieve detailed metrics about the browsing trends in the large scale. You can monetize this information by selling it to marketing agencies.
* Easy to market to the clueless public as a product of safe browsing.
* Allows you to jail anyone by faking the records.
* Reminds you of Tayyip and the limitlessness of the evil.

## Milestones

* unSSL; implementing unSSL feature which enables to decrypt all encrypted packages and internet traffic ongoing. With this update, all kinds of user sensitive data and instant message traffic can be observed.



## Get started

To enable this technology, follow the steps:

* Create and sustain a dictatorial government or get in high power to make influence on legislative institutions. The seperation of powers should not be in the business anymore to make sure jurisdiction can't get against of the deployment and execution of this technology. Read recent history of the Middle East  for influnece and success stories in this area.
* Pass certain acts to force ISPs to discontinue support for HTTP/HTTPs. Deactivate provider licenses if they disagree. Make them forward all HTTP/HTTPs requests to TYYP.
* Use child porn or safe browsing needs as excuses. Know the point of failures of your society. If you're in Middle East, the first example may not work.

## Architecture
~~~
+--------+      +----------+      +-------+
| Host A | ---- | Router A | ---- |  ISP  | -- central pipe to the Internet -+|
+--------+      +----------+      +-------+                                   |
                                       +----------+       +-----------+       |
                                       |  Host B  | ----- |  Router B | ------+
                                       +----------+       +-----------+

~~~
1. Host A makes a TYYP request, request headers and body are parsed by the ISP and logged before any action is taken.
1. ISP resolves the IP address of the destination host. It's often asked whether there aren't any design flaws since we address no DNS issues. The DNS is not required for this system to work, but we allow clients to make DNS requests not the break the existing software, such as legacy browsers.
1. ISP decides whether the end destination is allowed to be visited or not. If it's a yes, we authenticate the user automatically (if required) and make an identical HTTP(s) request to Host B.
1. Host B responses.
1. ISP receives the packet, parses it, logs the headers and the body, and puts an entry to the user's scorecard according to the destination resource's content rating.
1. The response is returned to the source as a TYYP response.
