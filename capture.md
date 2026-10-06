SPEAKER_07: turn it over to the more skilled individuals to share screens as needed. So we've got, you know, five key items to cover off. The first one is the level API, MRA level to scoping and scoping. There's a release on at the end of the week. Winston will talk about that. We have our regular updates with some specific topics to cover in between. I see Vinod, I swear I saw him. Yes, Vinod Dhan. I am, I am in. Yeah, you're a troublemaker. So we've got lots of things for you to cover. Release page updates, training topics. And then again, just a couple of reminders for the team due at the end of this week. So let's, let's dig, jump right in. Winston, sir, would you like to share your screen?

SPEAKER_02: Yeah, yeah, let me, let me share my screen. Thank you.

SPEAKER_07: Okay.

SPEAKER_02: Okay, so, so I'll just give you some background. We've been talking about the, the API MRA scope functionality for quite a while now, actually. And we've been releasing the functionality in phases. What I mean by that is that we've updated the API to expose the field on the API level. But it's only this week, Friday, where we're going to start using the field to enable the, the decision-making. Of this scoping and scoping of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of Of MRA level scope is driven mainly from the US hosting country, consuming group, member codes. So whether the hosting country has a US in there, because it's an array, so you could have multiple hosting countries for an API, or whether the consuming groups, again, is multiple, has US HBUS specified, and if either of those have been defined and the API isn't private, isn't a private API, then it would be deemed to be in scope. And while we did some analysis, we noticed that some applications only have private APIs, even though they're classified as in the MRA scope. So for example, if I go to the inventory um i'll move this out so that you can see it properly you've got this um this ba ba 3887 um and it's a cmb um application it's got one api and this application is internal it's internal uh so it's private sorry internal private or private it's got private api so when this functionality goes live what will happen in this case is that the um itso receive a book of work item to state that this um this application is is going to be taken out of scope can you confirm whether it should be out of scope yes or no similar to what what you currently have already for descoping um um and the itso so would confirm no or yes if they say yes then they'll need to update the data so that at least one api is in scope um now comms have been sent out to the itso's uh beginning of this month um regarding this functionality taking place to give them enough notice that um this functionality has been been um is going to take place and i've also done some outreach to some specific um itso's where um if they've modified their data so we had a um as part of one of the releases to do with the api mra we automatically defaulted some of the values which we found on on the business application level on the api level so if for example the business application had a hosting country of us we would automatically populate that for the api and we would then be able to do some of the work on the api level um and so what we found is that some teams have changed the us removed the us country code and to specify gb so i've done some outreach to some of those itso's and in some cases it's it was on it was intentional um so they said that it's not running in the us this api is only available in hosted in gb um and and so on so that type of work has already been done but today i'm just really just um bringing it here to this void for this box if you've got any questions or if there's anything that you want to ask you can feel free to ask me what does the category says the itso book of a category so it will be a descoping this this in the documentation here but i'll just go for it so so basically the category would be a demise api demise category um yeah so just research yes so it'll be an api um demise category now the similar it's a similar um in the reverse if you've got um if your application has been marked as out of scope but you've got apis which are hosted or consumed in the us then it's a similar case whereby that api application could be brought into scope as a result of those um white white white white white white white white white white ! white ! have level mra scope would also drive applications being brought into scope as a result of an api having um the um hosting being hosted in the us or wherever the consuming group is specified as us um um hbus okay and that release is scheduled for this friday um so that that's um that will go out this friday unless there's obviously major concerns with this functionality but otherwise it will go out this

SPEAKER_09: friday and it's a two-week task two-week deadline yes yeah okay okay any other questions thanks uh

SPEAKER_08: eastern uh thanks for granting access to the list is it possible to include gbgi in there

SPEAKER_02: yes i know what i'll do um because it takes a bit of while to generate i'll i'll ask the dev team to generate a new list just to make sure it's up to date and just have the gbgi in there as well

SPEAKER_08: right and that list includes uh both right in scope out scope both the potential this is just

SPEAKER_02: this is just these scopes but i'll ask them to add the ones which will be brought into scope as well the the the d scope was much more prevalent than the in scoping from memory i think was

SPEAKER_05: only one or two to come in scope right princeton from the last time we talked about it yeah so that that's why we've been focusing more on that one um so yeah it's one one one i'll ask

SPEAKER_02: the dev team just to add things the ones that would be brought into scope as well

SPEAKER_08: so uh both will be implemented together the right at the same time the request will be generated this weekend yes yes i mean this is

SPEAKER_02: it's it's basically the functionality dry would be would drive both the de-scoping as well as the um automated completeness check so yes it will drive both bringing items and scope as well as taking

