# CentOS Temperature Sensors

## CPU Temperature

### Install LM Sensors

`sudo yum install lm_sensors`

### Configure LM Sensors

`sudo sensors-detect`

Say YES to all prompts

### Get Current CPU Temperature

`sensors`

### Monitor CPU Temperatures

`watch sensors`

## HDD Temperature

### Install HDD Temp

`sudo yum install hddtemp`

### Get Current HDD Temperature

`hddtemp`
