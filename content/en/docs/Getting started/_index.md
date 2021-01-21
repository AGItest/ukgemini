---
title: "Getting Started"
linkTitle: "Getting Started"
weight: 2
description: >
  Starting to compile metadata conforming to UK GEMINI2 and are unfamiliar with the standard - understand the scope, terms used and the requirements 
---

{{% pageinfo %}}
This is a placeholder page that shows you how to use this template site.
{{% /pageinfo %}}

Information in this section helps your user try your project themselves.

* What do your users need to do to start using your project? This could include downloading/installation instructions, including any prerequisites or system requirements.

* Introductory “Hello World” example, if appropriate. More complex tutorials should live in the Tutorials section.

Consider using the headings below for your getting started page. You can delete any that are not applicable to your project.

## Prerequisites

Are there any system requirements for using your project? What languages are supported (if any)? Do users need to already have any software or tools installed?

## Installation

Where can your user find your project code? How can they install it (binaries, installable package, build from source)? Are there multiple options/versions they can install and how should they choose the right one for them?

## Setup

Is there any initial setup users need to do after installation to try your project?

## Try it out!

Can your users test their installation, for example by running a command or deploying a Hello World example?

<p><a title="Introduction" href="#Intro" rel="alternate">Introduction</a></p>
<p><a title="Scope" href="#scope" rel="alternate">1. Scope</a></p>
<p><a title="Normative Reference" href="#normative_ref" rel="alternate">2. Normative Reference</a></p>
<p><a title="Terms and Definitions" href="#terms" rel="alternate">3. Terms and Definitions</a></p>
<p><a title="Requirements" href="#requirements" rel="alternate">4. Requirements</a></p>
<p style="padding-left: 30px;"><a title="4.1 Datasets and dataset series" href="#4.1" rel="alternate">4.1 Datasets and dataset series</a></p>
<p style="padding-left: 30px;"><a title="4.2 Services" href="#4.2" rel="alternate">4.2 Services</a></p>
<p style="padding-left: 30px;"><a title="4.3 Element details" href="#4.3" rel="alternate">4.3 Element details</a></p>
<p><a title="Extended metadata" href="#extended" rel="alternate">5. Extended metadata</a></p>
<p style="padding-left: 30px;"><a title="5.1 Additional metadata elements" href="#5.1" rel="alternate">5.1 Additional metadata elements</a></p>
<p style="padding-left: 30px;"><a title="5.2 Extension of code lists" href="#5.2" rel="alternate">5.2 Extension of code lists</a></p>