SPEAKER_05: things out so you create api inventory tasks and api d scope tasks effectively yeah both yeah and and sorry sandy did you say did you ask about the timelines the due dates for these they should be in line with the existing ones which is four weeks for both well i thought he said two weeks i thought yeah if it's four weeks then it's it's four four weeks four weeks is for those two so those those two are standard four weeks and then the yeah yeah the other ones data quality and the sorry the api inventory in the d scope are four weeks the api scope and the data quality of two weeks

SPEAKER_02: i think you're good i think you might i think you may have confused them james so these ones here the api scope is is two weeks isn't it the api scope is two weeks yeah and the api demise what what what is that you these scopes four weeks ah okay so i i'll ask them to also update this documentation yeah yeah just so it's cool and uh i think uh it would be good right i in the uh thanks for the email you

SPEAKER_08: sent us today i'll spoke about the fii but you did also mention that you sent home to itso's on first of october yeah i think i sent it so would it possible for you to just send us to a spokes i mean we can just take that email as a base and uh just a fire to our ciab spokes or uh really on gbgs box so that they are aware of it uh the reason i am i need this because i'm not much concerned about this coping because it's easy uh the one i'm concerned about is the in scope one right so if you remember we had some nice title earlier that was a uh multiple book of work requests been triggered and it may be the case where we are triggering third time just for the correction right you mentioned that let's say application is not in scope but apis are in scopes and it will also result into the new book of work request maybe second or third time so just to give them heads up that this is coming uh so it would be helpful if we share the initial email with us and then we can take it i've shared it with you today

SPEAKER_02: that's what i sent out yeah which is exactly the same so i mean we want to have the email that you

SPEAKER_09: sent us ideas forward yeah forward the same email so that when we have a call with itso's we can say hey we are talking in reference to this email from winston or whoever sent it but basically it's a

SPEAKER_02: same email the only thing that's changed is the is who's addressed to ah okay fine okay notice yeah thank you yeah that's what i meant yeah do you think there will be many application in scope or potential no no it's only going to be a handful less less less than five i would say but i can get that figure tomorrow for you notice thank you so much because i believe this will cover from initial

SPEAKER_08: i mean whatever the application in scope it will validate all the applications right or the discrepancy between in scope and i mean api level as well as app level yes okay i thought it would be more number than five anyway but thank you i will wait for your list okay it's the the other thing to add is there's a feature which is

SPEAKER_05: coming up which will actually add in the reason as to why the it's a book of work tasks has created yeah that's great actually james thank you i was discussing with that but yeah the thing is

SPEAKER_08: people will still come with the question same question that why this was it is although you mentioned the reasons i am expecting those questions again sure no i i understand this

SPEAKER_05: but it should help out a little bit right and you know in the end we can start to because as at the moment it's not completely obvious it's not obvious at all you have to sort of dig into snow look at you know some of the snow data to look at and know what you're looking for as well

SPEAKER_08: so it's not entirely obvious so that is super helpful james yeah great thank you all right any

SPEAKER_07: other questions all right let's move on to the it's a book of work update so james um i'll let

SPEAKER_05: you go next share your screen thank you thank you so this is as of yesterday but i did a quick um spot check this morning oh this is yesterday afternoon uk time i did a spot check this morning and there's no material changes it's reduced by 160 as of about two hours ago to one created in two which were um which were uh were added in sorry two that were closed and one that was added in get it the right way around okay um so normal kind of setup that we have here um good burn down i would say from from last week um where we we've got you know 18 down um majority around the data quality side of things um the api scope and d scope d scopes come down a lot actually which is really good news um still some outstanding api inventories um and so you know this is where we are um so yeah um pretty good news i would suggest the one thing i would look at a little bit is we seem to sort of got a few which are you know i think it's a good thing that we've got a few that are you know we've got a few that are increased on the the the aged over 30 days so this would be my focus um to try to close those out because you know if you're kind of over by a couple of days it's okay it says it's over but it's a little bit different if it's over my born 30 days there's likely to be some kind of process issue or some kind of issue as to why that's the case so um you know we don't necessarily ask people to be chasing up here and obviously we still go to ron for for escalations but um i did just notice the over 30 days had increased from last time but generally a good story um and you can see here i've added this rag report sort of similar format to to what we've done with the um the api metrics um and you can actually see that in all cases we've got when we talk about overdue's we've got a you know a good sort of message here and these are the sort of dates here so so yeah um any questions i mean you know i i will i always say just to go back when we talk about the things that are outstanding and and overdue etc you know i always like to tie back to the fact that you know we've created 725 of these tasks and we've only got you know a a less well less than 10 percent which are overdue so a lot of them have been closed um uh yeah um complete and we've still got a few in review actually so we need to kind of work through those as well i mean promo's working on those but you know we can see that actually this process works pretty well um you know i don't like to we always ever talk about the the overdue ones but um and that's not to say that we shouldn't keep pushing to get them all entirely clean but but actually this is is quite a good story to be honest um sorry deb you're gonna say i was just gonna add we had a couple of other items that we

