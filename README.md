 
# About the SC4S  
In most cases this means a new SC4S filter must be developed. In this situation you can either build a filter or file an issue with the community to request help.


 SC4S can be used in production for a lot of data sources and new data sources are being added each day. Its a very well maintained product. You can deploy it in production. The only time I won't recommend SC4S is if you have like hundreds of custom data like application data you would like to onboard into splunk as syslog. You would end up writing parsers for all those manually in that case. Also remember its not a replacement for an intermediate forwarder i.e you can't accept data from a UF into sc4s and forward it to your indexer. For that you need to maintain an intermediate forwarder.


## Want to look at the raw message

Set the variable SC4S_SOURCE_STORE_RAWMSG=yes and look for the RAWMSG field in Splunk when a sample event is sent to SC4S. When you view the event in Splunk (which should have one of the two fallback sourcetypes – sc4s:fallback or nix:syslog) you will see other fields as well; these will be very useful when developing our log path.

## Develop log path

/opt/sc4s/local/config/log-paths

## Syslog-ng

Avoid UDP. syslog-ng will drop packets and doesn't multithread udp packets. TCP it can thread better.
