
Welcome to the Government Data Archiving Github Team. This repository is an overview for people who are just getting involved in the project. Here is a high-level overview:

## Recommendations and Lessons Learned

On Dec. 17, 2016, volunteers at the University of Toronto came together for an archiv-a-thon where, among other things, we put together some code for scraping and harvesting government websites. What follows is a list of some of the lessons we learned.

1. Clearly establish toolset and processes before the event

  Hackfests go by very fast! We spent a lot of time working out our process and deciding on tools for collaboration.  We recommend deciding on tools at least 24 hours before an event.  In our case this meant:
  - this Github organization
  - the #guerrilla-archiving channel on [the Civic Tech Slack Team](http://civictechto-slack-invite.herokuapp.com/)
  - specific formats of deliverables (esp. [WARC](https://en.wikipedia.org/wiki/Web_ARChive))

  Ideally, organizers will reach out to participants beforehand and ask them to be prepared (e.g., by signing up for Github and Slack, applying to join this Github organization, potentially looking at the [OpenZilla, Open Science Git collaboration Slidedeck](http://mozillascience.github.io/working-open-workshop/github_for_collaboration/)).   
  
  Organizing the Github organization is also very important.  @patcon gives some helpful background [in this issue](https://github.com/edgi-govdata-archiving/overview/issues/7), but basically, we wanted to create a structure that welcomed participants and their contributions, so that no one became frustrated and locked out.  We are using the "Lieutenants" organizational model, in which there are only a small number of owners, but a bigger team of lieutenants who have write access to all repos by default.In this model: 
  - Each working group at a Hackfest should appoint at least one person as a lieutenant.  
  - All participants should be added as team members, and encouraged to set their team memberhsip to "public". This makes it much easier to stay in touch later.  
    - (people may need reminders during the event to join the team -- the hack-time is pretty hectic)
  - finer-grained permisisons can be tweaked during and after the event.
  

2. Having infrastructure (VMs in advance)
  We had nowhere particular to run our code on the day of the event.  Ideally, the organization would have a VM already set up in which code could be test-run.  If there's no organizational infrastructure ofr this, it might be good to get participants to set up remote access to their (random) resources before the event -- many coders have access to pockets of ocmputing power and network bandwidth, but sometimes they have to arrange for it in advance.  

3. Better definition of tasks and communication across teams

  We tried hard to define our tasks before the event, but we still had a fair amount of confusion and overlap during the event. Ideally, the team should have at least (say) **3 very specific tasks defined and prioritized** before the event starts.  These tasks should be **spec'd** , e.g.:
  *[insert well-formatted spec here]*

  During the event, working groups should appoint leads or liaisons to co-ordinate work across groups. This oc-ordination work may take the form of check-ins, lightning meetings, and/or Post-It note boards.

4. Figure out what expertise you need!

  Most projects will need coders familiar with **web scrapers** and **harvesters**. The Internet Archive uses the WARC format, and **very few people have experience working with WARCS**.  We have had some difficulty making well-formed WARC's. *[Link to a tool that shows a good example]*

 If possible, **clearly curate the tools that would be helpful** and recruit people who are familiar with them.  

## Most Important Repositories

We've pinned the three most important repositories to the front page -- [our technical toolkit docs from the event](https://github.com/edgi-govdata-archiving/eot-sprint-toolkit) and [the eis-WARC-archiver](https://github.com/edgi-govdata-archiving/eis-WARC-archiver).  The latter is, we think, the most reusable of our tools, because it actually implements a harvester that can read CSV files of URL's.  Some of the other tools are more sophisticated and produce more highly-structured metadata in JSON formats, but none of htem has a working WARC harvester attached to it, so there is, potentially, less to learn.  

## What Else is in this GH Organization
The remainder of this repository consists of tools developed during sprints.  So far this includes:

Our organizing documents for the tech group at our archiv-a-thon (potential overlap with the current repo):
https://github.com/guerrilla-archiving/eot-sprint-toolkit

A Chrome extension to simplify the nomination process at archiv-a-thons:
https://github.com/guerrilla-archiving/presidential-harvest-nomination-tool

A sitemap tool to provide initial models of government domains -- intended to facilitate volunteer organization at archivathons:
https://github.com/guerrilla-archiving/epa

A PHP script to download all government Github repos:
https://github.com/guerrilla-archiving/dolley-madison

Scraper for the EPA Enforcement & Compliance History archives:
https://github.com/guerrilla-archiving/eotarchive-echo

Undocumented scraper for a set of databases accessible but obfuscated through one of the EPA data websites:
https://github.com/guerrilla-archiving/eotarchive-quantitative

Python scraper that feeds URL's to WGET and outputs a WARC archive and an accompanying CSV file associating URL's with scraped metadata:
https://github.com/guerrilla-archiving/eis-WARC-archiver

A scraper for the EPA search engine, that systematically feeds in search queries and extracts resultant URLs:
https://github.com/guerrilla-archiving/epa_search_utils