SPEAKER_07: wanted to talk about here around the trend view added and the clarity book of work task instructions which was of a no mood question so i wanted to just tee those up okay i was just gonna ask quickly on the other slide um

SPEAKER_01: if we move back i just um just out of curiosity while still smallish numbers and cto seems to be the highest overdue particularly in relation to the volumes i just didn't know if there's something um specific to cto that's either a knowledge gap or is just making those trickier to

SPEAKER_05: fully address i don't think so i i looked at that to be honest and i've got rid of my epic screen where i was looking to see which particular area of cto it was it was predominantly in cto ctoi cto data was a little bit less than cto platforms was was only three i think um so it's predominantly in ctoi i don't know staron are you on is there any any thoughts on this one um i'm on and i've had several discussions with si as to what operational model we should have to

SPEAKER_06: keep track of this um we've had discussions with the risk and compliance lead um who have had a lot of problems with this um and we have made some major changes and have made some major changes um and we have made some major changes and have made some major changes and have made some major We're having trouble finding people to do this. And basically, I think what will happen is the latest stats, when they go to SAI, I'll send them to me and say, can we do something about this, Darren? And it's like, okay.

SPEAKER_05: I mean, this is more around the it's a book of work rather than the ones that go to SAI. But I mean, yeah. Well, MSDS they end up landing on. Yeah, I mean, I'm trying to focus on analysis

SPEAKER_06: and getting the MSII remediation stuff all analysed and up and running. And I've tried to, I don't want to make excuses, but like I said, we don't, we're trying to get an effective operational model in place for dealing with this, but we haven't yet. And so I think that's why the numbers don't look so great. I'm sure other areas are putting focus on getting these things chased down. And I don't know who, if anybody is putting focus on chasing those down within C2I at the moment. I mean.

SPEAKER_01: Is it a lack of understanding by the it's so-so or not even to that?

SPEAKER_06: I can't, you know what it's like, Tan, you can't speak for, you know, generally some people do, you know, you know, do stuff. Other people ignore it until they're literally somebody standing over the desk telling them to get on with it. Yeah. So I can't speak in general terms. Humans are humans is what it is.

SPEAKER_05: Yeah, no, understood. Understood. But it is. Tan, you're going back to your comment. I did notice that, as you say, you know, it is quite high in comparison with with the rest of them and also with the size of the C2I is small by any stretch of the imagination. The other ones are a bit smaller. But yeah, there's something that I know Ron's been out. So I'm assuming we'll restart that process of escalations and whatever. He's back now. Maybe I'll just have a quick call of Psy.

SPEAKER_01: Yeah, this is probably a good idea. Just a little prompt.

SPEAKER_05: Okay.

SPEAKER_01: Okay.

SPEAKER_05: Anything else?

SPEAKER_07: Vinod, one of the key things that you had raised over the last couple of days is really around the clarity of the Book of Work task instructions. So I wanted to just open it up to you, sir, to see if you had any commentary you'd like to throw out there.

SPEAKER_09: So yesterday, one of the ITSO from UK reached out to me saying, his ITSO Book of Work task is overdue. And he was trying to understand what exactly needs to be done. And it was just a DQ ITSO Book of Work task. It only takes like two minutes, but he said the instructions weren't clear. So I know we are providing all the documentation, but the documentation doesn't say, okay, go here, do this. Okay. Do this, do that, this, whatever. Now, I know it might take a lot of time. I just wanted to ask other Sparks, are they getting similar reach out from the ITSOs saying, hey, I need to know exactly what needs to be done. I mean, all the documentation is out there on the conference page, but I think these ITSOs are not as familiar as we are with regards to the tooling.

SPEAKER_08: Vinod, it's on and off, right? So not everyone is on the same page, but sometimes we get, but now it has reduced, right? For CIB, at least I can say. Earlier it was. So what I am following and definitely feel has also guided me. So whenever someone asks me a question, I first provide the link of our API documentation. We all spend a lot of effort on creating those documentation, right? And just ask them to read at least this first. If they don't understand, they will read it. So it's a good thing. If they don't understand, then definitely I always try to help them. But most of the time when they go through the documentation, they automatically get the answer of their question. Okay. In case they are not clear, if we try to answer over call, then generally people will definitely try next time to call you because it is easiest way to just call someone and get done right away. So just sharing my experience for CIB. Thanks.

SPEAKER_05: I mean, I think. I think the data quality one is quite well put together. Actually, I kind of get, you know, I know there was talk, you know, around the, the DSCOPE ones, which is a bit more complicated and, you know, requires actions across multiple systems, et cetera. But the data quality one, I did look at the documentation again and felt it was actually pretty strong and, you know, even shows you, even gives you a link to click to the screen, see what your data quality looks like in instructions and how to fix it. So. Again, to be honest, James, this person was not a good person.

