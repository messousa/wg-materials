----
**Logistics:**

- **Meeting times:** Tue 9:00 to 10:00am EST

- **Location:** https://ietf.webex.com/ietf/j.php?MTID=ma0e97cc97c4cd71bb59cf1a094682686

- **Minute takers:** Ayoub Messos, Jensen, Jordi, Kai, Lauren, Lei Yixue, Luis, Mahdi, Motoyoshi Sekiya, Qiao, Qin, Richard, Roland, Sabine, Yuhang, Ziyang Xing. 


------------------------------

**IETF, ALTO Meeting: February 7th, 2023**

**Agenda:**

- Round-table updates
- Chartered items
- Review of 'In Progress/Discussion' tasks: https://github.com/orgs/ietf-wg-alto/projects/1/views/2


**Minutes:**

Note Taker: Ayoub Messos


**Attendees:**
Qin, Jordi, Richard, Sabine, Roland, Jensen, Kai, Ayoub (taking minutes)


**Agenda:**
1-	Round table / Priority Items
2-	Chartered items:

----------------------------------------------------------------
**1. Priority Items**

	- Date for the "interim meeting" 23rd or 24th of Feb (to be closed very soon).
	- Focus on the Chartered items and have them validated:
		- ALTO new Transport draft update
		- ALTO O&M data model draft update
		- ALTO Deployment
		
- Qin, Jordi, Richard, Sabine:
	- ALTO New Transport
		- Richard uploaded a new version of the draft.
		- Review is needed from partners.
		- Need some volunteers to help review both documents:
			- ALTO New Transport : Sabine, Jordi, (Luis?)
			
			
	- New time is the 23th of Feb: 9pm EST (3pm CET) (Qin will send the invite shortly)
	
	- Discussions for plans and the tentative agenda for the meeting in IETF 116 in Yokohama.
		- 1 hour meeting is planned. 

