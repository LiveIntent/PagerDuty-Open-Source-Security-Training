Title:
Lesson 1 | Identity
---

Lesson Notes:
:dart: Intended Audience: All employees, regardless of function.
:dart: Intended Frequency: The goal of today's training is to make sure that we can maintain and build customer trust by having a staff who are well trained against the most common security threats that we face.

---

Lesson Content:



---

External resources:



---

### Identity

_<input type="checkbox" id="092" /><label for="092">![]()</label>_

We're going to switch gears now and talk about physical security and identity. Hopefully this will be a fun section, because just like last year when I [taught you all how to crack passwords](), this year I'm going to teach you all how to break into our offices.

But first let's start by talking about badges.

---

### Badges Aren't Perfect

<input type="checkbox" id="093" /><label for="093">![]()</label>
_093. Just because they have a badge, doesn't mean they're authorized._

Just because someone has a badge, it doesn't mean they're meant to be there. As an example, the badge I'm wearing right now says my name is our Director of Infrastructure, Arup Chakrabarti. It looks nothing like our real badges, but it does have our company logo on it, and I'm wearing it on a PagerDuty branded lanyard that I picked up at a conference. It even has a little gold star that says "100% secure", so that you can tell it's legit.

---

### Badge Photos

<input type="checkbox" id="094" /><label for="094">![]()</label>
_094. Badge photos aren't massively useful._

Even though it doesn't look like our real badges, it has my photo on it though, so it must be fine, right?

Photos on badges are like the "from" address in emails. Just because it looks correct doesn't mean that it's the right person. Anyone can print their own badge with their own photo on it.

Case in point, my _real_ company ID badge says my name is that of our CEO, Jennifer Tejada. This isn't just a sticker I've put over the badge either (which would also work to be honest), this is a real plastic card.

???+ comment "Presenter's Comment"
I may have had access to our actual badge printer for a little while.

You can print whatever you want on these badges, so just because someone is walking around with one that looks correct and the photo matches them, it doesn't mean you should ignore them if they're doing something sketchy. If someone is sitting at your friends desk and using their computer and it's not your friend, don't ignore that just because they have a badge. Come and tell security straight away!

???+ warning "Redacted Content"
This slide was changed from the one originally presented to use Pagey as the image and to change the color we use for our badges. Originally it was my real badge. I'd rather not end up like that [LifeLock CEO]()(https://www.wired.com/2010/05/lifelock-identity-theft/) so figured it should at least be a bit harder to impersonate me than just printing this slide onto a badge and putting on an over-the-top British accent.

---

### RFID Badges

<input type="checkbox" id="095" /><label for="095">![]()</label>
_095. RFID badges are secure, right?_

OK, so photos on badges aren't foolproof. But our badges use RFID (Radio-frequency Identification), and those are definitely secure. Those cards that say ProxCard II on them. There's no way you could clone or steal one of them, right?

---

### Proxmark 3

<input type="checkbox" id="096" /><label for="096">![]()</label>
_096. Proxmark3 DevKit. [Reference]()_

Well, if you have $250 to spare, you can get one of [these cool kits]() that let you clone cards just by getting near them.

---

### Keysy

<input type="checkbox" id="097" /><label for="097">![]()</label>
_097. Keysy RFID duplicator. [Reference]()_

You definitely couldn't just spend say, $40, on an RFID duplicator like [this one here](), and clone your ID badge to a writeable RFID card and then get into the office with it. Definitely not possible.

???+ comment "Presenter's Comment"
At this point I showed folks my work badge cloned to both a key fob and a writable RFID card.

---

### Staff Doors

<input type="checkbox" id="098" /><label for="098">![]()</label>
_098. Only staff can open our doors, right?_

OK fine, so someone could clone our badges if they get close enough with one of those devices. But we have cameras, we have security on our front desk, only legitimate staff can get through our doors, right? You can't get through our doors unless you know codes or secrets or something.

Well that depends on how secure the doors are.

---

### Code 2861

<input type="checkbox" id="099" /><label for="099">![]()</label>
_099. Code 2861. [Reference]()_

And doors are only as secure as the humans using them.

Thankfully we don't do things like this (as far as I know), and if you do see something like this please let us know straight away. I have seen things like this out in the wild before.

---

### Push Button to Exit

<input type="checkbox" id="100" /><label for="100">![]()</label>
_100. Push button to exit. [Reference]()_

But this looks familiar. We have these same signs and setup in our own offices. Do you think the door will open if you push this button?

Well, yes, yes it will. Ours do too.

