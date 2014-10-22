ActiveMQ OpenShift Cartridge
============================

This cartridge will download ActiveMQ 5.10.0 and start it.

# Create the OpenShift Application

. Create a DIY application using this git repo as source code:
+
[source, text]
----
rhc app-create kaazing diy --from-code=git://github.com/arun-gupta/activemq-openshift-cartridge.git
----
+
. Create a port-forward from your local machine to your remote server
+
[source,text]
----
rhc port-forward activemq
Checking available ports ... done
Forwarding ports ...

To connect to a service running on OpenShift, use the Local address

Service Local                OpenShift
------- --------------- ---- -----------------
java    127.0.0.1:61222  =>  127.3.126.1:61222
java    127.0.0.1:61613  =>  127.3.126.1:61613
java    127.0.0.1:61616  =>  127.3.126.1:61616
java    127.0.0.1:61617  =>  127.3.126.1:61617
java    127.0.0.1:8000   =>  127.3.126.1:8000
java    127.0.0.1:8001   =>  127.3.126.1:8001
java    127.0.0.1:8161   =>  127.3.126.1:8161

Press CTRL-C to terminate port forwarding
----
