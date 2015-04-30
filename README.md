# BMP085-mqtt

Requirements:  

1. Configure RaspberryPi with a BMP085 attached so that it publishes tempoerature and pressure values to mqtt (mosquitto running on a separate RaspberryPi)

2. Publish the data to mqtt topic rrd/srt and rrd/srp for temperature and pressure respectively
3. Publish using the retain mode so that last value is 'retained'. 
   Then any subscriber to the mqtt topic will see the last value published rather than all historical data.
4. Publish/update the data every 5 minutes using cron

Cron - Configure crontab using crontab -e - See txt file for the command line

Device Tree: /boot/config.txt has been updated on cctvpi to address introduction of the Device Tree

Test Plan:

On any system with mosquitto client installed, subscribe to topic rrd/srt# and rrd/srp#

Expected result:






