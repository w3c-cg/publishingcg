---
layout: document
title: Launching Digital Comics Task Force - Publishing Community Group Plenary
date: 2026-10-01
---

![W3C Logo](https://www.w3.org/Icons/w3c_home)

**Publishing Community Group Plenary:** **Launching Digital Comics Task Force** 
**Minutes 01 October 2026 / 12:00 PM EDT = 16:00 PM UTC**

*A second discussion for this work is planned October 15th at 4 pm JST*


## Attendees

Chair: Wolfgang Schindler, Scribe:  Gautier Chomel

Invited speaker: Hadrien Gardeur, Shinya Takami, co-leads of the Digital Comics Task Force.

Present: Julientaq, Gregorio Pellegrino, George Kersher, Brady Duga, Dale Rogers, Henry Stark, Charles LaPierre, Ken Jones, Jim Saiya.


## Agenda

*Digital Comics Task Force aims to address specific non-normative work and challenges within the digital comics ecosystem. This plenary will present the challenges and process for this work, which, given the significant time zone differences, will prioritise writing-based collaboration via GitHub Issues labelled with TF: Comics and reach out to publishers and reading system creators to collect feedback and encourage participation.* 

## Notes

**Hadrien:** it’s been more than ten years since manga and comics were introduced in EPUB, in the early days of EPUB3. Still, we’ve done very little work on fixed layout for comics; the spec has evolved very little for this category of publishing. 

One issue is the lack of good practices; we’ve seen organisations doing their best, even sometimes creating proprietary metadata.

In the context of EPUB 3.4 and recent evolutions, including scroll layout, it seems like the moment to work on best practices. 

The intent of this TF is to document what exists, not to incubate new approaches. 
One issue is that comics work is not often at the centre of the maintenance WG; this segment of the industry is not well represented. We feel there is a need for an easier place for publishers and retailers working exclusively with comics and manga to join. A place for them to provide feedback so we can document what exists. 

The CG is the open door we need for industry representation.

Another point is that some markets are more represented in this topic. Japan for sure is a huge market that produces more comic manga than any other market. A different but also very old tradition is the BD market in Europe. 

A challenge is that spanning three continents makes it challenging; there’s also a language challenge. For those reasons, we want to keep it mainly text-based; we think it is a more inclusive approach.

So, using the GitHub issue tracker with a label ComicTF. So mostly written work and some occasions to meet in person, at TPAC or other events like DPS or Book Fairs.
We’re not chartering for a determined time; we plan to keep working as long as needed to shape existing best practices. 

**George:** So we will open issues, discuss them there, and update documents to reflect those discussions. 

**Brady:** We could discuss at TPAC

**Hadrien:** That soon; let's see if we can set up something

**Shinya:** We could present what we are doing in Japan; that’s a work in progress.


### SubTopic: metadata

**Hadrien:** we’ve discussed before and during 3.4; it’s important to document what publishers and reading systems can leverage with the new roll layout. [https\://github.com/w3c-cg/publishingcg/issues/109](https://github.com/w3c-cg/publishingcg/issues/109) 

Another point is identifying comics. EPUB has no Profile concept, while comics and manga need to be treated differently by RS. We’ve seen Amazon asking that for publishers and other integrators too. [https\://github.com/w3c-cg/publishingcg/issues/108](https://github.com/w3c-cg/publishingcg/issues/108)

Another point is variant or alternate covers. US comics for specific volumes sometimes have an alternate cover designed by another artist. Now we have only one cover in EPUB. A US publisher could include multiple covers in a spine but has no way to inform that in EPUB. [https\://github.com/w3c-cg/publishingcg/issues/110](https://github.com/w3c-cg/publishingcg/issues/110)

Another thing we should open an issue for: outdated rendition controls; we had this in the specs, but there is no real use case for how to use it.

Accessibility metadata remains mandatory for the EU market, even if the file is not accessible. A short list should be agreed on to inform about accessibility of comics consistently.

Series, volumes, collections, episodes, seasons, story arcs, etc.: there’s a variety of links between editions. It’s on the cover, yes, but agreeing on how to inform the RS consistently would be great so it could offer rich affordances. We have a way, but is it sufficient? [https\://www\.w3.org/TR/epub-34/\#sec-collection-type](https://www.w3.org/TR/epub-34/#sec-collection-type)

### SubTopic: Spine

**Hadrien:** The Spine raises questions too. 
* Images vs HTML https://github.com/w3c-cg/publishingcg/issues/107 
* Single vs multiple resources for a true spread https://github.com/w3c-cg/publishingcg/issues/111 Some visual pages really need to be displayed side by side; it’s quite common. Cutting those into separate resources is creating weird things. Because of third-party technical restrictions, most publishers still separate pages into resources; we need to discuss. I think the ideal approach is to be one image; that’s the opposite of what is being done, but it would be much better for the reading experience. Cut resources are creating bad reading experiences. 

**Brady:** that’s a difficult topic; combining separate resources can be a mess for RS developers, making sure the correct page goes in the correct place so they combine well. 

**Hadrien:** I think the spec has the tool, spread placement; the problem is how it is implemented, maybe an industry issue because of major players forcing not to use them. With good practices, we should be able to advocate for a wider implementation. 

**Hadrien:** Then Mixed Layout. There aren’t many, but they exist; most are fixed layout with an intro reflow. Support is poor; it’s allowed, but using it comes with risks of breaking in RS. 

### SubTopic: Images

**Hadrien:** A lot of people use only JPEG because it works, but we can do much more, even if we keep JPEG as fallback. 

**Henry:** The barrier is the RS; we need to convince as many of them to use modern formats. Maybe resolution also matters. 

**Hadrien**: Absolutely, it does not exist as a recommendation and needs to be.

### SubTopic: Accessibility

**Hadrien**: We can produce comics with embedded audio; we have metadata, so a lot can be done with the existing. Fixed-layout media overlay work; XHTML allows embedding text. Still, we are missing a spec for a concrete, complete accessible comic. It’s beyond our group work but could become an incubation for the PCG. One discussion after the other.

**Ken:** Regional navigation reading order and MO in region-marked images with live taste. So areas of a page with attached text and audio that can be navigated. Not perfectly accessible but still a great experience. It is possible to do valid region navigation epub; let’s include it.

**Hadrien**: panel-by-panel navigation is a topic broader than accessibility. But reading those on a smartphone is still challenging. We know Kindle has absolute position div with data attribute designed proprietarly. We know play book has something, i guess automatically generated

**Brady:** I confirm, you cannot author that; it’s auto but could technically be exported as region nav.

**Hadrien**: it’s a legacy from IDPF, there’s a discussion, and it would be good to author something that would be supported by RS. This is definitely a good topic, not only accessibility 

### General discussion

**George:** I wonder how many documents we are targeting; there’s a huge area to cover.

**Henry**: It’s also just ugly to have a visible gap, since many reading systems struggle to merge the two pages together if they’re separate files  
Japanese readers have in majority added a scrolling mode, and it is in strong demand by users  
(no double spread scrolling mode)  
   
**Henry**: Unfortunately the industry has ossified around the old formats  
   
**Dale Rogers** As a content creator, it also makes me wonder if I will need to have multiple versions of an EPUB because RS do things differently.  
   
**Henry**: One of my personal goals for this project is to create open source utilities to allow for conversion/optimization to our recommended EPUB format/spec  
@Dale Rogers that’s something I’ve considered, delivering “better” EPUBs to places that support them. Unfortunately that would require cooperation from the companies that distribute the files on behalf of most creators, though if you’re doing it yourself (which happens in my industry) then it is possible  
   
**Jim Saiya** On the subject of a11y/metadata for comics/manga; a couple of resources to consider:

* [ComicsML](http://comicsml.jmac.org/)  
* [Oh No Robot: comics search](https://www.ohnorobot.com/letsbefriends.php)

I would like the best practices document to talk about where the demand is. No need to build something that no one wants to buy.

## Decisions taken
No decision taken.

## Action items
Everyone is invite to comment in the existing issues or open new issues if necessary. 

## Resume
Comics and manga have been part of EPUB for over ten years, yet fixed-layout practices for them have barely evolved, and some organisations have resorted to proprietary metadata. With EPUB 3.4 and its new scroll layout, the time has come to document good practices.

The task force will document what exists rather than invent new approaches, working mainly in writing through GitHub Issues (label "TF: Comics") to bridge time zones and languages. Early topics include comics-specific metadata, double-page spreads, modern image formats, accessibility and panel-by-panel navigation.

Comics and manga publishers, retailers and reading-system developers are invited to join the Community Group and share their feedback.

## Links and ressources

* [True spread where both pages are needed together](https://github.com/w3c-cg/publishingcg/issues/111)
* [Alternate/variant covers for comics](https://github.com/w3c-cg/publishingcg/issues/110)
* [Backward compatibility with Japanese-style roll publications](https://github.com/w3c-cg/publishingcg/issues/109)
* [Identifying comics using dedicated metadata elements](https://github.com/w3c-cg/publishingcg/issues/108)
* [Using HTML and images as spine items in comics/manga](https://github.com/w3c-cg/publishingcg/issues/107)