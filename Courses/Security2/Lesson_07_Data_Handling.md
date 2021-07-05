Title:
Lesson 7 | Data Handling

---

Lesson Notes:
:dart: Intended Audience: All employees, regardless of function.
:dart: Intended Frequency: The goal of today's training is to make sure that we can maintain and build customer trust by having a staff who are well trained against the most common security threats that we face.

---

Lesson Content:

A quick recap on data handing,

* Make sure you know the classification of any data you handle. If you're not sure, assume it's customer data until you find out otherwise.
* Don't move data between systems.
* Don't discuss company info in public
* Don't bypass our security controls.
* If you need to share files, please use approved tools for internal and external sharing.

---

External resources:

### Data

_<input type="checkbox" id="142" /><label for="142">![]()</label>_

The next section is all about data, and brace yourselves for lots of Data from Star Trek puns. I'm not sorry.

Data is very important. Any kind of data loss or data leakage can be very damaging and embarrassing.

---

### General Data

<input type="checkbox" id="143" /><label for="143">![]()</label>
_143. General data._

We have three different flavours of data at PagerDuty, the first is **General Data**. This is anything intentionally available to the public. Our bog standard data that you can share freely with anyone. Ironically this slide isn't classified as public due to the internal wiki link.

???+ warning "Redacted Content"
When originally presented, these slides all contained links to our internal wiki with more detailed information. Those internal links have been removed from the public version. If you were to give this training in your own organization, we encourage you to provide links to your own documentation where employees can find more information.

---

### Business Data

<input type="checkbox" id="144" /><label for="144">![]()</label>
_144. Business data._

Then we have **Business Data** which is anything used to operate the business. Employee payroll, lists of social security numbers, things like that.

---

### Customer Data

<input type="checkbox" id="145" /><label for="145">![]()</label>
_145. Customer data._

And the finally, our most protected asset is **Customer Data**. This is anything that the customer gives us.

It's worth noting that even though it's called "Customer" data, a user doesn't have to be a paying customer of our service for their data to be classified as such. Customer Data is any data given to us by a user of our product, whether they're a paying user, a trial user, or a prospect reaching out to ask questions.

---

### Data Handling Policies

<input type="checkbox" id="146" /><label for="146">![]()</label>
_146. Follow our data handling policies._

Please please please follow all our data handling policies.

You have all agreed to follow these policies when you signed our employee handbook. If you don't know what our policies are, then you should go and read them today, because you have legally agreed to follow them and signed documents saying as much. Hopefully that's not a surprise to anyone.

If you have any questions about our policies, or something isn't clear in them (or even worse, you find contradictory information), please let us know. If there's a case that's not covered by our policies, we want to know about it. If you find our policies too restrictive and want to understand the reasonings behind them, or have suggestions for how to change them, we want to know that too.

The official handbook version can be a bit wordy and difficult to parse, so we've tried to make the internal wiki version a more plain English description.

---

### Data Handling Pricing Plan

<input type="checkbox" id="147" /><label for="147">![]()</label>
_147. Our data handling pricing plan._

I'm not going to just read a wiki page to you right now, so I'll present it quickly here in a format that might be a bit more familiar to you if you've ever seen our pricing page.

We have our **General** pricing plan, where you can access information, store it, and share it widely with anyone.

We have our **Business Data** plan, only $29 per user per month. This has a lot more protections in place, as we require things like encryption and privacy controls.

And then we have our most popular plan, the **Customer Data** plan. Unfortunately this plan can be a bit more expensive, anywhere up to about $23 million if we violate GDPR, or if we were to lost or leak any customer data. So as you can imagine, we have a few more restrictions in place there. So please please please protect our customer data.

If you're not sure what type of data something is, please don't hesitate to ask us. It's also a best practice to treat something as if it were customer data until you know for sure that it's not.

---

### Copying Data

<input type="checkbox" id="148" /><label for="148">![]()</label>
_148. Don't copy data to other systems._

A couple of things you can do to help protect our data. First, don't copy data to other systems. If you're on a production system, don't copy that information to staging or sandbox/developer/test accounts. This would involve a lot of cleanup and stress for everyone involved.

Definitely don't copy data to systems we don't own or control. This is especially important in AWS, where our infrastructure has a lot of controls and auditing in place, we have lots of automated checks and the ability to perform forensics and so on. If you were to move data outside of those controls, we lose that visibility.

---

### Data Protections

<input type="checkbox" id="149" /><label for="149">![]()</label>
_149. Don't turn off data protections._

Also don't turn off any of our data protection mechanisms. We run various tools and agents on our hosts which are all doing important things, please don't just turn them off. We have all sorts of audit tools running where if data gets leaked, we're able to see exactly who did it and where the data got transferred to and so on.

In most cases you won't even be able to turn off the controls, especially in AWS where even administrators can't turn these features off. But there's always going to be at least some folks with that level of access, so please be sure to use your permissions wisely. If anything, please think of the poor Security team on-call engineer, who will get paged immediately if you turn any of our protections off.

