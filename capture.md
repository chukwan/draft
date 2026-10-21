Seeny: across the board are and then we have five and six which are I think we have already reviewed one I think there is a great position on one and the last one is probably something which probably it says to be reviewed let's see if anybody has got any issues so that's the plan for today unless there is anything else anyone wants to add before we start so let's start with R1 right now what I have done here is I think we had a brief discussion last time and as sorry but as I see your hand is raised yeah sorry but I just want I am wondering

SPEAKER_02: are we going to add rules regarding all APIs should go through the API gateway or not and then we have to go through the API gateway and then we have to go through the API gateway which will help in the discovery and the inventory part or it's not in the scope for

Seeny: discussion it's not in scope of discussion for authentication certainly but it is I mean it is on the table for discussion in the wider standard so regarding that particular standard Mutaz I would just mention that we had added that to the original list of standards but there was pushback and we had taken it out so it was demised I can show you a record where that standard is demised for some reason I'll share some history around it but if you think and have a valid reason why we should have it maybe we can add it and we can bring it up for discussion right and see what the views across the board are but yeah thanks for raising that we'll make a note of it and we'll bring it up into future sessions so the first one is authentication methods I think we had a brief discussion about API API endpoints I think they were this discussion was in the last working group call

Daniel: Darren I think you had suggested it's generally when we talk about API it's generally API endpoints

Seeny: also I had another feedback saying why don't we merge this API endpoint and I think it's a good idea to merge this too so what I have done is I have removed the endpoint security coverage and something which was probably a bit of a duplicate and I have made this I've changed this to say that all API endpoints must implement authentication using an approved API security pattern unless it is a valid unauthenticated journey with an up accept exemption for this standard now I have also removed the health check and info endpoint and I have also removed the API endpoint based on something that Dennis raised last time I think it's more of an implementation detail so probably we can cover it in how we implement it by meeting the list of all the standard health and telemetry endpoints and excluding them from this assessment but at the same time if there are they are not available I think this will be published later on the as we implement the assessment but if they are not a part of the list you can still go ahead and raise a exception or an exemption for the standard and gradually probably we can end up having a process where that exemption specifically for health and info or telemetry endpoints can kept can can get added to this list Daniel yes I I think

Daniel: I I was there when Dennis was saying that the health checkpoint uh could be granted as an exception however I'm I'm not sure that we we we we should totally you know ignore that or you know take it out of the scoop when some API endpoint claimed that is an uh health check endpoint because you know uh that that is basically an an endpoint or you know there is an endpoint we expose it to the public which um we may uh leave it uh cam zero or you don't you know basically no no off authorization in order to you know get inside right so I'm not 100 sure that that is that is you know what I feel comfortable with because you're at at the world of AI you know you basically if you expose any like an authenticate endpoint out there you know it someone could be easily to you know to break it in or something like that so I'm I'm not 100 sure that we should allow this for a health check endpoint. I'm not sure what the other guys, what you guys think, but this is what I wanted to raise.

Seeny: I think maybe it's that for externally exposed endpoints rather than internal health and telemetry endpoints, Daniel. I get what you're saying. I get your concern. Just trying to explore it a bit more. Is your concern more on externally exposed, external APIs? Yeah, I think so. Yes, correct. Yeah, yeah. Okay.

Avinash: There has been some old debate related to health endpoints. It is a concern. It is always a concern. That should be a dedicated endpoint on production systems and telemetry. So in one way, that people keep authentication or other telemetry endpoints for another tool to consume to get the live status for it. Now that another tool which monitors the API live is they can't make authenticated. They don't have those credentials at least in production to make authenticated. So people go different route.

Seeny: Right. I think... What I would say is this standard is not now saying that the health check endpoints have to be unauthenticated or are automatically exempted. What it is saying is it's a bit more generic than that. And I think we can take care of those scenarios in this process, right? Where we approve such exemptions, right? And where we implement this curated list. So I think it's more about how we implement rather than changing.

SPEAKER_05: The standard.

Seeny: Do you agree, Daniel? Or do you think there is something we need to change in the wording of this rule here? Because it's more generic. We have removed health and info endpoint, which were there before by default.

Avinash: Yes. So by default, it just suggests that all the endpoint must have authenticated. Absolutely. It must be authenticated.

James: Yeah.

Avinash: Now for any exemption. So let's say it is a general practice that people have some... health endpoint, but they don't try. So if we find there is a health endpoint and this is not authenticated, then we will throw it away by default.

