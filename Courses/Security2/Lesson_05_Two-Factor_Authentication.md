Title:
Lesson 5 | Two-factor authentication (2FA)

---

Lesson Notes:
:dart: Always use two-factor authentication. 
:dart: Avoid using SMS if you can. And we strongly recommend U2F keys.

---

Lesson Content:

2FA, also called Two-Factor Authentication, is one of the best things you can do to improve your security online from an authentication point of view.

It could be something you know, like a password or security question answers. Something that's stored in your head essentially.

It could be a physical thing, like a USB stick or a phone.

Or it could be something you are, some form of biometrics, a fingerprint or iris scan for example.

Avoid using SMS for two-factor authentication, though using SMS is better than not using 2FA at all.

---

External resources:

### Two-Factor Authentication

_<input type="checkbox" id="046" /><label for="046">![]()</label>_

So let's now talk about two-factor authentication instead. I touched on this last time, but now I'm going to go into a lot more detail. 2FA, also called Two-Factor Authentication, is one of the best things you can do to improve your security online from an authentication point of view.

---

### Three Factors

<input type="checkbox" id="047" /><label for="047">![]()</label>
_047. The three types of evidence. [Reference]()_

It comes down to three types of evidence that you can provide, called factors of authentication. It's basically a fancy way of saying "Types of evidence to prove you are who you say you are".

---

### Knowledge, Possession, Inherence

<input type="checkbox" id="048" /><label for="048">![]()</label>
_048. Knowledge, Possession, and Inherence. [Reference]()_

So there's three types, and they each have technical terms, called Knowledge, Possession, and Inherence.

---

### In Plain English

<input type="checkbox" id="049" /><label for="049">![]()</label>
_049. In plain English. [Reference]()_

In plain English, that is "Something you know", "Something you have", and "Something you are". Those are the three types of evidence you can provide to prove that you're you.

---

### Factor Examples

<input type="checkbox" id="050" /><label for="050">![]()</label>
_050. Examples of the different factors._

It could be something you know, like a password or security question answers. Something that's stored in your head essentially.

It could be a physical thing, like a USB stick or a phone.

Or it could be something you are, some form of biometrics, a fingerprint or iris scan for example.

One of the ways to tell if something is "Something you are" is that you can't really change it. You can't change your fingerprint, or your face, for example. Well... I guess you could with surgery. Let's just say it's very difficult to change those things. Unless you're [Nicolas Cage and John Travolta]() of course.

---

### 2FA or Not 2FA

<input type="checkbox" id="051" /><label for="051">![]()</label>
_051. 2FA or not 2FA, that is the question._

So we're going to play a quick game now, called "2FA or not 2FA". I'm going to show you some factors of authentication and you shout out if it's 2FA or not 2FA.

---

### Password + TOTP

<input type="checkbox" id="052" /><label for="052">![]()</label>
_052. Password + TOTP = ?_

Let's start with a password and putting in a six digit number from your phone. 2FA or not 2FA?

---

### Password + TOTP = 2FA

<input type="checkbox" id="053" /><label for="053">![]()</label>
_053. Password + TOTP = 2FA._

Yes, this is 2FA. It's something you know, your password, and something you have, your phone. This is good authentication as it's verifying you based on two different types of evidence.

---

### Password + Yubikey

<input type="checkbox" id="054" /><label for="054">![]()</label>
_054. Password + Yubikey = ?_

What about a password and a USB key (such as a [YubiKey]() or [SoloKey]())?

---

### Password + Yubikey = 2FA

<input type="checkbox" id="055" /><label for="055">![]()</label>
_055. Password + Yubikey = 2FA._

Yes, this is the same thing. Something you know and something you have.

---

### Fingerprint + FaceID

<input type="checkbox" id="056" /><label for="056">![]()</label>
_056. Fingerprint + FaceID = ?_

OK, so what about fingerprint and FaceID?

---

### Fingerprint + FaceID = Not 2FA

<input type="checkbox" id="057" /><label for="057">![]()</label>
_057. Fingerprint + FaceID = Not 2FA._

This is not 2FA. Both of these factors are something you are, so this is not two-factor authentication. This is two different checks against the same type of evidence. It could be considered more secure than only checking one of them, but it is not as strong as checking different factors.

---

### Password + Security Question

<input type="checkbox" id="058" /><label for="058">![]()</label>
_058. Password + Security Question = ?_

What about a password and an answer to some security questions?

---

### Password + Security Question = Not 2FA

<input type="checkbox" id="059" /><label for="059">![]()</label>
_059. Password + Security Question = Not 2FA._

Correct, this is not 2FA.

As with the previous one, this might be considered a stronger form of one-factor authentication, but this is **absolutely not** two-factor authentication, as they're both the same type of evidence.

I'll admit that it's a bit of a pet peeve of mine when companies claim to implement "two-factor authentication" when they really don't.

---

### Password + SMS

<input type="checkbox" id="060" /><label for="060">![]()</label>
_060. Password + SMS = ?_