SPEAKER_09: I think it's a good thing. I think it's a good thing. I think it's a good thing. I think it's a good thing. I think it's a good thing. So, you know, sometimes this person was newly assigned to this role and probably to the application. So, and as soon as he joined the task was overdue. So he was like spending a couple of days trying to understand what exactly needs to be done. So I said, yours is a DQ one. It only takes two minutes. So just call me. So I, I was on a call and he was happy. I think he was worried that somebody would escalate that stuff.

Unknown: Yeah.

SPEAKER_05: Well, well, well, well, fair enough. Yeah. Yeah. Yeah. Yeah. Yeah. Yeah. Yeah. Fair enough. And you know, obviously, you know, the guidance would be back to, to everybody. It's so as included is don't leave it till the last minute to do that. So you have a little bit of time and, and, you know, maybe this is a certain story if he's being reallocated, maybe the other, you know, there's been a gap in the previous hit. So, and so, you know, that that's kind of happening, but it's always good to, you know, not to do something at the last minute so you don't need to worry about about things being escalated, et cetera.

SPEAKER_00: I think just to add though, I think if you've got somebody who's quite new to APEX and you've

SPEAKER_02: got fresh pair of eyes, they haven't got a clue what to do, it'd be a good idea just to gather some feedback to see how we can make it even better, the documentation.

SPEAKER_00: So maybe Vinod, you could just reach out to them, say how they improve, like the documentation

SPEAKER_02: to be improved. It could be that it's just an extra paragraph that's needed to be added.

SPEAKER_09: Sure.

Unknown: All right.

SPEAKER_07: Thank you, sir. Any other comments around documentation before we move on to the next topic?

Unknown: Okay.

SPEAKER_07: Promote, sir, you are up. We have release page updates. We want to cover manual toolkit exits and CRs that are not included requiring ongoing approvals. So I'll let you take the lead if you need to share. You've got the ability to do so.

SPEAKER_00: Sure. Just a quick context. I think I sent an email, but we probably didn't talk about it in our last SPOC call. So we had extended our SPP from September 30th to end of December, another three months. And when we extended that, that was kind of, we didn't provide enough time for covering any essentially CTAs. Okay. So we had to do a lot of work to get the CRs that get submitted well before the implementation date. So as part of the extension, we had about 22 CRs, which did not include the Tolgate approver group added to the CRs. And what it meant is that either they had to resubmit or they had to essentially be chased separately to make sure there's no impact on our inventory or governance point of view. So I had followed up with all the 22 CR creators and ITSOs and the review is closed. Some of them updated the CR adding the Tolgate approver manually. Some had to resubmit, so they did that. Some had already confirmed that there's no API changes. But we don't have any impact is what I wanted to confirm to this group. From a review point of view, all those 22 CRs are covered in terms of governance. Okay.

Unknown: Thank you so much, Pramod. No worries, Sanjay.

SPEAKER_08: Yeah, I think the lesson learned and I did set up a reminder for myself two, three weeks

SPEAKER_00: before the SPP is due for completion, because I think in December, many people will be out for last two weeks. So I don't want to be in a situation where we are looking at this last minute. So we'll probably talk about it earlier in the month than taking it all the way out. And also end of December, there should not be any CRs because of the embargo.

SPEAKER_09: So hopefully.

SPEAKER_00: Yeah, hopefully not for end of December. But if something they preplanned before going to the holidays, okay, let's put this for January first week, we want to be caught off guard on that as well. So yeah, we'll plan better on the next extension if you have to get there. Other related. But before I go to the next topic. Okay. Okay. Great. And any questions on those 22 CRs? Pramod, I just wanted to find out what's the plan for post December then regarding this?

SPEAKER_02: Exactly.

SPEAKER_00: Yeah. So that's what I'm going to next. Okay. Yeah. So let me share my screen now because I think it's relevant. So we originally even we actually introduced release page based solution.

Unknown: My, my thought was will be.

SPEAKER_02: Yeah.

SPEAKER_00: Yeah. Yeah. Yeah. So I was thinking about what I was thinking about was will be exiting quite a few applications rather in a shorter time than we have what we have actually seen. And I think probably a couple of weeks ago I also sent out a list of applications which already have released pages and, but they have not exited. And then we introduced the setting or what was that we should have I guess was raised the exit requests so that they're. switch happening from a separate group approving and reviewing versus what a regular CR approver should be doing when they look at the release page. And I'm not sure if they're already doing that or if the additional approver is not an issue. No one is raising an exit request. And then I reconciled all the data yesterday. We have about 106 applications which are in approval-based tollgate. And out of that, I see 52 already have release page usage. And if you see here, like 20-odd are close to all the data quality issues also. So there are quite a few candidates which are good to exit the approver-based tollgate, but I have not exited them because they haven't raised the request. So the question is, should we reduce our footprint on the approval-based tollgate by exiting them on our own? Of course, we'll be notifying them, but is it the right thing to do as we stand today? And I think next would be to review whatever is the remaining population. Hopefully, it will be less than 50 to see how we can kind of take them to the using release page. I think from starting this month, if I'm not wrong, there's also an enforcement of the control for using release page, right? So it's probably the right time for them to start navigating that path instead of staying on the approval-based tollgate. So just open to thoughts here. What should we do to kind of make best progress on this one? I mean, if you know why the people are not exiting or they just got comfortable with the next approval, I'm happy to hear that feedback. Yeah. So I did send a message in the group chat and even to EPA governance team within GFT saying

