# Install Steps

Install this content pack like you would any other. It should keep the mappings but I included them in this repo just in case they do not.
Modify the Lookup Data Adapters should something fail.

    sudo mkdir /etc/graylog/files
    sudo cd /etc/graylog/files
    sudo touch syslog_severity_mapping.csv
    sudo touch is_wpa.csv
    sudo touch facility.csv

After creating the files, paste the contents of the associated csv to the correct file.

    sudo nano syslog_severity_mapping.csv
    sudo nano is_wpa.csv
    sudo nano facility.csv

## To do

- [ ] Add basic alerts (will require manual adding of notifications by end user)
- [ ] Enhance Dashboard
- [ ] Convert fields to human readable
