# How to learn about how to read a datasheet.

I don't know how long it took me to learn to read a datasheet; learning as I went, it was probably a decade before I could get most of what I needed by instinct.

A datasheet is one of the critical documents we read when integrating software and hardware in an embedded system. For an electronics engineer (EE), this is their bread and butter. When first working on embedded software, these documents can be the source of some culture shock. They are replete with information in what might as well be a foreign language.

A few years ago, I had a real eye-opener: I could not find the information I was looking for in the PDF; it was not in the table of contents, and the keywords were not appearing in a search.  Only when I printed the datasheet did I find a whole section that hadn't been indexed, and the information had a synonym I hadn't tried yet.  To add insult to injury, this information I needed was in rendering a table that was not searchable.

I thought, "I have to write a webpage on how to read a datasheet as a software engineer".  I decided to look online and see if such a page exists. I mean, why reinvent the wheel? One Google search for `how to read a datasheet` later, I had a list of pages.

- https://www.egr.msu.edu/classes/ece480/capstone/read_datasheet.pdf
- https://www.circuitbasics.com/how-to-read-datasheets-and-application-notes/
- https://www.instructables.com/HOW-TO-READ-a-DATASHEET/
- https://www.screamingcircuits.com/resource-center/tips/reading-data-sheet
- https://digilent.com/blog/how-to-read-a-datasheet/
- https://www.microtype.io/how-to-read-an-electronics-datasheet/
- https://embedjournal.com/are-you-reading-the-datasheet/
- https://forum.digikey.com/t/tips-for-reading-datasheets/1008
- https://rheingoldheavy.com/how-to-read-a-datasheet/


There were more links on the first page, but they started talking about datasheets for test equipment. There were links to question forums like Quora, where brief hints were given as answers. There may be better pages that were not in the first fifty listed; I'm assuming the list is ranked by popularity.

I know "everyone" loves videos, but I prefer written articles. I'll be reading, not watching, if there is a video and text. Which of these links should you be spending your precious time on? Do I still need to write a guide for a software engineer?

You can see that the list has one example that is obviously from an academic institute. The Instructables link also seems to be from a university.  There are several hobbyist sites.  Digikey, a major distributor, has an offering; they generally have good educational content. The content is coming from all directions.  The question is, are any accessible to a software engineer who is learning about embedded systems? Are they all aimed at electronic engineering hobbyists and students?

## Michigan State University

- https://www.egr.msu.edu/classes/ece480/capstone/read_datasheet.pdf

- Academic

- Annotated datasheet

The example used in this how-to is a 555 timer. Early in my career, the 555 timer was widely used and could solve "almost anything". This timer device is an analog device that most software engineers can tune out completely. That said, the tutorial is still beneficial at some level as it helps understand pin-outs and equivalent schematic representations. The internal block diagram is almost skipped over.

There is valuable information in the "application" section. The presentation format is straightforward, as a marked-up datasheet with an introductory paragraph.

## Circuit Basics

- https://www.circuitbasics.com/how-to-read-datasheets-and-application-notes/

- hobbyist/maker

- Walkthrough example

Again, we see a 555 timer example, this time on a webpage.  The 555 is not a shining example of a datasheet that a software engineer would encounter.

There isn't much content, just a few labels pointing to critical features of the datasheet. There is a glaring error; the equivalent schematic is labelled a block diagram.  That is misleading; a block diagram would abstract away from transistors and show functional blocks. Indeed, what is labelled as a pinout diagram doubles as a pinout diagram and internal block diagram.

There is a paragraph at the end about Application Notes. Still, the focus is again on the EE component, without mentioning how a device may have a series of application notes covering EE, SW or both.

## Ank Labs - Instructables

- https://www.instructables.com/HOW-TO-READ-a-DATASHEET/

- academic (maybe)

- Section-by-section description

This time, the example given is an OpAmp (operational amplifier), an analog circuit that most software engineers will not be interfacing with directly.

