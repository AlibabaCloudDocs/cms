# ddosdip

This topic describes the system events for Anti-DDoS Premium.

|Type|Event|Description|State|Level|
|----|-----|-----------|-----|-----|
|Blackhole filtering|ddosdip\_event\_blackhole\_add|Blackhole filtering is triggered.|blackhole\_begin|Critical|
|Blackhole filtering|ddosdip\_event\_blackhole\_end|Blackhole filtering stops.|blackhole\_end|Critical|
|Traffic scrubbing|ddosdip\_event\_defense\_add|Traffic scrubbing is started.|defense\_begin|Critical|
|Traffic scrubbing|ddosdip\_event\_defense\_end|Traffic scrubbing stops.|defense\_end|Critical|
|DDoS attack|ddosbgp\_event\_blackhole|A blackhole event occurs.|blackhole|Critical|
|DDoS attack|ddosbgp\_event\_clean|A traffic scrubbing event occurs.|defense|Critical|

