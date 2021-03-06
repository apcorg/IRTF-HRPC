---
title: Human Rights Protocol Considerations - Research Report
docname: draft-doria-hrpc-report-01
date: 2016-03-21
category: info

ipr: trust200902
area: General
workgroup: Human Rights Protocol Considerations Research Group
keyword: Internet-Draft

stand_alone: yes
pi:
  rfcedstyle: yes
  toc: yes
  tocindent: yes
  sortrefs: yes
  symrefs: yes
  strict: yes
  comments: yes
  inline: yes
  text-list-symbols: -o*+

author:
-
  ins: A. Doria (ed)
  name: Avri Doria
  org: APC
  email: avri@apc.org

normative:

informative:
  RFC1958:
  RFC1984:
  RFC2026:
  RFC2639:
  RFC2919:
  RFC3365:
  RFC5890:
  RFC5891:
  RFC5892:
  RFC5893:
  RFC6162:
  RFC6783:
  RFC6973:
  RFC7230:
  RFC7231:
  RFC7232:
  RFC7234:
  RFC7235:
  RFC7236:
  RFC7237:
  RFC7258:
  UDHR:
    title: The Universal Declaration of Human Rights
    date: 1948
    author:
      org: United Nations General Assembly
    target: http://www.un.org/en/documents/udhr/
 
  HRPC-GLOSSARY:
    title: Human Rights Protocol Considerations Glossary
    date: 2015
    author:
      - ins: N. ten Oever
      - ins: A. Doria
      - ins: D. K. Gillmor
    target: https://www.ietf.org/id/draft-dkg-hrpc-glossary-00.txt
 
  HRPC-Method:
    title: Human Rights Protocol Considerations Methodology
    date: 2015
    author:
      - ins: J. Varon
      - ins: C. Cath
    target: https://www.ietf.org/id/draft-varon-hrpc-methodology-00.txt

  HRPC-Research:
    title: Research into Human Rights Protocol Considerations
    date: 2015
    author:
      - ins: N. ten Oever
      - ins: C. Cath
    target: https://www.ietf.org/internet-drafts/draft-tenoever-hrpc-research-00.txt
 
  Cath:
    title: A case study of codeing rights
    date: 2015
    author:
       - ins: C. Cath

  Clark:    
    title: The Design Philosophy of the DARPA Internet Protocols
    author:
      - ins: D. Clark
    seriesinfo: Proc SIGCOMM 88, ACM CCR Vol 18, Number 4, August
        1988, pp. 106-114.
    date: 1988

  Blumenthal:
    title: Rethinking the design of the Internet The end-to-end arguments vs. the brave new world
    author:
       - ins: M. Blumenthal
       - ins: D.D. Clark
    seriesinfo: ACM Transactions on Internet Technology, Vol. 1, No. 1, August 2001, pp 70-109.
    date: 2001

 
  Liddicoat:
    title: Human Rights and Internet Protocols
    author:
       - ins: J. Liddicoat
       - ins: A. Doria
    target: https://www.apc.org/en/pubs/human-rights-and-internet-protocols-comparing-proc
   
  Denardis09:
    title: Protocol Politics
    author:
      - ins: L. Denardis
    date: 2013

  Denardis14:
    title: The Global War for Internet Goverance
    author: 
    - ins: L. Denardis
    date: 2014
   
  Netmundial:
    title: NETmundial Multistakeholder Statement
    date: 2014
    target:  http://netmundial.br/wp-content/uploads/2014/04/NETmundial-Multistakeholder-Document.pdf

  Ostrum:
    title: Governing the Commons
    author: 
    - ins: E. Ostrum,
    date: 1990
   
  Post:
    title: Internet Infrastructure and IP Censorship
    author:
      - ins: D. Post
    date: 2015
    target:  http://www.ipjustice.org/digital-rights/internet-infrastructure-and-ip-censorship-bydavid-post/

  Zittrain:
    title: The Future of the Internet And How to Stop It
    date: 2008
    author:
      - ins: J. Zittrain

--- abstract

This document presents an overview snapshot of the HRPC project to map engineering concepts at the protocol level that may be related to human rights, with a focus on the promotion and protection of the freedom of expression and of association.