Seeny: Yeah. By default, if there is not an approved exemption or I think there is another level of implementation, right? So in the implementation, then we can do certain things, right? So for... say our standard platforms, say I'm just making it up. I think this needs more exploration, but I think it depends on what patterns people are using, right? To define their health and such endpoints, right? And if we come across some pattern followed by certain APIs on a certain platform, then we are aware of those patterns. And if those are internal APIs, we may exclude them. So that's an implementation problem. So it's an implementation decision that we can take later on, right? And we can say that, okay, by default, these are internal APIs which are sort of... and following this pattern. So it's a default list of approved exceptions, right? So something which we can take later on rather than worrying about it just now. Taren.

James: Yeah, just, I mean, one thing that... more that springs to mind in this whole conversation is authentication on its own is... I don't know what exactly you gain from that. I mean, it's usually... it's authorization what matters, but you can't do authorization without being sure that you're interacting with a genuine party, right? So if you just put aside authentication and say, okay, let's say we are doing authentication for a health endpoint, on what basis are we authorizing people to access that health endpoint or systems? Because if it is a case of, well, anybody can access that endpoint, what are we gaining by doing authentication to then say anybody can consume it? Does that make sense as a line of argument? In fact, for any endpoint, to be honest, yeah? If you're not doing authorization of the caller on any particular endpoint, what was the point of authenticating first?

Avinash: It depends upon system, isn't it? You can't make a generic statement. Like, there is a small application which has five endpoints. It doesn't need any further authorization. If you are authenticating, it's a little funny. That's the only other function. But in that case, what we're saying is

James: anybody can use it as long as they are authenticated, right? And so then if you look at, well, what are we getting out of that? We might be getting, for example, the caller name. Ultimately, it might be a case of, well, we authenticate them because then we know, then we can log their information. Yeah? But that's not authorization, is it? That's just getting information for logging purposes or whatever. I'm not saying this needs to be in the standard in any way. I'm just saying that if we're going to argue about whether it's appropriate to authenticate for a metrics or a health endpoint, right, then you've got to ask the question about what kind of authorization is required as well. Because for other endpoints, it's quite obvious. You know, you're doing authorization because you might need admin privileges or you might be restricting, you know, the data dependent on the area of the organization. You know, something that relates to the authorization side. And authentication is a necessary step to be able then to do authorization.

Seeny: I think I like the views. The main question is, does anything need to change in this rule?

James: Well, I don't think so, Sita, from that perspective. Yeah, because it's broad.

Seeny: I think we are leaving those sort of details up to the implementation, right? So this approved exemption, right? If we really think as a group, right, that there is no value in having authentication around health check endpoint of internal APIs, say, for example, we can, right, implement such that they are auto-approved for exemption. The standard ones that we are aware of and the ones which are non-standard, right, they go through a process for approval. So I think it covers those scenarios that way. But I think rather than, you know, I think going into a rabbit hole, I think this is quite straightforward. We have, in fact, removed the original clause which stated that standard endpoints will be exempted by the rule. So we are no more saying anything would be exempted. We are just talking about approved exemptions. So Daniel, Avinash, others?

Avinash: Yeah, the statement is fine. The only thing that I don't understand how we can validate is approved security pattern. The security pattern that the API uses. I think, yeah, I think you are coming, Avinash,

Seeny: purely from the perspective of how an assessment tool would work, right? I think there are two aspects to a rule. One is the implementation for API teams, right, what they need to do, right, which may not be very much assessment oriented. But you're right. From your perspective, you would rather see it from another angle where you would say, how would I assess against this, right? So I think I have been thinking about this question a lot. And I personally think this pattern, right, this statement is more applicable to the API teams than the assessment team. And I think the takeaway for the assessment team would be all endpoints. So you need to check all endpoints. You need to look for approved exceptions. Now, how to validate if they are indeed following an approved API security pattern is probably taken care of by few other rules here, like usage of trust token, usage of verification of that end-to-end trust token. Because these are the individual elements mentioned in that approved security pattern, right? Certain behaviors, right, that we are looking for. So that's what I think at point of enforcement, right, at enforcement points, basically having a valid policy or a plug-in configured, right? So I think those are the individual rules which will enable an assessment tool to show a strong indicator whether the API is meeting the standard or not, right? But I think you're right. I mean, how would you check for this particular rule if you look at it just independently, just individually? I think you might have to delve more into the security patterns and see what we can do there, right? Or we can have to come up with something. But I think this rule is more like a blanket rule applicable to API teams, right? Pushing them towards the right behaviors. And then you have few other rules which enable an assessment tooling to ensure that or provide rules which basically you can check against.

