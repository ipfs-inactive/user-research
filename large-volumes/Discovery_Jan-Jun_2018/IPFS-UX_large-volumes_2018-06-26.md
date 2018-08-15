# Research for “Large Volumes” Use Cases (50+ TB of Data)

+ [What we did](#what-we-did)
+ [Methodology](#methodology)
+ [Who we talked to](#who-we-talked-to)
+ [Findings](#findings)

## What we did

[Kelani Nichole](http://kelaninichole.com/) led an initial round of generative research (interviews and synthesis) over the first two quarters in 2018 to:

+ Gain deeper knowledge of user needs around handling large volumes of data (50+ TB)
+ Uncover blockers and knowledge gaps
+ Identify end user pain points

## Methodology

60-minute semi-structured interviews via remote videoconference (teleconference where video was not possible)
Video or audiorecorded (with permission), transcribed, and analyzed
30-Minute debrief after every interview with shared summary notes

## Who we talked to

5 people who manage large volumes of data (50+ TB)
Resource: [Why You Only Need to Test with 5 Users](https://www.nngroup.com/articles/why-you-only-need-to-test-with-5-users/)
- Professional Data Manager
  + Govenment Org
- Software Developers
  + University Library / Archive
  + Genetics Researcher
  + Startup
- Community Data Steward
  + Research Network / Initiative

## Findings summary
See all the details here: [Discovery_Jan-Jun_2018/IPFS_Large_Volumes_UX_Findings_FINAL.pdf](#)

### Theme: Metrics Matter
+ Metrics around data consumption are key to success in ‘Large Volumes’ use cases. People must prove value to sustain their work.
+ Opportunity: Provide great tooling for showing usage of data across the network (beat HTTP access logs)

> “High impact projects are recognized by the community for being impactful, citation counts. They want a metric how USED the data is, So how does that impact grants? Someone will have to be the first to take a hit on metrics.”

> “Projects are significantly more successful when we have buy-in from the line-office/scientist expertise.”

> “Our influencers I guess are other teams across the library, like the earth sciences and geospatial team. They drive a lot of our product and goals for the year.”

### Theme: Authenticity Adds Value
+ Verifying the source and authenticity of data is a common need across participants for accurate citations, reliable versions, and enhanced performance in addition to security.
+ Opportunity: The way IPFS uses content addressing gracefully addresses these issues. Provide people with the tools to wield that power in these cases.

> “What we need to ensure is that someone could audit it and verify we didn’t do anything with the bytes. We try to make sure the number of hands involved are very few, so we automate as much as possible.”

> “Content addressing is really interesting to me, one thing we are concerned with is data authenticity.”

> “If you've got the hash going in and the hash going out, and you refer all that with the root node in your merkle dag in your publication then all of a sudden you’ve cryptographically verifiable, mathematically confident link to everything being correct.”

### Theme: Deduplication
+ There is a clear need to reduce redundancy, manage sub-sets of data, and create efficiency in data management processes.
+ Opportunity: Align messaging about ‘deduplication’ to the key painpoints and provide better tooling.

> “We know we have a deduplication problem with other orgs, but we don’t know how to address it. Content addressing could help with that, but it hasn’t risen to the top of the priorities.”

> “How many copies of this same data are we storing locally? More importantly how much is the taxpayer spending to store all copies of this same data locally?”

> “In the cluster we don’t have to worry about which server has that file, and now more and more places are putting genomes from NCBI onto IPFS.”

> “We are leveraging the natural deduplication properties of the content addressing where, when the PDF doesn’t change, the hash doesn’t change, and we add nothing to our overhead.”

### Theme: Metadata
+ Producing metadata is a substantial overhead. In particular, due to the proliferation of schemas and identifiers, people struggle to connect and reuse data.
+ Opportunity: IPLD is positioned to solve this, but successfully applying it in this domain will require grappling with the complexities and nuance of metadata.

> “The primary bottleneck is management and prioritization of getting metadata created.”

> “The question is how do I refer to those files? The archive is centralized so I have to use an ID, it’s an arbitrary number. The search engine has discovered it but then there’s the problem of how do you talk to other people about the data. IPFS solves this because you have a global namespace, a method of talking to data, your multihash will be consistent so I think it can be helpful there.”

> “A lot is modeling of IPLD that surrounds the storage of the metadata. I don’t think IPFS will know that a string of bytes is a radiology image or a genome, so modeling the metatdata surrounded around that, and tying that to the code, So that’s an issue just in the piping, and how do you use a standard, there’s not one, so we need to create a standard and publish it.”

### Initial user journeys: data producers and providors
---------------------------------------------------------------------------------------------------------------------------
<img width="1100" alt="ipfs_large-vols_user-journey_producers" src="https://user-images.githubusercontent.com/4827522/44127455-b1e9d6f0-a080-11e8-9771-a0cdc27b5110.png">

--------------------------------------------------------------------------------------------------------------------------

<img width="1100" alt="ipfs_large-vols_user-journey_providers" src="https://user-images.githubusercontent.com/4827522/44127451-ac7a54d8-a080-11e8-891f-43ebd6742712.png">