It provides a framework while reporting on the study including: theoretical background, results and basic considerations. It will reference the detailed work being done on terminlogy and case studies documented in the research draft. It also folds in discussions from the research literature. The documents, {{HRPC-Research}} and this document, form an interrelated set that may later be combined into a single document.

Discussion on this draft at: hrpc@irtf.org // https://www.irtf.org/mailman/admindb/hrpc

--- middle


Background
============

Several reports from former United Nations (UN) Special Rapporteur on the promotion and protection of the right to freedom of opinion and expression, Frank La Rue, have made the relationship between the Internet and human rights explicit and led to the approval of the resolution "on the promotion, protection and enjoyment of human rights on the Internet" at the UN Human Rights Council (HRC). More recently, it led to the resolution "The right to privacy in the digital age" at the UN General Assembly. The NETmundial outcome document {{Netmundial}} affirms that human rights, as reflected in the Universal Declaration of Human Rights {{UDHR}}, should underpin Internet governance principles.

Although the application of human rights to Internet policy consideratons has a firm rights' basis, a direct relation between Internet architecture and protocols and human rights needs to be established and requires both exploration and description. As the full range of the interdependent and interrelated human rights would be challenging as a starting place for discussions, the research group has decided to start with the the rights of freedom of expression and association.  

An additional challenge in bringing the discussion of human rights into Internet engineering discussions is the absence of an agreed upon vocabulary for such discussions.  Developing a vocabulary for this discussion is a first requirement for the HRPC research effort.

It has been argued in {{Liddicoat}} that concerns for freedom of expression and association were a strong part of the world-view of the community involved in developing the first Internet protocols. Whether by intention or by historical coincidence, the Internet was designed with freedom and openness of communications as core values. But as the scale, as well as internationalization and commercialization of the Internet have grown, the influence of such world-views has had to compete with other values, such as ease and cost of development as well as the costs and difficulties in maintaining and upgrsding the network and network elements. The purpose of this research project is to discover and to document possible considerations, that is issues to be considered, involved in taking human rights into account when creating protocols.

Following the lead of work done for RFC 6973 {{RFC6973}} on Privacy Consideration Guidelines, the premise of this research is that some standards and protocols can either enable or threaten human rights on the Internet.

As stated in RFC 1958 {{RFC1958}}, the Internet aims to be the global network of networks that provides unfettered connectivity to all users at all times and for any content. Open, secure and reliable connectivity is essential for rights such as freedom of expression and freedom of association, as defined in the Universal Declaration of Human Rights {{UDHR}}. Therefore, considering connectivity as the ultimate objective of the Internet  makes a case that human rights are core values of the architecture of the network.

The IETF has determined that an essential part of maintaining the Internet as a tool for communication and connectivity is security. Indeed, "development of security mechanisms is seen as a key factor in the future growth of the Internet as a motor for international commerce and communication" RFC 1984 [RFC1984] and according to the Danvers Doctrine RFC 3365 {{RFC3365}}, there is an overwhelming consensus in the IETF that the best security should be used and standardized.

In RFC 1984 {{RFC1984}}, the Internet Architecture Board (IAB) and the Internet Engineering Steering Group (IESG), the bodies which oversee architecture and standards for the Internet, expressed: "concern by the need for increased protection of international commercial transactions on the Internet, and by the need to offer all Internet users an adequate degree of privacy." Indeed, the IETF has been doing a significant job in this area {{RFC6973}} and {{RFC7258}}, considering privacy concerns as a subset of security concerns. {{RFC6973}}

Besides privacy, the premise of this work is that it is possible to establish human rights consideratons for other aspects of connectivity embedded in standards and protocols. It also intended to build on the the idea that protecting all rights is as much a security concern in the Internet as is the protection of privacy. The research also intends to document other bases for consideration of human rights as core values in Internet architectures and protocols.  This first phase of reasearch focuses on freedom of expression and the right to association and assembly online.  In doing so, given the interrelationship of all rights, other rights may be touched upon in the discussion, but the primary emphasis will be to discover where there are considerations that relate specicially to the Freedoms of Expression and of Association and Assembly.  In the first phase there will also be a reliance on arguments based on securuty considerations, though the effect of other values will be considered.

