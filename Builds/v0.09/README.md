# Odd-Man Rush

A realistic 5-on-5 ice hockey simulation for Windows, Linux and macOS (64-bit), built with the Godot 4.3 engine.
All teams, players, names, art, and sounds are original. Nothing from EA, the NHL, or any real team is used.

## Running the game

- **Windows:** unzip and run `PCHockeySim.exe`. Windows SmartScreen may warn about an unknown publisher: click *More info → Run anyway*.
- **Linux:** unzip, then `chmod +x PCHockeySim.x86_64 && ./PCHockeySim.x86_64`. Needs a Vulkan-capable GPU driver (Mesa or proprietary).
  If you have no Vulkan driver: `./PCHockeySim.x86_64 --rendering-driver opengl3`
- **macOS (Intel and Apple Silicon):** unzip, move `PC Hockey Sim.app` to Applications, then **right-click → Open** the first time
  (the app is not notarized by Apple). If macOS says it is damaged: `xattr -cr "/Applications/PC Hockey Sim.app"`.

Each controlled player is marked by a shape floating above him (P1 gold triangle, P2 cyan diamond, P3 green square, P4 pink circle). The same shape appears in the scoreboard next to that player's name, number and stamina bar. When your player is off-screen, an arrow at the screen edge points to him. The puck is drawn slightly larger than life by default, with a light rim that stays visible behind players. Change it in the menu under **Puck size** (Realistic / Large / Extra large).

The goal horn is followed by an original goal song for home goals and your own team's goals (switch it off in Options). You'll also hear organ riffs at some whistles, skate carves, stickhandling taps, and a crowd that rises as play nears the net. All audio is synthesized by the game.

Settings are saved automatically. Graphics: *High* enables screen-space reflections on the ice and ambient occlusion. If the game runs slowly, choose *Medium* or *Low* in the menu and restart.

## Menus

The game opens on a title screen. Press any button to reach the main menu, a tile grid with:
- **Play Now** works in three steps, shown at the top of the screen:
  1. **Choose teams:** Left / Right picks the home team, A / Enter confirms, then the same for the away team.
  2. **Choose jerseys** (Home, Away/white or Alternate): pick and confirm the home jersey, then the away jersey.
  3. **Choose sides:** each controller moves its icon to HOME, CPU or AWAY, then A / Enter starts the game.
  B / Esc steps back one stage at a time; Up / Down switches between home and away within a step. Up to 4 people can play,
  on the same team or against each other, with colour-coded markers (P1 gold, P2 red, P3 green, P4 cyan).
- The keyboard and any recognised gamepad count as Player 1; additional gamepads are separate players.
- **Season** and **Create** (see below).
- **Options:** difficulty, period length, camera, rules, fighting, replays, sound, goal song, graphics, puck size, auto-switch.
- **Controls:** a full reference, also available from the pause menu.
- **Quit.**

## Presentation

Menus have their own animated backdrop (a dark gradient with sweeping light streaks and drifting particles); the rink only
appears once a game starts. Jersey previews and Create show the players on a lit studio platform in front of it.
The interface uses gradient panels, buttons, tabs, lists and sliders with gold focus highlights. Menu tiles shimmer and
lift when highlighted, screens slide in, and in-game banners sweep in and out.


The menus sit over a dimmed, spotlit arena with two players at centre ice wearing the selected home and away jerseys.
On the Play Now screen they face the camera, so you can preview jersey choices as you change them.
Each game opens with a warm-up (a cinematic arena fly-around and players skating laps) and "Welcome to" the home team's arena.
Press A / Enter / Shoot to skip it, or turn it off in Options. Give each team its arena name in Create.

## Pause menu

