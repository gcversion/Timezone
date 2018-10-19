# Timezone

Need to update few things here before running the code. For timezone details, we need to get API key from Google Maps (Time Zone API). Previously, it used to work without API key. But now, for more secure reasons they added this new behavior. 

How to get the API key?
In google maps, we need to create a new project & enable TimeZone API & Places API in order to get the new API key under Credentials tab. 

An example looks like (created a project for my testing): 
https://console.cloud.google.com/google/maps-apis/apis/timezone-backend.googleapis.com/credentials?project=wide-surge-219811&duration=PT1H


One API Key will work for one set of latitude, longitue, timestamp combinations. 
An example looks like:
https://maps.googleapis.com/maps/api/timezone/xml?location=-44.490947,171.220966&timestamp=1539920041&key=AIzaSyDckJf_hSJWzahzsnZLn8rrr_70m44iJis

Added "Input.csv" under src/main/resources in project. This contains input details given in the technical test. Along with timestamp, latitude, longitude, added the API key in Input.csv to get the timezone details as explained above. But, this api key may not be working because this is created under my own project (for testing purpose). Please create a valid & unique API Key for each set of data in Input.csv. Then, please run the application (TimezoneApplication.java). This will create a file called timezone.xml under src/main/resources in project which contains details about the timezone details (eg: Pacific/Auckland etc) and creates a file called Output.csv under src/main/resources in project. Output.csv will have timestamp, latitude, longitude, timezone id (eg: Pacific/Auckland or Australia/Sydney etc based on input data), Localized time. 

Please import the project to any IDE (Eclipse / RAD / STS / IntelliJIDEA), use Java 8. Make the API key changes as per the above & then run the application (TimezoneApplication.java) & expected output will be shown in Output.csv file. Please make sure TimeZone API key is valid & working before adding to Input.csv file.

Thank you
