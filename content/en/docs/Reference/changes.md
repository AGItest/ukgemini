---
title: "Changes"
linkTitle: "Changes"
date: 2020-04-07
description: >
  Changes
---

{{% pageinfo %}}
Changes
{{% /pageinfo %}}



<div class="row content">
<div class="content col-lg-9 col-md-9 col-sm-12">
<div class="item-page">

<div class="page-header">


<h1>UK GEMINI changes log</h1>

</div>

<p>Return to <a title="GEMINI 2.3 home page" href="/gemini/40-gemini/1037-uk-gemini-standard-and-inspire-implementing-rules">GEMINI 2.3 home page</a></p>
<h2>UK GEMINI 2.3</h2>
<p>In UK GEMINI 2.3, as well as restructuring the content, the following changes have been made:</p>
<ul>
<li>There is one new element which is mandatory for datasets and series:
<ul>
<li>Spatial representation type (Note: this element was in GEMINI v1, but was removed from GEMINI v2)</li>
</ul>
</li>
<li>The XML encodings for Use constraints &amp; Limitations on public access have changed</li>
<li>There are several additional mandatory "metadata on metadata" elements, which were already required to encode the record:
<ul>
<li>File identifier</li>
<li>Hierarchy level name</li>
<li>Quality scope</li>
</ul>
</li>
<li>There is one additional optional "metadata on metadata" elements: 
<ul>
<li>Parent identifier</li>
</ul>
</li>
<li>There are two additional conditional elements:
<ul>
<li>Character encoding</li>
<li>Data quality</li>
</ul>
</li>
<li>Four elements have been made mandatory
<ul>
<li>Conformity</li>
<li>Dataset language</li>
<li>Data format</li>
<li>Spatial reference system</li>
</ul>
</li>
<li>Unique resource identifier renamed to Resource identifier</li>
<li>The element Maintenance information has replaced Frequency of update</li>
<li>Vertical extent information may now have multiple occurrence.</li>
<li>There are changes to the guidance for a lot elements, bringing in guidance relating to INSPIRE and data.gov.uk:
<ul>
<li>Title</li>
<li>Alternative title</li>
<li>Abstract</li>
<li>Keyword</li>
<li>Temporal extent</li>
<li>Vertical extent information</li>
<li>Spatial reference system</li>
<li>Spatial resolution</li>
<li>Resource locator</li>
<li>Data format</li>
<li>Responsible organisation</li>
<li>Limitations on public access</li>
<li>Additional information source</li>
<li>Metadata language</li>
<li>Resource identifier</li>
<li>Resource type</li>
<li>Conformity</li>
<li>Coupled resource</li>
</ul>
</li>
<li>Dates (in both Temporal extent, and Dataset reference date) can no longer just be the century.</li>
</ul>
<h3>Editorial changes since the launch of GEMINI 2.3</h3>
<h4>April 2020</h4>
<p>Changed the <a href="/40-gemini/1048-uk-gemini-encoding-guidance">XML guidance</a> and examples to cope with the disappearance of the XML resources from <a href="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/" rel="nofollow">http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/</a>. The authoritative location is now on <a href="https://schemas.isotc211.org/">https://schemas.isotc211.org/</a>. Note: I didn't mark this as a revision to each element.</p>
<p>Fixed example file on <a href="https://github.com/AGIGemini/Schematron">GitHub</a>, and changed links to point there.</p>
<p><a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series#53">Maintenance information</a>:</p>
<ul>
<li>corrected maximum multiplicity;</li>
<li>expanded the description of the domain</li>
</ul>
<p><a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series#25">Limitations on public access</a>:</p>
<ul>
<li>clarified guidance on how to express more than one limitation, and added an example</li>
</ul>
<p><a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series#54">Metadata standard name</a>:</p>
<ul>
<li>minor change to guidance and example</li>
</ul>
<p><a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series#41">Conformity</a>:</p>
<ul>
<li>correct the description of what has changed in cases where the resource has not been tested against an INSPIRE specification</li>
<li>add note that it is mandatory for at least one conformity statement to relate to an INSPIRE document</li>
</ul>
<h4>January 2020</h4>
<p>Added guidance for two additional elements: <a href="/1062-gemini-datasets-and-data-series#54">Metadata standard name</a>, and <a href="/1062-gemini-datasets-and-data-series#54">Metadata standard version</a></p>
<p><a href="/1062-gemini-datasets-and-data-series#6">Keyword</a> for INSPIRE theme: fixed the URL in the encoding example</p>
<p><span style="font-weight: 400;"><a href="/1062-gemini-datasets-and-data-series#47">Hierarchy level name</a>: changed guidance and example to match INSPIRE. Note: this means the value is fixed depending on the value chosen for Resource type (Hierarchy level).<br /></span></p>
<p><span style="font-weight: 400;"><a href="/1062-gemini-datasets-and-data-series#41">Conformity</a> to an INSPIRE specification: minor fix to guidance, and added a new 'known error'</span></p>
<p><span style="font-weight: 400;"><a href="/1062-gemini-datasets-and-data-series#25">Limitations on public access</a>: improve guidance by listing the allowable INSPIRE reasons, with a hyperlink to the register</span></p>
<h4>March 2019</h4>
<p>Change to <a href="/40-gemini/1048-uk-gemini-encoding-guidance#2.1,">https://www.agi.org.uk/1048-uk-gemini-encoding-guidance#2.1,</a> to describe a wider choice of relevant XML Schema Definition Files (XSDs) that can be used to validate GEMINI instances.</p>
<p><a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series#8"><em>Dataset</em> reference date</a>: removed mention of the maximum occurence for service records, when viewing this element for dataset records.</p>
<p>Corrected the INSPIRE "corresponding element" entry for <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series#41">Conformity</a>, <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series#4">Abstract</a>, <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series#5">Topic category</a>, <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series#6">Keyword</a>, <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series#17">Spatial reference system</a>, <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series#21">Data format</a>, <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series#45">File Identifier</a>, <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series#47">Hierarchy level name</a>, and <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series#48">Quality scope</a>.</p>
<p>Corrected the "corresponding element" entries for service elements to reference ISO 19119 for <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1063-gemini-services#15">Extent</a>, <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1063-gemini-services#16">Vertical extent information</a>, <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1063-gemini-services#37">Spatial data service type</a>, and <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1063-gemini-services#38">Coupled resource</a>.</p>
<p>Corrected the ISO 19139 "corresponding element" entries for service elements <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1063-gemini-services#15">Extent</a>, <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1063-gemini-services#16">Vertical extent information</a>, and <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1063-gemini-services#18">Spatial resolution</a></p>
<p>Corrected the ISO 19139 "corresponding element" entries for <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series#1">Title</a>, <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series#2">Alternative title</a>, and <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series#4">Abstract</a>.</p>
<p><em>Note: these are all minor corrections of the way the element is referenced, rather than substantive changes to which element we consider equivalent. The largest impact is to note that INSPIRE only allows one Quality scope element - i.e. the metadata has to describe the whole dataset.</em></p>
<h4>January 2019</h4>
<p>New <a href="/about/resources/category/125-schematron">Schematron package</a>, in which the only change is to the "Technical Documentation" file (to version 1.7.1), clarifying in one paragraph that the Schematron file itself changed from 2.2 to 2.3, but the way one should use it didn't.</p>
<h4>October 2018</h4>
<p><strong><a href="/gemini/40-gemini/1062-gemini-datasets-and-data-series#27">Additional information</a> (source) and <a href="/gemini/40-gemini/1062-gemini-datasets-and-data-series#19">Resource locator</a></strong></p>
<p>Clarified that, in line with the underlying ISO standards, Resource locator is for links to access the resource, or obtain more information about accessing the resource. Links to further information about the resource itself, e.g. a user guide, should go in Additional information</p>
<p>Note: this is a change from the earlier UK Location guidance, which wanted all URLs (except licensing) in Resource locator.</p>
<p>The actual changes are in the 'purpose and meaning', guidance, and examples of both elements. Also noted that there is an INSPIRE element corresponding to Additional information, although it is only mentioned in an Annex of the Technical Guidance. We have also changed the name from 'Additional information source' to 'Additional information', because it is quite possible to provide the information in line, rather than by citation or link.</p>
<p>Note: additional information is not available for services.</p>
<p><strong><a href="/gemini/40-gemini/1062-gemini-datasets-and-data-series#36">Resource identifier</a></strong></p>
<p>Fixed two typos.</p>
<p>We have also turned internal cross references from one element to another, into hyperlinks.</p>
<h4>September 2018</h4>
<p><strong><a href="/gemini/40-gemini/1062-gemini-datasets-and-data-series#3">Dataset language</a> and <a href="/gemini/40-gemini/1062-gemini-datasets-and-data-series#33">metadata</a><a href="/gemini/40-gemini/1062-gemini-datasets-and-data-series#33"> language</a></strong></p>
<p>Corrected the name of the Irish language.</p>
<p><strong><a href="/gemini/40-gemini/1062-gemini-datasets-and-data-series#17">Spatial reference system</a> and <a href="/gemini/40-gemini/1062-gemini-datasets-and-data-series#48">Quality scope</a><br /></strong></p>
<p>Corrected that there is an equivalent INSPIRE requirement, although not a 'named' metadata element.</p>
<p><strong><a href="/gemini/40-gemini/1062-gemini-datasets-and-data-series#25">Limitations on public access</a></strong></p>
<p>Corrected the equivalent ISO 19115 &amp; 19139 elements</p>
<p><strong><a href="/gemini/40-gemini/1062-gemini-datasets-and-data-series#26">Use constraints</a></strong></p>
<p>Corrected encoding rules &amp; examples, from "gmd:LegalConstraints" (which doesn't exist) to "gmd:MD_LegalConstraints".</p>
<p>Corrected the service Example One.</p>
<p>Corrected the equivalent ISO 19115 &amp; 19139 elements.</p>
<h4>August 2018</h4>
<p><strong>Description of validation</strong></p>
<p>Fixed the description in section 1.5 of the <a title="Common Metadata Errors" href="/gemini/40-gemini/1053-common-metadata-errors-uk-location-discovery-metadata-service">Common Metadata Errors article</a>, which only described the GEMINI 2.2 / UK Location / data.gov.uk validation.</p>
<p><strong>Parent identifier</strong></p>
<p>Corrected to be slightly different guidance for service metadata.</p>
<p><strong>Spatial data service type</strong></p>
<p>Given that it is only relevant to service metadata, corrected the obligation (in that context) to mandatory</p>
<p><strong>Minimum length of Abstract</strong></p>
<p>Add mention in the guidance that the Schematron will complain if it's &lt;100 characters</p>
<p><strong>INSPIRE Default CRSs</strong></p>
<p>Fixed the reference - the list of INSPIRE CRSs is in Annex D.4 of the Metadata TG, not the Regulations</p>
<h4>July 2018</h4>
<p><strong><a title="UK GEMINI Encoding Guidance" href="/40-gemini/1048-uk-gemini-encoding-guidance">UK GEMINI Encoding Guidance</a></strong></p>
<p style="padding-left: 30px;"><strong>first line</strong>: remove misleading phrase "using XSD schemas"<strong><br /></strong></p>
<p style="padding-left: 30px;"><strong>section 2.2.14</strong>: minor clarifications, and improved the placement of figure captions.</p>
<p><strong>Change log </strong>(this article): reordered to bring newest to top; added this section (editorial changes)</p>
<p><a title="GEMINI 2.3 home page" href="/gemini/40-gemini/1037-uk-gemini-standard-and-inspire-implementing-rules">"<strong>Home page</strong>"</a>: fixed link to encoding guidance</p>
<p><strong><a title="Guidelines - part 1" href="/gemini/40-gemini/1052-metadata-guidelines-for-geospatial-data-resources-part-1">Guidelines - part 1 Introduction to Metadata</a></strong>: clarifications &amp; general update</p>
<p><strong>All pages</strong>: introduce a link back to the GEMINI 2.3 "home page".</p>
<p><strong><a title="Guidance for element 3 Dataset Language" href="/gemini/40-gemini/1062-gemini-datasets-and-data-series#3">Guidance for element 3 Dataset language</a></strong>: fix typo in anchor text for ISO 639 link</p>
<p><strong><a title="Guidance for element 44 Bounding box" href="/gemini/40-gemini/1062-gemini-datasets-and-data-series#44">Guidance for element 44 Bounding box</a></strong>: fix typos in two domain sub element names</p>
<h2>UK GEMINI 2.2</h2>
<p>In UK GEMINI 2.2, the following changes were made:</p>
<ul>
<li>The elements Frequency of update and Spatial reference system become optional;</li>
<li>For the elements Temporal extent, Spatial reference system, Spatial resolution, Unique resource identifier, Equivalent scale, multiple occurrences are allowed;</li>
<li>The elements West bounding longitude, East bounding longitude, North bounding latitude, South bounding latitude are merged to form Bounding Box for which multiple occurrences are allowed.</li>
</ul>
<h2>UK GEMINI 2.1</h2>
<p> Resource language, Metadata language:</p>
<ul>
<li>The code for the Ulster Scots language was changed to "sco".</li>
</ul>
<p><strong> </strong>Dataset reference date:</p>
<ul>
<li>Occurrence changed to multiple</li>
<li>Data type changed to a class comprising the elements:
<ul>
<li>date</li>
<li>date type (publication/revision/creation)</li>
</ul>
</li>
</ul>
<p>Extent:</p>
<ul>
<li>Deletion of "by country or subdivision of country" from definition, with data type changed to character string and domain to an identifier.</li>
</ul>
<p>Data format:</p>
<ul>
<li>Data type changed to a class comprising the elements:
<ul>
<li>Name of format</li>
<li>Version of the format (date, number etc.)</li>
</ul>
</li>
</ul>
<p>Limitations on public access:</p>
<ul>
<li>Equivalent ISO 19115 element changed from accessConstraint to otherConstraints, making domain free text.</li>
</ul>
<p>Unique resource identifier:</p>
<ul>
<li>Data type changed to class, comprising the elements:</li>
<ul>
<li>code</li>
<li>codespace</li>
</ul>
</ul>
<p>Resource type:</p>
<ul>
<li>Domain values changed dataset, series, service to match INSPIRE.</li>
</ul>
<p>Conformity, Specification:</p>
<ul>
<li>Combined into a new class Conformity, comprising the elements:
<ul>
<li>Specification</li>
<li>Degree</li>
<li>Explanation</li>
</ul>
</li>
</ul>
<p>Keyword, Originating controlled vocabulary:</p>
<ul>
<li>Combined into new class Keyword, comprising the elements
<ul>
<li>keyword value</li>
<li>originating controlled vocabulary.</li>
</ul>
</li>
</ul>
<p>An optional element, Equivalent scale has been added.</p>
<h2>UK GEMINI 2.0</h2>
<div>The following elements were deleted:
<ul>
<li>Presentation type</li>
<li>Supply media</li>
<li>Spatial representation type</li>
<li>Browse graphic</li>
<li>Metadata standard name</li>
<li>Metadata standard version</li>
</ul>
None of these were mandatory, and they are all part of the larger ISO 19115 set. </div>
<div> </div>
<div>The following element names were changed:
<ul>
<li>Subject to Keyword</li>
<li>Online resource to Resource locator</li>
<li>Date to Temporal extent</li>
<li>West bounding coordinate to West bounding longitude</li>
<li>East bounding coordinate to East bounding longitude</li>
<li>North bounding coordinate to North bounding latitude</li>
<li>South bounding coordinate to South bounding latitude</li>
<li>Access constraints to Limitations on public access</li>
<li>Date of update of data to Metadata date</li>
<li>Distributor and Originator (merged) to Responsible organisation</li>
</ul>
</div>
<div>The following elements were added to meet the requirements of INSPIRE:</div>
<ul>
<li>Unique resource identifier</li>
<li>Resource type</li>
<li>Conformity</li>
<li>Equivalent scale</li>
<li>Metadata language</li>
<li>Metadata point of contact</li>
<li>Spatial data service type (for services)</li>
<li>Coupled resource (for services)</li>
</ul>
<div>Other minor changes are identified in the element tables.</div>
<p><em>Last updated: August 2018</em></p>
<p><a href="http://creativecommons.org/licenses/by/4.0/" rel="license"> <img style="border-width: 0;" src="https://i.creativecommons.org/l/by/4.0/88x31.png" alt="Creative Commons Licence" /> </a> <br />This work is licensed under a <a href="http://creativecommons.org/licenses/by/4.0/" rel="license">Creative Commons Attribution 4.0 International License</a></p> 	
	