Tabs: **Team stats** (goals, shots, hits, takeaways, giveaways, possession %, faceoffs, blocks, interceptions, power plays, PIM),
**Display**, **Camera** (camera mode, overhead zoom and overhead angle sliders), **Gameplay** (difficulty, rules, and your team's strategy: offence Balanced / Puck-side attack / Crash the net, defence 2-1-2 forecheck / 1-3-1 trap / Prioritize defense),
and **Game sliders** (game speed, skating speed, hitting power).

## Goalies, skating and systems

- **Goalie stances:** stand-up when play is far away, a ready crouch in the zone, and down into the butterfly for scrambles in tight.
  When the puck goes behind the net he stays square to the ice at the near post and turns his head to follow it.
- **Stickhandling:** skaters stickhandle by default, wider when skating slowly. J/L (or the right stick) moves the puck across
  the blade with real momentum (about half a second side to side, quicker for good hands). The blade cups the puck and
  the hands and shoulders work with it.
- **Crossovers** show up on moderate turns, and pulling the stick against your direction of travel snaps into a hard hockey stop.
- **Hustling with the puck:** the carrier pushes it ahead with one hand on the stick while the other arm pumps.
  Cutting hard at full speed can cost you the puck (less often with good hands).
- **Hitting:** a red marker floats over the opponent your check would hit. Press check with him in range and close in front,
  and the hit lands immediately, powered by both skaters' speeds.
- **Hockey stops** use a real motion-capture pose (deep knee bend, skates turned across the line of travel, one leg leading, forward crouch). Pull the stick against your direction of travel at speed and you stop hard to a standstill,
  then have to skate again. Below about 15 ft/s, pivots between forwards and backwards are quick and cost little speed.
- **Mouse:** left button shoots (same as Space), right button dekes (same as Q). Use these if your keyboard drops
  key combinations like Q + W + Space.
- **Skate backwards:** hold LT / Ctrl while moving to skate backwards, facing away from your direction of travel. Standing still, you face the puck.
- **Checking and interceptions** are easier for human players: a longer check window, check assist toward the target,
  and more reach on passing lanes.
- **Skating:** less exaggerated lean in turns, and sharper hockey stops.
- **Defencemen** keep a speed-based gap to the puck carrier and retreat hard if they get beaten.

## Customization (Create)

Create opens on a start page asking **What would you like to do?** with four choices:
**Create a Player**, **Create a Team**, **Edit an Existing Player** and **Edit an Existing Team**.

The player creator has three tabs, **Player Info**, **Player Appearance** and **Stats**, with the player shown on the right.
Up / Down picks a row, Left / Right changes it, LB / RB (or Q / E / Tab) switches tabs, and B / Esc saves and goes back.
- **Player Info:** name, team (new players), number, age, height, weight, position, archetype (reshapes the ratings) and handedness.
- **Player Appearance:** preset, skin tone, head shape, eye colour, facial hair, shoulder pads and face protection.
  Skin tone, head shape and height show on the classic models; the other appearance choices are saved with the player
  and will show once the player models support them.
- **Stats:** all eleven ratings, from 40 to 99.

Creating or editing a team opens the team and jersey editor, and returns to the Create page when you're done.

## Practice mode

**Practice** on the main menu puts one skater on the ice against a goalie, with no clock, penalties, offside, icing or fights,
so you can work on skating, dekes and shooting. The puck comes back to you after goals, saves and whistles, and whenever it's
loose for a few seconds. Press Enter / B to reset it any time, and Esc / Start to pause and leave.

## Player models

Skaters use the procedural (Classic) model by default, with knit-mesh jerseys that drape in soft folds, quilted nylon
pants, leather gloves and skates. **Options > Player models** can switch to the sculpted, textured model (rigged for the game and driven by its animation system), with white cloth tinted
to each team's jersey and helmet colours, plus the team crest, back number, nameplate and sleeve numbers.
**Options > Player models** switches back to the classic generated models (takes effect after a restart).
Goalies use a sculpted, textured model too (catching glove on the left hand).

## Sound

Real recordings are used for wrist shots (3 takes), snap shots (4), slapshots and one-timers, hockey stops (4), the puck
hitting the boards, the skating sound (a loop that gets louder and slightly higher as players skate faster), and the
home goal horn with the crowd erupting. Like a real arena, the horn only sounds for home goals, and the celebration
fades out once play resumes. A random take is used each time, never the same one twice in a row.
Other sounds (passes, hits, saves, whistles, the crowd bed, organ) are synthesized.

## Officials

Four officials work every game, as in real hockey: two **referees** (orange armbands) and two **linesmen**.
Linesmen hold the blue lines along the boards and the lead linesman takes the dot to drop the puck at faceoffs;
the lead referee covers deep near the goal line and the trailing referee stays up ice. They skate into position
with realistic acceleration, always face the puck and keep out of the players' way.

## Arena and animation

- **Crowd:** thousands of fans fill the seating bowl, mostly in home colours with some away fans. They sway in their seats,
  get louder and livelier as play nears the net, and jump up when a goal is scored.
  The Graphics setting controls crowd density (Low: none, Medium: about half full, High: fuller).
- **Lighting:** a light arena haze over the stands, a reflection probe so the boards and lights reflect in the glossy ice
  (Medium/High), and rim lighting on players' gear.
- **Goalie saves:** butterfly, body, glove, blocker, pad kick, two-pad stack, paddle-down, the splits (toe save to the post),
  desperation dive (glove or stick across the crease), butterfly glove and butterfly blocker, chest save that smothers the puck,
  and a mask save. Each save type has its own rebound or freeze behaviour.
- **Animation:**
  - Passes sweep and follow through, on the forehand or backhand.
  - Defenders in the shooting lane drop to a knee with the stick flat to block.
  - Open teammates tap their sticks on the ice to call for the puck.
  - Five goal celebrations, varied by player: stick to the crowd, fist pump, both arms up, knee slide, and arms resting on the stick.
  - Snow spray on hard turns and crossovers as well as stops.
  - The stick flexes on slapshot and snapshot release.

## Gamepads

Any recognised gamepad and the keyboard both control Player 1 (unrecognised extra devices, such as a duplicate "raw"
controller created by DS4Windows, are ignored while a recognised one is connected). If your controller's buttons are
mixed up or don't respond, open **Options > Controller setup**, press any button on it, then press each button when prompted.
The mapping is saved and used every time you start the game.

## Controls

| Action | Gamepad (Xbox layout) | Keyboard |
|---|---|---|
| Skate | Left stick | WASD / arrows |
| Stickhandle | Right stick (side to side) | J / L |
| Wrist shot | Flick right stick up, or X | F |
| Slapshot | Pull right stick back, then push up — or hold RT | Hold Space |
| Snap shot | Tap RT | Tap Space |
| Pass (hold for saucer pass) | RB | E |
| Deke / shield the puck (hold) | LB | Q |
| Hustle (drains energy) | A or L3 | Shift |
| Face the puck | LT | Ctrl |
| Switch player | Y (or LB on defense) | C (or Q on defense) |
| Body check / net battle | RT (defense) | Space (defense) |
| Poke check / stick lift | RB (defense) | E (defense) |
| Pause | Start | Esc |
| Skip replay | B | Enter |
| Drop the gloves (at a whistle, next to an opponent) | Back / View | G |

**Dekes:** tap deke = side-to-side dangle · pull back + deke = toe drag · deke while winding up = fake shot (goalie bites) ·
hustle + deke = spin-o-rama · deke in tight near the goal line = lacrosse-style tuck.

**One-timers:** press shoot as the pass arrives. The closer your timing, the harder and more accurate the shot.

**Faceoffs:** press shoot or pass right as the puck hits the ice. Too early and you lose the draw.

**Defense:** poke from behind the carrier to lift his stick. Press check near a screener in front of your net to start a net battle.
A careless stick into a player's skates gets called for tripping.

## Create mode (custom teams, jerseys and players)

From the main menu choose **Create teams & players**. You can:
- add, duplicate or delete teams
- set the team name, 3-letter abbreviation, and jersey, trim/number, helmet and stripe-accent colours, with a live rotating 3D preview
- choose a stripe pattern for the hem, sleeves and socks: none, single, double, or triple (with the accent colour in the middle)
- edit the goalie (name, number, rating)
- build the roster: add or remove players, and set each one's name, number, position (C/LW/RW/LD/RD), which way he shoots, weight,
  and 8 ratings (speed, acceleration, agility, shooting, passing, puck handling, checking, balance)

The best-rated players at each position dress on the top lines. Your league is saved to `league.json` in the game's user-data folder,
and your players keep their names, numbers and ratings from game to game. Pick the home and away teams in the main menu,
and choose which side you control.

## Season mode (custom league)

Choose **Season mode** on the main menu. Pick your team and a season length (play each opponent 1, 2, 4 or 8 times).
The league fills out to 11 teams with 10 original CPU clubs, which play their own schedule.

- **Hub:** your record and place, your next game, and league news, including CPU-to-CPU trades.
  Play your next game, or simulate it, the next 7 days, or the rest of the season.
- **Standings:** games played, wins, losses, overtime losses, points, goals for and against, and goal differential.
- **Results:** recent scores and your upcoming schedule.
- **Leaders:** points, goals, assists, +/-, penalty minutes, shots, hits and fights; save percentage and goals-against average for goalies.
- **Rosters & Ratings:** every team's players with their ratings and season stats.
- **Trades:** select players on both sides and a meter shows how the other team feels about the deal.
  Value rises steeply with overall rating, and multi-player packages are worth less than their parts, so quantity won't buy a star.
  The CPU wants a small edge, protects its best player, and both teams must keep at least 12 forwards and 6 defensemen.

The whole league, including season progress, is saved in `league.json`.

## Player ratings

Skater ratings run from 40 to 99: speed, acceleration, agility, puck control, shot power, shot accuracy, passing, checking,
balance, endurance and fighting. The overall rating is weighted by position. All ratings affect play: shot power sets
shot speed, accuracy sets aim, endurance sets how fast a player tires, and fighting decides fights.
Edit them in Create mode.

## Fighting

Big hits, especially into the boards, can start a fight at the next whistle. When your team is involved, choose to
drop the gloves (Shoot) or skate away (Deke). To start one yourself, press G / Back at a whistle while next to an opponent.
In a fight, Pass throws a jab, Shoot an overhand and the wrist-shot button an uppercut. Hold Deke to block, and pull away on the stick to dodge.
Both fighters get a 5-minute major, so the teams play 4-on-4, and the winner's team gets an energy boost.
You can turn fighting off in the menu.

## What's simulated

- **Skating:** acceleration that falls off as speed rises, a turn radius that grows with speed, crossovers, glide friction and air drag,
  hockey stops, pivot speed loss, backward skating at about 75% speed, and fatigue with recovery on the bench.
- **Puck:** real puck friction, air drag, low-bounce boards, livelier glass and posts, shots that lift and drop, pucks that roll on edge.
- **Shots:** each type has its own speed and release time. Goals depend on distance, angle, rebounds, rushes, screens and cross-ice passes.
- **Goalies:** a goalie in position makes blocking saves (dead rebounds). One caught out of position makes athletic saves (live rebounds).
  They also make glove, blocker, stacked-pad and stick-down saves, and seal the post.
- **Hits:** based on body mass and impact speed. Most separate a player from the puck rather than knock him down, and you can pin a player on the boards.
- **Rules and team play:** delayed offside, icing (not called against a shorthanded team), delayed penalties and power plays,
  and 3-on-3 overtime.
- **Line changes:** four forward lines and three defense pairs. Tired players skate to the bench and change on the fly
  when it's safe, and fresh lines come out at whistles. Your own player changes automatically at the bench when he's exhausted.
- **Shootout:** a real, playable shootout, best of three then sudden death. You take your team's shots, and you play in goal
  when the CPU shoots: move with the stick, hold Shoot to drop into the butterfly (better down low, weaker up high),
  and press Pass to poke check.

## Editing the game

Open this folder in the free [Godot 4.3](https://godotengine.org) editor. The code lives in `scripts/`:
`sim.gd` (physics, rules and AI), `skater_model.gd` / `goalie_model.gd` (player models and animation), `rink.gd`,
`cam_rig.gd`, `audio.gd`, `ui.gd`, and `main.gd`.
To export builds, use *Project → Export*. The presets for Windows, Linux and macOS are already set up.

Font: Barlow Condensed (SIL Open Font License, included in `assets/fonts/OFL.txt`).
