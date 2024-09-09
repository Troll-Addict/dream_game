# STATS
|Base               |	Offensive                   |
| ---               |-------                        |
|Strength           |Physical Dmg   	            |
|Agility	        |Movement Speed	                |
|Stamina	        |Block Capacity 	            |
|Dexterity	        |Critical Strike Chance	        |
|Intelligence	    |Magic Dmg	                    |
|Wisdom	            |Mana Pool	                    |
|Knowledge	        |Spell Critical Strike Chance	|
|Constitution	    |HP	                            |
|Focus	            |Cast Speed	                    |

# ARMOR

## General Intent
Any Class can wear any armor type. Weight affects movement speed based on your strength. If you are wearing 100 Weight and you have 15 Strength you will have 85% movement speed reduction. Numbers will change but the idea is that you can put armor on, but if you're not strong enough to use it then it will slow you down. Weapons will have a similar mechanic to where your attack speed and damage will be reduced if you're not strong enough to use a certain weapon.

### Armor Types
| NAME          | WEIGHT    |
| -----------   | --------- |
| Plate         | 10        |
| Scale         | 8         |
| Mail          | 6         |
| Leather       | 4         |
| Cloth         | 2         |

### Armor Slots
| NAME          | WEIGHT    |
| -----------   | --------- |
| Helm          | 1         |
| Chest         | 3         |
| Gloves        | 2         |
| Pants         | 3         |
| Boots         | 2         |

### Accessories
- Earrings - 2 slots
- Necklace - 1 slot
- Bracelets - 2 slots
- Rings - 10 slots
- Belts - 1 slot
    - Used to increase hotbar slots

Accessories are used for utility, not for direct damage or spell effectiveness. Primary idea is to grant magic find or increased light radius, basic idea is to have a system where players can fuck around and stack stupid shit or create general utility.

### Shields
Shields allow you to block incoming physical attacks if you are not performing another action. Blocking is metered based on constitution and drains depending on the pre-mitigation damage of the attack.

# WEAPONS
## Weapon Types
|Name	    |Weight X	|Dmg	|Speed  |Range  |
|---------- | --------- | ----- | ----- | ----- |
|1H Sword	|4	        |5	    |8	    |4      |
|1H Axe	    |5	        |6	    |7	    |4      |
|1H Mace	|5	        |7      |6	    |4      |
|Dagger	    |2	        |4	    |10	    |2      |
|2H Sword	|8	        |8	    |2	    |6      |
|2H Axe	    |9	        |9	    |1	    |6      |
|2H Mace	|10	        |10	    |1	    |6      |
|Staff	    |3	        |3	    |3	    |5      |
|Bow	    |3	        |5	    |5	    |5x(Str/10)  |
|Crossbow	|3	        |6	    |4	    |10     |
|Spear	    |7	        |8	    |3	    |7      |

### Quality
|Wep Name           |Bonus% |
|------------------ | ------|
|Common 	        |0%     |
|Minimal 	        |5%     |
|Lesser 	        |10%    |
|Medial 	        |15%    |
|Standard 	        |20%    |
|Improved 	        |25%    |
|Greatly_Improved 	|30%    |
|Perfect 	        |35%    |

# COMBAT
## Melee
Attack damage and attack speed are determined by formulas below
> Attack_Speed = WepAS + (Agi*(Str/WepWT))

> Attack_Damage = WepDmg + (Str*(Str/WepWT))

## Abilities
Physical Abilities are learned by mastering weapon types. Example abilities below
- 1H Sword - Rank 10 - Lunge - Dash forward causing [AD+1SwLvl] Phys dmg to all enemies in path
- 2H Axe - Rank 10 - Cleave - Deal [AD+2AxLvl] Phys dmg to enemies in a cone in front of you
- Dagger - Rank 10 - Backstab - Deal + 25% bonus damage when attacking from behind

My desire for skills is to create a low skill entry but very high cap and lots of customization. I want anybody to be able to enjoy the game but I want elite people to be able to truly excel/shine.

## Spells

- Bolt - Shoot a ball that deals single target damage [Int*SpellSkill]
- Ball - Shoot a ball that explodes and deals AoE dmg on impact
- Cone - Deals damage to cone shape in front of you
- Burst - Deals damage in a circle around you
- Beam - Deals [Int*SpellSkill*timecasting] damage increasing in power over time
- STSE[Curse] - Single Target Status Effect
- MTSE[Ground] - Multi Target Status Effect

All spells are instant cast but have an linear growth factor for damage and mana cost with cast time. If you get hit while casting it cancels your cast. You can move while casting but at % speed.

# PROGRESSION
## Experience
Gained through completing any action in the game. If you craft an item you gain XP, if you kill a mob you gain XP, complete a quest, gather a resource. Idea is to allow all players to do whatever they want and still gain experience. Play testing will become extremely important in this aspect to ensure players FEEL like it's a balanced system.