Avinash: Okay. Yeah. Statement-wise, I don't have any problem. So let's move on during implementation. Of course, whatever challenge we face, we will discuss further. But for now, it's fine.

Seeny: Right. Yeah. No worries.

Avinash: Yeah. No problem.

Seeny: I think there is one more change I have made. I have removed API key statement from here. Now, the reason is in the original standard, the usage of security pattern itself was a should. And hence, we had this to stress out that this is a must, the non-usage of API keys, right? It should not be used. It's an absolute anti-pattern. Now, things have changed a bit. So we are saying API security pattern is a must. In API security patterns, none of the patterns at the moment talk about using API keys. So I feel this is a bit redundant. Now, having said that, there could be, right, there could be a security pattern in future which has gone through the system. It's been going through all the valid governance and has usage of API keys in a very secure way. Comes up, right, here. Then the standard goes for a toss. It needs to be revised, right? So I think we should not specify those individual elements because now we are completely, we are saying this is a must. And these patterns basically are driving the behavior. So I have removed this. This becomes a bit redundant. Does anyone have any issues or concerns with that?

Darren: Sini, what is the harm if we keep it right until we remove the updated standard? I just mentioned the harm, right?

Seeny: I think the harm is this security pattern is not controlled by this group, right? These patterns are now owned by cyber. It has a separate governance. It's a separate forum, right? I'm trying to, these patterns are being handed over. So I'm trying to get in contact with the right people so that we are up to date if anything changes here. But say tomorrow, I've seen few things, right, where there is probably usage of this, right? And if cyber has reviewed it thoroughly and they are in approval, if it is being used in a secure way, right, which is cyber approved, I think this standard then becomes absolutely invalid and in conflict. So that's the reason I'm removing this. And moreover, our security patterns at the moment, they don't indicate usage of API keys. So that's very clear there. So we really need to mention it.

Daniel: Because if we are mentioning this, we'll also have to mention don't use username, password,

Seeny: just username, password, right? And other things. So does it really add value is the question, Sanjay?

Darren: No, I think that was not my question. I got what you're saying. And this standard security pattern, it implies that whatever is there, we must be. And something which is not there, we shouldn't be mentioning again. I think I'm referring to a standard site. This is dual. If you go back to a standard where it is already mentioned. So are we updating that as well? Or are we waiting for API security? This is all going into standard only.

Seeny: So this is the next version of our standards. This will be going into our standards formally. And this version will be version one. I think it's version one just now. Once we go through governance, right, this will become version two with all the security. So this is not going to remain in its current form. Once we go through all the processes that are required here. So at the moment, you're right. This is very well applicable to this standard. But once this becomes live, right, it goes through all the governance phases and is a. You mean the rules, right?

Darren: Rules are actually parts of standards.

Seeny: So the rules will be in this instead of commentary. There will be rules here. So it will be standard. It's not separate from the standard. So we are not going to have. Okay. So I'm just trying to visualize any.

Darren: I got that. What I'm trying to understand the sequence of steps, right? So we have standards. And for each standards, we have set of rules. We are drafting those rules right now. What you're saying is once it is approved by X forum, it will be reflected back. Into the standards because it is part of the standard. So what you're saying is first we'll go through it. It will go for approval. Once it is approved, then the standard will be reflected back with the approved rules, right? Yes.

Seeny: Yes. Until then, this is the standard. This is applicable. Correct. Okay.

Darren: So that was my question until we get this updated. What is the harm? But you answer that. Okay. We are going other way around. We are up to in first rules and then we're updating the standards. Okay. That's always the process.

Seeny: So this what we are working on is draft. Once this draft goes into whatever platforms, AERG, TDTA and all that governance forums, right? Then this will be added to our standard and they will be live. So you won't have commentary anymore.

James: Just one more thing that springs to mind here, Sini. And it's, you know, like kind of like negative tests, right? So clearly API keys are a thing. And can be used because it's how you can identify where your traffic is coming from, you know, customer groups or whatever. It's just a case of not using them, using an API key for authentication. All right. So actually implementing the standard, if it was, you know, if you have to try and say, is an API key being used for authentication, that's probably hard to determine without looking at code at least. But that's different from say, basic off. If say we say basic off isn't it? You can actually test for that because the presence of a basic off header is an instant fail, isn't it? Whereas the presence of an API key is not an instant fail because it's much more complex is, you know, to understand whether it's being used for authentication. Is it being used?

