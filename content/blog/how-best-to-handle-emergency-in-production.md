---
title: 'How best to handle emergency in production'
description: 'Accept that incident will happen, this is just part of the innovation.'
date: '2020-01-12'
tags: ['culture', 'startup', 'incident']
ShowToc: true
---

> People make mistakes. But from mistakes, we learn and grow.

We've been trying really hard to complete the task, but sometimes things still slip up during development and cause a big impact in production.

And things like that are unavoidable. All we can do is face it and take responsibility.

I remember a few months after joining Bukalapak, I made a bug that caused a big impact. At that time I made a recurring transaction feature on the postpaid electricity bill page. The pull request has been tested locally or staging, and it's safe. Even when it rolls out to production, the feature works very well.

However, the bug arises from the the prepaid electricity token payment which is on the same page as the postpaid electricity bill payment.

This happened because during development, I didn't realize that the module and code for the postpaid electricity bill payment page was integrated with the electricity token payment page. I only tested the postpaid electricity bill feature and ignored the electricity token feature.

As a result, on that day Bukalapak customers were unable to make electricity token payments on the desktop web platform.

From that incident I learned some simple guidelines when an emergency occurs.

## Be relax

The first thing to do is to relax and not be in a hurry.

We may think that we should act as soon as possible to resolve the incident. But if we hurry, it can actually make things worse. It is far wiser to avoid making more mistakes by planning more carefully. Try to take a breath, or maybe a sip of coffee that is in front of us, then work quietly.

## Coordinate with squad or team

> Sometimes your emergency is not really an emergency.

Our product manager (or maybe project manager) probably already knows the situation, and they should be calculating the impact of the emergency. But if our PM doesn't know yet, then we must immediately inform him of the situation.

We can directly execute the solution that we have coded directly. if the solution just takes a few line of code changes and it's fast. But if we don't know how to solve it yet, and maybe it needs a big fix, we'd better wait for directions from our PM.

If the bug that we created is not an emergency situation, we can take a long time to determine a better solution for the long term. But if the bug is an emergency and needs deployment as soon as possible, coordinate with the leads on our team.

At Bukalapak, we have production issue levels & SLAs. The parameters used are daily GMV impact and daily revenue impact.

## Test our code intensively

Even though we are in an emergency situation, we always have time to do some testing. Test the code changes we made many times. Perform tests in all environments, be it local, staging, or even preproduction. Or if needed, we can do a test in production beta.

Don't hesitate to ask a QA partner or test engineer on our team for help. They must be very happy to help.

It is highly recommended to add unit tests in every change of our code. In essence, do the test many times until we are confident enough to do the deployment.

## Feel free to ask a more senior engineer

If our team or squad cannot help find a solution, we can always ask and ask for help from another team (or core team if there is one) who we think can provide a solution.

## Make sure the code that we have deployed is running well

We must have been very confident with the solutions we have used. But, always check again after deployment whether the code that we write really runs well in production. If needed, we can ask our lead for help to monitor the production metrics whether it is safe or not.

## Learn and share our experience

Learning from an emergency situation is one thing. But sharing the experiences gained from these emergencies is another matter.

There is no need to be ashamed to share about our emergency experiences, because it is part of the learning process. It doesn't have to be formal, at least we can share via group chat, or during meetings, or even through the documentation we make.

By sharing, we have helped other engineers not to fall in the same hole. The mistakes we make can be a very valuable source of learning for our colleagues.
