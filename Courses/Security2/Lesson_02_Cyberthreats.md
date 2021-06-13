Title:
Lesson 2 | Cyber Threats

---

Lesson Notes:
:dart: There are different types of cyber threats - nation states, hacker groups, lone hackers, bored engineers, and others.
:dart: We can never be 100% secure. Our goal is to manage risk based on the various cyberthreats against us.

---

Lesson Content:

There are several different cyber threats that we think about. Some are more relevant to our business than others.

Nation states target companies that house state secrets or store financial information. If we have customers that house this type of data, our company could be a target of attack to gain access to our customer data.

Hacking groups are similar to nation states with the one difference being that hacking groups will leak company data if they gain access to it.

Lone hackers are the cyber threat that we’re most set up to protect against. They typically attempt to damage the reputation of companies and t commonly use denial of service (DoS) type attacks.

A board engineer can cause as much damage as any cyber threat. The actions they take have serious consequences for the security of our company data.

We align our internal resources to address the cyber threats that pose the most damage to our company.

---

External resources:

### Cyber Threats

_<input type="checkbox" id="009" /><label for="009">![009](/slides/for_everyone_part_ii/for_everyone_part_ii.009.jpeg)</label>_

So we're going to start off by talking about cyber threats. What is a "cyber threat"? It's a term that's thrown about in the media a lot. But what actually is one?

---

### The Cyber Threat

<input type="checkbox" id="010" /><label for="010">![010](/slides/for_everyone_part_ii/for_everyone_part_ii.010.jpeg)</label>
_010. "The Cyber Threat". [Reference](https://www.cnbc.com/video/2019/04/11/watch-cnbcs-full-interview-with-pagerduty-ceo-jennifer-tejada.html)_

We have some help from CNBC who've very helpfully highlighted what a "cyber threat" is for us.

This isn't Photoshopped by the way. I know I would normally edit this type of stuff, but this is a genuine screenshot from [an interview our CEO Jennifer Tejada did](https://www.cnbc.com/video/2019/04/11/watch-cnbcs-full-interview-with-pagerduty-ceo-jennifer-tejada.html) a few months back. I'm still not sure why they had a banner saying "The Cyber Threat", but it made for a good screenshot.

Now you may be thinking that they're saying Jenn is the cyber threat here, but I'm not entirely convinced that's true...

---

### Nation States

<input type="checkbox" id="013" /><label for="013">![013](/slides/for_everyone_part_ii/for_everyone_part_ii.013.jpeg)</label>
_013. Nation states?_

Nation States? Russia, China, North Korea, etc. Do we really care about them hacking us?

Well, kind of, but they have so many resources at their disposal that if we are specifically targeted by them there's not a lot we're going to be able to do to defend ourselves.

The silver lining there is that we're probably not going to be the ultimate target for those types of threat actors. We don't store financial information, we don't store state secrets or classified information, there's not going to be a lot of value in breaking into our company systems for them.

It's more likely that one of our customers is specifically targeted and that they would try to use our company to get to them. We're unlikely to be the first choice there though, since things like a direct phishing attack on the target customer are going to be much easier to pull off.

The other silver lining here is that if a nation state does manage to break in and steal every bit of data we have, they're unlikely to leak any of that data in the wild. They don't want others to know about the capabilities they have or that they've broken into somewhere.

So while nation states are a real threat, and we do have some protections in place (for example, we use a [Zero Trust approach](https://www.oreilly.com/library/view/zero-trust-networks/9781491962183/) to our networking whereby all information in transit is encrypted, even internally), we don't focus our efforts on defending against nation state actors, preferring to focus on other more likely threats instead.

---

### Hacking Groups

<input type="checkbox" id="014" /><label for="014">![014](/slides/for_everyone_part_ii/for_everyone_part_ii.014.jpeg)</label>
_014. Hacking groups?_

What about organized hacking groups? Well, unless we put out a press release saying we're "unhackable" or something like that (pro tip: there's no such thing), we're unlikely to be a focus for these groups either. These groups tend to be in it for the money, and as before, we don't store any financial information. Like nation states, they're more likely only going to want to use us to pivot to one of our customers.

One difference though is that if these groups managed to break in and steal our data, they definitely would leak it online. They'd try and blackmail us first no doubt, but then would eventually leak it online anyway. So there is that side to the threat too.

Most of our defenses will protect us against this type of threat, but if they're persistent enough and advanced enough, there's not a lot we're going to be able to do to protect ourselves here. It's likely to be a big game of Whack-a-mole. Given enough money and resources, they'd likely be able to steal _something_. The silver lining here is that it would generally cost more to get any data from us than that data would be worth, which hopefully makes us a less likely target.

---

### Lone Hacker

<input type="checkbox" id="015" /><label for="015">![015](/slides/for_everyone_part_ii/for_everyone_part_ii.015.jpeg)</label>
_015. Lone hacker with a grudge?_

OK, so that about a loan hacker with a grudge?

We're pretty well set up here to defend against this type of threat actor, but they can potentially cause a lot of damage, and will tend to go for more denial of service (DoS) type of attacks rather than outright stealing information. They tend be less motivated by financial gain and more about causing reputation damage or gaining notoriety for themselves. Most of our controls are in place to protect against this type of threat, so we hopefully do a pretty good job of keeping loan hackers out.

As far as we know of course. We only know about the threats we know about. If someone is in our system and we don't know it, that's just as bad. And if that thought keeps you up at night, welcome to the party!

You can never be 100% secure or 100% confident you're not being hacked. All you can do is try your best to keep attackers out and to add monitoring to detect if they get through. The other side is to not store data we don't need. If we don't have any data worth stealing, then we're not as much of a target. We'll be talking more about what data we should be storing and things like GDPR later.

---

### Bored Engineer

<input type="checkbox" id="016" /><label for="016">![016](/slides/for_everyone_part_ii/for_everyone_part_ii.016.jpeg)</label>
_016. Bored engineer?_

So the threat we _really_ care about is the bored engineer with $30, an Amazon account, and some free time. You'd be amazed at the damage that could be done by such a person, as I'll demonstrate today.

But in all seriousness, we can never be 100% secure, instead it's all about risk. We look at which types of attacks are the most likely, and could cause the most damage, and focus most of our defensive efforts there. The aim is to make it not worth the effort for an attacker to come after us, whether it's by making it take too much time, cost too much money, or because we don't have anything worth stealing in the first place.

So with that in mind, let's talk a bit more about "cyber threats"...

---

Lesson Scenario:
What is the cyber threat we are best set up to defend against?

- <input type="checkbox"> `Lone hacker`
- <input type="checkbox"> `Internal employee`
- <input type="checkbox"> `Nation state`
- <input type="checkbox"> `Hacking group`

<div class="reveal-answer">
	<button class="button">Reveal Answer</button>
	<blockquote><p>Lone hackers are the cyber threat that post the most risk to our company.
</p></blockquote>