<h2>Foreword</h2>
<p>UK GEMINI was originally produced in 2004 by collaboration between the Association for Geographic Information (AGI), the (then) e-Government Unit (eGU) and the UK Data Archive. It was designed for use in the UK geospatial metadata service <em>gigateway</em> to replace the NGDF (National Geospatial Data Framework) metadata standard with metadata that is compatible with ISO 19115.</p>
<p>In 2006, a Working Group was set up under the auspices of The Association for Geographic Information (AGI) to revise UK GEMINI. It contained representatives from the following organisations:</p>
<ul>
<li>AGI</li>
<li>British Geological Survey</li>
<li>Cabinet Office</li>
<li>EDINA</li>
<li>Environment Agency</li>
<li>gigateway</li>
<li>Natural England</li>
<li>Ordnance Survey</li>
<li>UK Hydrographic Office</li>
</ul>
<p>The principles of the revision were as follows:</p>
<ol>
<li>to meet the requirements for metadata of the EU INSPIRE Directive – where an element is mandatory in the INSPIRE Implementing Rules, it is included in UK GEMINI with the same domain and occurrence, but the element name and description may be different in order to maintain compatibility with the previous version of GEMINI and to provide greater clarity;</li>
<li>to be conformant with the International Standard ISO 19115 Geographic information – Metadata, within the limits of the requirements of INSPIRE;</li>
<li>to be consistent with the GEMINI 1.0 where possible;</li>
<li>to be compatible with the e-Government Metadata Standard where possible;</li>
<li>to correct errors in GEMINI 1.0 and take into account experience of its use.</li>
</ol>
<p>Further changes were made in version 2.1 in 2010, in the light of experience of use of UK GEMINI2, and changes to the INSPIRE Technical Guidelines.</p>
<p>UK GEMINI 2.2 included further changes requested by the UK Location Programme Metadata Working Group.</p>
<p>In 2018, changes were made that had been requested by various user communities as well as the revised metadata technical guidance from INSPIRE.  This updated version is known as UK GEMINI2.3.</p>
<p>Further details of all these changes are given <a title="Major changes from v1.0" href="/component/content/article?id=1055" target="_blank" rel="alternate noopener noreferrer">here</a>.</p>
<p>A set of guidelines for metadata for geospatial datasets was originally produced in 2006. The Guidelines were in three parts:</p>
<ul>
<li>Part 1 Introduction to Metadata</li>
<li>Part 2 Creating metadata using UK GEMINI</li>
<li>Part 3 Metadata quality</li>
</ul>
<p>These Guidelines were intended for general use in the UK geographic information environment, and particularly in support of the national geospatial metadata service, <em>gigateway</em>. They were developed within the context of a national geospatial metadata service, and UK GEMINI. These Guidelines have now been updated to incorporate the changes made in the revised version of UK GEMINI, 2.3, and their content made available on the AGI website: <a title="Metadata Guidelines for Geospatial Data Resources - Part 1" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1052-metadata-guidelines-for-geospatial-data-resources-part-1">Introduction to Metadata</a>; parts of <a title="Metadata Guidelines for Geospatial Data Resources - Part 2" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1049-metadata-guidelines-for-geospatial-data-resources-part-2">Creating metadata using GEMINI</a>; material in Part 2 which was specific to particular elements has been moved to the element descriptions. </p>
<p>This Standard is maintained by the AGI Standards Committee. Any feedback on it should be sent to <span id="cloak46f25c68743112774ba4b40f7559bc9f">This email address is being protected from spambots. You need JavaScript enabled to view it.</span><script type='text/javascript'>
				document.getElementById('cloak46f25c68743112774ba4b40f7559bc9f').innerHTML = '';
				var prefix = '&#109;a' + 'i&#108;' + '&#116;o';
				var path = 'hr' + 'ef' + '=';
				var addy46f25c68743112774ba4b40f7559bc9f = 'st&#97;nd&#97;rds' + '&#64;';
				addy46f25c68743112774ba4b40f7559bc9f = addy46f25c68743112774ba4b40f7559bc9f + '&#97;g&#105;' + '&#46;' + '&#111;rg' + '&#46;' + '&#117;k';
				var addy_text46f25c68743112774ba4b40f7559bc9f = 'g&#101;m&#105;n&#105;' + '&#64;' + '&#97;g&#105;' + '&#46;' + '&#111;rg' + '&#46;' + '&#117;k';document.getElementById('cloak46f25c68743112774ba4b40f7559bc9f').innerHTML += '<a ' + path + '\'' + prefix + ':' + addy46f25c68743112774ba4b40f7559bc9f + '\'>'+addy_text46f25c68743112774ba4b40f7559bc9f+'<\/a>';
		</script></p>

