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
![1](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

### Step 2. Setting up Adafruit IO

1. I created a new feed in "feeds" and named it "Garbage".

### Step 3. Setting up Zapier

1. I created a new zap and selected that I wanted to use Google Calendar as a trigger.
2. I chose "Event start" as my event and logged in to my Google account.
3. I chose my newly made calendar with the data of the garbage days.
4. Then I picked how much time before an event you want the light to be on. I picked 12 hours before so you can put the garbage outside the night before.
5. As "action" I searched and selected Adafruit IO and logged in.
6. As feed key I used a custom whith the name of my newly made feed in Adafruit IO.
7. As value I used "1. Event Begins (Pretty)".
8. When I tested my action I ran into a problem. Zapier couldn't recognize my feeds in my Adafruit account.
9. 