# Terminology

The terminology being used in this project was defined in {{HRPC-GLOSSARY}} and is applied in {{HRPC-Research}}.

The process of developing a glossary has involved taking the variety of glossaries defined by the IETF in its various RFCs, comparing the terms both among the various RFC definitions and with terminology used in human rights field to produced a synthesized set of definitions after discussion in the research group. The goal is to produce a set of terms, using existing terminology, that can assist clear discussion among engineering experts and human rights experts.  At this point in the research this vocabulary has been provisionally accepted in the rresearch group.

The glossary also includes the definitions of some complex terms, such as security and connectivity that relies of several of the other defined terms. Some of these complext defintions are still under discussion.

# Theory

## Universal Declaration of Human Rights (UDHR) and Internet Architecture

This project is focused on two rights defined in the UDHR {{UDHR}}, Article 19 on Freedom of Expression and Article 20 of Freedom of Association.

Article 19
   :   Everyone has the right to freedom of opinion and expression; this right includes freedom to hold opinions without interference and to seek, receive and impart information and ideas through any media and regardless of frontiers.

Article 20
   :  1 Everyone has the right to freedom of peaceful assembly and association.
   :  2 No one may be compelled to belong to an association.

## Link between protocols and human rights

The Methodology includes defintions of the basic human rights in terms of the engineering terminology. For example from {{HRPC-Method}}

+ Right to Freedom of Expression builds on definitions of 
 - Connectivity
 - Privacy
 - Security
 - Content Agnosticism
 - Internationalization
 - Censorship resistance
 - Open Standards
 - Heterogeneity support
 
 + Right to Association builds on the defintions of
 - Connectivity
 - Decentralization
 - Censorship resistance
 - Pseudonymity
 - Anonymity
 
 Detailed defintions of the included terms can be found in {{HRPC-Method}}

When looking at protocols the considerations can apply from several perspectives.

+   The protocol's direct effects on human rights on the Internet.
-   The protocol's direct effect  on human rights in combination with other protocols
-   The effect of specific protocol elements, separately or in combination with other protocol elements on human rights on the Internet
-   The ability to determine when various effects are occurring, i.e. transparency
-   The effect of deployment or non deployment.  While this may be may seem beyond the protocol itself, often the design of protocol, its difficulty in implementation and the degree to which it contains required elements, poison pills or other protocol artifacts that either encourage or discourse implementation or deployment can be significant in the overall human rights affect of a protocol.

Several key pieces of researched are discussed in this section.  Readers/reviewers who have other recommended sources for relevant research that should be discussed in this document are invited to submit such for inclusion.


## Related research

This section will look at the theoretical work that has been done in the are of rights and protocols.  It will include the academic research on the topic including the work of David Post {{Post}}, Jonathan Zittrain {{Zittrain}} and Laura Denardis, among others.


In Protocol Politics {{Denardis09}} Denardis discusses "how values enter, or should enter, Internet protocol design." She describes the "IETF process itself self-consciously expresses certain values." The discussion goes on to define some examples of of IETF values, including:

+ "Universality and competitive openness - one objective of developing a standard is for it to become widely used in the marketplace;
- "participatory openness in the standards=setting process;
- "the end-to-end architectural design principle specifying that intelligence should be located at network end points rather than in media res."


To demonstrate the point, she presents a case study where engineers at the IETF "identified privacy as a value pertinent to IPv6 address design and embedded this design into design choices" with a detailed description of the issue of including Ethernet Addresses as part of the IPv6 address culminating in the design of IPv6 privacy features and changes.  Interestingly she also describes how the IETC engineering community was aware of the privacy challenges, the rights challenges, before media and government discovered the problem and where working on the problem before the fire firestorm began.

The description ended with the following: "this episode is a reminder that some of the most critical Internet governance questions concern individual civil liberties and that design decisions can present an opportunity to advance libertarian and democratic values or to contain these values.  IPv6 privacy design implications and value-conscious design choices reinforce the notion that Internet architecture and virtual resources cannot be understood only through the lens of technical efficiency, scarcity, or economic competition but as an embodiment of human values with social and cultural effects."

## Theory discussed in the research group

