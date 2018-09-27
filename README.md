### **What does this doo**

The main usage of this script is to color whispers received and sent with colors of choice through an easy to use configurable file.

In addition to that, it's meant to bring some extra customization such as, switching the message color of a specific character(or group of characters) name...And that's the only extra thing pretty much.

(If you randomly came accross this respository do search "tera proxy" as the script it's meant to be run on it).

![Sample](imgs/sample.png)

#### Usage/Customizing with the script

Here i'll explain how to edit the settings file *`settings.js`*. Most of it, it's pretty self explanatory(no, seriously, ignore it if you have basic knowledge). Futhermore into that, the script has in game accesible commands(that will be explained way below) to control some of the attributes however do note that changes made through them won't be saved when restarting!(Because i'm lazy).

```json
{
  "globallyEnabled": true, // Enables and disables the whole script from coloring any whisper(true, false).
  "me": { // Identifier for the user whispers(Yours).
    "enabled": true, // Enabled/disabled(true, false).
    "color": "#3399FF" // Hex color of choice.
  },
  "others": {
    "enabled": true, // (true, false) 
    "color": "#e82121" // Hex color.
  },
  "particular": { // Identifier for whispers of char names we want to give a particular message color.
    "enabled": false,
    "characters": [ // Each name and color enclosed by { } contains the used data. You can add as many as you need, don't break the format.
      {
        "name": "singleNameExample", // If you're modifying just one name, use this type of syntax.
        "color": "#hexcolorhere"
      },
      {
        "name": ["Array", "Of", "Names", "Example"], // If you're modifying a group of chars whispers messages with a color of choice, use this syntax.
        "color": "#hexcolorhere"
      }
    ]
  }
}
```
*What the heck is hex color tho??*: https://www.hexcolortool.com/


#### In-game Commands

* ***`cw`***  *`[on/off]`* turns on and off the whole module functionalities. Simple.
######
* ***`cw`*** *`[me/others/particular]` + `[on/off]`* turns on and off specific module functionalities.
######
* ***`cw`*** *`+`* ***`color`*** *`#hexcolor`* Sends a message directly from your cute kouhai to get an idea of how the hexcolor of choice would look in game.

###### Credits

* Me.
* Caalitos because it autoupdoots thx to him.
* Mushu cuz she wrote the first version of the js proxy.
* Salty cuz he helped making my code actually work.
* bubby cuz he's a qt.
* All the people i randomly whispered when testing.