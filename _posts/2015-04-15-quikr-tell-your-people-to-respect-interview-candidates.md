---
layout: post
title: Quikr, a little respect for interviewing candidates please !
date: 2015-04-15 15:00:00
summary: I was called for Engineering Manager role interview at Quikr. It was probably the most harrowing interviews I ever had in my life. 
categories: recruitment
---

Dear Quikr, 

I got called for an in-person interview for Engineering Manager role on April 15. 

![Email invite for the interview](/images/quikr-in-person-interview-invite.png)

As told to me by Sandeep Shadankar, I was suppose to meet 3 people - Rizwan Iqbal, Vishnu Agarwal and Ramsyam Missula. I had to leave after the first two, specially the 2nd one, as I felt humiliated. I am going to describe my rest of the experience below, with actual instances based on memory (it has been 15 days & I was reasonably busy, also I wanted to make sure I really want to write this piece before actually starting to write). 

Before I go ahead, I would like to tell you that I had been away from interview world for a very long time. But before this interview, I must have attendted at least 5 (or may be more). So I am reasonably sure that I am not exaggerating as I have reasonable understanding of the interview process. You may read more about me [here](http://pocha.rocks).

My first interview was with Rizwan. Rizwan was cheerfull. I was asked various questions & I made it reasonably clear that I have not really worked on large scale apps (I was an entrepreneur primarily with little success to his apps which never hit the kind of scales Quikr has for sure). I could see that Rizwan is not impressed. But overall, it looked a regular interview. Rizwan left & I waited for next interviewer to come in. 

![Vishnu Agarwal Quikr](/images/quikr-vishnu-agarwal.png)

Vishnu entered the room with a very lets-get-the-job-done face. He handed over some papers to me & spoke in a tone that looked a bit dominating. The words were something like 

<blockquote>
<p>You need to write a database class for me. I am not going to judge you for incorrect syntax. But the code need to be production quality.</p>
</blockquote>

 I did not have much issue with the words, but the way it got delivered, I got reminded of my college days. It felt like a professor is delegating me an assignment. The conversation went like

<blockquote>
<p>Me: What language you want me to write this. Can I use Ruby ?</p>
<p>Vishnu: I would prefer PHP. We work in PHP.</p>
<p>Me: (loosing a bit of temper) but I had talked to Pradeep & mentioned to him that I would need some time to brush up PHP if I am going to be tested on that.</p>
<p>Vishnu: ok, write in Ruby then (which looked like a hands-thrown-in-the-air gesture)</p>
</blockquote>

Well, by this time, I had not only lost all my motivation to do good, I was feeling extremely uncomfortable. It felt like those dreadful exams where you dont know anything, the professor is looking over you & the time is about to run out. 

I wrote some code & handed over the paper back. I actually ended up writing it in Java. Vishnu looked at the code, then looked at me & asked 

<blockquote>
<p>can you do anything better ?</p>
</blockquote>

 It sounded pretty much like **is this the best you could do ?**. I pointed to some enhancements which did not impress him. He made a lets-dismiss-it gesture & started to prepare to moved on to the next question. I insisted what he thinks about the code. He took the paper back in hand, looked at the code & started evaluating the way professors do, striking off a part of the code saying **you did not catch error here**. He was actually right. I felt stupid. 

He then moved to next question which is tracing all possible paths from top left corner to bottom right corner in a MxN grid. The condition being, only right & down movement allowed. I asked him **should I optimize on time or space**. He replied **lets optimize on time, space is cheap anyway (& something around putting extra hard-disk which I dont remember much now)**. I wrote a recursion based code reasonably quickly 

		def next(path_so_far, x, y)
			path_so_far << "x,y"
			if x < M - 1
				next(path_so_far, x+1, y)
			end
			if y < N - 1
				next(path_so_far, x, y+1)
			end
			if x == M - 1 and y == N - 1
				puts path_so_far
			end
		end
		
		next([],0,0)

I thought I did decent. I looked at Vishnu for his response. He said 

<blockquote>
<p>I have not checked what you have done, but surely, you could do a better job with time optimization.</p>
</blockquote>

He was right. He also pointed that a point is visited multiple times & hence the complexity is more than O(N). I suggested that I can run through each point, store all possible paths at the point & use them to build paths for right & bottom point. Vishnu replied by saying **that is too much of space. Assume M & N are in millions. That is not acceptable.** At this point, I asked him to tell me the solution but he quickly brushed the problem aside & we are now set for a new problem. 

Well, after this, I have been asked questions on designing things on scale (how would you design notification system for facebook) & stuff around that. The answers I gave, I was told that I am designing it like a developer. I need to tell him components. Well, I was not entirely sure what he meant by 'component' here. Also, I needed to make sure that is highly scalable. I was not sure how exactly to respond. Clearly I have not designed anything with scalability in mind before.

The next question was to design a real estate site. When I started to design the DB structure etc, I was stopped & the 'component' thing was asked again. 

**At this point, I was reasonably frustrated & told Vishnu that I dont think I am the right fit for the job.** That surprisingly made things better. Looking back, it feels like, it was a fight of supremacy & I had conceded which made my interviewer happy (or probably content). I told him that the kind of questions he has asked are more like questions for an Architect who has worked on large scale apps. 

Vishnu then asked questions around API design, responsive design (question on how to selectively show & hide things on the view for different screen sizes), front-end MVC & how different templates can be used for different screens etc. Again, it was my relative in-experience working on a 'very responsive' design. I clearly told what I did not know, only to keep feeling worse. 

By this time, I really wanted to get out of the place. We were done with questions & Vishnu left the room. He fleetingly mentioned about **how some of the interview candidates have cribbed that programming questions have been asked for Engineering Manager position & they expressed their discontent on social media**. I nodded & asked him to send Pradeep in. Once Pradeep came in, I told Pradeep the same that I & the job requirement does not have a fit & quickly left your office. 

Well, this is pretty much it. I think as the top guys, you probably are not aware of whats happening inside & how interview candidates are being treated like. Also, a lot of such incidences go unreported because clearly, by writing these articles, I am jeopardizing my chances of getting interviewed at any other company. 

But on 2nd thoughts, I would actually not like to get interviewed with a company whose HR thinks that their process is probably not that good & a post like this can emerge. So I guess I am good :-). 

Thanks<br/>
Ashish Sharma

<small>P.S. - I really like what you doing at Quikr, specially Quikr Next. Even if the EM role would not have worked out because of my inability to **talk-components** & **large-scale-inexperience**, I could have been reasonably interested in the PM role. But guess, I would pass it for now (not that you really want me to have it, but guess saying that would defnitely give me some level of ego satisfaction :-] )</small> 