SPEAKER_09: that people probably got comfortable with the current arrangement of manual tollgate. So I will, if you send me this list, Pramod, our APR already sent apologies, but if you could send me the list, I can follow up within the GFT. And as you said, because of the really good feedback, I think it's a good time to start doing that. So I'm happy to hear that feedback. Of course. Of course. Of course. Of course. Of course. GFD as well. They are pushing to adopt the CR minion mostly.

SPEAKER_00: Yeah. Yeah. So we are kind of lined up in the, in the right sequence of events, they will control being in place that's being monitored separately. And that kind of also is helping us to get, get up teams on to the release page, which will hopefully enable them to get exited. Yeah. So I can send the data, but should we wait for inputs from Spock? So ITS was to raise the exit request for the ones which are already there. Of course, whichever applications are not yet there, I think they have to work towards it, but the applications, for example, here, right. You see I've tried the sequence sorted it by the data quality. So these, these already have released pages. They have the data quality a hundred percent. So they are technically ready. The key question is when, when we exit them just because they don't have an extra approver, are they, are they going to look at the release page information that flag with API updated or not? Because remember these are not strategically ingested, right? So maybe there's probably there's only one here, but whoever is not strategically ingested, they will have this red, amber green flag on the release page to indicate whether the API is updated in APICS or not. And they have to review and act upon it. So it doesn't happen automatically. It's still a manual toll gate.

SPEAKER_05: Yeah. Yeah. On the release page, it does. So, so, you know, if you prove and you know, the APICS or the governance, you know, the API governance flag goes up, you have to come up with a reason as to why you're bypassing it. And, and yeah, so, I mean, it's not something where the re there are checks on the release pages as well. Sorry, Sanjay, Karen.

SPEAKER_08: No, I didn't think, yeah, we'll just inform was team because not everyone is aware that this is the criteria. We have to keep reminding them that, okay, once you meet this credit, you can, this is the exit, the question, et cetera, but we'll let you know from what I don't see any blocker exiting manual toolkit. I think it is just matter of they're not aware of this criteria.

SPEAKER_05: So we have to keep reminding our teams.

SPEAKER_08: Yeah. Regularly.

SPEAKER_05: I mean, it, you know, it was a request specifically from Phil to, to, to, to, to, to, to, to add to it because it would release the amount of manual effort. Right. So, you know, it's there, it's, it's ready to be used. Now I think you're right. People get comfortable with processes and don't necessarily look to change them if things work. And maybe these aren't high volume release applications either, et cetera, but you know, obviously we prefer them to, to go to the, um, release page manual toll gate, um, rather than the approval group. It's better. It's better. From a scalability point of view, and it's better for them as well. So,

SPEAKER_02: so promote, I, I just got a question for you though, because some, some applications, it doesn't make sense going to this enhance release page solution. So for example, vendor solutions where the third party manages the infrastructure and so on. So I, I'm assuming we still gonna have to have this manual, um, process in place post December. Yeah.

SPEAKER_00: Yeah, likely, but I, I think, uh, the way I'm looking at this, we probably should be reduced to maybe 5% of the population in terms of applications in school. And then maybe we can, uh, review what, what are the best options in terms of how do we kind of, uh, manage this? Of course, I don't think we ever said that we'll be, um, only enforcing automated solution or not, not, um, keeping the approval based option, but it's just the way we want to go on it or manage it, right? I think, uh, we don't want to keep it for the application that they don't need to. So, yeah, we, we definitely have to think beyond December. You're right, Princeton. But, um, I think that the current, uh, population is definitely, I think it's quite big than what we probably thought it to be.

SPEAKER_02: Yeah. I think also the other aspects of this is that although we've got the enhanced release page solution, that is still a manual process. So, we should really be trying to drive the various different teams to use the automated pipeline solution.

SPEAKER_00: Yeah. Yeah, absolutely. That's, I think, uh, the enhanced pipe enhance release pages.

SPEAKER_02: They should really be moved to the, trying to target the automation for automation.