<h2><a id="Intro"></a>Introduction</h2>
<p>Geospatial data is data containing a locational element relative to the Earth. Many datasets that at first sight do not appear to be geospatial nevertheless do have a geospatial component, in that they apply to a limited geographic area, for example statistics for a local authority area. Geospatial data contains spatial references which may take the form of coordinates, for example in latitude and longitude, or references to geographic names, for example street data.</p>
<p>Metadata is data about data. It provides additional information about a data resource, to enable the data resource to be better understood and used to good effect. There are a range of uses for metadata:</p>
<ul>
<li><strong>discovery</strong>: the user aims to find out what available data resources are potentially able to satisfy a specified set of requirements.</li>
<li><strong>evaluation</strong>: the user needs to go deeper in the metadata (e.g. looking at the quality information) in order to ascertain whether a candidate data resource is fit for the intended purpose.</li>
<li><strong>use</strong>: the user has selected a candidate data resource, but needs to access it and to configure a system or software to process it.</li>
</ul>
<p>There are many metadata standards in existence. These have been produced at different times by different bodies for different purposes. The main one that is relevant to geospatial datasets is:</p>
<ul>
<li><strong>ISO 19115, </strong>the International Standard which describes all aspects of geospatial metadata and provides a comprehensive set of metadata elements that are widely used as the basis for geospatial metadata services.</li>
</ul>
<p>The <a href="https://inspire.ec.europa.eu/about-inspire/563">EU INSPIRE Directive</a> [<a title="References" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1047-metadata-guidelines-for-geospatial-data-resources-part-3" target="_blank" rel="alternate noopener noreferrer">7</a>] mandates the collection of metadata for use in Europe. Implementing Rules define the requirements for metadata for discovery purposes. These are based on ISO 19115, and outlined <a title="INSPIRE metadata requirements" href="/component/content/article?id=1008" target="_blank" rel="alternate noopener noreferrer">here</a>.</p>
<p>The aim of UK GEMINI is to provide a core set of metadata elements for use in a UK geospatial metadata service, that are compatible with the INSPIRE requirements for metadata. It does not preclude organisations recording additional metadata elements for their own internal business purposes.</p>
<p>In this document the term ‘data resource’ is used, in preference to ‘dataset’. This is to allow UK GEMINI to be applied to resources in addition to datasets, such as services supplying data.</p>
<h2><a id="scope"></a> 1. Scope</h2>
<p>This Standard specifies a set of metadata elements for describing geographic information resources. These resources may be datasets, dataset series, services delivering geographic data, or any other information resource with a geospatial content. This includes datasets that relate to a limited geographic area [<a title="References" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1047-metadata-guidelines-for-geospatial-data-resources-part-3" target="_blank" rel="alternate noopener noreferrer">1</a>]. The data resources may be graphical or textual (tabular or free text), hardcopy or digital.</p>
<p>The metadata elements are intended for use in a metadata service for discovering what data resources exist. The elements include the mandatory core set defined in ISO 19115 Geographic information – Metadata, and comply with the <a href="https://inspire.ec.europa.eu/metadata/6541">INSPIRE Implementing Rules for Metadata</a> [<a title="References" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1047-metadata-guidelines-for-geospatial-data-resources-part-3" target="_blank" rel="alternate noopener noreferrer">7</a>]. In any implementation or community, it is likely that additional metadata elements will be included for other purposes, such as data management, and a method for specifying such elements is defined. The UK specific guidance is designed to ensure that the metadata records work correctly with the national catalogue, <a href="https://data.gov.uk">https://data.gov.uk</a></p>
<p>Guidance on transferring metadata records to the national catalogue are given at <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1054-operational-guide">Operational Guide</a>.</p>
<p>This Standard is applicable to data creators, data owners, data publishers and suppliers of metadata services. Although it is primarily designed for data resources held within the UK on a national basis, by following the principles and structures of ISO 19115, it is also applicable within an organisation, user community or nation.</p>
<h2><a id="normative_ref"></a> 2. Normative References</h2>
<p>The following referenced documents are indispensable to the application of this document. For dated references, only the edition cited applies. For undated references, the latest edition of the referenced document (including any amendments) applies.</p>
<p>ISO 639-2 Codes for the representation of the names of languages – Alpha-3 code</p>
<p>ISO 8601 Data elements and interchange formats – Information interchange – Representation of dates and times</p>
<p>ISO 19115:2003 Geographic information – Metadata</p>
<p>ISO 19115:2003 Cor.1:2006 Geographic information – Metadata Technical corrigendum 1</p>
<p>ISO 19119:2005 Geographic information – Services</p>
<p><a href="https://inspire.ec.europa.eu/Technical-Guidelines2/Metadata/6541">The INSPIRE Metadata Technical Guidance</a>, v2.0.1, published 2017-03-02</p>
<h2><a id="terms"></a> 3. Terms and Definitions</h2>
<p>See the <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1056-glossary">Glossary</a>.</p>
<h2><a id="requirements"></a> 4. Requirements</h2>
<h3><strong><em><a id="4.1"></a>4.1 Datasets and dataset series</em></strong></h3>
<p>UK GEMINI specifies a set of metadata elements for use when describing geographic information resources.</p>
<p>The metadata elements are listed in the <a title="GEMINI element summary" href="/component/content/article?id=1250">summary table</a>, which shows the metadata element names, their GEMINI element id (consistent with element numbers in previous versions of GEMINI), the obligation (whether their inclusion is mandatory, optional or conditional, and the number of possible occurrences of the element (whether there may be many (N), or only one (1)), and whether the element is available for both data and services.</p>
<p>Some metadata elements concern the metadata rather than the data resource itself. These are termed ‘metadata on metadata’. These elements are likely to have common values for a set of metadata records provided by an organisation.</p>
<p>For metadata to conform to this Standard, it is necessary that all mandatory elements are provided, and that all conditional elements are provided when the stated condition is met. Optional elements should be provided where they are applicable. A checklist for conformity is given <a title="here" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1040-checklist-for-conformity2" target="_blank" rel="alternate noopener noreferrer">here</a>.</p>
<h3> <strong><em><a id="4.2"></a>4.2 Services</em></strong></h3>
<p>The INSPIRE Implementing Rules apply not only to datasets and datasets series, but also to (data) services. These are external applications (e.g. web services) that deliver data to a user or process, rather than complete datasets. For such services, some additional metadata elements are required. These additional elements are Spatial data service type and Coupled resource.</p>
<p>Note that services are not described in ISO 19115, but in ISO 19119 (with an associated amendment). This results in a slight inconsistency of approach regarding the way that metadata is recorded for services. Some of the other metadata elements may not apply to particular types of service. The UK GEMINI metadata elements for services are identified in the <a title="GEMINI element summary" href="/component/content/article?id=1250">summary table</a>.</p>
<h3><strong><em><a id="4.3"></a>4.3 Element details</em></strong></h3>
<p>Details of the metadata elements are given in :</p>
<p><a title="GEMINI - Datasets and dataset series" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series" target="_blank" rel="alternate noopener noreferrer">GEMINI - Datasets and dataset series</a></p>
<p><a title="GEMINI - Services" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1063-gemini-services" target="_blank" rel="alternate noopener noreferrer">GEMINI - Services</a></p>
<p>Each element listed separately, with the following information:</p>
<p style="padding-left: 30px;">- <strong>Metadata element name</strong> – the name of the UK GEMINI element;</p>
<p style="padding-left: 30px;">- <strong>UK GEMINI id </strong>– the identifier of the UK GEMINI element; note: these do not change between versions of GEMINI; ids of deleted elements are not re-used.</p>
<p style="padding-left: 30px;">- <strong>Definition</strong> – the formal definition of the element;</p>
<p style="padding-left: 30px;">- <strong>Purpose and meaning</strong> - an explanation of what the element is, and why it is required</p>
<p style="padding-left: 30px;">- <strong>Obligation</strong> – whether the element is mandatory, optional or conditional (where the element must be supplied when stated conditions apply);</p>
<p style="padding-left: 30px;">- <strong>Occurrence</strong> – whether the element is single-valued or can have multiple values;</p>
<p style="padding-left: 30px;">- <strong>Data type</strong> – the form of the entry, whether it is a character string (CharacterString), real number (real), integer, code or other class. Where the data type is another class, it is described as a set of sub-elements. Examples are Distributor and Vertical extent;</p>
<p style="padding-left: 30px;">- <strong>Domain</strong> – the allowable set of values;</p>
<p style="padding-left: 30px;">- <strong>Guidance</strong> – advice on how to complete the entry [<a title="References" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1047-metadata-guidelines-for-geospatial-data-resources-part-3" target="_blank" rel="alternate noopener noreferrer"><span style="color: #0066cc;">2</span></a>];</p>
<p style="padding-left: 30px;">- <strong>Comment</strong> – other other information of relevance;</p>
<p style="padding-left: 30px;">- <strong>Examples</strong></p>
<p style="padding-left: 30px;">-<strong> Corresponding element in </strong>INSPIRE Metadata, ISO 19115:2003, ISO 19139:2007</p>
<p style="padding-left: 30px;">- <strong>Change history</strong> – how the element has changed from v1.0 of the Standard;</p>
<p style="padding-left: 30px;">-<strong> Encoding guidelines &amp; example</strong> - how to create an XML instance of this element</p>
<p style="padding-left: 30px;">- <strong>Errors observed</strong> - observations on errors noted with each element</p>
<h2><a id="extended"></a> 5. Extended metadata</h2>
<h3><strong><em><a id="5.1"></a>5.1 Additional metadata elements</em></strong></h3>
<p>In many organisations, there is a need to record additional items of metadata to meet specific local requirements. This may be to incorporate particular characteristics of the data resources, or for particular applications. Additional metadata elements may be included in a metadata implementation. These elements should be taken from ISO 19115 [<a title="References" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1047-metadata-guidelines-for-geospatial-data-resources-part-3" target="_blank" rel="alternate noopener noreferrer">18</a>], which includes a comprehensive collection of metadata elements for geographic information, and also allows for further extensions.</p>
<h3><strong><em><a id="5.2"></a>5.2 Extension of code lists</em></strong></h3>
<p>Several metadata elements specified in UK GEMINI use enumerated code lists. These are pre-defined sets of values identified by codes. They are useful to standardise the entries to aid searches of metadata for specified values. The code lists included in UK GEMINI are taken from ISO 19115. In some cases, the explanations of the values have been modified to make them more appropriate to the UK context.</p>
<p>Some of these code lists will require extension. Additional codes may be created as follows:</p>
<ol>
<li>identify the new value, which should be distinct from existing values;</li>
<li>choose a name that encapsulates the essential concept;</li>
<li>provide a definition that is understandable and concise;</li>
<li>chose a new code that has not been used before for this element;</li>
<li>document the new codes, and disseminate them to users.</li>
</ol>
<p>Such code extensions may be either specific to a metadata implementation in an organisation or sector, or for general usage. In the latter case, proposed new codes should be submitted to <span id="cloakbe999b9ac8b6b788bcf2633efe8e499a">This email address is being protected from spambots. You need JavaScript enabled to view it.</span><script type='text/javascript'>
				document.getElementById('cloakbe999b9ac8b6b788bcf2633efe8e499a').innerHTML = '';
				var prefix = '&#109;a' + 'i&#108;' + '&#116;o';
				var path = 'hr' + 'ef' + '=';
				var addybe999b9ac8b6b788bcf2633efe8e499a = 'g&#101;m&#105;n&#105;' + '&#64;';
				addybe999b9ac8b6b788bcf2633efe8e499a = addybe999b9ac8b6b788bcf2633efe8e499a + '&#97;g&#105;' + '&#46;' + '&#111;rg' + '&#46;' + '&#117;k';
				var addy_textbe999b9ac8b6b788bcf2633efe8e499a = 'g&#101;m&#105;n&#105;' + '&#64;' + '&#97;g&#105;' + '&#46;' + '&#111;rg' + '&#46;' + '&#117;k';document.getElementById('cloakbe999b9ac8b6b788bcf2633efe8e499a').innerHTML += '<a ' + path + '\'' + prefix + ':' + addybe999b9ac8b6b788bcf2633efe8e499a + '\'>'+addy_textbe999b9ac8b6b788bcf2633efe8e499a+'<\/a>';
		</script> for inclusion in the next version of UK GEMINI. It is expected that future editions of UK GEMINI will incorporate such modified code lists.</p>
<p><strong>Note that any new code values cannot be used in a national metadata service until incorporated in the Standard, nor will they be valid for the purposes of INSPIRE.</strong></p>
<p><em>Last updated: May 2018</em></p>
<p><a href="http://creativecommons.org/licenses/by/4.0/" rel="license"> <img style="border-width: 0;" src="https://i.creativecommons.org/l/by/4.0/88x31.png" alt="Creative Commons Licence" /> </a> <br />This work is licensed under a <a href="http://creativecommons.org/licenses/by/4.0/" rel="license">Creative Commons Attribution 4.0 International License</a></p> 	

