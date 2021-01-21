---
title: "UK GEMINI standard and INSPIRE implementing rules"
linkTitle: "Documentation"
weight: 20
menu:
  main:
    weight: 20
---

{{% pageinfo %}}
This is a placeholder page that shows you how to use this template site.
{{% /pageinfo %}}


## Introduction 

GEMINI 2.3, June 2018)

This section of the website is for those producing or maintaining metadata for geographic information.

It describes the requirements and guidance for metadata conforming to the UK standard known as UK GEMINI. Conformance to GEMINI should ensure conformance to the INSPIRE Implementing Rules. UK specific guidance is provided.

Both UK GEMINI and the INSPIRE Technical Guidance have been developed from the International Standard [ISO 19115:2003](http://www.iso.org/iso/catalogue_detail?csnumber=26020) Geographic information - Metadata, with supplementary material from ISO 19119:2005 Geographic information - Services. The XML encoding follows ISO 19139:2007 Geographic information - Metadata - XML encoding.

If you're thinking, why GEMINI? Why not just use the INSPIRE Metadata guidance or the ISO standards? [Click here for some reasons.](/why/)

The requirements and guidance are comprehensive and accessible whether the metadata is about datasets and dataset series, or services. It should prove of value not only to those documenting metadata about geographic data and services, but also those responsible for encoding the metadata. Note that GEMINI (and the INSPIRE Guidance) are about metadata for datasets, series, and services (collectively, 'resources'); not everything in a GEMINI record can be assumed to be true individually for each feature instance in the resource. The underlying ISO standards (19115, 19139) do allow for metadata at the instance level.

The information here has been derived from a number of sources originally created as standalone documents which partially overlapped in their scope. For GEMINI 2.3, the content of these documents has been aggregated and presented in a more consistent and complete manner. The original documents relating to GEMINI 2.2 and the INSPIRE Implementing Rules remain available on the <a href="http://www.agi.org.uk/gemini/" rel="alternate">AGI </a>and <a href="http://data.gov.uk/location" rel="alternate">UK Location</a> websites. This work was sponsored by <a href="https://www.gov.uk/government/.../department-for-environment-food-rural-affairs">Defra</a>, and carried out by members of the <a href="/agi-groups/standards-committee">AGI Standards Committee</a>.
Here is a <a href="https://www.agi.org.uk/agi-groups/standards-committee/uk-gemini/40-gemini/1055-uk-gemini-major-changes-since-1-0">summary of changes</a> from earlier versions.
Here is a <a title="GEMINI element summary" href="https://www.agi.org.uk/component/content/article/40-gemini/1250-element-summary?Itemid=310">summary</a> of the GEMINI elements (similar to Table 1 and Table 2 in GEMINI 2.2).
{{% alert title="Note" %}}in GEMINI 2.3, the GEMINI Element number is called "GEMINI id"; the actual numbers have not changed, where the same element was in GEMINI 2.2.{{% /alert %}}

## How to use

If you are:
<ul>
<li><strong>new to metadata</strong> then follow <a title="GEMINI Guidelines" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1052-metadata-guidelines-for-geospatial-data-resources-part-1" rel="alternate">this link</a> to gain a general introduction to metadata for geographic information before going any further. The <a title="GEMINI Glossary" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1056-glossary" rel="alternate">glossary of terms</a> and <a title="GEMINI References" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1047-metadata-guidelines-for-geospatial-data-resources-part-3" rel="alternate">list of references</a> may also be useful;</li>
<li><strong>starting to compile metadata conforming to UK GEMINI2</strong> and are unfamiliar with the standard, then follow <a title="GEMINI requirements" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1051-uk-gemini-v2-2-specification-for-discovery-metadata-for-geospatial-resources" rel="alternate">this link</a> to understand the scope, terms used and the requirements and also <a title="GEMINI guidelines 2" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1049-metadata-guidelines-for-geospatial-data-resources-part-2" rel="alternate">this one</a> which provides general guidance;</li>
<li><strong>familiar with UK GEMINI</strong> and require specific information about the requirements and guidance for the metadata elements, then follow one of these links: to describe <a title="details; GEMINI datasets and series" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series" rel="alternate">datasets or series</a> or for <a title="Details; GEMINI; services" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1063-gemini-services" rel="alternate">services</a>;</li>
<li><strong>encoding UK GEMINI metadata in XML</strong>, then <a title="GEMINI encoding" href="/component/content/article?&amp;id=1048" rel="alternate">general guidance</a> is supplemented with detailed guidance for each metadata element at <a title="Detailed guidance – GEMINI; datasets and series" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series" rel="alternate">datasets or series</a> or for <a title="Detailed guidance – GEMINI; services" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1063-gemini-services" rel="alternate">services</a></li>
<li><strong>quality assuring metadata</strong>, then information on common metadata errors can found <a title="UKINSPIRE Errors" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1053-common-metadata-errors-uk-location-discovery-metadata-service" rel="alternate">here</a>.</li>
<li><strong>Schematron rules</strong> which check many of the constraints in GEMINI is available as a <a title="GEMINI 2.3 Schematron GitHub" href="https://github.com/AGIGemini/Schematron">on GitHub (free link)</a>, under a Creative Commons license.</li>
</ul>

## Why UK GEMINI

Why we in UK had developed separate documentation known as UK GEMINI 2.3 in parallel with the INSPIRE Technical Guidance – why not just adopt the INSPIRE Technical Guidance? It’s a good question; here are some answers – I’ll leave it to you to say whether you think they’re sufficient!


### Background

“UK GEMINI” is the UK geographic metadata standard. Or perhaps profile – in that it’s a subset of the family of ISO standards clustered around ISO 19115:2003<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a>. Or perhaps it’s guidance on how to publish geographic metadata in the UK, in the context of INSPIRE and particularly the UK national implementation of INSPIRE. In reality, it’s all those things.

GEMINI was originally published in 2004, as an evolution of the GI Gateway metadata standard to take into account the then new UK eGovernment Metadata Standard. It was updated in 2009 to version 2, to come in line with the INSPIRE Metadata Regulation, which had been published in 2007, and had adopted ISO 19115:2005 and ISO 19119:2005; that was the biggest change – introducing metadata to describe web services. GEMINI 2.1 and 2.2 kept track with changes in the INSPIRE guidelines, and meanwhile, Defra’s UK Location programme published an independent set of guidance, including how to encode GEMINI in XML (ISO 19139).

In June 2018, AGI published GEMINI 2.3, updating GEMINI 2.2, partly to bring it up to date with the INSPIRE “Technical Guidance for the implementation of INSPIRE dataset and service metadata based on ISO/TS 19139:2007” (2.0.1) – aka the INSPIRE Technical Guidance. GEMINI 2.3 brings together three AGI documents (GEMINI 2.2 as amended, and two of the three separate guidance documents) and three UK Location (Defra) documents – a national INSPIRE profile of GEMINI, encoding guidance, and a document about errors).