SPEAKER_00: Yeah. In fact, probably I can say this maybe in last month or so, but most of the exits have been to the release page based solution than the full automation. So, uh, you're right. I think we have probably, uh, lost some focus in that other bit. I actually also wanted to give me a second field and come back to your question is I think when we have a reduced population, we probably have to review if we should continue to have SPP based solution or just stay with the group, uh, mapping because SPP comes with, uh, a three month, uh, period of time and it has to manage separately, right? So it is, it's a bit additional overhead than just dealing with the direct mapping solution. So that those are the options we have to review. And I think when we looked at SPP, it was primarily to see if we have so many applications, so many changes, they should have the, they should have a way to filter out software based changes. So that was the reason behind it. But if we have lesser number of applications, I think we may have to see if just the direct mapping, uh, serves the purpose and just demise the SPP based solution. That could be one way to go. But yeah, once we have a, well, reduce this population, we probably can look at the options beyond December.

Unknown: Yeah.

SPEAKER_00: Good. Phil.

SPEAKER_04: Um, what's, what's driving the three month review and in reality, considering we've been through that once, what value did it bring?

SPEAKER_00: You mean, uh, we should get beyond three months or are you saying, uh, are we adding three months? I'm not sure if I understand the question.

SPEAKER_04: So, um, the three month element of this means that every three months we've got a risk of this process failing unless we're on top of it. So the question is why, why not six months? Why not yearly? Um, oh, okay.

SPEAKER_00: Yeah. And the question is why do we have it at all?

SPEAKER_04: You know, what value is that bringing?

SPEAKER_00: Right. Right. Yeah. I think when we, when we, of course, brought in, it was to, uh, enable high, high cadence, high release cadence teams to have a smaller population to look at it, to have other types of changes and they, they can filter out software only changes. And to what I know, uh, based on, if you look at this concept of service production period, they're not supposed to be there forever, right? That they are a temporary arrangement to enforce controls. They're not supposed to be additional control that, that lives all the time. So, in, in nature by the, by the design of that solution, that's supposed to be temporary. And my understanding from service management team is that the maximum they can keep one, a particular block of, uh, these, these production period is three months. And that's why we need to kind of review every three months. So they cannot be put in the calendar, uh, or into the service now for keeping for a year or so. That's my understanding. I can go back and double check on that with first management team. But, but just by the nature of it, it is, it is a temporary arrangement supposed to be temporary. And yeah,

SPEAKER_04: no, that makes sense. I remember those discussions. Thanks for reminder. I guess. So I think what you're saying is if we agree to renew this in the first week of December, we get three months from the first week of December.

SPEAKER_00: Um, what, what I would do. Yeah, you're right. I think when we really reach first week of December, it's the clock starts from the, right?

SPEAKER_04: So we're kind of,

SPEAKER_00: we're looking at it. Yeah.

SPEAKER_04: Yeah. I, I, I worry you see. So if we say we're going to, um, extend this in the first week of December, we know that changes get booked up in because of the change freezes in December and get pushed to January. Right. But immediately we might already been missing some changes. So you kind of de-risk that background. Well, I'm going to move into November and then actually we then need to review in February, which means we need to review in January. It just kind of doesn't make sense for this. Cause we're this process, the cliff edge. Isn't there as long as we catch it before midnight, the day before we're good, this process is we've no control on people when people raise changes. So I'm just worried that we're going to have issues.

SPEAKER_00: Uh, sorry. If the change request is created, it doesn't add approvals at that time, only when it is submitted. So if you submit a change for January in December, he's going to miss it. But if you created it, it is not going to, it's not going to trigger. But let's say if you, if you submit it in end of December, or even if in November that it would already have the approval group. So it doesn't check or add approval groups. When you create this ERT is when you submit it.

SPEAKER_04: And do you know when teams submit changes, how long ahead of time?

SPEAKER_00: I would think that they, they shouldn't be doing once in advance at best two weeks is what I would think. But, and that's exactly the only reason I'm saying, that the only reason we're doing it in the second half of December for the next extension is because we'll have embargo or people going off on leave towards the second half of December. So they might want to submit some CRS for first week of January or second week of January. That's the only reason I'm saying December, early December. Otherwise it's okay to maybe do it a week or 10 days prior to the extension expiry.

Unknown: We don't have to do it a month before every time.

SPEAKER_04: It's a, it's a, we're gambling, aren't we? Basically that's the challenge. Yeah.

SPEAKER_00: Yeah. And then we can, of course, don't like gambling with controls. Yeah. And then we of course can look at CRS. So we just like what we did this time, we caught 22. So we can of course look at what the population that missed it every time we extended, just to make sure we are not missing any controls. But hopefully if we give enough time, we'll have zero instead of 22, what we have this time. But yeah, it's something we have to of course check with the extension if you missed anything. I'm just worried that this doesn't feel like a,

SPEAKER_04: this doesn't feel like a governance process that is robust because we are kind of gambling as to when people would submit a change. So the only way to de-risk that is to, to agree this, like, you know, a month in advance and the hopes that nobody wrote submits to change that early on. And actually if we could evidence this through some form of data that would help, right? Cause I'm guessing you're guessing.

