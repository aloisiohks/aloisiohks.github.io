---
layout: page
title: Publications
---

{{ page.title }}
================

<p class="meta">23 Oct 2008 - San Francisco</p>

For an entrepreneur, the line between horrible mistake and runaway success can
be so thin that even Kate Moss would be envious. I lived with
[Gravatar](http://gravatar.com/) for nearly four years before that line even
became thick enough to measure.

As it's become one of my favorite parables, I'll save the details of how I came
up with the idea for Gravatar for a future post. What's important to know is
that the idea was spawned not from a business perspective, but from a desperate
desire to create something new in the world of blogging.

Spin the clock back four years and you'll find me sitting at my Windows desktop
machine in my underwear with a box of Life cereal to my left and a day old Coke
to my right. Since I'd been laid off from my job as a Java developer some months
earlier, I'd decided to take the entrepreneurial plunge doing what I knew best:
web design. Working in a cone of isolation, I'd become accustomed to waking up
late, swinging my legs over the right side of the bed, and in one fluid movement
sliding over to the ratty chair I stole from my old college dorm room. I'd spend
most of the day working on client projects in ColdFusion or PHP. It was hard
work and could become a bit tiresome. I needed an outlet, something that didn't
have a suit on the other end of a telephone telling me how blue was the wrong
color and things would be so much better if only the photo had a slightly bigger
border. Gravatar would become that outlet for me.

I was really big into web standards at the time, having recently read Zeldman's
seminal work, and became a true believer. Eric Meyers, Dan Cederholm, and Jon
Hicks became like gods to me. I worked very hard at making relevant and witty
comments around the right kinds of blogs. Being a part of that movement became a
significant goal for me. My Movable Type weblog rarely went more than two days
days without a post on design or standards.

Two weeks after I had the idea for Gravatar the first version was written and
deployed. Every request hit the database and dynamically generated a properly
sized gravatar via PHP's gd2 api. Premature optimization and all that, right?
The first thing I did after getting the system to a workable state was email all
the bloggers I looked up to (and that had no idea who I was). Blog comments at
the time were a pretty dreary affair and I guess Cederholm was intrigued enough
by my idea that he linked to it in a sidebar micro-post on simplebits.com.

That single mention kicked off a slow but steady trickle of interest in the
system. A few blogs here and there installed the plugin and the world started
seeing avatars that mysteriously followed them around. At the same time, just as
people must have thought Cheez Whiz was a stupid idea when it first came out,
some bloggers started railing against Gravatar, calling it frivolous,
inefficient, and "an abomination." This was my first nibble at the smorgasbord
of what was to become the "horrible mistake" aspect of Gravatar.

Due to the inherently self-advertising nature of gravatars (the "what the hell
is that and how do I get one?" brand of advertising), Gravatar adoption
increased at a rapid rate. Having crafted the idea for Gravatar without any
semblance of business model or growth projection or build-out strategy, things
took a rather dramatic dive away from "runaway success" as my server (yes,
singular) buckled under the pressure of tens of requests per second! As it turns
out, regenerating a gravatar on every request is not very CPU efficient.
Gravatars worldwide suddenly turned into little red Xs. Then, in what has become
known as the Twitter Effect, a barrage of emails hit me complaining about how
the free service on which they had come to depend was down, and how this would
adversely impact my well-being.

I fixed the code. Gravatar came back online with caching. All the while I'd had
the bright idea that gravatars would be rated for content, MPAA-style. Because
users clearly were not fit to rate their own images, I was manually rating 400
or more avatars each day. If I missed a day, I'd have damn near a thousand
waiting for me the next day. In addition to the angry mob, I was very fortunate
to have an amazingly supportive group of users that volunteered to help me rate
images. I owe them my sanity, and it freed up enough time for me to work on the
next iteration of the site.

G2, as I called it, would be written in Rails and use lighttpd plus a convoluted
directory structure of symlinks to enable me to pre-render every gravatar (1x1
up to 80x80) and serve only static images. I did this to avoid having to rent or
buy the kind of hardware necessary to hook up a properly scaled system. Up until
the end I ran Gravatar on a maximum of two rented commodity servers that set me
back a mere $300/month, a pittance for the kind of traffic I was serving. I say
it was a pittance, but that's not really true. Donations didn't even come close
to covering that cost.

At some point early in the development of G2, Toni Schneider, the CEO of
Automattic (the company behind WordPress.com and Akismet) contacted me after
hearing my [interview about the future of
Gravatar](http://blog.gravatar.com/2007/10/18/automattic-gravatar/) on the
WordPress podcast. This was exciting news! How perfect a fit would it be for
Gravatar to be bought by Automattic? I was already planning a trip up to San
Francisco to meet with the Powerset guys, so the timing worked out perfectly for
me to meet in person with Toni. I ended up having lunch with Toni and Matt
Mullenweg at 21st Ammendment on 2nd Street. It was a bit intimidating to come to
the mecca of tech startups to meet with such huge players in the blogging
community. Turned out that both Matt and Toni are great guys and so we had
drinks for about two hours, talking about my ideas for Gravatar and how we might
be able to work together. Everything seemed great&#8212;I was jazzed and they
seemed excited&#8212;but a few weeks later Toni let me know that the timing was
wrong and they couldn't make a play at that time. He suggested I proceed with G2
and they'd proceed with their own avatar system. I was pretty bummed about the
outcome, but I took their advice and kept going.

A few weeks before G2 was finished, the site imploded in a big way. One machine.
Hundreds of requests per second. That poor CPU must have thought it was the End
Times. Instead of wasting time on getting the existing system back up, I put on
my headphones, turned it up to eleven, and got back to work on G2.

I'm not sure if you've ever had to work on a project while your users are
publicly skewering you on your blog for allowing the service to go down, but
it's as close to depression as I've ever come. If I'd had less pride, I would
have popped everyone a huge middle finger and let the service die, but instead I
waded through the hundreds of comments and deleted the ones with threats,
hatred, or my favorite, the words "fuck you" repeated 600 times. It wasn't fair,
I told myself, that I should be sitting here with high blood pressure trying to
raise Gravatar from the dead while the unappreciative masses do what they do
best on the internet. The only thing that kept me going was never being able to
tell which side of the mistake/success boundary I was sitting on. It was hard to
think of the situation as anything but a huge failure, but the shitstorm the
downtime was causing indicated that people found the service valuable. I want to
say that Twitter went through the same thing, but they suffered their downtime
with millions of dollars in the bank. The only thing I had was a full time job
unrelated to Gravatar and a credit card that reminded me every month of my bad
judgment.

Finally G2 was done, deployed, and fully operational. I have no idea how many
users I lost due to the several weeks of downtime, but I don't think it was very
many. There seems to be a corollary to the Twitter Effect that I'd call the
Forgiveness Effect. It dictates that if a user enjoys a free service and that
service is currently up, all past atrocities will be easily and quickly
forgiven. With the site running again, things looked to be shifting back towards
a success.

Things were not all rainbows and unicorns though. My Rube Goldbergian
architecture had a few quirks that needed to be dealt with. The site still had
some elusive bugs from the overly-rapid development cycle. And just like new
lanes on freeways always fill up immediately, the two new servers I was running
started causing expensive bandwidth overages. I had taken a job at Powerset at
this point and the combined pressures of these two commitments started to weigh
me down. Once again I started feeling like all the effort I put into Gravatar
was for nothing. Like I would never benefit from any of it.

In a last ditch effort to save Gravatar from final doom, I emailed Toni and
pitched him again on Gravatar. I figured it was a long shot, but what the hell,
couldn't hurt. Things must have changed in the prior 6 months because Toni was
very receptive to the idea. We met again, at 21st Ammendment, and hashed out a
tentative deal over drinks. I'd never sold anything like this before, so my
technique was probably very amateurish. I'm almost certain I could have gotten a
better deal out of it, but I had the smell of desperation about me and I really
did want to see Gravatar end up in Automattic's hands.

Four days later, Automattic made their official offer. On September 21st, 2007
we inked the deal and Gravatar became both the first company that I ever sold
and the first company that Automattic ever acquired.

I am quite satisfied with the sale to Automattic. Some will say that I should
have pursued VC funding. Indeed, I was contacted by several firms but never
travelled very far down that road. I always felt like Gravatar was a feature,
and I wasn't comfortable building a company on such a tiny foundation.
Reinforcing this decision, no viable business model ever coalesced during the
time I was building the site. It was also made clear by Toni that Automattic
would maintain Gravatar as a separate brand and continue its evolution (instead
of just absorbing it into WordPress). This appealed to my ego. Most companies
kill or maim everything they acquire, but here was a chance for Gravatar to
carry forward with all of Automattic's resources behind it (instead of two
measly servers). Part of me just wanted to see what Gravatar could become with
time, money, and man-power moving it forward.

Things always seem so clear in retrospect. But it was pride and persistence that
kept me in the game long enough to have anything to look back on at all. While
the line between horrible mistake and runaway success may be difficult to see,
you can still find it if you look hard enough.
