# Custom Filter or Parser for SC4S 

The SC4S Documentation isn't very helpful to be honest on this topic, but the SC4S github repo does, I learn how to write custom filter and parser for SC4S while reading the documentation and reading their code in their github repo. 

Refs: 
- https://splunk.github.io/splunk-connect-for-syslog/main/gettingstarted/create-parser/
- 

## How to create a Parser/Filter 

My Blog on  how to create a Parser and Filter, it will explain more about how to create it and what is my use case for the configuration 

https://zeroska.gitbook.io/zeroska/computer-and-technology/splunk-learning-experience/sc4s-custom-filter-for-windows-event-log-in-syslog-format


For using Xml parser

xml(
      prefix('.values.')
      template('t_msg_only')
      drop-invalid(yes)
);

I create a xml parser because I want to test whether the xml forward by NXLog any differ from using json and does it work automatically with Windows TA or CIM or not
because if you want to have the Splunk UF windows event log schema you must using NXLog Enterprise 