We have to have those buttons by law, since there are no fire exits in the non-secure part of our offices. We can't have someone trapped in the elevators if there's a fire just because they don't have an access card.

But if you push the button in our offices it sets off a very big and loud alarm, and the door doesn't open right away. It gives us enough time to go and see what's going on and make sure someone doesn't just hit the alarm and then walk in and disappear in the panic.

For other places, it may not be the case. You can push the button and then the door opens and no alarm goes off.

---

### Keep Out

<input type="checkbox" id="101" /><label for="101">![]()</label>
_101. Keep out._

At that point it's basically the equivalent of a "Keep Out" sign and isn't going to change anything, people will just use it to get in.

I've visited data centers before where they will have all sorts of biometric security to get in the front door, but once you're inside there's an emergency door to the parking lot that's propped open so people can go and have a smoke break more easily. Which door do you think an attacker would end up using?

---

### Door Bypass with Air

<input type="checkbox" id="102" /><label for="102">![]()</label>
_102. Door bypass with can of compressed air. [Reference]()_

So what if we don't have a badge, don't want to set off an alarm, but we still want to get through our doors? You've probably noticed that our doors have sensors on our side of them, so that when you walk up to the door from the inside they'll open for you. There's a little sensor at the top, where maybe a little red light turns on and the door clicks open.

Have you ever seen these before around the office? Little cans of compressed air to clean keyboards. Have you ever tried turning them upside down when you spray them?

It shoots out a cloudy jet of very cold air. This will open most of those door sensors from the other side. You can just put the nozzle in the gap between the doors, or even underneath the door, spray it for a second and the sensor will trigger and the door will open. You don't look too out of place walking around an office with a keyboard cleaner either, as demonstrated by the fact I was walking around with this can earlier today and just like with my "100% secure" legit looking ID badge, no one really took any notice.

The screenshot here is from [a video by Samy Kamkar](), who you might know posts a lot of videos online about penetration testing, electronics, and things like that. In the video it shows him bypassing the request-to-exit sensor (REX sensor) of a door and showing this technique working out in the wild. After this session I'd be happy to show it working on our own office doors too if you don't believe me that it works.

---

### Door Bypass with Whiskey

<input type="checkbox" id="103" /><label for="103">![]()</label>
_103. Door bypass with some whiskey. [Reference]()_

There are other fun ways to do this too. This is a screenshot from [a video of Deviant Ollam breaking into a bank]() by spit-taking some whiskey through the gap in the doors. It really is just like it sounds, he takes a sip of whiskey and spits it through the gap, then the doors open. Deviant Ollam has [lots of other videos]() of things like penetration testing and lock picking, and are well worth checking out.

---

### Door Sensors Aren't Perfect

<input type="checkbox" id="104" /><label for="104">![]()</label>
_104. Door sensors aren't perfect._

So door sensors, they're great right? The key takeaway here is that door sensors aren't perfect. Don't assume people are authorized to be there just because they're walking around the office or wearing a badge. It doesn't mean their badge is legitimate, or that they came through a door by legitimate means. Still stay on alert and stay suspicious.

---

### Following

<input type="checkbox" id="105" /><label for="105">![]()</label>
_105. Check who's following you._

When you do walk through the doors, check who's following you. Tailgating (also called Piggybacking) is one of the easier ways to get into an office building. This is when someone follows you through a door without swiping or tapping their badge. So just be aware of who's following you in on your card swipe and try not to let others follow you unless you know who they are.

---

### Don't Let Others Follow

<input type="checkbox" id="106" /><label for="106">![]()</label>
_106. Don't let someone follow on your entry._

If it's someone you don't recognize, ask them to tap their card. If you get asked by someone else to tap your card, please don't give them a hard time and just tap your card. Don't be offended, say hello and make a new friend!

If you're uncomfortable asking a stranger to tap their badge, or you ask and they refuse to tap their badge, come and tell security at the front desk. Don't put yourself into a situation where you feel uncomfortable, and under no circumstances should you ever try to physically stop or restrain someone from entering our offices.

---

### Suspicious

<input type="checkbox" id="107" /><label for="107">![]()</label>
_107. If you're suspicious of someone, tell us._

If you're walking around our offices and see something sketchy or suspicious, see someone pretending to be someone else, etc. Please come and tell security and we'll come and sort it out. Either tell security at the front desk, or anyone from our facilities team, security, or even HR. Again, don't put yourself in danger or any situation where you feel uncomfortable.

---

### Desk Drawers

<input type="checkbox" id="108" /><label for="108">![]()</label>
_108. Desk drawers are secure, right?_

OK, so our doors aren't very secure. Our badges aren't very secure. Surely our desk drawers are secure? We can lock things in those and they're safe, right?