Seeny: Yeah.

James: But nevertheless, you want, you also want developers to know, right, that API keys shouldn't be used for this and X, Y and Z shouldn't be used. So I don't know if that's how we cover that. Just general sort of advice to people. You know, not something that's necessarily checked via the rule base. Yeah, tooling. But it still needs to be mentioned in the standard. Maybe it belongs in the preamble at the top before you get down to rules. You know, it's just general points of principle.

Seeny: I mean, I'm happy to keep it here, right? And if Sanjay, Taryn, if everyone thinks, I think it's good to have it here. No issues. I was just thinking that it's a bit redundant now that we are saying it must be an approved security. No, I agree with that.

James: And I agree with the author that if we include this one, then you might as well add on and you should not use basic op. You should not do X, Y and Z. Yeah, exactly. Right. So I generally support the idea that it's redundant in this particular box. Maybe a best practice, Taryn? It's just that the actual information, I think, is still useful to be expressed somehow. So people are aware. Yeah. They're aware of the danger of using API keys in this way. And yes, if you use an approved API security pattern, you should not end up then using API keys for authentication. Right. It's just useful to let people know that in some way. But maybe it doesn't belong in this one.

Darren: Yeah, I think.

James: Thank you. I agree with that.

Darren: And I think I feel that, OK. I think we should really understand why we are writing this rule. Just to make our team very much informed about what the standard is talking about. I understand the redundancy, but at least it will be very clear to our developer or whoever is developing the tool. Right. It will be any victim that, OK, this is there. I agree. API security patterns are there. But we know that API keys also use somewhere accidentally or intentionally. So it should be very clear that, OK, this is not the pattern. This is not the right thing to do. And we are just mentioning it. Now, whether you are implementing in tool or not is different thing, actually. So I mean, I'm happy to add a note if everyone thinks it does add value.

Seeny: I mean, it's there at the moment. Not a big issue. It's all valid. What we are seeing here is not untrue. Right. It's an anti pattern just to use it. Just to use API keys. So. I think I'm fine with that statement in there. If everyone is OK with it. I mean, we can add keep it there as a note. All right. Daniel, I see. Oh.

Daniel: Sorry, it wasn't a race. Sorry. I passed the wrong button. My bad. All right.

Seeny: OK. No worries. All right. So let's keep it for now. OK. And maybe we can come back to it in future revisions to see if it's still applicable or do we want to get rid of it. So I think that those are the main changes. Darren, I think you rightly pointed out in your comment that mentioning API classification was not right. So I've removed that part. So I think we should be good with this. So before I move on to the next big change that I've made, any other thoughts on this? This is what we are keeping.

Darren: Right. I'm not sure. So we're writing rules, right? So we are detailing all the standard as much as possible for our team to help. Correct? From implementation point or from the guidelines point of view as well. Let's say you remove the second point, right? The API endpoint. Because we are coding in R1 as well already. Yeah. And. And you feel that it is already covered. But even if we keep the second one, we can always just give more guidance to our team, right? It's not that you have to implement. Whenever you are implementing, you will be implementing R1 as well as R2, both. So earlier it was just API, right? Now we are referring to API endpoints. So I'm okay with anything. But I don't see even, I mean, any drawback of removing the second as well. That every endpoint must be required one of the approval authentication.

Seeny: Yeah. So this is where we are removing that because we have merged. We are here making it clear that this is all, all API endpoints rather than just saying all APIs.

Darren: Okay. And our title of the rule standard. Standard itself same, right? It is saying the same thing. If we just go back to the standard page, it is saying the same thing. Instead of endpoint, I think it is just mentioning all API must implement authentication using a approved. It is kind of same thing. The implementation should support. Go up a little bit. So here it doesn't say API or anything.

Seeny: It says the implementation should support. So I think we are making, this is a bit. Vague. And that's the reason we are doing this. Right? So this, I believe this is more clear now. Right? What we are expecting here. We are not keeping any do's ands. I think all API endpoints make sense. And we are mentioning API endpoints right here. Then we don't need to mention it again. Right? So this is, this becomes redundant duplicate. Because it's saying the same thing. Fine.

Unknown: Okay. Just one thing. Last.

Darren: Okay. That's fine. So we can merge that. Implement. Right? We are talking directly about implementation here. And not enforcing anything about the declaration. So are you saying that implementation would cover everything? Everything. Yes. The declaration. Declaration. Absolutely. I think we moved away from that. Right? So. So. So. So. So.

Seeny: So.