### Principles from NetMundial Multistakeholder Statement

NETmundial was a bell-weather event held in October 2014, where stakeholders from academia, business, civil society, governments came together to discuss Principles and a Roadmap for Internet governance.  While the Principles did not address protocol development specifically, they did include a principle on Open Standards:

"Internet governance should promote open standards, informed by individual and 
collective expertise and decisions made by rough consensus, that allow for a global,
interoperable, resilient, stable, decentralized, secure, and interconnected network,
available to all. Standards must be consistent with human rights and allow
development and innovation." {{Netmundial}}

The NETmundial Roadmap on the other hand was a bit more specific on certain topics including digital security and arbitrary surveillance:

 - "Initiatives to improve cybersecurity and address digital security threats should
involve appropriate collaboration among governments, private sector, civil society,
academia and technical community. There are stakeholders that still need to
become more involved with cybersecurity, for example, network operators and
software developers."

 - "Mass and arbitrary surveillance undermines trust in the Internet and trust in
the Internet governance ecosystem. Collection and processing of personal data by
state and non-state actors should be conducted in accordance with international
human rights law. More dialogue is needed on this topic at the international level
using forums like the Human Rights Council and IGF aiming to develop a common
understanding on all the related aspects." {{Netmundial}}

### Value laden engineering as discussed in A case study of codeing rights by Cath

This work discusses four basic architectural principles that are encoded in Internet Technology:

- Openness, Permissionless Innovation, and Content Agnosticism
- Interoperability
- Redundancy and the Distributed Architecture
- The End-to-End Principle

The work by Cath explores the relationship of the architectural principles to the human right of freedom of expression and asks whether the IETF has a repsonsiblity toward human rights.  The paper shows that that there are numerous refeences to normative principles among the body of work of the IETF. It argues that provides the necessary indication that ethics are within the purview of IETF considerations.  The research question asked by the work is: "Should the right to freedom of speech be instantiated in the protocols and standards of the Internet Engineering Task Force?" This quetion is one of the questions being asked in this research group.

Despite this ethical basis in Internet potocols, the threat of fragmentation by countries that do not accept human rights suggests that and an answer to the normative research question is negative: support for human rights should not be intitiated in the Internet in order to avoid fragmentation.  This can be understood to mean that care must be taken to turning into protocols political targets.  On the other hand the principles that are encoded in the Internet do make it better at enabling rights.  This encourages work such as the work done for privacy consideration in the IETF and the research done of protocol consideration for the freedoms of expression and association, as long as these are just considerations and not requirements.  The paper cautions against using protocols to achieve advocacy goals.

### "Values and Networks" work by Roland Bless

TBD

## Protocols as either a public good or a common pool resource.

While not specifically part of the research, a background theoretical discussion in Internet rights discussion involves discussion of whether the Internet is a public good. Becasue of the requirement that a public good be something that is non-excludable in that that is a good that cannot be withheld from any individual.  To be a public good the Internet must also be non rivalous meaning that is use by some does not preclude its use by others.

Strictily speaking, the Internet does not meet these requirements.  The fact that much of the world still does not have Internet access shows that it is still excludable.  Addtionally there is question of whether in terms of bandwidth and scalability, it is non-rivalrous.  Many have argued that is is a Common Pool Resource (CPR), as defined by Ostrom {{Ostrum}}.  This claim has yet to be substantiated as the interent needs to satisfy various design principles as a CPR. Discussion of this issue is beyond the scope of this draft.

While the discussion on whether the Internet itself, as an infrastrucure, is either a public good or CPR, is open and contentions, it may be simpler to establish whether the set of core protocols is a public good.  This is relavant to the research in this group dealing with protocol considerations.  It can be argued that for Internet protocols to be non-excludable, it has to be possible to all to use them.  Through the use of the core Internet protocols, anyone can create a network that connects into the Internet.  while some protocols are encumbered by propoerty rights, a core set of protocols that are not encumberd, and thus freely avaialble to all, can be described. It can also be easily argued that one party's use of the core set of Internet protocols does not have the effect of precluding use by others. 

