# Content Pack for Parsing Cisco Meraki syslogs

---

## Requirements

Uses Whois and Spamhaus DROP. Please make sure those Content Packs are installed and enabled.

## Includes

- Input (Raw/Plaintext UDP, port 1514)
- Streams (Stream for Input, and File Type Conversion)
- Pipleline Rules and Stages
- Lookup Tables, Data Adapters, and Data Cache
- Dashboard
- Event Definitions (WIP)

## Install Steps

Install this content pack like you would any other. You will need to manually save the csv files. Here are some commands to create the files, but you will need to copy/paste the information in. I have provided the csv's used. I set the lookup tables to reference /etc/graylog/files but feel free to modify to meet needs.

For Event Definitions, you will need to create your own notifications section, and modify the event definitions to send the appropriate notification but the event definitions themselves will exist. Since there are so many options I left it blank intentionally.

The "Meraki - UNIX Epoch Conversion with Timezone" and "Meraki - UNIX Event Timestamp Conversion with Timezone" will need to be edited to desired timezone. Change "America/Los_Angeles" as needed.

Run these commands to make the various files you will need. The contents of the files are available in this repo.

    sudo mkdir /etc/graylog/files
    sudo cd /etc/graylog/files
    sudo touch is_wpa.csv
    sudo touch fc_combined.csv
    sudo touch band.csv
    sudo touch reason.csv
    sudo touch icmp_type.csv
    sudo touch protocol.csv
    sudo touch radio.csv
    sudo touch snort_priority.csv

After creating the files, paste the contents of the associated csv to the correct file.

    sudo nano is_wpa.csv
    sudo nano fc_combined.csv
    sudo nano band.csv 
    sudo nano reason.csv
    sudo nano icmp_type.csv
    sudo nano protocol.csv
    sudo nano radio.csv
    sudo nano snort_priority.csv

## To do

- [ ] Add basic alerts (will require manual adding of notifications by end user)
- [ ] Enhance Dashboard
- [x] Convert fields to human readable where possible