Darren: So. So. So.

Seeny: So. So. So. So. So. So.

Darren: So. So. So. So. So. So. So. So. So. So. So.

Seeny: So. So. So. So. So. So. So. So. So. So. So. So. So. So. So. the dependent library somewhere it should be called out actually i'm not talking about any

Darren: contract or any particular open api specifications or whatever but at least i think we should call it out somewhere that this includes the contract as well as the actual so people may take meaning of this that okay i i have implemented it but i don't have any contract so do you see any issue with this there shouldn't be anything with that i guess if they have they are following

Avinash: important isn't it contract is it is still important contract is important but not from

Seeny: an authentication perspective yes yes i i i agree with the point i agree with your explanation of

Avinash: implementation i was just trying to highlight see there is there are java codes we can write to develop an api there are tools that can generate an api and everything is used in hsbc so my view is that from a standard perspective if we go bit if you try to go in detail here in the standards and its definition then it might raise further more questions that how much we are going to where we are going to stop uh writing details exactly yes

Darren: too much details i mean right at least whatever we used to do whatever our teams are doing we should we are trying to mention it i'm not saying we should write one pager details for just authentication implementation is very broad right so

Seeny: i mean i'm i'm happy uh sanjay for you to rephrase it if it makes more sense to the teams if if you can come up with new wording i'm okay with that I mean, whatever works, right, makes more sense to the teams. I'm happy with that. I'm just wondering the other option is maybe we can clarify here implementation means whatever contract, runtime, implementation, right? I mean, it's the entire API implementation. I don't know how better to define it. I think defining it will cause more issues, right? If I don't touch a certain aspect, people will come back asking, oh, your implementation definition is not covering this. So I'm just wondering what is the best way to clarify. I'm happy to make changes if this is not right. Let me come back with something.

Darren: I have something, okay? You see whether it works or not. But I'm not asking for too many details. Just some more details that whatever we use. Otherwise, there wouldn't be any difference between the standard definition and the rules, right? We're writing rules because we are providing more details around the standards. We're not deviating from the standards. But at the same time, we're ensuring that our teams understand the rules whenever they are checking or implementing or building any tools, right?

Seeny: Agreed, agreed.

Darren: I think this rule, like Avinash also raised before, right?

Seeny: It's more applicable. I get this is a blanket rule. I think. It's I have. I had those thoughts, Sanjay. What you are thinking, I get what you're saying, right? I think this particular rule is very much what the standard actually is, right? Maybe a little more deeper we are going, but we are not going into absolute low level details. Now, I started with the way these patterns are implemented. But then I thought. It's not right for me to define explicitly here, right? All these patterns because it's managed by someone else. So it will always easily go out of sync. Hence, I think we made it a bit more generic. We brought it level up, right? Now, this rule is more applicable for API teams to understand that they have to comply with one of these security patterns, right? They can't just use anything. Any other. Method, right? Which has not been through governance and which they think is right, right? So it's not a kind of it tightens things up, right? When we associate it with patterns. So I think this the first standard might be a bit more generic and would make people go to different pages, which is the actual security patterns. But then when you look at the other aspects, other rules, right? They are all. Not all, but some of them like this one, right? These are all indicators that they are using one of the approved security patterns. So it's a little bit more specific as to what we are asking them to do. But I agree. The first rule is a little bit more generic because it's dependent on this documentation and approved patterns.

Avinash: The I am just going to add one more point in here on security pattern. I wanted to move on. But. I see. You. When we were being audited for MR. The reason for rewriting all this is that there are standards which we can't validate. We don't have mechanism to validate. So let's say we are defining this rule that API security patterns should be implemented. And then for some other country being audited, then we can show that. Yeah, there is this tool which does this. Can. But we won't be able to prove that API security. Pattern. Is being validated. Neither the having its HSBC to each other. So when I authenticated it, authentication header ensures that one of the security patterns is security back.

Seeny: But is it just me or it's not?

SPEAKER_03: No, it's not. I think not just you. Yeah. Yeah. Yeah.

Seeny: I mean, actually, there.

Darren: Yeah. Yeah. I think I was on. All right. No, it was happening on an offer. Yes. All right.

Seeny: No worries.

Darren: Yeah.