## Skill Experience
Completing actions also give you experience in that actions field. Say you swing a sword 100 times, you get 10 1H Sword XP. Maybe you craft 100 Potions, 10 Alchemy. Each skillset will give you xp in that field. This is SEPARATE from general experience, consider changing the name to be "Alchemical Knowledge" or something in order to differenciate.

# ELEMENTS
|Base       | 	Status Effect	    | Increases Dmg From|
|---------- | ------------------    |  -------------    |
|Fire       |Damage over time       |Earth              |
|Water      |Armor Pen              |Lightning          |
|Ice        |Frozen                 |Earth              |
|Lightning  |Reduced Physical Attack|Physical           |
|Earth      |Knocked Down           |Ice                |

## General Intent for Elements
- All elements build up status effect to 100%
- Once status effect is applied it will deteriorate at an exponential rate so you can't maintain uptime forever.
- Increase damage OR status effect application % to a maximum of 100%
- Resistances reduce the buildup of the elements

I Want to create a system that promotes weaving different attacks rather than just shooting a million fireballs

## Ailments (Related to Elements, maybe consider merging)
- Poison - small damage over time [must be cured]
- Stun - stops all actions 
- Disarm - can't use weapons [attacks are unarmed]
- Frozen - {how is this different from a stun}
- Knock Down - {how is this different from a stun}
- On Fire - large damage over time that falls off
- Armor reduction- temporarily reduced dmg reduction 
- Heal Reduction - reduces healing received 

## Poisitive Status Affects
- Accessories
    - Increased Light Radius - increased vision
    - Magic Find - increases chance of bonuses
    - Gold Find - % increase of gold
- Weapon & Armor Enchants
    - Life on Hit - flat life with each attack that deals damage
    - Leach - % of post-mitigation dmg dealt heals (Probably only for single target damage, not sure how to best balance this but I'd like it to provide survivability but not replace the need to heal by other means)
    - Life Regen - health recovery if not hit for n seconds 
    - Chance to cast when struck - yup
    - Thorns/Spines/Quills - % dmg received returned

    

# PROFESSIONS
## General Intent
I would like crafting to have a primary element of skill to generate higher quality items. Each profession will have a different minigame and depending on how well you do the quality will be increased.

This means that in order to craft the **BEST** item you need to complete a __perfect__ gather for all appropriate reagents, craft a __perfect__ item for all appropriate component-items (hilt, blade, etc.), and craft the final item as __perfect__, enchant the item as __perfect__, bejewel the item as __perfect__, and finally have __perfect__ balms or poisons to apply as necessary.

## Crafting Professions
- Blacksmithing - uses reagents, primarily metal, to craft weapons, armor, and other components.
    - Weaponsmith
	- Armorsmith
		- Plate
		- Mail
- Tanner - Uses hide & scales to create leather & scale armor, quivers, and belts and other components.
- Tailor - Uses fibers to create cloth armor and other components.
- Woodworker - Uses wood to craft the below items as well as other components.
	- Staff
	- Bows
	- Crossbows
	- Arrows
    - Bolts
- Jeweler - Uses gems and metal to craft most accessories and bejewel other equipment.
- Engineer - creates devices or specialized buildings using metals and other components.
- Alchemist - uses herbs and other gathered materials to create potions, elixirs, balms, and other components.

Not sure how I want to handle recipe's right now. The way I'm leaning toward the most is to have it all be "secret" and have players figure things out. My biggest reservation with this is how quickly a wiki will be stood up to basically get rid of the mysticism and sense of discovery players get.

## Gathering Professions
- Mining - Gather Metals
- Skinning - Gather Creature Hides/Scales
- **Cloth gatherer...?**
- Lumberjack - Collects wood
- Geologist/Rockhound - Collects gems
- Herbalism - Gather plants/plant resources

## Potion Types
- Instant Heal
- Heal over Time
- Exp Boost
- Resistance
- Movement Speed

### Quality
|Name               |Bonus% |
|------------------ | ------|
|Common 	        |0%     |
|Minimal 	        |5%     |
|Lesser 	        |10%    |
|Medial 	        |15%    |
|Standard 	        |20%    |
|Improved 	        |25%    |
|Greatly_Improved 	|30%    |
|Perfect 	        |35%    |

# BUILDINGS
- Crafting
    - Blacksmith
    - Tailor
    - Wood crafting
    - Alchemist station
    - Tanner
    - Jeweler
    - Engineer
- Defensive
    - Wall
    - Archery tower
    - Cannon tower
    - Mages tower
- Passive Resource Gathering
    - Mines - For metals
    - Slaughterhouse - For hides/scales
    - Silkworm Farm? - For cloth
    - Lumbermill - For wood
    - Digsite - For Gems
    - Greenhouse (or something... for herbs and shit)

# implementations 
	## class hierarchy
- entity 
	- x, y coordinates
	- h, w, z dimensions
	- collideable?
	- visible?
 -  
