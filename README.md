# JSMC

## Installation
```html 
<script src="https://withdrew.github.io/jsmc/jsmc@v1.2.min.js"></script>
<script>
  var name = "Seeped"; //Username Here
function code() {
//code here
}
jsmc(name);
</script>
```

## APIs used

https://playerdb.co/

https://crafatar.com/

https://api.gapple.pw/


## Usage

```javascript
player.username; //returns the players username. Ex. Seeped
player.uuid; //returns the players uuid with dashes. Ex. eb74d592-71f8-4b1e-a1b1-ba76a12d8858
player.id; //returns the players uuid without dashes. Ex. eb74d59271f84b1ea1b1ba76a12d8858
player.name_history; //returns the players name history.
player.status; //returns the status of the name. The response can be taken, available, blocked, or invalid.
player.type; //returns the account type of the player. The response can be mojang, msa, legacy, or nonexistent.
player.skin; //returns an image of the players skin. Ex. https://crafatar.com/skins/eb74d59271f84b1ea1b1ba76a12d8858
player.cosmetics.cape.official; //returns a image of the players official cape. Ex. https://crafatar.com/capes/403e6cb7a6ca440a80417fb1e579b5a5
player.cosmetics.cape.optifine; //returns a image of the players optifine cape. Ex. https://api.gapple.pw/cors/optifine/Seeped
player.cosmetics.cape.labymod; //returns a image of the players laby mod cape. Ex. https://api.gapple.pw/cors/labymod/cape/6a836b80-2488-4703-85a7-f130b2097ee0
player.cosmetics.bandana.labymod; //returns a image of the players laby mod bandana. Ex. https://api.gapple.pw/cors/labymod/bandana/65ec6b8e4d44439eaf64fe3b572f9b8b
player.icon; //return an image of the players head. Ex. https://crafatar.com/avatars/eb74d59271f84b1ea1b1ba76a12d8858?overlay
player.avatar; //returns a render of the players avatar. Ex. https://crafatar.com/renders/body/eb74d59271f84b1ea1b1ba76a12d8858?overlay
player.head; //returns a render of the players head. Ex. https://crafatar.com/renders/head/eb74d59271f84b1ea1b1ba76a12d8858?overlay
player.error; //returns if there is a error or not. The response can either be true or false.
```

## Example Usage
[See it in action](https://withdrew.github.io/jsmc/)
```html
<html>
   <head>
      <script src="https://withdrew.github.io/jsmc/jsmc@v1.1.min.js"></script>
      <script>
         var name = "Seeped"; //Username Here
         function code() {
         document.getElementById("title").innerHTML = player.username;
         document.getElementById("uuid").innerHTML = `UUID: ${player.uuid}`;
         document.getElementById("img").src = player.avatar;
         document.getElementById("namehistory").innerHTML = `Original Name: ${player.name_history[0].name}`;
         }
         jsmc(name);
      </script>
      <title></title>
   </head>
   <body>
      <h1 id="title"></h1>
      <p id="uuid"></p>
      <p id="namehistory"></p>
      <img id="img" src="">
   </body>
</html>
```
