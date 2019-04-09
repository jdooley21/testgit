Ticket #1: Rejected pull request from fork
To start, I have to say I LOVE GITHUB. You guys rock. I was at your 4th birthday party, thanks for the cupcake and booze!

Anyway, here's my problem. I sent a pull request to technoweenie, and he rejected it because my master branch is out of sync. What can I do to fix this?

Help me supportocat, you're my only hope!

/.Steve

Hint: You'll want to address their question, and you could add an explanation of topic branches as a better workflow.

Ticket #1 response:

Hi Steve,

We're so glad you were able to celebrate with us! Hopefully we can resolve your issues well enough for you to want to come hang out with us again.

So first off, can you run the following command on the command line to make sure you have a good remote upstream configured?

git remote -v

You should get something like the following back:

> origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
> origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)

Next, run the following command to specify the remote upstream you want to sync to, replacing the original owner with technoweenie and the repo you're syncing to:

git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git

Then run git remote -v again, you should get something like this in return:

> origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
> origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
> upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (fetch)
> upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (push)

Now that you have your remote repository configured pointing to the upstream, run the following command:

git fetch upstream

This will make a new upstream/master branch on your local machine. Now run the following to check out your fork's local master branch:

git checkout master

Finally, to sync with the original repo, run the following:

git merge upstream/master

Now your master branch is synced up to the original repo. Once you push your local branch to GitHub, you can try your pull request again!

You may also think of creating a topic branch for your future workflows. A topic branch is a short-lived branch that you can create to work on singular bugs or issues. You can work on multiple "topics" simultaneously without using just one single branch. 

 Let us know if you need any further assistance and we hope to party with you again soon!

Regards,

Support


-----------------------------------------------------------------------------------------


Ticket #2: Syncing internal server and GitHub?
Hi GitHub! My company has an internal Git server used for deployments, we use GitHub, and I work on a local copy of the repository. For workflow purposes, how do I sync my repository to GitHub and the internal Git server?

Thanks,
vmg

Hint: One common option is Git remotes. There are others!

Ticket #2 response:

Hi vmg,

Thank you so much for reaching out to support regarding this issue.

The most common way to sync your local repository with github is to create a remote repository that points to the original repo you want to work with on GitHub. You can do so by running the following command on the command line:

git remote add <name> <url>

where name is what you want to call the remote, and the url is the repository url on GitHub.

You can also clone a repository, using the following command:

git clone <url>

You can then make commits and push changes to the original repository using git pull and git push.

Please let us know if you need any further assistance!

Regards,

Support

-----------------------------------------------------------------------------------------

Ticket #3: Unhappy about forking
JamesTK here, I have another question.

One of my dev collaborator forked my private repo without explicit permission to do so... is that typical? I am surprised that the system did not notify me if it was okay to grant the fork permission. Is there a way to setup permissions of this sort? Also, other than asking the collaborator to delete the forked repo, can I actually delete it?

Thanks, jamestk

Notes:

You've checked the account in our admin view, he only has one personal repository (jamestk/tribbles), which has one collaborator. Any documentation you may need is available on help.github.com.

Ticket #3 response:

Hi James,

We're sorry to hear you are dealing with this issue and will give you some information that will hopefully benefit you.

It appears you only have one personal repository (jamestk/tribbles) with just one collaborator. If you remove this collaborator from your repository, any forks they've made will be deleted, however any clones they have made of your repository to their local machine will be retained.

For future cases, by accessing repository settings, you can set access levels for collaborators as well as have notifications sent to you for any push events with the repository. To access the settings, click into the repository and then click the Settings tab.

Please let us know if you need any further assistance, and again our sincere apologies for any inconvenience.

Regards,

Support

-------------------------------------------------------------------------------------------


Name?
Jason Dooley

Location?
San Ramon, CA

What's an impressionable experience you've had with customer service/support, and why?

A customer at a previous company was known to verbally abuse and harass support team members and CSM's. My manager came to me after such an experience and asked if I would be willing to be the dedicated support representative to the customer since I had experience dealing with difficult types in my military career. I of course responded that I would be glad to take the customer on and went to work researching their issues. I determined that their previous support issues had not been handled in a generally timely fashion as many SLA's had been broken. The quantity of support tickets open for them was also quite extensive, so I decided my first task would be to try to cut down the number of tickets they had open. I was able to resolve 75% of their tickets within the first month of handling the account, and from there I never seemed to have any issues with the account contact that had been so demeaning to other team members previously. I believe it's never appropriate for a customer to treat their support teams with disrespect, but we also owe an outstanding support experience to them. If we don't live up to our end of the deal, they can't be expected to live up to theirs either.

Tell us about a time where you helped someone.

A customer had a large quantity of tickets, most of which had been opened for months and had no work done on them. My Manager asked me to help this specific customer because they were thinking of not renewing their contract with us. I took on their account alone for a few weeks and was able to bring their ticket count down from over 100 to under 20. With all of the issues they were able to get fixed and the ticket count itself going down, they decided to renew after all and we were able to retain them as a customer. I believe the best course of action for both parties was achieved as they would have had to look for another solution for their business, which would have made them spend extra money, and we would have lost their business. I helped both the customer and my manager in this respect.

What appeals to you about GitHub, as a company you'd potentially be working for?

I've worked in GitHub for years and have always been impressed with the version control system they have mastered. Of all the tools available to programmers, I believe git is one of the most useful and GitHub has really revolutionized the industry with it's integration. Having the chance to help customers make their programs better is a dream and being a part of this company is a goal I have always placed in front of me. 

How would you describe what GitHub does to a non-technical person?

I would tell a non-technical person that GitHub stores collections of code in a publicly accessible forum which allows programmers from all over the world to collaborate with each other and make projects even more amazing.

What motivates you to work in support?

Seeing the issues that customer's face and being able to resolve them is truly a passion that I have refined over the years. When people say they want to do what they truly love, I have the benefit of knowing that I do what I truly love in helping people fix technical issues with their products. My work isn't just somewhere I go; it's what I do, whether that's at 10 in the morning or 10 at night. I've been known to go into my ticketing queue after putting my kids to sleep at night just for the simple fact of knowing that I can possibly resolve another issue before going to bed myself. I love fixing customer's issues and knowing that their business can keep rolling because of the help I give them.


