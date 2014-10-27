## Constructor Review

> Let's build a game!

```html
<div class="hero-unit">
  <div class="welcome">
      <h3>Choose Your Character</h3>
      <button name="1">Mario</button>
      <button name="2">Princess Peach</button>
      <button name="3">Toad</button>
  </div>
  <div class="fight">
      <p id="player" class="ggName"><span class="ggHealth"></span></p>
      <p>Vs</p>
      <p id="monster" class="bgName"><span class="bgHealth"></span></p>
      <button id="fight">Attack <span class="bgName"></span></button>
  </div>
</div>
```

```js
var BadGuy = function (name) {
  this.name = name;
  this.health = 100;
  this.attack = function (attackee) {
    return attackee.health = attackee.health - _.random(5, 10);
  };
  this.special = function (attackee) {
    return attackee.health = attackee.health - _.random(15, 50);
  };
};

var GoodGuy = function (options) {
  var special_pt, attack_pt;
  options = options || {};
  this.name = options.name;
  this.type = options.type;
  this.health = 100;
  switch (this.type) {
      case 1:
        attack_pt = 10;
        special_pt = 20;
      break;
      case 2:
        attack_pt = 15;
        special_pt = 25;
      break;
      case 3:
        attack_pt = 5;
        special_pt = 30;
      break;
  };
  this.attack = function (attackee) {
    return attackee.health = attackee.health - attack_pt;
  };
  this.special = function (attackee) {
    return attackee.health = attackee.health - special_pt;
  };
};


// Starting the Game
var player, monster;

$('.welcome button').on('click', function (event) {
  event.preventDefault();

  // Create an Instance of my Good Guy
  player = new GoodGuy({
    name: $(this).text(),
    type: parseInt($(this).attr('name'))
  });

  // Create an Instance of my Bad Guy
  monster = new BadGuy('Bowser');

  // Get Ready to Fight
  $('.welcome').fadeOut(500, function () {

    // Set Player/Monster Names & Health
    $('.ggName').prepend(player.name).find('.ggHealth').text(player.health);
    $('.bgName').prepend(monster.name).find('.bgHealth').text(monster.health);

    $('.fight').fadeIn();
  });

});

// Fight Sequence

// 1. Health drops below 0
// 2. Winner is not random

$('#fight').on('click', function (event) {
  event.preventDefault();

  var attack_type = _.random(1, 2);

  if (attack_type === 1) {
    player.attack(monster);
    console.log('Regular Attacks being used!');
  } else {
    player.special(monster);
    console.log('Special Attacks being used!');
  }
  if (monster.health > 0){
    $('.bgHealth').text(monster.health);
    if (attack_type === 1) {
      monster.attack(player);
    } else {
      monster.special(player);
    }
  } else {
    $('.bgHealth').text('0');
    $('#monster').css('text-decoration', 'line-through').css('color', 'red');
    $('#fight').fadeOut();
  }

  if (player.health <= 0) {
    $('.ggHealth').text(0);
    $('#player').css('text-decoration', 'line-through').css('color', 'red');
    $('#fight').fadeOut();
  } else {
    $('.ggHealth').text(player.health);
  }

});
```

```css
body {
  background: #fafafa;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  color: #333;
}

.hero-unit {
  margin: 50px auto 0 auto;
  width: 600px;
  font-size: 18px;
  font-weight: 200;
  line-height: 30px;
  background-color: #eee;
  border-radius: 6px;
  padding: 60px;
  .welcome {
    text-align: center;
  }
  .fight {
    display: none;
    text-align: center;
  }
  .ggHealth, .bgHealth {
    color: green;
    padding-left: 15px;
  }
}
```