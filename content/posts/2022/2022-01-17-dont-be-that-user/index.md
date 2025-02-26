---
title: "Don't be that open-source user, don't be me"
date: 2022-01-17T00:00:00+00:00
draft: false
author: "Jacob Tomlinson"
categories:
  - blog
tags:
  - Community
  - Open Source
  - Maintaining
aliases: 
  - /posts/2022/dont-be-that-user-dont-be-me/
---

Before I was a maintainer of open source software I was a user of open source software, and I sometimes behaved badly.

While using some application or library I would discover a bug or something would break my workflow with a new release and I would head to GitHub to report it. Sometimes when I got there I would find that it has already been reported, so I would comment on the issue to add anything else I thought was useful and to add weight to the report. I also occasionally returned to issues that hadn't been resolved to see if I could add any more useful information or to ask if there was an ETA on a fix. I felt I was being helpful.

What I didn't consider was that my interactions were taking time/attention/resources/patience from the project. User support is a cost.

If you take anything away from this post I hope it is that these costs need to be paid by someone, the maintainer.

## Small costs add up

Open source projects come in many shapes and sizes, from solo developer side projects to sprawling ecosystems backed by Fortune 500 companies. You would be surprised how often something you consider foundational or critical in your workflow is maintained by just one person.

[![xkcd #2347](https://imgs.xkcd.com/comics/dependency.png "xkcd #2347")](https://xkcd.com/2347/)

As projects grow so do the support costs from their users.

One particular example of note was an [issue on grafana/grafana](https://github.com/grafana/grafana/issues/6983) that was opened shortly after the [alerts feature](https://grafana.com/docs/grafana/latest/alerting/) was added. Alerts only supported graphs and I wanted to get alerts if any of my single stats crossed their threshold too. So I stopped by and added a `+1` to the issue.

Over time more and more folks stopped by to `+1` the issue, but it didn't get implemented. As time went on the wording of the `+1`s got stronger, people demanded that it be implemented and expected it to be scheduled into future milestones.

I find reading this thread painful because if you scroll down a while you'll find comments from me [behaving like a super entitled user](https://github.com/grafana/grafana/issues/6983#issuecomment-363380128). I regret the way I behaved on this thread, and the temptation to delete the comments is strong, but instead I want to share this here in the hopes that you'll learn from my mistakes and not behave this way in open source communities yourselves.

Grafana is a free and open source dashboarding tool which is very popular in devops communities. What I didn't understand at the time was that Grafana, like most projects, was being maintained by only a [handful of developers](https://github.com/grafana/grafana/graphs/contributors?from=2013-05-01&to=2018-05-27&type=c). I couldn't see past the branding and hype to the group of humans building it, and I couldn't understand why this project wasn't implementing one of the most requested features by the community.

The biggest thing that I failed to understand was that with every user commenting

> this feature is essential for me to keep using Grafana

or asking

> why hasn't this been implemented yet?

a barrier was being built to stop anyone from ever working on it.

## How open source projects are funded

While some open source projects are created by large companies in a structured and planned way I think it is fair to say that most grow organically. Often they will start as a small side project by one person who has a particular need. That person will be excited to create the thing and to put it out there to help others who also have the same challenges.

Those projects have low cost, both in terms of development time but also support, maintenance and other community activities. That cost is covered by the individual, they donate their time to building it and are happy to help users as they start to discover the project.

Over time projects grow, they gather more users and more lines of code are added. Eventually the project will surpass the original requirements of the creator. Folks will keep popping up with new requests for features and the maintainer will add them because they are excited that the community wants to use their tools.

Eventually the maintainer finds things less like fun and more like work. This is a normal stage of many OSS projects and it is important to recognise that once it feels like work it should be treated like work. This is where funding is needed, both in terms of development time and community support.

Some projects attract more developers and contributors who also volunteer to take on this burden. This can defer that feeling of work to a later date and spread the burden, but I think it is inevitable that eventually someone has to pay for this software to continue existing.

There are different approaches that projects take to find a sustainable source of income. Sometimes projects use the open source software to power a for-profit business that adds an extra layer of value and charges for it, such as a managed service. Other times projects will try to attract donations in order to pay the maintainers. Occasionally large companies who have grown dependent on these tools will hire maintainers directly (I am fortunate to be in this group today). In all of these cases the bulk of the community for the open source software will not contribute financially and will continue to expect continued free service.

If you're interested in how open source projects grow and become sustainable you should check out [Working in Public](https://www.goodreads.com/en/book/show/54140556-working-in-public).

Coming back to the Grafana example, I was one of those open source users who had service expectations despite never paying for anything. This is a terrible mindset.

## Paid vs free software

If you were to develop a closed source iOS app and charge for it in the Apple App Store your user base will have certain expectations. They will expect the App to continue working for a reasonable period of time. If the app relies on a web service to operate they will expect that to continue working. If they have problems with the app they will expect to be able to ask for help.

There is an exchange of value here, money in exchange for an app, and this is reasonably well understood. However there are still practical issues for businesses to figure out such as how much time a developer can dedicate to each user and how long an app should work for after it has been purchased. I recently enjoyed [an episode of Under the Radar](https://www.relay.fm/radar/231) on managing customer support when you are a lone developer that goes into detail on this topic.

But what happens if we remove the money from the equation. Open source software is free. However there is still an expectation from many users for the maintainer to provide some level of support.

If a user buys an iOS app and the next update changes or removes some functionality they care about they are reasonably entitled to complain. If a user downloads a free open source tool and an update changes functionality should they be entitled to complain?

My opinion is that they can by all means report this unwanted change to the developer, but with no expectation that they will be accommodated. The relationship is completely different here. The user is interacting with a person who gave them something for free, not a business who charged them for something.

## Funding muddies the waters

Hopefully we agree that when something is paid you have a right to some amount of support, and when it is free you do not. So what happens when the person creating the open source project finds a way to fund that project? What happens if that project grows into something that more closely resembles a company?

I want to argue here that nothing has changed. Even if the maintainer is paid to maintain the software they aren't paid to do exactly what you tell them to do.

Users who still receive free software shouldn't expect free support as well, and if the project changes direction or does something they dislike they should interact with the project without entitlement.

Let's turn back to our Grafana example. Grafana Labs is a for-profit company that makes money off the back of Grafana. It has a nice logo, a website and all the other things you would expect from a company. Without trying to excuse my past behaviour I think part of the reason why I was so surprised and vocal about the issue not being fixed was because I had expectations that a for profit company would fix things the community was asking for.

However I now see that my use of the tool provided no value to the company, and I was not a paying customer of any of their services, so why should they provide me with free support.

Based on my own experience I assume that the folks at Grafana Labs have some portion of their time dedicated to developing the open source project. They likely work on things that their paying customers care about and things that they personally want to work on.

## Avoiding unpleasant tasks

The way that I and the countless other members of the Grafana community behaved on that issue made it an unpleasant thread to read. So it is no wonder that none of the maintainers chose to work on that task for five years. Last summer the issue was finally closed with support for single stat alerts being implemented. Perhaps a customer finally asked for it to be implemented, or perhaps a maintainer finally decided enough was enough and they pushed through the unpleasantness to be able to close the issue.

Either way I am eternally grateful to the Grafana maintainers for building an awesome open source project that I've been able to use for free, and I apologise for adding to the bonfire that was issue `#6983`.

## Moving forwards

I'd like to close with my thoughts on how I as a maintainer would like users to behave when I inevitably break something.

Firstly, be kind. If you do an update and something breaks your workflow it is normal to feel frustrated, but the person who made this change did not intend to inconvenience you. Head over to the repo and if there isn't already an issue then open one. Be thankful to the maintainer for all the value you've had already and craft a [minimal bug report](https://matthewrocklin.com/blog/work/2018/02/28/minimal-bug-reports) to let them know what is wrong.

If there is an existing issue then add a thumbs up emoji to the original comment and only add a further comment if you have new information related to the issue. If what you want to say has already been said then don't say it. When interacting with maintainers remember that you are asking for their help, not telling them what to do.

If the problem is a clear bug and the only possible next step is to fix it then consider raising a Pull Request if you have the ability to do so. But if there may be different opinions on how to proceed don't just blindly raise a PR with your preferred solution.

If the project accepts donations and you have the means to contribute then send the developers some funds and let them know you care about that issue in a note. Just remember that you are donating to the project as a whole, not buying their time to fix that specific thing.

If the project is backed by a large organisation then you may have an existing business relationship and an account manager. If so then get in touch that way as that can help divert funding inside that company to fix things.

Lastly you always have the option to fork the project. This is often said in spite because it is no small undertaking but for many it can be a viable path forwards. By taking ownership and responsibility for a fork you have full control over it's development and can make it exactly what you need it to be.

But most of all ![Be excellent to each other, party on dudes](https://i.imgur.com/zJcoRpK.gif).