I think you can probably tell where this is going.

---

### Lockpicks Aren't Hard

<input type="checkbox" id="109" /><label for="109">![]()</label>
_109. Lockpicks aren't as hard to use as you may think._

Lockpicks aren't as hard to use as you might think and desk drawers can be pretty easy to get in to.

---

### Lockpicks Are Legal

<input type="checkbox" id="110" /><label for="110">![]()</label>
_110. Lockpicks are legal (mostly). [Reference]()_

A lot of people seem to think you need a license to use lockpicks, that you need some sort of locksmith license. Not true, they're perfectly legal in most places.

???+ comment "Presenter's Comment"
I'm not a lawyer, this is not legal advice, please don't go and start using lockpicks on things just because someone on the internet said it was OK.

---

### Intent

<input type="checkbox" id="111" /><label for="111">![]()</label>
_111. The need to show criminal intent. [Reference]()_

In California at least, you need to show intent to commit a felonious act with them. If you're just walking around with some lockpicks, you're not doing anything wrong. If you're putting them into someone else's locks, then you're maybe going to get arrested.

---

### Lockpicks on eBay

<input type="checkbox" id="112" /><label for="112">![]()</label>
_112. Lockpicks on eBay. [Reference]()_

OK, but these are professional tools used by locksmiths, surely they must be really expensive? Well, for some of the professional ones probably. But you can _pick_ up (get it?) some cheap ones on eBay for about $10 and they'll work well enough for things like our desk drawers.

---

### Practical Lock Picking

<input type="checkbox" id="113" /><label for="113">![]()</label>
_113. "Practical Lock Picking" on Amazon. [Reference]()_

Then for $30 on Amazon you can get [a book that teaches you how to do it]() (Written by the same Deviant Ollam from the opening-a-bank-door-with-whiskey video earlier). Again, this takes us back to our "bored engineer with $30 and an Amazon account" threat actor.

Now it's all well and good me telling you this is possible, but I feel like I cheated you a bit with not being able to do the SMS demo earlier, so I thought it would be fun to teach you all how to pick locks.

After the training, I'll also have a bunch of locks and picks up here on stage if you'd like to come and play with them. Some of them are transparent so you can see what's going on inside them, and some are regular chunky padlocks you'd probably use to lock things up yourself.

---

### Lock Internals

<input type="checkbox" id="114" /><label for="114">![]()</label>
_114. Lock construction. [Reference]()_

So let's start by looking at the inside of a lock, specifically a [cylinder pin tumbler]() lock. There are lots of other types of locks, but this is the one you'll probably be most familiar with. This diagram shows the lock from the side.

There are some technical names for the various parts, but you don't really need to know them to understand how the lock works. All you really need to know is that there are some springs which push down some pins into the cylindrical part of the lock that turns (called the "plug").

---

### Shear Line

<input type="checkbox" id="115" /><label for="115">![]()</label>
_115. Shear line of a lock. [Reference]()_

One important concept is something called the "Shear Line". When all the pins line up on that line, the drive pins (the blue ones in this diagram) are outside of the bit that turns, while the key pins (the yellow ones in the diagram) are entirely within the bit that turns. This means that the plug (the brown section in the diagram) is free to turn and the lock can open.

If the pins do not line up on the shear line, then the lock is mechanically stopped from opening, as the pins will block the plug from turning.

---

### Correct Key

<input type="checkbox" id="116" /><label for="116">![]()</label>
_116. The correct key._

