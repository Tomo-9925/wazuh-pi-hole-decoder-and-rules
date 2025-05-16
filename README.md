# Wazuh Synology DSM decoder and rules

Wazuh decoder and rule for pi-hole.log sent from Wazuh Agent.

## Important

- Decodes Pi-hole logs that are not in Syslog format as Syslog.
- DNSSEC rules have not been created.

## Installation

### Wazuh

1. Import decoder and rule from this repository.
2. Restart Wazuh Manager.

### Pi-hole Host

1. Install Wazuh Agent.
2. Set below config to `ossec.conf`.
3. Restart Wazuh Agent.

```xml
<localfile>
    <location>/var/log/pihole/pihole.log</location>
    <log_format>syslog</log_format>
</localfile>
```

## Reference

- [localfile - Local configuration (ossec.conf) · Wazuh documentation](https://documentation.wazuh.com/current/user-manual/reference/ossec-conf/localfile.html)
- [Pi-Hole Integration With Wazuh | PDF](https://www.scribd.com/document/765969006/Pi-hole-integration-with-wazuh)
