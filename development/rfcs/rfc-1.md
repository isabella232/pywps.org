---
layout: default
title: RFC-1 Project Steering Committee Guidelines
description: RFC-1 Project Steering Committee Guidelines
keywords: PyWPS, community, development, PSC, RFC
---

# RFC 1: Project Steering Committee Guidelines

- date: 2016-02-20
- author: Jachym Cepicky
- contact: jachym.cepicky gmail com
- status: final
- modified: 2016-02-22

## Summary

This RFC describes the PyWPS Project Steering Committee rules of engagement and decision making process for all aspects of the project.

Examples of PSC responsibilities:

* setting the overall development roadmap
* technical standards and policies (coding conventions, etc.)
* ensuring a regular release schedule (major and maintenance)
* reviewing RFCs
* project infrastructure (issue tracker, source code management, hosting, etc.)
* formalization with external entities such as OSGeo, OGC (CITE), etc.
* setting project priorities

In brief the project team votes on proposals on the [pywps-dev](http://pywps.org/community/#mailing-lists) mailing list.  Proposals are available for review for at least two days, and a single veto is sufficient to delay progress though ultimately a majority of members can pass a proposal.

## Detailed Process

* Proposals are written and submitted to the pywps-dev mailing list for discussion and voting, by anyone
* Proposals need to be available for review for a least two business days before a final decision can be made
* Respondents may vote using the following rubric:
 * +1: support the proposal and a willingness to support implementation
 * -1: veto the proposal, but must provide clear reasoning and alternate approaches to resolving issues within the two days
 * -0: mild disagreement, but has no effect
 *  0: no opinion
 * +0: mild support, but has no effect
* Anyone can comment on proposals, but only PSC member votes will be counted
* A proposal will be accepted if it receives +2 (including the author) and no vetoes (-1)
* If a proposal is vetoed, and it cannot be revised to satisfy all parties, then it can be resubmitted for an override vote in which a majority of all eligible votes indicating +1 is sufficient to pass it.  Note that this is a majority of all committee members, not just those who actively vote
* Upon completion of discussion and voting the author should announce whether they are proceeding (proposal accepted) or are withdrawing (vetoed)
* The Chair gets a vote
* The Chair is responsible for keeping track of who is a member of the PSC.  The authoritative and current PSC membership list is maintained at <http://pywps.org/community/psc.html>
* Addition and removal of members from the PSC, including selection of a Chair should be handled as a proposal to the committee
* The Chair adjudicates in cases of disputes about voting

## When is a Vote Required?

* changes in committee membership
* significant changes to project infrastructure
* backward compatibility issues
* significant feature implementation(s)
* Changing the inter-subsystem API, or objects
* Issues of process/procedures
* Release management
* Relationships with external entities (OSGeo, OGC, etc.)
* Anything controversial

## Observations

* The Chair is the ultimate adjudicator if things break down
* The absolute majority rule can be used to override an obstructionist veto, but it is intended that in normal circumstances vetoers need to be convinced to withdraw their veto.  We are trying to reach consensus
* It is anticipated that separate activities will exist to manage conferences, presentations, websites, demos, etc.

## Committee Membership

The PSC is comprised of individuals who are:
* technical contributors
* documentation and training contributors
* other prominent members of the PyWPS community
* contributors of strategic direction to PyWPS as an SDI component

### Adding Members

Any member of the pywps-dev mailing list may nominate someone for committee membership at any time.  Only existing PSC members may vote on new members.  Nominees must receive a majority vote from existing members to be added to the PSC.

### Stepping Down

If for some reason a PSC member is not able to fully participate then they are free to step down.  If a member is not active for a period of 12 months then the committee reserves the right to seek nominations to fill that position.  PSC members who have stepped down or have been replaced are openly welcome to return upon nomination.

## Membership Responsibilities

### Guiding Development

Members should take an active role guiding the development of new features they feel passionate about.  Once a change request has been accepted and given the go ahead to proceed does not mean the members are free of their obligation.  PSC members voting +1 for a change request are expected to stay engaged and ensure the change is implemented and documented in a way that is most beneficial to users.  Note that this applies not only to change requests that affect code, but also those that affect the website, technical infrastructure, policies and standards.

### Meeting Attendance

PSC members are expected to participate in pre-scheduled virtual meetings.  Initial frequency is set once every two weeks.  Meeting information shall be maintained on the [PyWPS wiki](https://github.com/geopython/pywps/wiki/Meetings). Meetings are usually organized through Google Hangout, but can also be organized using IRC, in the #geopython channel at freenode.net.

### Mailing List Participation

PSC members are expected to be active on the pywps-dev mailing list.  Non-developer members of the PSC are not expected to respond to coding level questions on the pywps-dev mailing list, however they are expected to provide their thoughts and opinions on user level requirements and compatibility issues when RFC discussions take place.

### Bootstrapping

Prior to the PSC anointing itself the PSC this RFC must be distributed before the PyWPS community via the pywps-dev mailing list for review and comment.  Any and all substantive comments are encouraged to be discussed via the pywps-dev mailing list or Meetings.

Initial PSC members are (in alphabetical order):

* Jachym Cepicky
* Jonas Eberle
* Jorge de Jesus
* Tom Kralidis
* Luís de Sousa

Initial Chair of PSC is Jachym Cepicky

### Updates

Status: final

Approved on 2016-02-24 as per <https://lists.osgeo.org/pipermail/pywps-dev/2016-February/000519.html>