I was discouraged reading the early part, as the formatting was not as polished. Maybe this was formatted on a different platform, and alignment got messed up on the transfer. At times, it is hard to distinguish quoted examples from the datasheet and the actual how-to text.

The early sections are described with dictionary definitions "Description" and "Application".  When you start reading about electrical characteristics, especially why limits are so important, there is more quality information. Despite such saving graces, I still have trouble recommending this page. 


## Screaming Circuits

- https://www.screamingcircuits.com/resource-center/tips/reading-data-sheet

- Design services company (quick turn CM)

- High-level overview

This is a clean, elegant glossary of data sheet sections. Again, the emphasis is on EE usage and not SW.  I like the brevity and simplicity. It's a great primer, but I don't believe it holds enough information to help a software engineer on their second foray into a datasheet.



## Digilent

- https://digilent.com/blog/how-to-read-a-datasheet/

- tools vendor (academic and hobbyist test equipment)

- Tutorial complete step by step

So here we have a very software-centric view of a datasheet.  This is a great example. The starting point returns to "How do you even get a datasheet".

Once the PDF is downloaded, the discussion starts with getting an overview of the component and how to find guiding hints in the description that will lead you to information you didn't know you needed to know.  It's a great primer on how to read a data sheet. It legitimises my belief that you can skip most of the datasheet. You don't have to read the whole dictionary to understand one word, do you?


## Microtype

- https://www.microtype.io/how-to-read-an-electronics-datasheet/

- Design services company

- Tutorial

I keep complaining about how EE-centric these pages are, but this one is well-presented.  There are common areas between EE and SW needs, especially in description, theory of operation, pinout and block diagram.  Though the text is brief, it is insightful.

The best takeaway from this was the discussion on Errata and having the latest datasheet. I often rely on the information from my supplier; Digikey and Mouser are my plans A, and B. Kyle rightly points out that those libraries are snapshots, and the manufacturer datasheets may be more up-to-date. You may find that the best documentation requires an account to access them on the manufacturer's website.

## Embed Journal

-  https://embedjournal.com/are-you-reading-the-datasheet/

- hobbyist/maker

- tutorial

It's another cleanly presented page with a few issues that seem to be from a platform change.  I've written enough markdown to recognise when an MD has been imported to a wiki or website, and things have gone wrong.  That aside, this page has a good balance of EE and SW information.  The greatest strength is in the discussion on how to decode a functional block diagram.  Such diagrams are essential, showing how register bits map to logic circuits and IO, so I am happy to see them explained.

## Digikey

- https://forum.digikey.com/t/tips-for-reading-datasheets/1008

- supplier

- tips and hints

I don't think this page tells you how to read a datasheet, but more how not to in a series of bullet points pointing out how to interpret values and spot nuance and implicit information in the datasheet.

It's a valuable guide, not an entry point, but a reference to strengthen your datasheet reading skills.


## Rheingold Heavy

- https://rheingoldheavy.com/how-to-read-a-datasheet/

- hobbyist/maker

- guided tutorial

I'm glad I stumbled on this one. It's part of an educational program coupled with a catalogue of PCBs you can add to your project.

The content is encouraging and is an interactive tutorial for self-guided learning. It's not an exhaustive guide, but it does help you dip your toe into the world of schematics. The best takeaway from this page was "Documenting the Documentation". I am a fan of hard-copy datasheets for marking up, but I like the idea of making a summary sheet. I would probably make that summary a wiki page at work or in a GitHub repo; I can keep that when I change jobs.

# Summing up

This small sampling shows that there is no perfect guide for software engineers. There is a heavy assumption that you are an EE, and that is what you are interested in. For hobbyists and makers, it seems that you are expected to want to build your own board or integrate modules, so again, more information about getting voltages and current information.  Even when we get a SW view, it tops out at bus protocols and register-map definition.  There probably is room for a new page on the subject, but to include everything, then that page would start to get very long.