# Install Steps

Install this content pack like you would any other. You will need to manually save the csv files. Here are some commands to create the files, but you will need to copy/paste the information in. I have provided the csv's used. I set the lookup tables to reference /etc/graylog/files but feel free to modify to meet needs. There are probably better ways to do this but here is how I found. If you find any issues or recomendations let me know!

Some of these things can be done as a Decorator instead of a new field but I prefer to have a description field to pull from later as needed. Similar could be said for not parsing as a key=value initially but I found it to be more the same amount of work but with less precision and control. If any fields were missed I will make revisions to this content pack as needed.

    sudo mkdir /etc/graylog/files
    sudo cd /etc/graylog/files
    sudo touch syslog_severity_mapping.csv
    sudo touch is_wpa.csv
    sudo touch facility.csv
    sudo touch fc_combined.csv
    sudo touch band.csv

After creating the files, paste the contents of the associated csv to the correct file.

    sudo nano syslog_severity_mapping.csv
    sudo nano is_wpa.csv
    sudo nano facility.csv
    sudo nano fc_combined.csv
    sudo nano band.csv    

## To do

- [ ] Add basic alerts (will require manual adding of notifications by end user)
- [ ] Enhance Dashboard
- [x] Convert fields to human readable