Establising that Internet protocols are a public good adds an economic consideration to the discussions and provides possible avenues for basing human rights consideraton on more that just security allowing other bases for discussion of the trades off in considerations when designing or deploying a protocol. The question still needs to be explored as to whether Internet protocols as a public good has any effect on the protocols considerations to be defined in this group.

# Methodology

The methodology is defined in detail in Research into Human Rights Protocol Considerations {{HRPC-Research}}.  

The purpose is to map the potential relations between human rights and protocols so that considerations can be derived.

+ the first step involved scoping the research problem
- Translating Human Rights Concept into Technical Definitions
  - Mapping protocols and standards related to Freedom of Expression and Freedom of Assembly as defined in human rights covenants and agreements
  - Extracting concepts from any and all RFCs that use and define these terms
  - Building the common glossary to be used linking engineering and human rights concepts
- Discovering cases of protocols that have an effect on human rights 
  - Enablers of rights
  - Enablers of abuse 
- Working though the cases to determine and describe the issues that affect human rights
- Applying the human rights technical definitions to the cases
- Derivation of possible considerations

## Case Studies

The case studies and their initial status is being documented in draft-varon-hrpc-methodology {{HRPC-Research}}.

In each of the case studies, the behavior of the protocols is analysed for its positive and negative effects.  In some case these effects are due to the design of the protocol itself, in others they are due to existing or absent features.

Initial versions of the analysis on the following protocols are currently being discussed on HRPC list and being describe in the methodology document.  

Additionally, discussion of the rights themselves and the evidence of these rights being implicits in the IETF design principles {{Clark}} and in some of the existing architecture and protocols, Cath and Liddicoat suggest other considerations.


+ IP

Covering issues concerning the network visibility of source and destination, address translation and mobility

+ DNS
- HTTP
  - HTTP code 451
- XMPP
- Peer to peer
- VPN
- Middleboxes
- DDOS

## Methodology Issues

The current methodology is based on discourse analysis and ethnographic
research methods.  This method is explain in {{HRPC-Research}} While this is a good basis for intitial discussions, questions can be asked as to whether the hypothesis formed as a result of this anaylisis can be abstracted and whether evidence for simalr effects can be shown to be of wider application.  A full anlaysis also requires that some attempt be made to test any candidate considerations for other effects and for unintended consequemces.

# Possible areas for protocol considerations

Using the definitions derived, for the the rights of freedom of expression and freedom of assembly, and the protocol attributes discovered in the use cases, a set of questions can be developed that enable a protocol designer to consider whether their design has any positive or negative effects on these human rights. The questions shold also give guidance in terms of protocol atributes that can aid in creating procols that enable as opposed to hinder human rights.

{{HRPC-Research}} includes a first take on such questions.  This work is still at an early stage.  There have been recommendations in the list that the form of the questions be based on best practices for questionnaire development.  the questions will need to be tested to determine whether they are fit for purpose.

## Emergent Issues/Questions

This records some of the question opened in discussion of the group that open broader questions that those centered on protocol considerations.  Often the question involved the manner in which the protocols are deployed or used.


+ Can DDOS be considered freedom of expression when used for advocacy?
+ Even if it does, does this matter?  Is interruption of communication in the Internet such a negative aspect that it is never acceptable? Is DDOS a moral equivalent to "capital" infractions in that its use is never permitted by Human Rights under any situation.
    
+ How do we differentiate between protocol effects that are inherent to the protocol and those that arise from implementation, misuse or from avoidance of non mandatory features. This includes factoring for lack of updating. Differentiating these effects from each other is important in designing the considerations.

#  Next Steps

As discussed in the methodofy section, a set of test needs to be undertake to determine whether the protocl attributes that are isolated from the various use case can be abstracted and ested in situation other thn in the test cases.

Once this is done, a set of considerations can be drafted and discussed by the research group.

The current revision of {{HRPC-Research}} includes a first set of possible considerations.

Once the first take at considerations are defined, what are the next steps for creating something that can be usable for protocol designers and implementers in considering freedom of expression and and freedom of association in their work.


Acknowledgements
===============

A section that include the many contributors of text as as commenters and those who are assisitng this project in existing.

IANA considerations
===================

There shouldn't be any.

Security Considerations
=======================

There shouldn't be any.