SPEAKER_00: Yeah. No, and, and the other bit is right, of course, as we discussed, if we have lesser number of population of applications into SPP is it of course reduces the footprint of number of teams that, that would raise the CR or submit the CR, right? If, if we have more application, the chances are more for us to kind of provide that greater window. But yeah, every time we have to cross check with the data, we can't be sure that just the extension is going to take care of it.

SPEAKER_04: I just don't recognize any of the kind of governance control that we have. That is a numbers game like this.

SPEAKER_00: But, but I think what we've got to look at is if we still need SPP based solution or a direct map, mapping of applications in service now would, would serve the purpose for a pro based toll gate, because that stays that that doesn't necessarily wait for SPP or a temporary block, right? That, that will stay with the application no matter when you raise the CR and the approval based toll gate will get added if you, if you do mapping directly and not use the service protection period. So what I'm suggesting is even if we keep the approval based toll gate, and if we have lesser more application, there's no case for having a service product, we should get away with service production period and just stay with the direct mapping solution for the best toll gate.

SPEAKER_05: So just, just taking a step back. So we know that the process, the SPP process is, is not necessarily, I wouldn't say it's not fit for purpose, but we know that there's gaps in the process, right? We also know the SPP shouldn't be lasting forever by its nature as a service protection, and it should be a, you know, it should have a finite end. It shouldn't be, an, an, you know, in, in perpetuity as, as a setup. So what we should do is have a target of removing it. Now, whether that's removing it this particular quarter at the end of this quarter with the challenges we have around releases over Christmas, or whether that's, you know, pushing that into February, 2027, I still think we should target to get rid of this SPP process. And, you know, if there are items or there are, there are, you know, concerns or, or things that need to be done to facilitate that, then we look at those.

SPEAKER_00: Yeah, and exactly that was the reason for me suggesting that I think we start reducing this, start exiting the application, which are already there. And we, when we have a lesser population to look at, I think our review will be much, much easier to do. Yeah, exactly. Exactly. Let's probably work towards exiting the applications that we can, and maybe regroup. So, yeah, in a month's time or a couple of weeks time,

SPEAKER_02: if we have better data to look at.

SPEAKER_00: probably just a question for you.

SPEAKER_02: You mentioned that moving, there's an option to move teams to the direct approach. Yeah.

SPEAKER_00: Yeah.

SPEAKER_02: What's the difference between the SPP and the direct approach?

SPEAKER_00: With the direct approach, all changes get additional approval added, even if you have like a patching or configuration patching. So SPP is more of a subset?

SPEAKER_02: Yeah. SPP is more of a subset.

SPEAKER_00: If you have a particular team that has high cadence of releases, they have hundreds going every week, and they have only maybe 20 out of that as software changes, they are reviewing extra 80 changes that is, we know doesn't have API changes. So it just provides that filter. And that's exactly what my suggestion was, right? If you have less than number of applications, easier to review, do they need SPP or not in the first place? Maybe we don't need SPP.

SPEAKER_02: So could you, um, I suggest setting up a, uh, an actual meeting with those with SPPs and seeing what, what, what we're exploring the options that you've just mentioned as in moving them, moving directly to using the direct method or the release page solution, or even for automation. Um,

SPEAKER_00: yeah, because where we are now,

SPEAKER_02: we don't want to be, we, we could be in danger of being in the same position, um,

SPEAKER_00: Yeah. And I think those conversations already happen.

SPEAKER_04: Certainly in CIB, those conversations are constantly happening around the efficiency of this. But we will struggle to drive that, right? Because if they're happy doing the manual process, I think the key is that once the control requirements land for the release pages and they adopt these pages, there's an easy off ramp, isn't there? Which is what Promote highlighted at the start of the call. So this will be a mechanism driven by the adoption of release pages, not being driven by us as a program, unfortunately. Certainly that's what I see in CIB. But I think that will organically change the scale of the problem here.

SPEAKER_05: So I'm happy to kind of kick this down the line.

SPEAKER_04: I absolutely think that when it comes to, say, the first two weeks of November, we need to stop there and go, right, let's plan for Christmas, because what we can't have is all these changes. They get raised and we find we've missed loads and we've got to try and troubleshoot this because we've got a governance gap. I know you're ahead of the curve on that. I just I worry about December is always a problematic month. They're trying to get anything done.

SPEAKER_03: Where are we in terms of numbers using SPP to when we started? Has it gone down at all?

SPEAKER_00: Yeah, it has gone down. So if you can see this, this is the number of applications we have. Of course, this is just just white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white white I can clean this up, but it's definitely quite a bit there.

SPEAKER_03: Okay. Because I think to James's point, I guess what we could do is say, right, we're renewing it this time, but in six months, we are closing it as an option, as a non-strategic solution.

SPEAKER_00: Yeah. Yeah. Okay, folks.

SPEAKER_07: I know we did a lot of discussion on this item. Are there any final comments? We do have a couple more quick topics that I think we need to get through. Just a quick question.

