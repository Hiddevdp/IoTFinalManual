# IoTFinalManual
Manual for my final assignment. The automatic garbage bin.

In this manual I will connect a google calendar with the arduino ESP8266. This will light up 12 hours before an event in the calendar, in this case when the garbage will be picked up.

##### Before you start
this are things you will need before you start the manual:

- Zapier account
- Google account
- Adafruit IO account
- Arduino IDE
- NodeMCU ESP8266

### Step 1. Setting up a calendar

1. I searched for the local calendar of the garbage pickup this was of [Alkmaar]( https://www.hvcgroep.nl/zelf-regelen/afvalkalender).
2. I created a new calendar in google using URL and import the data of the website I just found. This was explained on the website.
<p align="center">
<img src="https://github.com/Hiddevdp/IoTFinalManual/blob/main/1.jpg"  width="500" >
</p>

### Step 2. Setting up Adafruit IO

1. I created a new feed in "feeds" and named it "Garbage".

### Step 3. Setting up Zapier

1. I created a new zap and selected that I wanted to use Google Calendar as a trigger.
<p align="center">
<img src="https://github.com/Hiddevdp/IoTFinalManual/blob/main/2.jpg"  width="500" >
</p>
2. I chose "Event start" as my event and logged in to my Google account.
3. I chose my newly made calendar with the data of the garbage days.
4. Then I picked how much time before an event you want the light to be on. I picked 12 hours before so you can put the garbage outside the night before.
5. As "action" I searched and selected Adafruit IO and logged in.
6. As feed key I used a custom whith the name of my newly made feed in Adafruit IO.
7. As value I used "1. Event Begins (Pretty)".
8. <p align="center">
<img src="https://github.com/Hiddevdp/IoTFinalManual/blob/main/3.jpg"  width="500" >
</p>
9. When I tested my action I ran into a problem. Zapier couldn't recognize my feeds in my Adafruit account.
<p align="center">
<img src="https://github.com/Hiddevdp/IoTFinalManual/blob/main/4.jpg"  width="500" >
</p>
10. I've been trying to fix this for some hours now, but there is close to nothing on the internet about this problem. I found one forum where someone asked this and  he got one reply asking for more info wich was the only reply on the thread. The Zapier troubleshooter says:

> Your Zap is likely to be missing a required field, or a field value wasn't in a recognized format. For example, if a field in your action step is expecting an email > address, but the value given is a name, the app may return a 400 error.
> Check that your fields are correctly set up and mapped to each other.

Helaas ben ik er niet meer uit gekomen en ben ik tot de conclusie gekomen het hierbij te laten.