Seeny: I think that's fine. I think we have spent a lot of time. I was planning to do to hopefully. Sorry. This is. I don't know. No, no, no, no. Don't be sorry. I put an action on you, Sanjay, to rephrase this so that it makes more sense to the teams. Right. And maybe I mean, give it a try. I think simply. Maybe adding some note here would help. Or you think this needs some more words to define it better than happy with that as well. Okay. So let's see that in the next session. But let me move on to the next one, because this was the one which we already had reviewed a few times. But this one is something which has drastically changed. So let me at least introduce the changes to you. And maybe we can discuss in the next session. So originally, we had something saying executed tests must demonstrate that authentication fails when tokens are missing, expired or invalid. So I think it was a national data. Both of them commented and quite rightly, basically, it seemed that the focus was on the token. And that was the focus. That was the focus. That was the focus. That was the focus. That was the focus. And the focus of that standard was more on the test case availability, right? So existing test cases to prove this rather than the behavior of the API. So I took that. And I think there was another standard around using an approved ITP, which also was a bit vague, because then we have to show what are the list of approved ITPs. We do have one, which I've got. But then I think the assessment, too, was that we have to show what are the list of approved ITPs. So I think the assessment tool doesn't bother. I mean, it's difficult for them to verify this. At the same time, the API teams, it's difficult because they would use one of the existing authentication implementations mostly, okay, provided by DSP. So I have changed, now merged the two aspects here, right, what we were trying to do here, right? And it's not just the IDP. But I think we should be validating. There are a few other things. There are a few other things that needs to be validated. So I have changed this. I've removed the test case part of it. Absolutely. That's not what we want the standard to be. So now the standard says the APIs must validate every incoming end-to-end trust token, right, using a valid trust token verification mechanism, unless it is an approved unauthenticated endpoint, right? So if it's an exemption, then obviously it doesn't apply. So it's not valid. It doesn't apply. For all authenticated journeys, authentication must fail when tokens are missing, expired, or invalid, and request must not be processed in such cases. Okay. So that's the behavior that we are expecting from the API in such scenarios. Now, I've listed at the moment valid trust token verification mechanisms. It's mainly the two DSP instances, CIB and IWPB, right? And I think the IWPB one also includes Kong. So I'm just before this call I pinged the contact who developed the Kong plugin for the end-to-end trust token verifier just to validate the latest version. I think I have a response, but I haven't seen it yet because of this call. this call. Once he confirms, I will add that as well to the list, right? So that's the change I've made. Thoughts on this? First of all, I'll ask Darren, because I know Darren, you had a comment here where you were indicating something similar, right? It's not just IDP, but there are other things that needs to be validated as well, right? Like token signature and so on. And yeah, I think the test part, I don't remember if you had a comment on that. So do you think this addresses your comment or the area that you're looking to resolve?

James: Yeah, yeah, I think so. Yeah, the main thing you're calling out, you know, it's less about the IDP and more about checking that that trust token can be trusted. And it behaves in the right way when there's

Seeny: something wrong with that token. Yeah. Okay. That's good. Sorry, Avinash, were you saying something?

Avinash: Yeah, the good part of this rule is that I like it better than the IDP. It ensures sort of IDP as well. And approved IDP, I think, apart from DSP, there is none. Nobody is trying to do something else. No, I have a list of approved IDPs I'll share with you, Avinash. But you're right. Yes.

Seeny: So I think that was a bit more a level deep, which probably even API teams don't know and assessment team would find it challenging. So I think this makes more sense.

Avinash: Yes. Yeah. So this is a good part of that. We are ensuring at least that the valid token verifier is used either in the code or in the gateway. The variation is still a challenge, but it is going to be challenged for all the rules. That is also fine. One more aspect of it is that like for internal tools, apix itself, we authenticate the user using DSP token in Ui.hermetic naminghermetic naminghermetic naminghermetic naminghermetic naminghermetic naminghermetic naminghermetic naminghermetic naminghermetic naminghermetic naminghermetic naminghermetic naminghermetic naminghermetic naminghermetic naminghermetic naminghermetic that AM token we generate Apex Spaceship token and similarly there are other tools which is also used. So we are not going beyond the security pattern, this is just that we are not using the short-lived token generated by DSC. You are using long-lived token. Long-lived tokens are used,

Seeny: yeah, long-lived tokens. I think I was going to add a table on rules that we haven't touched upon or covered and one was, one at the top of my mind was short-lived tokens. We have not, we don't have anything covering that. I thought the trust token verifier, I think it mainly verifies the signature. Of short-lived tokens.

Unknown: Yeah. Yeah. Yeah. Yeah. Yeah. Yeah. Yeah. Yeah.

Seeny: Yeah. Of short-lived tokens. Not yours, right? Or does it?

