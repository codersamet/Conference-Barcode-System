# Conference Barcode System

The application was developed for YIAMUN'19 conference. It was used to record the entrance and exit times of the participants of the conference, to verify while providing access to lunch and tickets.

## How is it works?

The working logic of the application, the application takes the barcode analysis using the built-in barcode reader program on your phone, verifies the data from google tables using the google script. And it gives feedback by sending toast messages via mobile application.

## Preparation

Create a google spreadsheet. 

Copy the file to the spreadsheet url.

Open yiamun19_barcode_system.aia file on MIT App Inventor website.

## Installation

Edit the code.

Add the link to the SpreadsheetApp.openByUrl section in the barcode.json file.

```
SpreadsheetApp.openByUrl(\"https://docs.google.com/spreadsheets/d/1eOyXeIaGwOxGXWs3o484TClMEtt1LSdAe4379b9nzVo/edit#gid\u003d111898187\");
```

Type the Excell page name in the getSheetbyname parameter.


```
ss.getSheetByName(\"barcode_system\");
```

You can read the data in your table with the getRange parameter.

```
sheet.getRange(2,1,sheet.getLastRow(),1).getValues();
```


Then upload Bar_Code.json to <a href="https://script.google.com/home/start">Google App Script</a>. 

And copy the share link. Open the file on the MIT app inventor.

In the code section, paste the link that you copied to the part with script url.

<img src="https://i.imgur.com/5FNBGpi.jpg" />


## Important notes

This app works through the barcode application installed on your phone.

## Usage

Download the androidapp file via MIT App inventor. And install it on your device.
You can customize it as you wish.

## Features

* Instant feedback
* No server costs
* records barcode read time
* barcode reader can be added for multiple events

## Author

* **Samet Zengin** - *Software Developer* - [Personal Website](https://sametzengin.com.tr)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details