OK, final one, what about password and an SMS text message?

---

### Password + SMS = Not Good

<input type="checkbox" id="061" /><label for="061">![]()</label>
_061. Password + SMS = Not Good_

Correct, it is 2FA, but it's also not good, and now we're going to talk about why.

I know, trick question, that wasn't very fair.

---

### Avoiding SMS

<input type="checkbox" id="062" /><label for="062">![]()</label>
_062. We want to avoid SMS._

Using SMS as a second factor, while technically two-factor authentication, is something we want to avoid whenever possible.

---

### Why Avoid SMS

<input type="checkbox" id="063" /><label for="063">![]()</label>
_063. "Why can't we use SMS for 2FA?"_

We recently disabled SMS as an allowed method of authentication across all of our tools, and _literally everyone_ asked "Hey! Why can't we use SMS for 2FA?".

OK, so some of you asked. But it's a perfectly valid question and one that I wanted to give you a better answer on than just "Because we say so".

---

### SMS Can Be Intercepted

<input type="checkbox" id="064" /><label for="064">![]()</label>
_064. SMS can be intercepted. [Reference]()_

The reason is because SMS can be intercepted and read by anyone.

Well, maybe not _anyone_, that's a bit of an exaggeration, but it's certainly not considered a secure method of authentication by modern standards.

---

### Demo Banned

<input type="checkbox" id="065" /><label for="065">![]()</label>
_065. Demo banned._

What I was going to do at this point was show you a cool demo with this antenna I brought with me and some software that lets me control it. I was going to live intercept and decrypt SMS messages out of thin air for you all to see.

But on the advice of legal counsel... the demo was banned for being far too awesome... and quite probably illegal. So I'm sorry about that.

---

### Signalling System 7

<input type="checkbox" id="074" /><label for="074">![]()</label>
_074. Signalling System #7. [Reference]()_

The real reason we don't want to use SMS for two-factor authentication is because of a vulnerability in something called ["Signalling System 7"](). This is a set of protocols which all phone carriers throughout the world use to communicate with one another.

---

### Intercepting Calls with CAMEL

<input type="checkbox" id="075" /><label for="075">![]()</label>
_075. Intercepting calls with CAMEL. [Reference]()_

Unfortunately, SS7 has vulnerabilities which can allow attackers to intercept your messages and voice calls without either side (you or your phone company) knowing that it's happening. I'm not going to expect you to read everything on this slide here, this is a screenshot from a [talk by Tobias Engel of the Chaos Computer Club from 2014]() which goes into much more detail on it.

But essentially, someone can sit between your phone and the phone company and intercept all voice communication and SMS, and get your location, without either side knowing that they're doing it.

???+ comment "Presenter's Comment"
There are methods you can use to detect if these vulnerabilities are being exploited. But unless you actually look for them, you wouldn't know that they're being exploited.

This isn't just a theoretical attack either, this has actually been exploited in the real world. In [May 2017](), O2 (a mobile provider in Europe) confirmed that SS7 vulnerabilities had been used and exploited to bypass two-factor authentication in order to withdraw money from bank accounts.

In a lot of cases, you don't even need to go down the route of exploiting SS7 vulnerabilities. Sometimes a much easier path is to simply social engineer the phone company in order to perform a [SIM swap](). I call your mobile provider and pretend to be you, telling them I've bought a new SIM card. They transfer your service to my SIM card and now I can get all of your two-factor codes.

SMS is not a secure method for the purposes of two-factor authentication.

---

### Avoid SMS for 2FA

<input type="checkbox" id="076" /><label for="076">![]()</label>
_076. Avoid SMS for 2FA._

Pagey's Key Takeaway is to avoid using SMS for two-factor authentication. I've resisted saying "Never use SMS" here, and rather just say "Avoid". **SMS two-factor authentication is still better than not using any two-factor authentication at all**. If you have a choice of SMS 2FA or no 2FA, then definitely use SMS 2FA. It will still add an extra layer of protection. It's just not as secure as other methods if you have the choice.

---

### TOTP Codes

<input type="checkbox" id="077" /><label for="077">![]()</label>
_077. TOTP codes._

Speaking of other methods. TOTP codes, Time-based One Time Password codes. These are those 6 digit numbers you get on your phone that always...

---

### TOTP Codes (2)

<input type="checkbox" id="078" /><label for="078">![]()</label>
_078. TOTP codes._

...seem to have about 3 seconds left so by the time you open up your phone and start to type the number into the website it disappears so you have to start again...

---

### TOTP Codes (3)

<input type="checkbox" id="079" /><label for="079">![]()</label>
_079. TOTP codes._

...then by the time you've actually entered the next one you realize you got a number wrong so you have to type it in again and then the codes have changed yet another time. Eventually when you've got it done, you're stressed out and things are all going wrong and you don't know what to do any more and you just want to give up.

No? Just me then. I personally don't like TOTP codes.

To be clear before anyone panics, we're not getting rid of them, if you like to use them you're more than welcome to continue using them. But we strongly recommend something called U2F instead.

