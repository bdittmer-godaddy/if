"Christmas Hunt 2022" by Brad Dittmer
Include Exit Lister by Gavin Lambert.
Include Underside by Eric Eve.
[Include Hybrid Choices by Aw Freyr.]
[Include Basic Screen Effects by Emily Short.]

Use full-length room descriptions.

Release along with cover art.


[A person can be Calista, Corrina, Kyra, or Keona.]
[The player is Calista.]
[Move the player to the Family Room, without printing a room description.]


[Rule for printing the banner text:
    say "[header style][my title][roman type][line break]";
    say "[story headline][line break]";
    rule succeeds.]

[When play begins:]
[
The player's forename is a text that varies. The player's full name is a text that varies.
After printing the banner text:
    now the command prompt is "What is your name? > ".

To decide whether collecting names:
	if the command prompt is "What is your name? > ", yes;
		no.

After reading a command when collecting names:
    now the player's full name is the player's command;
    now the player's forename is word number 1 in the player's command;
    now the command prompt is ">";
    say "Hi, [player's forename]![paragraph break]";
    say "[line break]It's a race to find your present, you must find your present in this virtual world to find it in the real world.  Make haste, the first to complete this gets first choice of an extra prize.[line break][line break]Hint:[line break]Try n, s, e, w, sw, etc. to move; up or down for stairs.[line break]Try inventory, look, look at, look under, look in, read, take, put, sit, ask about, enter, get on, push, ask x about y, give x to y, play, turn on x, etc. for actions.[line break][line break][line break]You find yourself in this virtual world holding only your phone.  You are standing in the Family Room.  You hear a beep, you might have just gotten a text.[line break][line break]";
    move the player to the location;
    reject the player's command.]



Volume 1 — The Game

Book 1 — Setup, etc


After printing the banner text: say "[line break]It's an interactive quest to find your present, you must find your present in this virtual world to find it in the real world.[line break][line break]Hint:[line break]Try n, s, e, w, sw, etc. to move; up or down for stairs.[line break]Try inventory, look, look at, look under, look in, read, take, put, sit, ask about, enter, get on, push, ask x about y, give x to y, play, turn on x, etc. for actions.[line break][line break][line break]You find yourself in this virtual world holding only your phone.  You are standing in the Family Room.  You hear a beep, you might have just gotten a text.[line break][line break]Hint: you might want to look at your phone.[line break]".

Figure of Snowflake is the file "snowflake.jpg".
Figure of ChristmasTree is the file "tree.png".
Figure of CandyCane is the file "candycane.png".
Figure of Snowman is the file "snowman.png".
Figure of Reindeer is the file "reindeer.png".
Figure of Key is the file "key.jpg".
Figure of Chest is the file "chest.jpg".
Figure of Present is the file "presents.png".
Figure of TV1 is the file "vat-of-acid.png".
Figure of TV2 is the file "christmas-story.jpg".

When play begins: display the Figure of Present.

[
Game Play:
[x] You get a text on your phone.
[x] Clue #1 - Snowflake - Present Under Christmas Tree
[x] Clue #2 - Tree - Under Kiki's bed.
	[x] have to get flashlight. (in kitchen cupboard)
[x] Clue #3 - CandyCane - Out By Pool (bottom)
	[x] have to get net.
[x] Clue #4 - Snowman - Mailbox.
[x] Clue #5 - Reindeer  - Basement. (secret room)
	[x] Ask mary about clue
	[x] sends to go talk to mary, hints that it's in the couch cushion.
[x] Clue #6 - Key - Couch Cushion.  (key to chest)
	[] chest appears where? in living room.
	[] what is in chest?  map to where presents are
	[] where are presents?  
			if the player is.....


[] Experience Pts.

Easter Eggs:
	Guinea Pig / Outside / Feed
	Patches
	Coffee
	Pokemon Card
	Book to bookshelf - ends game
	Mary - to do interaction
	TODO: Fireplace - portal to Hoovie
]


[A person can be Calista, Corrina, Kyra, or Keona.]
[A room can be private or public. A room is usually public.
Check going to public room when the player is B:
    say "You can't do that." instead.]
[
The player's forename is a text that varies. The player's full name is a text that varies.

When play begins:
    now the command prompt is "What is your name? > ".

To decide whether collecting names:
	if the command prompt is "What is your name? > ", yes;
		no.

After reading a command when collecting names:
    now the player's full name is the player's command;
    now the player's forename is word number 1 in the player's command;
    now the command prompt is ">";
    say "Hi, [player's forename]![paragraph break]";
    say "[banner text]";
    move the player to the location;
    reject the player's command.

The description of Edge Park is "[Edge_Park_desc]."

To say Edge_Park_desc:
	if the player is Harriet, say "You're at the south edge of the park. It's super hot today and the sun is pouring down on the grass and the flowerbeds[sick tree desc].[paragraph break]From here, paths lead north, east and west through the park, and to the south is the picnic area where mum and dad will set up lunch later";
	if the player is Demi, say "This is the south edge of the park. The sky is blue and bright today, and the air is warm[sick tree desc].[paragraph break]Paths lead north, east and west, and to the south is the picnic area";
	if the turn count is 1 and given_intro is 0 and player is Harriet:
		say ".[paragraph break](If this is your first time playing Six, type HELP to learn some very helpful stuff)";
...
now the player is Pirate Jenny
]



[Def: Reading]
A thing has some text called the reading-material. The reading-material of a thing is usually "".
Understand the command "read" as something new.
Reading is an action applying to one thing and requiring light. Understand "read [something]" as reading.
Check reading:
	if the reading-material of the noun is "":
		say "Nothing is printed on [the noun].” instead.
Carry out reading:
	say "[reading-material of the noun]."

[Def: musical instrument]
A musical instrument is a kind of thing.
Playing is an action applying to one touchable thing. Understand "play [something]" as playing.
Report playing:
	if the noun is a musical instrument:
		say "You play a tune on [the noun]. It sounds lovely.";
	otherwise:
		say "You canot play that, it's not an instrument.".

[Def: Stairs]
Before climbing stairs:
say “Just use the direction on its own - up or down.”;
Stop the action.

[Def: Climb]
Understand “climb [up]” or “climb [down]” as going.

[Def: Animal]
The can't take other people rule does nothing when taking an animal.

[Def: TV]
A television is a kind of device. A television has a number
called the channel. Understand the channel property as
referring to a television. Understand "channel" as a
television.


Book 2 - The Main Floor

The player is holding a Phone.
A Phone is a object. The description is "There is a text message on the phone, Merry Christmas, you may want to get started by checking where Christmas gifts are kept."

Section 1 - Family Room

Family Room is a room.  The description is "The room is decorated wall to wall with the usual Christmas decor (fireplace, stockings, nativity, etc).  There is torn paper all over the place, looks like a small tornado went through here.  There is a Christmas Tree by the window. There is a Chair against the wall with a book in the basket next to it.[line break][line break]To the south is the Dining Room.[line break]To the west is the Foyer."

A Christmas Book is in the Family Room. The description is "T'Was the Nightmare Before Christmas.". The reading-material of the Christmas Book is "T'Was the Nightmare Before Christmas.[line break]And all through the house.[line break]Not a creature was stiffing.[line break]Not even a mouse."
The Christmas Book can be xread or unread. The Christmas Book is unread.
After reading the Christmas Book:
	now the Christmas Book is xread;
	say "Well it wasn't a Steven King classic like Dark Tower, but what'cha gunna do, gotta do the Christmas thing.";
	rule succeeds.

A Chair is a enterable supporter in the Family Room.  The description is "The chair has a warm blanket draped across the back and a Christmas pillow on it.  It appears very inviting.".
[A Family Room Fireplace is a supporter in the Family Room.  The description is "There is a fake fireplace here decorated with stockings and the usual garb."
A Christmas Stocking is a open container.  The description is "The stocking is empty, you already got all the goodies."
The Christmas Stocking is on the Family Room Fireplace.]
A Family Room Fireplace is a scenery in the Family Room.  The description is "There is a fake fireplace here decorated with stockings and the usual garb."
A Nativity Scene is a scenery in the Family Room.  The description is "There is a Nativity Scene here showing us the true reason for Christmas!".

A Piano is a musical instrument in the Family Room.  The description is "There are a few keys out of tune.".


A Christmas Tree is a supporter in the Family Room.  The description is "The tree is decorated beautifully.  You can just make out something under the tree, perhaps there is a missed present under the tree.".
A Present is a openable closed container.  The description is "The tag says From: Mom & Dad."
A Snowflake Clue is a object in the present. The description is "A small note card on white paper.  There is a snowflake insignia in the top left corner."
The reading-material of the Snowflake Clue is "Ha Ha, Tricked you.  I've hidden your present and now you have to follow the clues to find it.  - Buddy The Elf[line break][line break]Guess I can give you a hint, you may want to look under a bed."
Before reading the Snowflake Clue:
	display the Figure of Snowflake.
[This seems important, you may want to take the clue and read it.]

There is a Present. [This places it "off-stage" until we move it somewhere else.]
Instead of looking under the Christmas Tree when the Present is off-stage:
    say "There seems to be a present under the tree.";
    move the Present to the Family Room.
After opening the Present:
	say "You open the Present, revealing a Snowflake Clue.  This seems important, you may want to take the clue and read it.".

Every turn:
	if the player is on the Chair:
		say "'Oh, thank you!' I was getting tired!'";


Section 2 - Dining Room

The Dining Room is a room.  The description is "The room has a large table in it with various stuff spread all about.[line break][line break]To the north is the Living Room.[line break]To the west is the Kitchen."
A Dining Table is a object in the Dining Room.  The description is "There is a scrumptuous breakfast on the table, stuffed french toast and orange juice.".
[An Ornament is on the Dining Table.]
The Dining Room is south of the Family Room.

[TODO: clean this up]
Mary is a woman in Dining Room. The description is "Mary has just gotten breakfast ready and is busy cleaning up papers from the Christmas presents.".

Table of Mary's Replies
Topic	Replies
"clue"	"[TheClue]"
"goonies"	"[GooniesMovie]"
"school"	"[Preschool]"
"preschool"	"[Preschool]"
"christmas story"	"[TheChristmasStory]"
"christmas"	"[TheChristmasStory]"
"story"	"[TheChristmasStory]"
"glasses"	"[LostMyGlasses]"
"phone"	"[LostMyPhone]"
"rick and morty"	"[RickMorty]"
"rick"	"[RickMorty]"
"morty"	"[RickMorty]"
"bojak"	"[RickMorty]"

To say TheChristmasStory:
	say "Did you say The Christmas Story.  That is my all time favorite Christmas movie.  Hey, that's a great idea, let's watch it tonight.".

To say Preschool:
	say "OMG, i just love those Kiddos.".

To say GooniesMovie:
	say "That is my all time favorite movie.  Hey, that's a great idea, let's watch it tonight.".

To say LostMyGlasses:
	say "OMG, I think I lost my glasses, have you seen them anywhere?  Oh wait, nm, here they are..".

To say LostMyPhone:
	say "OMG, I think I lost my phone, have you seen it anywhere?.  Oh wait, nm, here it is.".

To say RickMorty:
	say "Ugh, I just don't get it.".

To say TheClue:
	say "Oh, I'm so glad you asked, some elf ran up and gave this to me.  He didn't really say much just ran off.[line break][line break]Here you go, oh wait, I just had it, now I cannot find it.  I was just in in watching the best movie ever, Christmas Story.  Must have fallen out when I was sitting down on the Patio Couch?".
	[if Mary carries an clue:
		say ".."
		[try Mary giving the clue to the player;]
		[move the clue to the player;]
	else:
		say "Mary says, 'sorry, I already gave away the clue that I had.' ".]

[After asking Mary about a topic listed in the Table of Mary's Replies, say "[replies entry]".]
Before asking Mary about something: if the topic understood is a topic listed in the Table of Mary's Replies, say “[replies entry] [paragraph break]” instead;
otherwise say “[the noun] says 'Nonya'.” instead.



Section 3 - Foyer

The Foyer is a room.  The description is “This room has shoes all over the place.[line break][line break]A grand staircase decorated with all sorts of Christmas decorations leads up to the 2nd level.[line break]A separate plain set of stairs leads down to the basement.[line break]To the south is the Kitchen.[line break]To the east is the Family Room.[line break]To the north, the Front door leads outside.[line break]To the west is the Laundry Room[line break]To the south west is the First Floor Bathroom”.
The Foyer is west of the Family Room.
The Foyer is north of the Kitchen.
Down from Foyer is Basement.
Up from Foyer is Second Floor Hallway.
Stairs are scenery in Foyer.
The Front Yard is north of the Foyer.

A Rug is an supporter in the Foyer.
A Pokemon Card is a object. The description is "500 points Chizzrad, ultra rare Golden."
There is a Pokemon Card. [This places it "off-stage" until we move it somewhere else.]
Instead of looking under the rug when the Pokemon Card is off-stage:
    say "There seems to be a pokemon card under the rug.";
    move the Pokemon Card to the Foyer.


Section 4 - Laundry Room

The Laundry Room is a room.  The description is "There is clothes and coats and shoes all over the place.[line break][line break]To the east is the Foyer.[line break]To the west is the Garage."
The Laundry Room is west of the Foyer.


Section 5 - Garage

The Garage is a room. The description is "There is a Jeep and a Traverse parked in the garage.  The doors are closed.[line break][line break]To the east is the Laundry Room."
The Garage is west of the Laundry Room.

Section 6 - Kitchen

The Kitchen is a room.  The description is "The Kitchen has the usual appliances (Stove, Microwave, Fridge, Dishwasher, etc.).  There are a few dirty dishes in the sink.  There is the strong smell of coffee.[line break][line break]To the north is the Foyer.[line break]To the east is the Dining Room.[line break]To the west is the Living Room.[line break]To the south is the Outside."
The Kitchen is west of the Dining Room.
The Back Porch is south of the Kitchen.
A Kitchen Table is a object in the Kitchen.  The description is "This is where all the papers and junk gets thrown."

The Refridgerator is a fixed in place openable container in the Kitchen.  The Refridgerator is closed.  The description is "The Refridgerator is full of all sorts of food and drinks."

The Carrot is edible. The Carrot is in the Refridgerator.  The description is "A nice juicy carrot w/ the green top till in place".
After eating the Carrot, say "Uh, I'll bet the Guinea Pig would have liked that.".


[cupboards]
The Cupboard is a fixed in place openable container in the Kitchen.  The Cupboard is closed.  The description is "The cupboards are full of various random things, there is one with dishes, etc...."
The Flashlight is an object. The Flashlight can be switched on. The Flashlight is switched off. The Flashlight is in Cupboard.  The Flashlight is not lit.
Carry out the Flashlight switching on:
	say "The Flashlight is On'";
	Now the Flashlight is lit;
Carry out the Flashlight switching off:
	say "'The Flashlight is Off'";
	Now the Flashlight is not lit.

[coffee]
The Mug is a portable container in the Cupboard.  The description is "The coffee mug is a large bowl like cup.  There is Rick and Morty characters printed all over it.".

A K-Cup is a kind of thing.  The description is "Starbucks Sumatra.  In small print it reads, Warning: drinking this may cause you to never want another type of drink ever again."

The Keurig is a open container.  It is in the Kitchen.  The description is "Keurig 5.0.  There is a red 'brew' button.".
The Brew Button is part of the Keurig.
There are 3 K-Cups in the Keurig.
Instead of pushing the Brew Button:
	if a K-Cup (called the kcup) is in the Keurig:
		if the Mug is in the Keurig:
			if the Coffee is in the Mug:
				say "Hey, I get you need more caffeine but you may want to try drinking the one you already have first." instead;
			otherwise:
				say "The coffee maker makes some noise, then coffee drips into the cup below.";
				move the Coffee to the Mug;
				now the KCup is nowhere;
		otherwise:
			say "You may want to put a cup or something in there or else this is going all over the floor." instead;
	otherwise:
		say "You are out of K-Cups, so nothing happens.[line break]You shed a tear.  NO!!!! Out of coffee!!!".


A thing can be drinkable. A thing is usually not drinkable.

Coffee is drinkable. The description is "The dark sumatra has a deep rich smell.".
Instead of drinking the Coffee:
    say "Wow that was good!";
    now the Coffee is nowhere.


Section 7 - Bathroom

The First Floor Bathroom is a room.  The description is "This is a small bathroom.  There is a toilet a sink and a mirror.[line break][line break]To the north east is the Foyer."
The First Floor Bathroom is southwest of the Foyer.

Some fixtures are scenery in the First Floor Bathroom. Understand "sink", "toilet", "faucet", "mirror", "cabinet",
"tub", "basin", "shower", "towel", "bath", and "mat" as the fixtures. The description is "The bathroom
fixtures are not very interesting."
Instead of doing anything other than examining with the fixtures:
	say "You have more important things to do right now than fiddle with the bathroom fixtures."


Section 8 - Living Room

The Living Room is a room. The description is "This is a small room with couches on the north and west walls. There is a patio chair in the corner.  On the wall is a fireplace surrounded by bookshelves.[line break][line break]To the east is the Kitchen".
The Living Room is west of the Kitchen.

[A Bookshelf is a container in the Living Room.
A Sofa is an enterable supporter in the Living Room.
A Love Seat is an enterable supporter in the Living Room.]
A Living Room Fireplace is a scenery in the Living Room.  The description is "The fireplace hasn't been used in years.  There is a slight draft coming from the outside."

A Lawn Furniture Couch is an enterable supporter in the Living Room.  The description is "Though first done as a joke, the annual tradition of bringing in the Lawn Furniture has stuck.  Surprising it is the most comfortable couch in the house.[line break][line break]You spot something sticking out from underneath the cushion.".
A Cushion is an enterable supporter on the Lawn Furniture Couch.

The Skeleton Key is a object. The description is "This is a Skeleton Key.  It looks like the Alpha key from Locke an Key."
Instead of looking under the Cushion when the Skeleton Key is off-stage:
    say "There seems to be a key and a clue under the cushion.";
    move the Skeleton Key to the Cushion;
    move the Key Clue to the Cushion.

There is a Key Clue.  The description is "A small note card on brown paper.  There is Key insignia in the top left corner."
The reading-material of the Key Clue is "Well, you did it, gotta hand it to you...ok, maybe just one more riddle[line break][line break]Your quest is almost done[line break],
   Your persistence cannot be reputed[line break].
This key will help you[line break]
   As long as you're not stupid.[line break]".
["Pandora wouldn't like it very much if you opened her chest."]
Before reading the Key Clue:
	display the Figure of Key.


[TODO: Charlie Brown nativity sings hark the herald]

[TV is playing christmas story / remote change]
The Living Room TV is a television in the Living Room.  The description is "The TV has been playing Christmas Story all day long.  You cannot find the remote".
The Living Room TV is switched on.
Before examining the Living Room TV:
	display the Figure of TV2.



Book 3 — The Basement

Section 1 - Basement Landing

The Basement is a room.  The description is "You are in the landing at the bottom of the stairs.  The basement is a big open space centered around the stairs.[line break][line break]Up is the 1st floor.[line break]To the east is the office.[line break]To the west is the Basement Hallway".

Section 2 - Basement Office

The Basement Office is a room.  The description is "There is a computer desk and some random stuff here.[line break][line break]To the south is the TV Room.[line break]To the west is the landing".
The Basement Office is east of the Basement.
[closet]

Section 3 - TV Room

The Basement TV Room is a room.  The description is "There is a TV here with a Switch hooked up to it.[line break][line break]To the north is the Office.[line break]To the west is the Game Room".
The Basement TV Room is south of the Basement Office.
The Basement TV Room is east of the Basement Game Room.
[cable closet]
[TV is playing Rick and Morty / vat of Acid / remote change]
The Basement TV Room TV is a television in the Basement TV Room.  The description is "The TV is playing Rick and Morty; one of the best episodes ever.  You cannot find the remote".
The Basement TV Room TV is switched on.
Before examining the Basement TV Room TV:
	display the Figure of TV1.


Section 4 - Hallway

The Basement Hallway is a room.  The description is "There is a armoir full of blankets here.[line break][line break]To the west is the Bathroom.[line break]To the south is the Game Room.[line break]To the east is the landing.".
The Basement Hallway is west of the Basement.

[water softner]

Section 5 - Bathroom

The Basement Bathroom is a room.  The description is "There is a toilet and a sink here.  There are a couple of cabinets full of makup and various other things.[line break][line break]To the east is the Hallway".
The Basement Bathroom is west of the Basement Hallway.

[mirror]
[toilet]

Section 6 - Game Room

The Basement Game Room is a room.  The description is "...[line break][line break]To the west is a Bedroom[line break]To the east is the TV Room.[line break]To the north is the Hallway".
The Basement Game Room is south of the Basement Hallway.

[TODO: play game]


Section 7 - Bedroom

The Basement Bedroom is a room.  The description is "The bedroom has a bookshelf filled w/ various items[line break][line break]To the east is the Game Room".
The Basement Bedroom is west of the Basement Game Room.
[secret closet]
[closet]
[bookshelf]
The Basement Bed is a fixed in place openable enterable container in Basement Bedroom.


The Secret Room is a room.  The description is "This is a not so secret room.[line break][line break]To the east is the Bedroom.".
The Bookcase is a door. It is west of the Basement Bedroom and east of the Secret Room. The Bookcase is closed and not openable.  The description is "A custom built bookcase is part of the west and north walls.  It is full of books, cups and other personal effects."
[An inconspicuous control panel is a device in the Basement Bedroom.
After switching on the panel:
    say "One of the bookcases slides upward, revealing a passage to the east!";
    now the Bookcase is open.
After switching off the panel:
    say "The secret door closes again.";
    now the Bookcase is closed.]
Instead of pushing the Bookcase:
	now the Bookcase is open;
	say "The part of the bookcase slides back revealing a secret room to the west.  It is dimly lit but you can see tubs and bags filled w/ decorations for all holidays and seasons of the year.[line break][line break]To the west is the Secret Room.".

There is a Reindeer Clue.  The description is "A small note card on brown paper.  There is a Reindeer insignia in the top left corner."
The reading-material of the Reindeer Clue is "You may want to go and ask about a clue from the young lady named 'your mom' . And that's not an urban diss.".
The Reindeer Clue is in the Secret Room.
Before reading the Reindeer Clue:
	display the Figure of Reindeer.


Book 4 — The Upstairs

Section 1 - Hallway


The Second Floor Hallway is a room.  The description is "This is a long narrow hallway.  There are pictures and inspirational sayings on all the walls.  There is a short bookshelf along the wall.[line break][line break]Down is the foyer[line break]To the north is a Bedroom.[line break]To the west is a Bedroom.[line break]To the south is a Bedroom.[line break]To the east is a Bedroom.[line break]To the southwest is a Bathroom."
[put book in bookshelf???]

A Second Floor Hallway Closet is a openable closed container.  The description is "The closet contains various board games, towels, etc... ".
The Second Floor Hallway Closet is in the Second Floor Hallway.

A Hallway Bookshelf is a container in the Second Floor Hallway.  The description is "This bookshelf has it all, kids books, young adult, self help, and more.".


Section 2 - Bathroom

The Second Floor Bathroom is a room.  The description is "This is a small bathroom.  There is a toilet a sink and a mirror.[line break][line break]To the northeast is the hallway."
The Second Floor Bathroom is southwest of the Second Floor Hallway.
[shower / toilet]
A Second Floor Bathroom Shower is a openable open container.  The description is "The shower is empty except for lots of soap and shampoo bottles."
The Second Floor Bathroom Shower is in the Second Floor Bathroom.
[you're in a race, odd time to shower]


Section 3 - Kiki's Bedroom

The Kiki's Bedroom is a room.  The description is "This is a Kikis' bedroom.  There is a messy bed covered in stuffed animals.[line break][line break]To the north is the hallway."
The Kiki's Bedroom is south of the Second Floor Hallway.
[desk]
A fish is an animal in Kiki's Bedroom. The description is "Luna is just swimming away.".

[bed]
[The Pillow is on the Kiki's Bed. ]
The Kiki's Bed is a fixed in place openable enterable container in Kiki's Bedroom.

Visibility rule when looking under Kiki's Bed:
	if the player is carrying a switched on thing (called flashlight):
		say "You shine [the flashlight] under [the noun]...";
		there is sufficient light;
	otherwise:
		say "You probably need a flashlight to see under here, where is that bad boy usually kept?...";
		there is insufficient light.

There is a Tree Clue.  The description is "A small note card on green paper.  There is a Christmas Tree insignia in the top left corner."
The reading-material of the Tree Clue is "Well, you got this one, but you'll not get the rest.  You'll have to solve this riddle to get your next clue.[line break][line break]I am filled up, however never go down.[line break]
When you jump in you get all wet.[line break]
Spend a day with me and you'll have a smile I bet.[line break]
Sometimes I'm cold, other times I am not.[line break]
It's best to use when it is hot.[line break]
What am I?"
The Tree Clue can be found or lost.  The Tree Clue is lost.
Instead of looking under the Kiki's Bed when the Tree Clue is lost:
    move the Tree Clue to Kiki's Bedroom;
    now the Tree Clue is found;
    say "Ah, you found a clue under the bed!".
Before reading the Tree Clue:
	display the Figure of ChristmasTree.


The Kiki's Bedroom Closet is a room.  The description is "This is a Closet.  There hanging clothes in there and several dressers with clothes.[line break][line break]To the east is the Bedroom".
The Kiki's Bedroom Closet is west of the Kiki's Bedroom.

Section 4 - Kyra's Bedroom

The Kyra's Bedroom is a room.  The description is "This is a Kyra's bedroom.  There is a messy bed covered in stuffed animals.  There is a couch, a desk and other various things.  There are 2 closets on the east wall.[line break][line break]To the east is the Hallway."
The Kyra's Bedroom is west of the Second Floor Hallway.

The Kyra's Desk is a supporter in Kyra's Bedroom.  The description is "There is makeup and various other random things on the desk".

The Kyra's Couch is a supporter in Kyra's Bedroom.  The description is "This is a futon like couch, not that comfortable".
A Squishmallow is an object on Kyra's Couch.  The description is "This overly soft stuffed animal is just irresistable so we must buy 100's of them.".

The Kyra's Bed is a fixed in place openable enterable container in Kyra's Bedroom.
A Stuffed Animal is an object in Kyra's Bed.  The description is "This overly soft stuffed animal is just irresistable so we must buy 100's of them.".

A Kyra's Bedroom Closet is a openable closed container.  The description is "The closet contains clothes, clothes and more clothes of all various states, clean, dirty, folded, not folded... ".
The Kyra's Bedroom Closet is in the Kyra's Bedroom.

A Guinea Pig is an animal in Kyra's Bedroom. The description is "Midnight is chomping away on celery.".
[feed carrot from fridge]
Instead of giving Carrot to the Guinea Pig: say "Midnight, says thank you and gobbles up the carrot."; remove Carrot from play


Section 5 - Extra Bedroom

The Extra Bedroom is a room.  The description is "This is the Extra bedroom.  There is a messy bed covered in stuffed animals.  There are barbies and toys all over the place.  There is a closet on the south wall.[line break][line break]To the south is the Hallway."
The Extra Bedroom is north of the Second Floor Hallway.
The Extra Bed is a fixed in place openable enterable container in Extra Bedroom.
There is a junk. The junk can be found or lost. The junk is lost.
Instead of looking under the Extra Bed when the junk is lost:
    move the junk under the Extra Bed;
    now the junk is found;
    say "There is an odd shaped purple animal eating the trash saying 'Mmmmm trash, I love trash!'".

A Extra Bedroom Closet is a openable closed container.  The description is "The closet contains all sorts of stuff.  Opening it will cause all sorts of junk to all out."
The Extra Bedroom Closet is in the Extra Bedroom.


Section 6 - Master Bedroom

The Master Bedroom is a room.  The description is "This is the Master bedroom.  There is a neat bed with a Rick and Pickle Rick plush on it.  There is a TV and 2 dressers.  There is a closet on the east wall.[line break][line break]To the south is the Master Bathroom.[line break]To the east is the Master Closet[line break]To the west is the Second Floor Hallway."
The Master Bedroom is east of the Second Floor Hallway.
The Master Bed is a fixed in place openable enterable container in Master Bedroom.

The Master Closet is a room.  The description is "This is the Master Closet.  There hanging clothes in there and several dressers with clothes.[line break][line break]To the west is the Master Bedroom".
The Master Closet is east of the Master Bedroom.

The Master Bathroom is a room.  The description is "This is the Master Bathroom.  There is a couple of sinks with a large mirror.  There is a shower a bathtub and a toilet.  There are several barbies in the tub.[line break][line break]To the north is the Master Bedroom".
The Master Bathroom is south of the Master Bedroom.

[closet container]
A Master Bathroom Closet is a openable closed container.  The description is "The closet contains clothes, shoes, etc...".
The Master Bathroom Closet is in the Master Bathroom.


[TODO: Place this somewhere]
A Strange Ornate Chest is a locked container.  The description is "Pandora's Chest.  There is an old looking lock on the chest, keeping it's contents safe."
[The Strange Ornate Chest is in the Master Closet.]
The Skeleton Key unlocks the Strange Ornate Chest.
The Chest Clue is a object. The description is "A small note card on orange paper.  There is a chest insignia in the top left corner.".
The reading-material of the Chest Clue is "What are you waiting for, you won the game, go claim your prize in the real world. Go get your present in the Master Bedroom Closet.".
The Chest Clue is inside the Strange Ornate Chest.
Before reading the Chest Clue:
	display the Figure of Chest.
[Before opening the Strange Ornate Chest:
	display the Figure of Chest.]
After reading the Chest Clue:
	say "Congratulations you won the game.!";
	end the story.
[	if the player's forename is "Calista":
		say "You wazzup";
		rule succeeds;
	otherwise:
]

A CandyCane Clue is a object. The description is "A small note card on blue paper.  There is a candy cane insignia in the top left corner."
The reading-material of the CandyCane Clue is "All right, gotta hand it to you, doing pretty good so far.  Let's make this more difficult.[line break][line break]I Start with M, end with X and have never ending amount of letters. What am I?"




Book 5 - Outside

Section 1 - Front Yard

The Front Yard is a room.  The description is "The front of the house is lit up nicely with some awesome led lights that are flashing.  The driveway is empty.  There is a mailbox at the end of the driveway.[line break][line break]To the south is the house."

A Mailbox is a openable closed container in the Front Yard.  The description is "1581 Charleston Dr.".

There is a Snowman Clue.  The description is "A small note card on red paper.  There is a Snowman insignia in the top left corner."
The Snowman Clue is in the Mailbox.
The reading-material of the Snowman Clue is "The next clue is not so obvious.  It is hidden in a secret room named after our favourite mystery solving dog.".
Before reading the Snowman Clue:
	display the Figure of Snowman.


Section 2 - Back Yard

The Back Porch is a room.  The description is "The back porch has a celiing fan and several wicker chairs.  It looks comfortable but probably too cold to hang out.[line break][line break]To the north is the House.[line break]To the south is the Outside."

The Back Yard is a room.  The description is "The back of the house has a pool, a large tree and a dog.  There is a chain fence surrounding the yard.  There is a gate in the fence.[line break][line break]To the north is the Back Porch.[line break]To the southwest is the Pool Area (behind a gate).[line break]To the northeast is the Neighborhood (behind a gate)."
The Back Yard is south of the Back Porch.
The Neighborhood is a room.  The description is "This is the open space of the neighborhood.[line break][line break]To the south is the Back Yard".

A Patches is an animal in Back Yard. The description is "Patches is getting cold and hungry."
The Fence Gate is a closed door.  The Fence Gate is northeast of the Back Yard and south of the Neighborhood.
After opening the Fence Gate for the first time:
	now the Fence Gate is open;
	say "You let Patches go, now she's lost forever.";
	move the Patches to the Neighborhood.


A Oak Tree is a supporter in the Back Yard.  The description is "A large tree has a long yellow rope tied to it.".
[TODO: add climb rope]

[Pool]
The Pool Area is a room.  The description is "There is a Deck and Swimming Pool behind a gate.[line break][line break]To the northeast is the Back Yard".
The Pool Area is southwest of the Back Yard.

A Deck is a enterable supporter in the Pool Area.  The description is "The deck next to the pool has a gate which is closed."
A Swimming Pool is a open container in the Pool Area.  The description is "The pool is quite cold but feel free to jump in if you want.".

The Net is an object on the Deck.
A CandyCane Clue is a object. The description is "A small note card on blue paper.  There is a candy cane insignia in the top left corner."
The reading-material of the CandyCane Clue is "All right, gotta hand it to you, doing pretty good so far.  Let's make this more difficult.[line break][line break]I Start with M, end with X and have never ending amount of letters. What am I?"
Before reading the CandyCane Clue:
	display the Figure of CandyCane.

Instead of entering the Deck:
	move the CandyCane Clue to the Swimming Pool;
	say "You can now see something in the bottom of the pool.";
	continue the action.

[need to take net, then take clue]
Instead of taking the CandyCane Clue when the player does not have the Net:
  say "I don't know, that water looks pretty cold, you may want to try another way to take it.".

Instead of taking the CandyCane Clue when the player has the Net:
  say "You use the Net to scoop up the Clue.";
  continue the action.


Book 6 - Game Rules

Section 1 - Turn Checks

SHOWCHEST is a number variable.
[GPTAKEN is a number variable.]
When play begins:
	now SHOWCHEST is 0.
[	now GPTAKEN is 0.]

Every turn:
	if the Guinea Pig is in Back Yard:
[		if GPTAKEN is 0:
			increase GPTAKEN by 1;]
		say "OMG, NO!!!!!!   An Eagle just swooped down and took the Guinea Pig.";
		remove the Guinea Pig from play.
Every turn:
	if the Christmas Book is in the Hallway Bookshelf:
		say "Thanks for picking up for me, you know what, you're all good.  Go get your present in the Master Bedroom Closet.";
		end the story.
Every turn:
	if the player is carrying the Snowflake Clue:
		if the player is carrying the Tree Clue:
			if the player is carrying the CandyCane Clue:
				if the player is carrying the Snowman Clue:
					if the player is carrying the Reindeer Clue:
						if the player is carrying the Key Clue:
							if SHOWCHEST is 0:
								increase SHOWCHEST by 1;
								say "As you pick up the last clue, they all start to glow.  They float up in the air in front of you, there's a big flash and the clues disappear and a Strange Ornage Chest appears.";
								move the Strange Ornate Chest to the player;
								remove the Snowflake Clue from play;
								remove the Tree Clue from play;
								remove the CandyCane Clue from play;
								remove the Snowman Clue from play;
								remove the Reindeer Clue from play;
								remove the Key Clue from play.
								[end the story.]

[

]