Avinash: Yeah. No, no. It doesn't verify the long-lived token, AM token. It doesn't verify.

Unknown: Okay.

Seeny: I don't know. I think that aspect we haven't covered. Do we need to cover it is a question for the group, maybe. I'll make a note of it.

Avinash: Yeah. And also there are mechanisms, like in Nexus, you can generate a token. In Git, you can generate a token. Okay. And using that token, you can generate a token. Okay. And using that token is very valuable.

Seeny: Yeah.

Avinash: Similarly, in Epix, you can generate a token.

Seeny: Right. It's not a best practice, though, to have those long-lived tokens. But the question is... Long-lived tokens.

Avinash: Yeah. The mechanism of translating the long-lived token. So, of course, there is an authentication mechanism, which where you will find the roots on DSP, that a valid ITSO can generate a token for a specific business application. So, in a way, the token is generated by the validator. But that token can be used to generate a short-lived token, and that short-lived token performs other things, like other operations. And it is practiced in different... It is not only Epix. Now I have... You know, it's been some time I have looked at the security patterns, but yeah, so I can't comment on the security pattern. What is this security? Security pattern. But it is also commonly used, and it could impose some challenge sometimes.

Seeny: Okay. All right.

Avinash: Let me have a few discussions on this pattern.

Seeny: So, you are saying these long-lived tokens are not just directly used, but they are used to generate short-lived tokens.

Avinash: Yes. Yeah. And it is widely practiced. Like, there are long-lived tokens. Internally, the short-lived token is generated, and then short-lived tokens are used for further exchange. Okay. Take that.

Unknown: Okay.

Avinash: And this case, I have seen for internal billing mostly. For customer-facing APIs, I mean, what you have written is, you know, all the banking APIs mostly, you know, apart from... In my life, I have seen a CI... They use short-lived. Yeah, they use a DSP-generated long-lived token, the session tokens, and then the session tokens for every API call. Okay. Okay. Okay. Okay. Okay. Okay. Okay. Okay. Okay. So, every token is converted into this E2E trust token with a short-lived token, and valid for the customer setting, you know banking APIs for internal tool links.

Seeny: Okay, all right, now thanks for letting me know. Let me check with Jonathan Higgins and if possible I'm trying to reach out to Maxscope as well who is going to own the patterns. So, let me see if there is some variation that covers this scenario. Daniel, thanks for naming me.

Daniel: Thanks for naming me. Actually, a question to James right, remember back in the day that I was referring the statement 3 of the authentication authorization of an API, I raised the question- Yes, DST issue right? So, right when you guys saying that this is like a kind of like an end-to-end token, does that mean that if the traffic come from external is go from either eAPI, PAPI and SAPI. If there is end-to-end transfer, does that mean that the PAPI itself doesn't need to re-authenticate the token? And that is possible because it's like an end-to-end, meaning that as long as the first gateway, which is the API gateway, external gateway, validate that token, the PAPI and SAPI will not necessarily need to re-authenticate that token anymore. Is my understanding correctly?

Avinash: No. Every layer of the API needs to validate the token. So the full exchange for banking journey is that from external, like from mobile app, when you biometric or credential, whatever is the authentication mechanism, when you complete that authentication cycle, there is a session token generated by DSP. And that is still, it is a long-lived token. Now for every operation, that long-lived token is converted into the short-lived token. Call it a trust token. And that trust token has validity of almost two minutes, as I remember. And every layer of the API has to have this validation of this token. Otherwise, how we can defend our API from ours?

SPEAKER_03: Yeah, I would agree with that statement, Abhinash. Certainly from a design principle point of view, I don't know if there's any situations, Daniel, where you would do that. But it feels like, you know, if you go in through and you had a single token that was created at the gateway level, and then that allowed you access to everything else, that doesn't sound like a secure patent,

SPEAKER_05: right? It should not cross HSBC's network, right? Exactly. Exactly. Yeah. It doesn't go outside. Yeah.

Avinash: Yes. So when you then there is a two token scenario sometimes. And Sanjay might add it that, you know, one token is used internally. And if you're that internal API need to communicate with other system, which is externally hosted, then there are, you know, other token, you know, rotates within the journey. It is very edge case anyway. But this trust token, every API has to be, you know, I'm talking from banking journey, that 100% of the API has to be public. There are

Daniel: anonymous tokens also. Right. Thanks. Public API should not be 100% public. Yeah. Thanks for the feedback. Also, Daniel, I've shared the link of that external API security pattern, right? If you