---

### We Recommend U2F

<input type="checkbox" id="080" /><label for="080">![]()</label>
_080. We recommend U2F keys. [Reference]()_

This is a very rare moment in security where one of the more convenient methods is also more secure. We almost never see something which combines both security and convenience.

U2F stands for Universal Two-Factor, and is a physical device you can use for authentication, usually a USB device of some kind.

---

### All Shapes and Sizes

<input type="checkbox" id="081" /><label for="081">![]()</label>
_081. U2F keys come in all shapes and sizes._

They come in all shapes and sizes. There are bluetooth ones, lightning ones, USB-A, USB-C, you name it. Even NFC ones.

---

### No More Fiddling

<input type="checkbox" id="082" /><label for="082">![]()</label>
_082. No more fiddling with phones._

One of the main benefits is that there's no more fiddling with your phones and typing things in manually. You typically just need to insert the device into a USB port and tap a button on it (or just have it near your device for bluetooth and NFC versions).

There are even ones that are low profile, which you can just always keep plugged into the side of your laptop. Then you simply touch the side of your laptop to login to things.

Much more convenient than 6 digit codes.

---

### Just Tap It

<input type="checkbox" id="083" /><label for="083">![]()</label>
_083. Just tap it. [Reference]()_

And it really is just the tap of a button. Insert the key, tap the button, you're done. Simple!

---

### Mix Business and Personal

<input type="checkbox" id="085" /><label for="085">![]()</label>
_085. You can mix business and personal._

And even better, you can mix business and personal on the same device. So you don't have to have a PagerDuty key and a personal key. They can all be on the same device. If you ever leave PagerDuty we have no ability to revoke any of your personal stuff, we just block your key from being used in our systems.

So you can absolutely mix personal and work as well.

---

### Any U2F Key Will Work

<input type="checkbox" id="086" /><label for="086">![]()</label>
_086. Any U2F key will work. [Reference]()_

And any key that says it's "U2F compatible" will work. There are open-source ones, this one here is called the [SoloKey](), you can even [build your own U2F key]() if you're so inclined. You can get them for $5, or you can get ones for $70 will all sorts of extra features.

We like [YubiKeys]() ourselves, and most of you were probably issued with those ones if you're in engineering, but don't feel like those are the only ones you can use.

A quick warning for those on engineering teams, if you want to use a key to access our infrastructure with SSH, you will need a key that supports "OTP" mode (One Time Password) as well as U2F. A U2F-only key will not work with SSH. You'll also need to work with Security or HelpDesk teams to get them set up for SSH access, that is not self-service. If none of those acronyms mean anything to you, come and speak to Security or HelpDesk afterwards and we can go into more detail on it. If you're not in engineering, then you don't need to worry about that, just look for a U2F key.

---

### Big Players

<input type="checkbox" id="087" /><label for="087">![]()</label>
_087. All the big players support them. [Reference]()_

All major players support U2F keys now: Facebook, Google, Dropbox, even the US and UK governments.

---

### Use U2F

<input type="checkbox" id="088" /><label for="088">![]()</label>
_088. Use U2F for all your two-factor needs._

So we **strongly** recommend U2F keys for all your two-factor needs. They are extremely convenient, and get a big thumbs up from your Security team.

---

### You Can Still Use TOTP

<input type="checkbox" id="089" /><label for="089">![]()</label>
_089. You can still use TOTP and push notifications._

And again, to be very clear, we're not getting rid of push notifications or 6 digit codes. If you prefer those methods of authentication, you're welcome to continue using them. We have absolutely no plans to get rid of them as they're still perfectly secure methods of authentication.

But we encourage you to at least give U2F keys a try, as we think you'll immediately agree that they are more convenient.

---

### Always Use 2FA

<input type="checkbox" id="090" /><label for="090">![]()</label>
_090. Always use two-factor authentication._

The big takeaway here is to **always always always use two-factor authentication**. We enforce it everywhere at PagerDuty, so you won't have a choice here, but you should be using it for all your personal things as well.

It really is one of the biggest single things you can do to improve the security of your online accounts. We've been protected by two-factor authentication a few times over the years, as attackers were blocked from getting into our systems as they couldn't get past the second factor of authentication. This is a big deal!

---

### Pagey's Summary Two-Factor Authentication

<input type="checkbox" id="091" /><label for="091">![]()</label>
_091. Pagey's summary of 2FA._

So a quick summary of all the stuff I just talked about. Passwords should be long, random, unique, and private. Use a password manager. Always use two-factor authentication. Avoid using SMS if you can. And we strongly recommend U2F keys.

---

Lesson Scenario:
What is the weakest form of 2FA?

- <input type="checkbox"> `Biometric`
- <input type="checkbox"> `Physical device`
- <input type="checkbox"> `TOTP codes`
- <input type="checkbox"> `SMS`

<div class="reveal-answer">
	<button class="button">Reveal Answer</button>
	<blockquote><p>SMS is the weakest form of 2FA and should be avoided if possible.
</p></blockquote>
