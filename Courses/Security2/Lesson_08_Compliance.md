Title:
Lesson 8 | Compliance

---

Lesson Notes:
:dart: SOC 2 is a report with standardized controls that we can use to validate our security to the market.
:dart: GDPR grants specific rights on all EU-citizen data. 

---

Lesson Content:

SOC is a type of certification companies go through in order to prove to their customers that they practice what they preach when it comes to security, and that they follow security best practices. It stands for "Service Organization Control"... I don't know what it means either. But it's a standard within the industry.

A SOC2 report shows that we've been independently vetted by auditors that came onsite to validate we do what we say we do from a security point of view, and aren't just saying it for the sake of appearances. It's all done by independent external auditors, so you can't fake it.

GDPR is important. We have to get consent to use customer's data. We have to appoint a Data Protection Officer. Customers have the right to access their data whenever they want. They have a right to get that data deleted. They need to be able to extract data and move it to a competitor if they want, and on and on.

And the penalties are huge. It's 20 million Euros, or 4% of your annual global turnover, whichever is higher. 

---

External resources:

### Socks

_<input type="checkbox" id="160" /><label for="160">![]()</label>_

For our final topic of the day, let's talk about socks. Yes, we have company socks, they're very comfortable. But that's not the type of socks I'm going to talk about.

---

### SOC2 Type 1

<input type="checkbox" id="161" /><label for="161">![]()</label>
_161. SOC2 Type 1. [Reference]()_

Good news, [we are SOC 2 Type 1 compliant]()!

What does that mean exactly? SOC is a type of certification companies go through in order to prove to their customers that they practice what they preach when it comes to security, and that they follow security best practices. It stands for "Service Organization Control"... I don't know what it means either. But it's a standard within the industry.

Some of you have probably heard about all the SOC work we've been doing over the last year and wondering what it's all about and why it's important. You may not get an insight into all the processes that go on behind the scenes, so I thought I'd give you a sneak peak at what usually happens when a customer wants to use PagerDuty.

---

### Sales Process

<input type="checkbox" id="162" /><label for="162">![]()</label>
_162. Sales process without compliance._

The customer will come to us and ask us about security. We tell them that we're secure, but they come back saying "We don't believe you. Please fill out this billion page questionnaire". These questionnaires will contain really far reaching and in-depth questions like,

> What is the name of your company?

and deeply relevant questions such as,

> What is your business continuity plan in the event of a global pandemic?

Not joking by the way, those are genuine questions we get on these vendor security questionnaires from customers. A global pandemic? Really?! I'm going to be home and hiding. Or I'll work remote that day.

So then of course, we get frustrated that we have to spend a week answering these obtuse and barely relevant questions, only for the customer to come back with a huge number of followup questions asking things like why we don't use a firewall appliance in our data center. Now we have to spend more time to explain that we don't have a data center and describe what AWS is and so on. Basically the process takes a really long time and gets extremely frustrating for everyone involved. The security team, the sales team, the customer, everyone.

You'd think there's be a standard format for these questionnaires, so you can provide your answers once and share them with everyone. And there is! Except there are 20-30 different standards and everyone seems to use a different one or a different version. And some just send you a spreadsheet to fill in.

So this takes a long time and it can be a few weeks before we've been able to properly respond to the questions. When the customer comes back with followup questions, it adds even more time as we need to then justify why we do things the way we do, which may go counter to how they do things. For example, a lot of financial institutions ask why we don't force password rotations every 90 days for our staff, and we then have to spend time justifying why we don't do that, etc.

