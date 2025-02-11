# Contents

## Player
### Properties

**start_position** - The spawn position of player. If player spawns on the left, it is -5. If the player spawns on the right, it is 5. \
This is also the respawn position of the player object. \
**states** - 'walking' | 'standing' | 'turnaround' | 'air_turnaround' | 'sprinting' | 'stun' | 'in_air' | 'dodge' | 'attack' | 'dash' | 'backdash' | 'KO' | 'taunt' \
You can access which state the player is in by **player.state** where player is the Player object \
**facing** - Which side the player is facing. \
Facing.RIGHT | Facing.RIGHT \
**damage** - Damage that the player object does. The maximum value is 700 \
**damage_taken** - The total amount of damage that the player has taken  \
**damage_taken_this_frame** - The amount of damange taken in the current frame by the player. \
**damage_done** - The amount of damage that the player has done on the opponent \
**stocks** - The number of lifes that the player has. Default is 3. \
**prev_x** - The x-position of the player in the previous frame. \
**prev_y** - The y-position of the player in the previous frame. \
**just_got_hit** - A bolean flag of when the player just got hit. Should be used by signal.\

**body.position.x** - The x-position that the player is in \
**body.position.y** - The y-position that the player is in \

### State Index
The state index can be accessed through **player.state_index**. \
'WalkingState': 0 \
'StandingState': 1 \
'TurnaroundState': 2 \
'AirTurnaroundState': 3 \
'SprintingState': 4 \
'StunState': 5 \
'InAirState': 6 \
'DodgeState': 7 \
'AttackState': 8 \
'DashState': 9 \
'BackDashState': 10 \
'KOState': 11 \
'TauntState': 12 

### State Properties
**is_grounded()** - Returns a boolean value of if the player is on the ground \
**is_aerial()** - Returns a boolean value of if the player is in air \
**vulnerable()** - Returns a boolean value of if the player is vulnerable. Used by dodge to create iframes \

### Parameters
**move_speed** = 6.75 \
**jump_speed** = 8.9 \
**in_air_ease** = 6.75 divided by fps \
**run_speed** = 8 \
**dash_speed** = 10 \
**backdash_speed** = 4 \
**turnaround_time** = 4 \
**backdash_time** = 7 \
**dodge_time** = 10 \
**grounded_dodge_cooldown** = 30 \
**smoothTimeX**  = 0.33 multiplied by fps \
**air_dodge_cooldown** = 82 \
**invincible_time** = 3 multipled by fps (3 frames) \
**jump_cooldown** = 0.5 multipled by fps (0.5 frame) \
**dash_time** = 0.3 multipled by fps (0.3 frame)
**dash_cooldown** = 8 \
**Hitbox Size** - Capsule.get_hitbox_size(290//2, 320//2)  This is not a property.\

### Methods
**is_on_floor()** - Returns  boolean value of if the player is touching the ground or not