SPEAKER_00: So to conclude on this, right, I'll send the data out. I think what I need guidance from is if we should start exiting the applications which already have release pages, maybe just start having them, raise the exit request and we can start getting this population down as quickly as we can. And our data is clean to the extent where we know that teams do not have application using release pages and we can start focusing on them. So I'll send the data out and then wait for maybe more traction on this one. Yeah. Or if it's something that I should be reaching out to ITS directly, I can do that as well. But we just need to get the data out. Okay. Okay. So to get this population cleaned up, this is what I'm suggesting.

Unknown: Okay.

SPEAKER_07: Okay. Thanks. Thank you, sir. Okay. The next couple of items we have, I see we've lost Vinod. But he had brought up another item specific about training in general and that the assignment of the training on APIs. So the four modules is missing on the manager's dashboard. So we wanted to talk about that and then ask if there are any FAQ updates that anyone is seeing as it relates to the training. What I'll do since Vinod raised this topic is I'll reach out to him specifically, see if he can document some of the concerns that he has, and then we'll bring this item back unless folks have specifics they want to cover here and now.

Unknown: So I think, I think, I think, I think, I think, I think, I think, I think, I think, I think, I think, I think, I think, I think, I think, I think, I think, I think, I think, I think, I think, I think, I think,

SPEAKER_05: I think, I think, So the visibility from a manager perspective is a problem with my learning. And I think he put... I put the update there and the FAQs. So Tanya sent me some of the data that promoted to mention to her. I reviewed the FAQs. I'm still, I still think the FAQs are quite good. Right. And, you know, it's going to be, we've just assigned two and a half thousand additional training because it's the start of the new quarter and we've added additional parameters into the training groups. You know, if we start to try to go down at a person by person level on people wanting to complain about doing training or unallocate training for themselves, we're never going to do anything else. It's not valid use of the time. So I'm keen to keep the commentary in the FAQs is this has been decided by senior management. It's mandatory. Please just go ahead and do it. And, you know, the hour that you've spent trying to get yourself out of training is probably much better. Spent learning something on APIs, even if it's not 100% directly relevant to your job.

SPEAKER_07: Thank you, James. And James, there is a little question on that.

SPEAKER_08: I mean, since you about the training, right? So sometimes people challenge that I don't have any connection with APIs. Why am I assigned this training? So what generally Kevin used to do is just search for the pod and just share. So the detail that you are part of this pod and this pod is developing API, right? So generally the solution is if someone is it's very early on to someone, they just update the pod actually, either they remove the people from that. So this kind of question coming. So we had a lot of back and forth email that are going, why they have been assigning training and they keep saying, I don't do anything with the APIs. Why you're still assigning me. So I think we should take this into consideration. I mean, you are updating FAQs. That why the training has been assigned. It's not just about EPA, but it's about because you are part of the pod and the pod is responsible for.

SPEAKER_05: The FAQs have that in there. Absolutely. So that's fine. I agree. But I say, I would also, I, you know, if people spend a long time trying to get, you know, learning is a good thing. You know, people, even if it's not necessarily exactly aligned to your particular job, this is not a bad thing to start. Becoming familiar with because APIs are all over. Right. So, so yeah, but no, there is, there is logic in there as to why people are in there and why they've been assigned, et cetera. And we can do that, but from an administrative perspective, you know, and I know Kevin was, was good on this one. But it just, I don't think it's time well spent.

SPEAKER_07: Fair enough.

SPEAKER_05: Thank you.

SPEAKER_07: Yep. Yep. Okay. Uh, last tidbit for us today. Is that the, uh, action tracker has been updated. We're not going to go through it cause we're out of time. Um, but you'll be able to see the latest and greatest items that are closed as well as open. There is one item though, that I want to highlight here. This is due at the end of the week. The high level estimates and plans are due to some on to support the MSI closure preparation, aiming for a draft by the end of this week. So this is a Spock activity, just wanting to reiterate this because it was. Mentioned on last week's call.

SPEAKER_04: Do we have a plan yet from our CTO colleagues around when the tooling will be available to do X, Y, and Z? Yes.

Unknown: Cool.

SPEAKER_04: Could I either see that or is it in, is it in a consumable format? It is obvious to me.

Unknown: Yeah.

SPEAKER_04: Yes.

Unknown: All right.

SPEAKER_07: So we'll take an action to set it up. Okay. Okay. So we'll send that across to the team and then again, uh, please direct any and all questions to James and Sumana.

SPEAKER_04: Brilliant. Thank you.

SPEAKER_07: All right. Cool beans. That brings us to any other business, uh, with just a minute left. Um, actually we're over time, but we had a lot to cover today. Um, anybody have anything else they want to raise? All right. Notes, minutes, actions will be out shortly. Thanks everyone for all of the discussion. If you need something, you can give a shout. Have a great day.

SPEAKER_09: Thank you. Thank you. Bye now.

SPEAKER_07: Yes.