???+ comment "Presenter's Comment"
The reason we don't force password rotations on a timed schedule is because it's considered a bad practice by modern standards. For example, it's specifically recommended against by both [NIST]()(https://pages.nist.gov/800-63-3/sp800-63b.html#memsecretver) and [NCSC]()(https://www.ncsc.gov.uk/collection/passwords). Users are more likely to chose a password that's a minor variation on the previous one, rather than unique secure passwords each time. One of the arguments for forced rotations used to be that it limited the window of opportunity for an attacker to use stolen credentials, but most attackers will use a password straight away so it's not really a solid argument any more. We force the rotation of passwords under only one circumstance, which is whenever they're suspected of being compromised, as recommended in [NIST Special Publication 800-63B (§10.2.1)]()(https://pages.nist.gov/800-63-3/sp800-63b.html).

---

### Sales Process With Compliance

<input type="checkbox" id="163" /><label for="163">![]()</label>
_163. Sales process with compliance._

Well, with SOC2, the process becomes much easier! We just give them our SOC2 report and the customer asks where they sign. Simple!

OK, so that's a bit of a dramatization. As is probably clear, I don't work in sales. But you get the idea. Having SOC2 certification greatly speeds up the efficiency of our sales process, and builds a lot more trust with customers.

A SOC2 report shows that we've been independently vetted by auditors that came onsite to validate we do what we say we do from a security point of view, and aren't just saying it for the sake of appearances. It's all done by independent external auditors, so you can't fake it.

---

### Type 1 vs Type 2

<input type="checkbox" id="164" /><label for="164">![]()</label>
_164. Type 1 vs Type 2._

I mentioned earlier that we have a Type 1 report. There are actually two types of SOC2 report you can have, a Type 1 (sometimes "Type I") and a Type 2 (sometimes "Type II").

The one we have at the time of this presentation is Type 1, which essentially asks "Did we do what we said we did at a particular point in time". So an auditor came onsite, looked at all the things we do, and evaluated all the evidence we provided, and as long as we did all of those things at that particular point in time, we got the compliance.

That's all well and good, but what customers really want to know is can we do all these things continuously. It's no good having strong security practices on the day of an audit if you then just turn around and do things insecurely the very next day.

That's where the Type 2 report comes in. That's asking "Do you do all these things continuously for six months" (there can be other durations, it doesn't need to be six months, but that's the standard). So auditors come onsite for six months, and make sure we do everything we say we do every single day and that it's not just for show. As you can imagine, this one is a bit harder to achieve, but it's the one that most customers want.

At this point in time, we have our Type 1 report, which no exceptions noted, and we're currently in the middle of our audit for the Type 2 report. We can't promise a date for that report to customers yet, but you're welcome to tell customers that we're in the middle of the audit if they ask.

---

### Controls

<input type="checkbox" id="165" /><label for="165">![]()</label>
_165. What are controls?_

I've mentioned "controls" a few times throughout this talk. At last when I started looking into this stuff I had no idea what a "control" was, so I figured I'd try and define it for you.

From my experience, a control is just a fancy word for "this is a description of something we say we do from a security point of view". So you can see why it's shortened.

For example, one of our controls might be "We encrypt all information in transit".

---

### Follow Controls

<input type="checkbox" id="166" /><label for="166">![]()</label>
_166. We must follow all controls._

The idea is that we have to follow all our controls. We can't say we do something and then not do it. That will flag up in the report, and we can't hide a certain bit of the report. Then every customer is going to see that we say we do something but really don't. Which obviously wouldn't reflect very well on us.

---

### Provide Evidence

<input type="checkbox" id="167" /><label for="167">![]()</label>
_167. We must provide evidence we follow our controls._

Importantly we have to provide evidence to the auditors that we follow all our controls. They're not just going to take our word for it. For example, one of our controls is that all of our employees go through annual security training.

We have to provide evidence to prove this. So when you answer the quiz with the colour and animal, which last year was Blue and Llama, the auditors will want to see that. And yes, for our Type 1 report our auditor really did go and check that everyone replied with "blue" and "llama" and that we had 100% coverage of all staff.

---

### Six Months

<input type="checkbox" id="168" /><label for="168">![]()</label>
_168. We have six months to comply._

And we have six months to comply with all these controls. But that's just for the audit, we need to always be following our controls at all times, whether we're in an audit period or not. Otherwise what's the point?

So don't think that this compliance stuff is just a one time thing, and that once we've passed the test we can just forget everything and go out partying. There may be partying, but we will always need to keep up our controls.

So enough about SOC2...

---

### What Happened With GDPR

<input type="checkbox" id="169" /><label for="169">![]()</label>
_169. What happened with GDPR?_

...I know you're all sitting there thinking "Whatever happened with that GDPR thing from last year?"

No one? Just me then.

---

### GDPR Still A Thing

<input type="checkbox" id="170" /><label for="170">![]()</label>
_170. GDPR is still a thing._

I'm once again required to tell you that GDPR is still a thing.

It stands for General Data Protection Regulation. It is in effect now, as of last year, and it's not just some imaginary thing. We've had requests from customers to delete their data per GDPR and so on.

---

### GDPR

<input type="checkbox" id="171" /><label for="171">![]()</label>
_171. GDPR. [Reference]()_

There are so many things involved in GDPR though, and I'm not going to go through them all. I'm just going to show you this really cute animated slide that I spent far too long on.

We have to get consent to use customer's data. We have to appoint a Data Protection Officer. Customers have the right to access their data whenever they want. They have a right to get that data deleted. They need to be able to extract data and move it to a competitor if they want, and on and on.

And the penalties are huge. It's 20 million Euros, or 4% of your annual global turnover, whichever is higher. So y'know, that's a lot of coin.

---

### Pagey's Summary - Compliance

<input type="checkbox" id="172" /><label for="172">![]()</label>
_172. Pagey's summary of compliance._

Bottom line here, our second SOC2 audit is underway right now. It's going to make our sales process much smoother. It's very important. And so is GDPR I guess... No, of course I'm kidding, GDPR is very important too.

---

Lesson Scenario:
What is accurate of SOC 2?

- <input type="checkbox"> `It is antiquated and being replaced by GDPR`
- <input type="checkbox"> `It is primarily for internal use`
- <input type="checkbox"> `It is performed by the internal audit team`
- <input type="checkbox"> `It is used to validate security to the market`

<div class="reveal-answer">
	<button class="button">Reveal Answer</button>
	<blockquote><p>SOC 2 is a standardized report, performed by an approved external auditor, and is use to validate security.
</p></blockquote>
