---
layout: document
title: Asian Focus - Digital Comics Task Force - Publishing Community Group Plenary
date: 2026-10-15
---

![W3C Logo](https://www.w3.org/Icons/w3c_home)

**Publishing Community Group Plenary:** **Launching Digital Comics Task Force** 
**Minutes 15 October 2026 /4:00 PM JST | 9:00 AM CEST | 7:00 GMT | 3:00 AM EDT**


## Attendees

Chair & Scribe: Gautier Chomel

Invited speaker: Hadrien Gardeur, Shinya Takami, co-leads of the Digital Comics Task Force.

Attendance: 25 persons


## Agenda

*Digital Comics Task Force aims to address specific non-normative work and challenges within the digital comics ecosystem. This call will focus on Asian market challenges and a proposed process for this work, which, given the significant time zone differences, will prioritise writing-based collaboration via GitHub Issues labelled with TF: Comics and reach out to publishers and reading system creators to collect feedback and encourage participation.* 

## Notes


Gautier: we had a first call at a suitable time for US and Europe; this one is at a suitable time for people from Japan. Shinya will help us with translations so we can make sure the information is understandable for everyone. 

Hadrien: we can do comics and manga in EPUB, but we observe different practices. The goal of this group is to document practices and agree on common practices. So we don’t want to add anything in the specifications, just document existing practices and discuss.

Hadrien: We really want this group to be international, and that’s challenging to do via calls. We think text is more inclusive because it’s easier to work asynchronously, and it also makes it easier to use translation tools and local discussions. 

Hadrien: It happens in the community group because access is free, and we really want to have people involved in production.

### Topic: EPUB 3.4

Hadrien: EPUB 3.4 is on track; the main change is a new layout called Roll. I know some EPUBs produced in Japan already use this property. Another point is that we simplified things. One control now only says if the pages go left, right or centre. That’s impactful for manga; before, some controls didn't work.

### Topic: spine

#### Subtopic: Images & HTML

Hadrien: we know EPUB is mainly used for manga distribution files but not for consuming; the reading system (RS) extracts images and display images. We think we need to balance the needs of specialised stores and RS with the ability to read manga in any reading system, even one not specialised for manga. This discussion is at [https\://github.com/w3c-cg/publishingcg/issues/107](https://github.com/w3c-cg/publishingcg/issues/107) 

Hadrien: what we propose for his issue is to keep HTML in the spine but include an image as a fallback; this way you respect the spec, and any RS can display correctly. For specialised stores or RS, it's easy to find the image you need and forget HTML. 

Toshiaki: it’s good; it is worse knowing we also use the image map feature. We use XHTML for content so we can use image map features. 

Hadrien: I see that linked to the ability to draw regions in images; today there are many ways to do this, like panel by panel and defining sequences. I suggest we open an issue to discuss that. We may want something stronger in the future, but for now, documenting the way you do it in Japan would help. 

#### Subtopic: true spread

Hadrien: True spread is the right and left pages, and you need one to follow the other because panels could move from one to the other. Or panels drawn partially on each page (so you need the two pages together to see the complete image. Those properties were misused and therefore dropped from EPUB 3.4. We can now only say left, right, centre. When the image is split and the user scrolls, the reading experience is poor. [https\://github.com/w3c-cg/publishingcg/issues/111](https://github.com/w3c-cg/publishingcg/issues/111) 

Hadrien: How to deal with two spreads? Using metadata does not work sufficiently. I think the recommendation would be to draw complete images and place them in the centre. That raises questions: if I’m on a smartphone in portrait, that will make a miniature image. Reading apps should consider the image ratio, screen ratio, and orientation to fit it best and let readers scroll horizontally or vertically. We see more and more devices with new ratios (i.e., dual-screen phones), we cannot draw for each device ratio. Instead of trying to pre-optimise by cutting images, draw the image as it needs to be and let the RS be smarter. 

Shinya: it would be good to have demos and mockups to visualise how this could work.

Hisahi: that’s letting the user choose how he wants to read (portrait or landscape, paginated or scrolled). Reading systems will need to take that into account.

### Topic: metadata

Hadrien: There are several points regarding metadata; for example, covers: we sometimes want more than one cover. Another point is which accessibility metadata we should include; that’s mandatory in Europe, even for non accessible ebooks. Other metadata includes seasons, episodes, series, volume, and collection information to aggregate several files. Those are a few examples; there are more in the issue tracker. 

Nagao: In order to include information in the metadata about which seasons or series a product belongs to—rather than just information about the individual product itself—I believe it would first be necessary to standardize the product management systems used internally by each company. That would take a considerable amount of time and effort, and I felt that reaching an agreement on this would be quite challenging.  
Henry: I don’t think this specific issue is much of a blocker since almost every distributor does provide the series name and the “order” number in the series as part of their metadata. For multiple levels, yes, but for simple volume number it’s doable

Hadrien: remember best practice are a mean to push people in the right direction, we know it will tak time. 

Hadrien: in EPUB 3.4 we included new image formats support, it’s also a good discussion to have, can we leverage on those formats and work on image resolutions and quality. It would be good to move from vendor requirements to industry recommendation. 

## Action items

Everyone: look at the [issues with label TF:Comics](https://github.com/w3c-cg/publishingcg/issues?q=label%3A%22TF%3A+Comics%22), discuss them in your organisation and comment in the issues.` 

## Resume

The Publishing Community Group held a plenary meeting on October 15, 2026, to launch the Digital Comics Task Force, co-led by Hadrien Gardeur and Shinya Takami. To accommodate global time zones, the task force will prioritize asynchronous, writing-based collaboration through GitHub Issues labeled "TF: Comics" to gather feedback and participation from publishers and reading system creators. Key discussions covered the EPUB 3.4 standard—featuring a new roll layout and simplified page-direction controls—as well as spine management for images and HTML fallbacks, true spread handling, and metadata enhancements including series and accessibility information.


## Links and ressources

* [True spread where both pages are needed together](https://github.com/w3c-cg/publishingcg/issues/111)
* [Alternate/variant covers for comics](https://github.com/w3c-cg/publishingcg/issues/110)
* [Backward compatibility with Japanese-style roll publications](https://github.com/w3c-cg/publishingcg/issues/109)
* [Identifying comics using dedicated metadata elements](https://github.com/w3c-cg/publishingcg/issues/108)
* [Using HTML and images as spine items in comics/manga](https://github.com/w3c-cg/publishingcg/issues/107)