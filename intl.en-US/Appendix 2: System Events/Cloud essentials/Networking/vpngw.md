# vpngw

This topic describes the system events for VPN Gateway.

|Type|Event|Description|State|Level|
|----|-----|-----------|-----|-----|
|Exception|CertKeyExpired|The certificate expires.|Expire|Critical|
|StatusNotification|ipsec\_health\_check\_failed|The health check fails.|0|Warn|
|StatusNotification|ipsec\_health\_check\_success|The health check is successful.|1|Info|
|StatusNotification|ipsec\_phase1\_nego\_failed|The first phase of the Internet Protocol Security \(IPsec\) negotiation fails.|0|Warn|
|StatusNotification|ipsec\_phase1\_nego\_success|The first phase of the IPsec negotiation is successful.|1|Info|
|StatusNotification|ipsec\_phase2\_nego\_failed|The second phase of the IPsec negotiation fails.|0|Warn|
|StatusNotification|ipsec\_phase2\_nego\_success|The second phase of the IPsec negotiation is successful.|1|Info|