So when you have the correct key, all of those pins line up along the shear line. The impressions on the key match the pattern of the key pins (this is why they're called the key pins), and the lock is free to turn and open.

You may also notice that there's a number on the key here, you'll sometimes see this on your own keys. That's called the "bitting code", and is a numerical representation of the pattern on the key. So if I have that number, I can copy your key. If you look at your house keys for example, they'll probably have a 6 digit bitting code on them, that's basically the code to get into your house.

???+ comment "Presenter's Comment"
It's true that you will need to know the brand of key too (Schlage, Kwikset, etc), but there are only so many and they're easy to identify at a quick glance once you know what to look for.

So it's a good idea not to leave your keys out where someone can take a photo of them. Even if I don't quite get the pattern in my photo, or the angle is wrong, if I can get that number then that's all I'll really need.

---

### Incorrect Key

<input type="checkbox" id="117" /><label for="117">![]()</label>
_117. An incorrect key._

If you use the wrong key, the pins don't line up on the shear line and the lock physically can't open.

So that's typically how a lock of this style works. Now let's look at how we can open it without the correct key.

---

### Tension Wrench

<input type="checkbox" id="118" /><label for="118">![]()</label>
_118. Tension wrench. [Reference]()_

In order to pick a lock, we need two tools. The first is something called a "Tension Wrench", or a "Torsion Wrench". It's a small L-shaped piece of metal. The intention is that you stick the short part into the lock and then use the longer part to try and turn the lock as if there was a key in there.

It has the same effect as if you put the wrong key in and tried to turn it. But with a key in there you wouldn't be able to put anything else in the lock. With a tension wrench, there's plenty of room for you to put another tool into the lock as well. A tool such as...

---

### Pick

<input type="checkbox" id="119" /><label for="119">![]()</label>
_119. A pick._

...the pick itself, which is just a piece of metal with a part on the end that sticks out. There are all sorts of shapes of lockpick with various different patterns on the end, and they can all be used for different things. Here I'm just going to show a basic one (called a "Short Hook").

And yes, you can even use paper clips for this if you want to be just like MacGyver! That's not a made-up Hollywood thing. You'll need two paperclips to pick a lock, but you can indeed do it with paperclips if they're strong enough.

OK, so we have our tension wrench trying to turn the lock, and we've put a pick inside the lock. What's next?

---

### Push Pins

<input type="checkbox" id="120" /><label for="120">![]()</label>
_120-124. Push pins up._

While applying gentle pressure to try and turn the lock with the tension wrench, use the pick to push up the pins one at a time.

---

### Pin Moves Freely

<input type="checkbox" id="124" /><label for="124">![]()</label>
_124. Some pins move freely._

If the pin drops back down freely, that means nothing has changed. That pin isn't doing anything right now, and we can move on to the next pin instead.

---

### Pin Getting Stuck

<input type="checkbox" id="125" /><label for="125">![]()</label>
_125-127. One pin will get stuck._

Eventually you'll get to one pin where after you push it up, you'll hear a little click, and you'll feel the lock turn ever so slightly. Keep applying gentle pressure to the tension wrench when this happens, don't let go otherwise the pin will drop back down.

The reason one pin will stay up is because there are always going to be some tolerances in the machining of the lock itself. Because you are applying pressure with the tension wrench, the pin stays up as the plug turns just a little bit and blocks the pin from dropping back down. If you were to let go of the tension wrench the plug would return to it's original position and the pin would drop back down.

---

### First Pin Held

<input type="checkbox" id="127" /><label for="127">![]()</label>
_127. First pin is now held._

You'll now have one pin held in place above the shear line. So what do we do next?

---

### Repeat

<input type="checkbox" id="133" /><label for="133">![]()</label>
_128-135. Repeat on other pins._

We now repeat the process with all the other pins. You may find some drop back down again, if that happens just move on to the next one. Eventually you'll reach another one that stays up and you'll feel the plug turn slightly.

If you do everything correctly (and it's not a lock with special pins that make picking the lock harder), you'll reach a point where all the pins are now held above the shear line.

---

### Lock Open

<input type="checkbox" id="136" /><label for="136">![]()</label>
_136. Once all are done, the lock will open._

When all the pins are stuck above the shear line, the plug will turn and the lock will open (thanks to the pressure being applied with the tension wrench). You've just picked a lock!

???+ comment "Presenter's Comment"
I did a quick live demo of this using a lock to demonstrate that you can do it from feel alone in about a second with some types of locks.

It can be very easy to do, and great if you like puzzles. Each lock is a new challenge. So feel free to come up to me afterwards if you want to play with various locks and picks to try it out for yourself. I have big chunky locks, transparent locks, various different picks and so on. I'll think you'll be amazed at how easy it is.

???+ comment "Presenter's Comment"
You can also [view the full animation of the lockpicking section (20MB GIF)]()(/slides/for_everyone_part_ii/animations/full_lockpicking_example.gif).

---

### Three Laws of Lockpicking

<input type="checkbox" id="137" /><label for="137">![]()</label>
_137. The three laws of lockpicking._

I should mention that there are a few rules to follow if you do want to start playing with lockpicking. You can't just go around opening locks everywhere.

1. Please never pick or attach a lock you don't own yourself, or that you do not have explicit permission to pick. All of the ones on stage here are mine, and you have my permission to pick them.

1. And don't pick a lock that's actually being used to lock something up. Because if you damage the lock, you've now got to cut it off to get to the thing being locked.

And the third law there is the third law of robotics... because I have to have a little fun with the slides.

---

### Locks Are Still Good

<input type="checkbox" id="138" /><label for="138">![]()</label>
_138. Locks are still worth using._

So what am I saying with all of this? **I am absolutely not saying don't use locks**. That is not the key takeaway here. **Locking things is better than not locking them**.

I just wanted to point out that all of these things are not foolproof, and they're not designed to be. Our ID badge photos, RFID badges, door sensors, cloning cards, the locks on your drawers, etc. All of these can be overcome by a sufficiently advanced attacker... or sometimes a bored person with $30.

But all of these things together are what we call ["defense in depth"](). If I'm going to break into an office in order to steal a bunch of laptops, am I going to go and pick the lock on everyone's desk drawer to hunt for laptops? No, I'm just going to walk around and take the ones I can see out in the open and walk off with them.

In that scenario, we have successfully defended against this attack by using the crappy locks on our desk drawers.

My point is that I'm not trying to say these things are completely ineffective, but together they can present an effective solution to the most likely scenarios.

The corollary is that if you are specifically targeted, then things can start to fall apart. Let's say you put $10,000 in cash in your office drawer and someone knows that, they're not going to have a hard time picking your lock and getting it. These controls would be ineffective against that very specific targeted attack. So it always depends on your threat model.

The idea of defense in depth is to have multiple layers of defenses, not necessarily there to completely prevent an attack, but rather to slow down an attack enough for it to either be spotted or to frustrate the attacker enough to give up.

---

### Always Lock Computers

<input type="checkbox" id="139" /><label for="139">![]()</label>
_139. Always lock your computer._

Speaking of locks, always lock your computers. Lock picks do not work on computers... I don't think they do anyway.

When you're away from your desk, please please please lock your computers. We've all done it, we've walked away and left our computer unlocked. I've done it too. Just try and remember not to do it.

Everyone makes mistakes, so if you see someone else's computer unlocked please resist the urge to troll them. We used to go on Slack and type "I don't care about security" in the #security channel, but that doesn't really set the working environment we want. In the past people have also gone and changed various desktop background images and so on. It's all well meaning, but please don't do any of that stuff. If you do find someone's computer unlocked, just lock it for them and then ping them on Slack to say

> "Hey, I locked your computer for you, you'd left it unlocked".

That's the nice thing to do. Shaming people because they made a mistake is never going to be an outcome we want.

---

### Report Lost/Stolen Items

<input type="checkbox" id="140" /><label for="140">![]()</label>
_140. Immediately report lost/stolen items._

Speaking of laptops, if you lose any of your company equipment, even your badges, report it to us immediately. If you lose your laptop on a Friday night out, don't wait until Monday morning to let us know. Page us on Friday as soon as you see it's gone. If you're not sure how to page us, there's this great tool called PagerDuty that can help with that. I think our sales team can set you up with an account for a reasonable price.

You can also send us an email, but those page with a lower priority, so paging is the best bet. But if you've just lost your device then you may not be set up for that. So just contact us in any way you're able to do so and we'll all do our best to get on it as quickly as possible.

Even if you lose your personal device, and that device had access to any PagerDuty things such as email, let us know and we can remotely block it from all our systems. We can also help you to protect your phone and walk you through the steps on how to get things back up and running and secure on a new device and protect any other accounts you may have had on your device.

As I said before, we're not just here to keep PagerDuty safe, but to help you all stay safe too.

---

### Pagey's Summary - Physical Security and Identity

<input type="checkbox" id="141" /><label for="141">![]()</label>
_141. Pagey's summary of identity and physical security._

So that was a lot of information on identity and physical security. I hope you learned something interesting. Here's Pagey's quick recap of the important points,

* Don't let people piggyback or tailgate your entry into our offices.
* If you're suspicious of someone, please report it to us.
* Use locks, but remember they only keep honest people out.
* Do lock your computers when you're not at your desk. (You can even get apps that do it for you, they detect when you walk away with your phone and lock your computer for you, so that could be worth looking in to).
* If you lose anything, even if you think you just misplaced it and it wasn't necessarily stolen, please still let us know. We can always re-activate things later if you end up finding them.

---

Lesson Scenario:
What is security theater?

- <input type="checkbox"> `This is a production house in London focused on digital forensic stories.`
- <input type="checkbox"> `This is where you spend time and effort on things which merely give the _appearance_ of improved security, without actually providing it. `
- <input type="checkbox"> `Similar to broadway, these are high quality theatrical productions focused on cybersecurity.`
- <input type="checkbox"> `As a security exercise, this is where small groups act out real world security scenarios.`

<div class="reveal-answer">
	<button class="button">Reveal Answer</button>
	<blockquote><p>Security theater is purely for show and does not improve security.
</p></blockquote>
