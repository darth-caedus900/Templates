# Graylog Clarificaitons

## Credits

### The Cisco Meraki Extractors

This extractor is based on [Graylog-Meraki-Content-Pack](https://github.com/ddbnl/Graylog-Meraki-Content-Pack?tab=MIT-1-ov-file). While I have made modifications and enhancements, the original work by [ddbnl](https://github.com/ddbnl) was instrumental in shaping this project.

---

### Cisco Meraki Content Pack

Please use updated content pack available here [Cisco-Meraki-Content-Pack-Manual-Field-Types](https://github.com/kbrown900/Templates/blob/main/graylog/cisco-meraki/Cisco-Meraki-Content-Pack.json). Removes need for manual field types.

The content pack requires a custom index and Field Profile type which cannot be exported at the time of writing this (3/21/25).
To get everything working correctly first follow these steps before import.

- 1 Create a new Field Type Profile in System > Indices > Field Type Profiles
- 2 Give it a name. For example "Meraki"
- 3 Setup the source mappings as follows

| Field Name                  | Field Type            |
| --------------------------- | --------------------- |
| meraki_dst_port             | Number                |
| meraki_syslog_priority      | Number                |
| meraki_action               | String (aggregatable) |
| meraki_translated_port      | Number                |
| meraki_ssid                 | String (aggregatable) |
| meraki_dhcp_lease_completed | Number                |
| meraki_protocol             | String (aggregatable) |
| meraki_vap                  | Number                |
| meraki_arp_src              | IP                    |
| meraki_auth_neg_dur         | Number                |
| meraki_src_mac              | String (aggregatable) |
| meraki_fc_subtype           | String (aggregatable) |
| meraki_client_mac           | String (aggregatable) |
| meraki_ip_src               | IP                    |
| meraki_channel              | Number                |
| meraki_src_port             | Number                |
| meraki_epoch                | String (aggregatable) |
| meraki_dst_mac              | String (aggregatable) |
| meraki_mac_address          | String (aggregatable) |
| meraki_syslog_ver           | Number                |
| meraki_radio                | Number                |
| meraki_dhcp_server_mac      | String (aggregatable) |
| meraki_arp_resp_time        | Number                |
| meraki_translated_src_ip    | IP                    |
| meraki_url                  | String (aggregatable) |
| meraki_pattern              | String (aggregatable) |
| meraki_fc_type              | String (aggregatable) |
| meraki_duration             | Number                |
| meraki_dns_server           | IP                    |
| meraki_dhcp_server          | IP                    |
| meraki_dns_req_rtt_time     | Number                |
| meraki_dhcp_ip              | IP                    |
| meraki_ip_resp_time         | Number                |
| meraki_agent                | String (aggregatable) |
| meraki_last_known_client_ip | IP                    |
| meraki_band                 | Number                |
| meraki_dns_resp_time        | Number                |
| meraki_host                 | String (aggregatable) |
| meraki_bssid                | String (aggregatable) |
| meraki_is_wpa               | Number                |
| meraki_full_conn_time       | Number                |
| meraki_src_ip               | IP                    |
| meraki_request              | String (aggregatable) |
| meraki_dhcp_resp_time       | Number                |
| meraki_rssi                 | Number                |
| meraki_category             | String (aggregatable) |
| meraki_da_vendor            | String (aggregatable) |
| meraki_last_auth_ago        | Number                |
| meraki_wireless_type        | String (aggregatable) |
| meraki_port                 | Number                |
| meraki_aid                  | Number                |
| meraki_dst_ip               | IP                    |

- 4 Create a new Index and attach the newly created Field Type Profile to it.
- 5 Import the Content Pack
