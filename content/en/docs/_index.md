
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


# Introduction 

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

# How to use

If you are:
<ul>
<li><strong>new to metadata</strong> then follow <a title="GEMINI Guidelines" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1052-metadata-guidelines-for-geospatial-data-resources-part-1" rel="alternate">this link</a> to gain a general introduction to metadata for geographic information before going any further. The <a title="GEMINI Glossary" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1056-glossary" rel="alternate">glossary of terms</a> and <a title="GEMINI References" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1047-metadata-guidelines-for-geospatial-data-resources-part-3" rel="alternate">list of references</a> may also be useful;</li>
<li><strong>starting to compile metadata conforming to UK GEMINI2</strong> and are unfamiliar with the standard, then follow <a title="GEMINI requirements" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1051-uk-gemini-v2-2-specification-for-discovery-metadata-for-geospatial-resources" rel="alternate">this link</a> to understand the scope, terms used and the requirements and also <a title="GEMINI guidelines 2" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1049-metadata-guidelines-for-geospatial-data-resources-part-2" rel="alternate">this one</a> which provides general guidance;</li>
<li><strong>familiar with UK GEMINI</strong> and require specific information about the requirements and guidance for the metadata elements, then follow one of these links: to describe <a title="details; GEMINI datasets and series" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series" rel="alternate">datasets or series</a> or for <a title="Details; GEMINI; services" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1063-gemini-services" rel="alternate">services</a>;</li>
<li><strong>encoding UK GEMINI metadata in XML</strong>, then <a title="GEMINI encoding" href="/component/content/article?&amp;id=1048" rel="alternate">general guidance</a> is supplemented with detailed guidance for each metadata element at <a title="Detailed guidance – GEMINI; datasets and series" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series" rel="alternate">datasets or series</a> or for <a title="Detailed guidance – GEMINI; services" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1063-gemini-services" rel="alternate">services</a></li>
<li><strong>quality assuring metadata</strong>, then information on common metadata errors can found <a title="UKINSPIRE Errors" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1053-common-metadata-errors-uk-location-discovery-metadata-service" rel="alternate">here</a>.</li>
<li><strong>Schematron rules</strong> which check many of the constraints in GEMINI is available as a <a title="GEMINI 2.3 Schematron GitHub" href="https://github.com/AGIGemini/Schematron">on GitHub (free link)</a>, under a Creative Commons license.</li>
</ul>