---

### Be Mindful

<input type="checkbox" id="150" /><label for="150">![]()</label>
_150. Be mindful of how you treat data._

The key takeaway here is to always be mindful of how you treat data. Treat data as if it were your own. If you're logged in as an administrator somewhere, it can be easy to misclick something and then you've suddenly leaked data somewhere you shouldn't have.

If you do that, don't be embarrassed to come to us. We will always help you to fix it.

But things like that are why we practice something called the ["Principle of least privilege"](), where every user only has the permissions needed to perform their job, and no more. For example, an engineer on our pipeline team doesn't need the ability to create S3 buckets in AWS, so they won't have that permission granted to them.

This is also why most engineers will have the ability to use "read only" roles for their services, for when you need to debug things. It allows you to view the data you need, without worrying about an accidental click doing something wrong. It's always a good idea to login with the lowest set of permissions you need to do your current task. For example, I have the ability to login as an administrator to our AWS accounts, but I rarely login with those permissions. If I'm just trying to look up some logs, then I would typically log in with "read only" permissions instead.

---

### Discussing in Public

<input type="checkbox" id="151" /><label for="151">![]()</label>
_151. Don't discuss company information in public._

Another way to protect our data is to not discuss company information in public. The number of times I would be out at bars of restaurants and overhear people talking about things they shouldn't be, their company's financial information, or big deals they just signed, and so on. A lot of information that shouldn't be discussed. Please don't do that with any PagerDuty information.

---

### Insider Trading

<input type="checkbox" id="152" /><label for="152">![]()</label>
_152. Familiarize yourself with our insider trading policy._

Similarly, familiarize yourself with our insider trading policy. We have one of those now. It's not the most thrilling read, but it is very important. So please do make sure you know what's going on, as you really don't want to get into trouble with the SEC, the IRS, or any other three letter agency. Remember that very few people at PagerDuty are authorized to share certain information publicly. If you're not sure whether you're one of those people, then you're probably not.

---

### Shouldn't Have Access

<input type="checkbox" id="153" /><label for="153">![]()</label>
_153. Report things you shouldn't have access to._

If you find something you don't think you should have access to, like a big bag of cash marked "employee wages", or a list of employee payroll information and so on, please report it to us promptly.

You're not going to get into trouble for accessing something you shouldn't have, since our access controls shouldn't have let you in in the first place, so it's our fault not yours. You might get into murky waters if you don't tell us though, as we may find out months later and start performing forensics. We'd see that you accessed the data and didn't tell anyone, which makes it look like you were stealing the information and trying to hide it.

So please do let us know if it happens, and we'll be able to help you out. **You're never going to get into trouble for reporting security issues to us. Ever.**

---

### Another Company

<input type="checkbox" id="154" /><label for="154">![]()</label>
_154. How would you want someone else to treat your data?_

It all really comes down to, how would you want your personal information to be treated by another company? How would you want Facebook to treat your data? How would you want Dropbox to treat your data? and so on. Treat our customers data the same way, because they're people too. It shouldn't surprise you to learn that our customers want us to treat their data appropriately.

---

### Data Sharing

<input type="checkbox" id="155" /><label for="155">![]()</label>
_155. What about sharing data?_

A question we get a lot is "How do I share data?" How do I share data with someone else in the company?, how do I share data with a third-party vendor?, how do I share data with a customer when they request data from their account?, and things like that.

---

### Restrict Access

<input type="checkbox" id="157" /><label for="157">![]()</label>
_157. Restrict access to only those who need it._

And try to ensure you're restricting access only to the people who need access to the file. Don't make it where anyone who knows the link can access the file. Because if that link gets leaked everyone's going to be able to view it. If someone tweets that link out and it'll be copied very quickly.

---

### Confirm Account

<input type="checkbox" id="158" /><label for="158">![]()</label>
_158. Confirm which account you're on._

And please confirm which account you're on. I have embarrassingly emailed a customer from my personal email account by mistake before. So you know, anyone can do this, please don't fall into the trap of thinking "Well, I'd never do something that silly!".

So please verify which account you're on when you use these tools.

One tip you can do is to use a different avatar or userpic for your personal and work accounts, or change the background theme colour and so on. Some big visual representation of which account you're on will make it much easier to not accidentally send things from the wrong account.

---

### Pagey's Summary - Data Handling

<input type="checkbox" id="159" /><label for="159">![]()</label>
_159. Pagey's summary of data handling._

That's everything I had on data classification and handling. A quick recap from Pagey,

* Make sure you know the classification of any data you handle. If you're not sure, assume it's customer data until you find out otherwise.
* Don't move data between systems.
* Don't discuss company info in public
* Don't bypass our security controls.

I should point out a caveat for support teams when you want to share files. It's the customer's data, if they want you to share it with them in a certain way, then they are authorized to allow you to do that. You can caution them against certain ways, but if they insist, and you've verified you are actually talking to the customer, then just make the customer happy and share the data with them however they want.

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