I led that update, as chair of AGI’s Standards Committee.

For a background to INSPIRE, see <u><a href="http://inspire.ec.europa.eu/">http://inspire.ec.europa.eu/</a></u>, especially <u><a href="http://inspire.ec.europa.eu/about-inspire/563">http://inspire.ec.europa.eu/about-inspire/563</a></u>.

For UK GEMINI, see <u><a href="/agi-groups/standards-committee/uk-gemini">https://www.agi.org.uk/agi-groups/standards-committee/uk-gemini</a></u>.

### Reasoning

#### Simplification

The INSPIRE Technical Guidance is 178 pages (in PDF form), although to be fair it’s only 86 pages of actual guidance (plus the easily overlooked three page Annex C.7 which summarises other metadata elements that are specified in particular theme guidance!).

We believe we’ve made that easier for various audiences to use: those creating metadata (for datasets, with a separate view/entry point to GEMINI for services), those creating metadata tools, and those validating metadata instances.

#### Reducing implementation choices

Leaving aside that INSPIRE Technical Guidance is just that – it’s not binding – the INSPIRE TG still contains a number of choices. We believe we have made metadata creators’ jobs easier by reducing those choices – either with an instruction, or (more often) with a ‘heavy hint’.

Examples:

<em>This one is ‘so trivial as to be hardly worth stating’, in a UK context: </em>Metadata language &amp; Resource language: for INSPIRE, these can be any of the official languages of the EU. We point out which are the two in formal use in the UK, and recommend (strongly!) that the metadata be in English.