Seeny: go over that, right, probably it would answer some of the questions. Yeah. But when I was talking to

Daniel: the API team, they, you know, they, they were, you know, they were, you know, they were, you know, they, most of them saying that, you know, in PAPI, there's always a pass through, right? They do not do anything like they basically pass through the, the API from, you know, from the external to the right SAPI, right? So, so the, so the PAPI itself actually doesn't do any authentication authorization, right? So that's why I raised it, you know, that, that, you know, that concern of the traffic.

Seeny: Implementation should also do it. It's not just at the gateway that you do and it's skipped at the fulfillment, the fulfillment. Yeah. Yeah. Yeah. Yeah. Yeah. Yeah. Yeah. Yeah. Yeah. Yeah. Yeah. Yeah. It's not a straightaway. Right? Yeah. At least authentication should be done in fulfillment.

Darren: Yeah. It depends upon technology though. And EEAPI P and S is our internal terminology. So we need to better understand what exactly it is policy enforcement point and what is triggering from. You can call it PAPI or EEA experience API. It doesn't matter.

Daniel: Right. Understood. Yeah. I'll so, so that is the next question that we need to at least I I need to look at it is whether you know the DSP has you know the capacity to take up all the traffic which they do not call right now. So I think that is you know that's what I need to go back to the team and find out.

Seeny: Okay, alright. Do you have the right DSP contact, Daniel, for that?

Daniel: I do, I do, yeah. In the Hong Kong period there is you know I was talking to the DSP 3.0 team which they have it developed right now. So I raised that that you know the traffic will go wide or you know go much higher if everybody in Hong Kong region implemented authentication across all three layers. That is why I raised that point.

Avinash: It is authentication, Daniel, sorry I'm just begging you. So on one layer we do authentication. Authentication means generating the short-lived token from long-lived. And then short-lived token is just verified in FW. So for that verification the token libraries that CME has listed in this rules, those token libraries are listed there. So it does not call for every layer, it does not call the DSP service. It is just the token verification against the signature. So how do the validator validate the token if it doesn't talk to the DSP? It has to, so those token libraries have the signatures. Okay. So the token libraries have the signature and the manifest. Using that manifest they get those keys and validate the token. So it is just the validity of token and the expirability. That's it. Right. You can, you know, one of the two links have, one of the two links that CME has listed have this detail, you know, there are sequence diagram on the token exchange and the . Okay. So it is not like it sends the token to DSP. Okay. Okay. Okay. So it is not like it sends the token to DSP and DSP says, yes, your token is valid. It happens inside the library itself. Yeah. DSP in fact generates the token.

Unknown: Yeah.

Seeny: So at, yeah. So short-lived token is generated at DSP on, you know, external facing API or whatever

Avinash: at one place. And then that short-lived token is rotated within the journal and validated at every layer. Okay. So that's it. Thank you.

Unknown: Thank you. Thank you.

Avinash: Thank you. Thank you. So thank you guys for listening.

Unknown: So thank you guys for listening.

Seeny: So thank you guys for listening. So thank you guys for listening. So thank you guys for listening. So thank you guys for listening. So thank you guys for listening. So thank you guys for listening. So thank you guys for listening. So thank you guys for listening. So thank you guys for listening. So thank you guys for listening. So thank you guys for listening. So thank you guys for listening. So thank you guys for listening.

Unknown: So thank you guys for listening. So thank you guys for listening. So thank you guys for listening.

Daniel: So thank you guys for listening.

Darren: So thank you guys for listening. So thank you guys for listening. So thank you guys for listening. So thank you guys for listening. So thank you guys for listening. same rule next time or what because i have two questions on that i think yes i'm going to yeah

Seeny: so do send me your questions offline that will help um so that there are any major concerns we can address those and we can be ready for the next call so this will carry on in the next call and here sanjay we need your help uh if you could review and get us your version uh we could review that as well again i would request sanjay yourself as well if you could review each of them offline and provide your comments that would be better because uh i mean such issues you can easily raise offline as well right uh review comments so that we can address them and hopefully the next working group we can uh finalize and agree on this i think it's in a good shape now uh but yeah just a little bit more to go um so yeah apologies we didn't have much time to discuss anything else but hopefully daniel uh we yep helped you with your query all right okay then that's the end of today's session thanks everyone for your time and hope you have a great day thank you

Unknown: thank you hmm hmm hmm hmm hmm hmm hmm hmm hmm

James: hmm

Unknown: Thank you.

SPEAKER_02: Thank you. Thank you.

Unknown: Thank you.