- Richard <> Qin:
	- Discussion about: "Multi domain contact use case": the sparsity of information (issue#1), ambiguity of information(issue#2)
		- Scenario 1:
		- Scenario 2: Multi-Domain Settings (2 ALTO entities in 2 different domains)

------------------------------------------------------
**2. Chartered items: **

*2.1- O&M:
	Jensen (Reviewer of the O&M document)
	- Already have 2 colleagues helping with the review, but might need other volunteer!
	- Update about the progress on the latest O&M document.
	- Will uploaded the new version before Friday for others to review.
	
	- Qin will send the template for Jensen's consideration and will ask some other people to help with review.
	- Richard will also provide some review.


*2.2- Transport documents (Richard)
	- Already submitted a newer version with a lot of changes with the help of Roland and Kai.
	- Provides details about the updates related to references and InfoWorkFlow.
	- Comments from Qin about: Lifecyle /  maybe a diagram would be helpful/ Transport State: Create, Read or Delete / use of absolute uri and relative uri /
	- Taking the discussion about the use of "Absolute/Relative" State to the mailing list for further discussions.
	- Should decide: What to include as part of the current draft and what to cover as part of a future document/work. (a full comprehensive read is needed)

*2.3- Deployment


------------------------------

**IETF, ALTO Meeting: January 31, 2023**

**Agenda:**

- Round-table updates
- Chartered items
- Review of 'In Progress/Discussion' tasks: https://github.com/orgs/ietf-wg-alto/projects/1/views/2


**Minutes:**

Note Taker: Jensen

WG charter items:
- New transport (Richard):
  - Allow client to request information of each update queue; client can delete the queue later.
  - Incremental update queue
  - Use stack to maintain queue status
  - Kai: whether to reuse info in IRD
- OAM (Jensen):
- Deployment (Jordi & Luis):
  - Kai and his students have migrated Client/Server/App implementation table from the old wiki page
  - Luis will update telefonica deployment
WG Recharter:
  - Richard introduced the on-going network-aware, application-layer connection control work
  - Richard talked about a tree-structure resource constraint spec mentioned by CERN
    - Another potential use case: pods network traffic shaping
    - Whether it should be consider as a charter item in the future

------------------------------

**IETF, ALTO Meeting: January 24, 2023**

**Agenda:**

- Round-table updates
- Chartered items
- Review of 'In Progress/Discussion' tasks: https://github.com/orgs/ietf-wg-alto/projects/1/views/2


**Minutes:**

Transport:
- RY: targeting sending a new version today.

O&M:
- [RY] O&M is very overarching, a lot of content. Is it standard or experimental.
- [JZ] The target is standard
- [JR] Any plans to implement a portion of the O&M in the standard to OpenALTO?
- [RY] Would be very positive and we can consider

Deployments:
- [JR] reminder to update the wiki with your deployments info: https://wiki.ietf.org/en/group/ALTO/deployment

[RY] CERN/OpenALTO Project:
- Two pieces: (1) Scheduler and (2) data orchestrator
- ALTO for visibility and scheduling. 

- [QW] Time slot request for next IETF meeting
- [QW] Goal for next IETF meeting for transport should be working group last call
- [RY] We will push for it
- [QW] Who will be going to Japan? We need to start organizing.

[RY] Three directions:
- General path model for multidomain visibility. Can be presented at PANRG too. Presentation with CERN, NRP, etc.
- Collecting visibility info about environmental impact. For hackathon, to work together to get energy impact
- Trust

------------------------------

**IETF, ALTO Meeting: January 17, 2023**

**Agenda:**

- Round-table updates
- Chartered items
- Review of 'In Progress/Discussion' tasks: https://github.com/orgs/ietf-wg-alto/projects/1/views/2

Chartered items
--- Transport - Richard 
new name added way of publishing...
major change: 4 requirements = tips. R5 optional (no MUST)
R14 = MUST
overall, pip can request server from anywhere. session-based transport. 
ready to be posted when tips are done. 
qin: intro still keeps SSE fig => will be deleted. no need compare w SSE. 
richard: abstract positions wrt SSE that is great. Pb: SSE not allows naming individual updates. Thus all pushed updt are anonymus updates => client cannot pull them (no ID).
=> tips incl allowing distribution of ID from server to client. server can now push. 
qin: diff in workflow? 
richard: use tips, ID see fig before section 3
qin: SSE needs 2 channels: ctrl + data. new transport does not need to introduce any specific channel, just a transp queue 
richard: bundled in same connection
qin: hopefully post this week?

--- O&M - Jensen
simplified Yang model for ctrl part. 
client auth delegated to other server. no need passwd & user name => role-name. example in appendix
auth server can be 3rd party, see fig 3. 
qin: why use oauth in ALTO scenario? 
jensen: can be different server. 
qin: not convinced oauth is more relevant. Commented on the list. compliancy w base protocol is needed. base prot does not use "access control" term. Can be rather TLS. need double check. 
jensen: will discuss on mailing list. 
kai: ...
jensen: can use other prot, user & passwd. can drop oauth if too complex. 
qin: use TLS maybe. better not expand to oauth. 
kai: jensen put text in appendix showing how can extend to oauth. oauth = example
qin: ok if appendix as an example. 
jensen: can upload after meeting to have feedback. 

qiufang: ALTO server can push (reactive) data and pull (proactive)?? . There should be these 2 modes for ALTO server, with relevant config eg how often pull data. also need to specify data store. 
qin: URI not enough to spec yang data store, you need target path to locate...
kai: data store only specifies the type. 
qiu: to identify data store.... 
qin: maybe add example in appx. we can schedule editing session. 

--- ALTO deployments: 
qin: reminder we have wiki page. please populate your section. right now, NRP documented only (nat research platform)
richard: can add info on CERN. 
jordi: is a wiki page ok as a deployment deliverable?
qin: is ok, we also need Luis input. we also have Internet protocol journal (IPJ) paper. 
qin: wiki needs distinguish ALTO deployment (cern, telefonica) from  implementations experiments. IETF wants shutdown old wiki pages. We need complete migration and advise secretary. 
jordi: will edit to separate. 

---  IPJ article
qin: exchanged w editor who provided suggestions. 

AOB: richard will discuss next meeting. 
we also have Marcos Schwarz
Ayoub: could not catch up, hopefully will update next week integrate fujistsu work in ALTO WG. need talk w jordi and luis. 
Meeting concluded


------------------------------

**IETF, ALTO Meeting: January 10, 2023**

**Agenda:**

- Round-table updates
- Chartered items
- Update on ALTO Multi-Domain activity
- Review of 'In Progress/Discussion' tasks: https://github.com/orgs/ietf-wg-alto/projects/1/views/2


**Minutes:**

Note Taker: Roland

Participants:
Lauren, Kai, Chunshan Xiong, Jensen, Jordi, Mahdi, Marcos Schwarz, Motoyoshi Sekiya, Qin, Richard, Roland


*-**Round-table updates:**-*

Motoyoshi:
Preparation of a presentation regarding "Secure Trusted Networks" for the next IETF Bits & Bytes.

Roland:
Still working on ALTO new transport, no major updates compared to meeting last week.

Jordi:
Everyone who is working on ALTO deployment should update the Wiki, too.

Jensen:
OAM document, going over the document reviewing data model.

Chunshan (chunshan.xiong@cictmobile.com):
Background information on 5G in China, 5G service is currently not heavily used and operators want
to push the usage of 5G network. Segment Routing (SR) will be deployed and the 5G capabilities are increased
for use case like gaming. 
Question of Richard: What is the relevant capability of SR that is beneficial for this use cases?
Answer: Helping to reduce bandwidth for real-time communication. 

*Start Discussion:*

Discussion on congestion and congestion prediction and estimation of capacity on the path and if it is in line
with the ALTO bottleneck discussion in this group.

Congestion Control -> impact on RTT

Bottleneck Structure -> predict future behaviour

More offline-discussion is needed for clarification.

*End Discussion:*

Lauren:
Open-ALTO project came up with requirements on Multi-Domain.
e.g., easy to use, stable design, correctness.
Suggestions of the group regarding the requirements are welcome.
Ambition is to demonstrate for Rucio.
Idea to write a paper and go to IRTF.
Pseudo-Code is available and can be shared.

Qin:
Not ready to go for re-chartering of ALTO and need to finish already chartered items first.
New Transport still requires a revision.

Mahdi:
OAM still needs some updates and comments.

Conclusion: => prioritisation of chartered items is necessary.

------------------------------