#### Making explicit some things that are hidden

Some things are rather hidden in the INSPIRE TG, perhaps appearing in examples, or as subordinate paragraphs in other requirements. We make these explicit.

Examples


- Hierarchy level name. Because INSPIRE (reasonably) uses the ISO 19115 quality metadata, some records require a ‘hierarchy level name’. This is a subordinate clause of the INSPIRE service metadata resource type, but in practice also applies to ‘series’ metadata.
- Spatial reference system. This is not named in INSPIRE, but is a requirement (metadata/2.0/req/isdss/crs)
- Topic category. INSPIRE rightly refers to the ISO 19115 code list – the reader is left to find out for themselves what values this allows. We have brought the list into GEMINI, with the intention of making the guidance easier to use.
- Data quality: we’ve brought together into GEMINI the recommendations that are scattered across the theme Data Specifications in INSPIRE.



#### Closer alignment with the ISO standards

Sometimes GEMINI just “change the name” of the element – usually to that used by ISO. This makes it easier for communities already using the ISO metadata standards to see how to bring their metadata across to INSPIRE.

In the case of “Resource identifier”, we had found that the INSPIRE/ISO name “Unique resource identifier” confused people for two reasons:


- You can have more than one, so in that sense, it’s not “unique”
- Many people muddled it up with the W3C concept “Universal resource identifier” (URI)



### UK specific things

#### data.gov.uk

Some extra things are required just to make the metadata work in the infrastructure, including with <u><a href="http://data.gov.uk">data.gov.uk</a></u>. Others are useful to make it work better in that environment.

Examples:


- File identifier: INSPIRE doesn’t actually require “fileIdentifier”, although the Technical Guidance does recommend it. We require it for data.gov.uk – and I suspect all other metadata processing systems do too.



Previous versions of GEMINI added the function, name, and description sub elements to Resource locator. But INSPIRE has now included these as recommendations. GEMINI just describes how they get displayed in data.gov.uk.



#### code and term lists

For some elements, we mention UK specific lists that could be used. For example:


- Keyword: we mention the Integrated Public Sector Vocabulary (although some Local Authorities have suggested that this is no longer useful, let alone required).


### Community requests 

We included some things at the request of user communities in the UK. For example


- Parent identifier. MEDIN and others find this useful for relating dataset metadata records that are part of a series to the series record. This one is new in GEMINI 2.3.
- Alternative title: experience of using GEMINI suggests that some resources are known by more than one title. So to increase the chances of human users finding them in searches, GEMINI includes an explicit element for these.
- Extent (as a word / reference to controlled list): again to aid searching, GEMINI has always encouraged that metadata indicates the geographic extent that the data (or service) covers by means of a word (preferably from a controlled list).
- Vertical extent information: the marine science &amp; navigation domains, and the atmospheric scientists are all interested to make it explicit what the vertical extent of their data is, and ISO provide for that, so GEMINI has included it for some time.

### Conslusion 

The aim is to make UK geographic metadata more consistent and better quality.

There are several kinds of ‘extras’ in GEMINI:


- Restriction by guidance
- Extension on request
- Extension for infrastructure



All these restrictions and extensions are still within the scope of the underlying ISO standards, and are known to work in the INSPIRE infrastructure. None of the actual extensions beyond INSPIRE (allowing for INSPIRE’s hidden requirements!) is mandatory.

The other changes just aim to bring information together into one place, for ease of use.

<sup>[1]</sup> ISO 19115:2003 itself, ISO 19119:2005 (service metadata), ISO 19139:2007 (XML encoding), and the never-published ISO 19119 extension to ISO 19139. NOT TO BE CONFUSED with their replacements: ISO 19115-1:2014 and ISO 19115-3:2016. <em>Perhaps this footnote answers ‘why?’!</em>	
  



