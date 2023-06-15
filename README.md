# NiFiTemplates

These are NiFi Sample Templates created as part of Learning
Has examples for Real Time API's

NiFi
Generated Username [56c08f3f-83c5-4854-aac2-6277913ff28d]
Generated Password [OHrvQSmGVi2mP8WZjHWjGukoMUSohdCW]

bin/nifi.sh status , stop , start

 https://localhost:8443/nifi


Nifi to Kafka
From Json use JasonPath to read json and set fileattribute
and use it as kafka message key


Wikipeida Edits
Http Invoke to read api
split json to get actual data
jolt transform to select fields
set key EvaluateJsonPath
Create avroSchemaRegestry

{
 "namespace": "nifi",
 "name": "wikipedia",
 "type": "record",
 "fields": [
 { "name": "type", "type": ["null","string"] },
  { "name": "ns", "type": ["null","int"] },
  { "name": "title", "type": ["null","string"] },
  { "name": "pageid", "type": ["null","int"] },
  { "name": "revid", "type": ["null","int"] },
  { "name": "old_revid", "type": ["null","int"] },
  { "name": "rcid", "type": ["null","int"] },
  { "name": "user", "type": ["null","string"] },
  { "name": "userid", "type": ["null","int"] },
  { "name": "bot", "type": ["null","string"] },
  { "name": "oldlen", "type": ["null","int"] },
  { "name": "newlen", "type": ["null","int"] },
  { "name": "timestamp", "type": ["null","string"]}
 ]
}

kafka-topics.sh --bootstrap-server localhost:9092 --delete --topic nifi-topic

kafka-topics.sh --bootstrap-server localhost:9092 --topic nifi-topic --create --partitions 1 --replication-factor 1

kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic nifi-topic



#WebHooks

##HBase Integation

create 'wikipedia''pageid' 'edit_info'
