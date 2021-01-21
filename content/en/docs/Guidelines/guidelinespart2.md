---
title: "Metadata Guidelines for Geospatial Data Resources - Part 2<"
linkTitle: "Part 2"
date: 2017-01-05
description: General Metadata Guidelines for Geospatial Data Resources - Part 2<
---

{{% pageinfo %}}
Metadata Guidelines for Geospatial Data Resources - Part 2<
{{% /pageinfo %}}

		
<h3>Creating metadata using UK GEMINI (v2.3) May 2018 - <em>being revised</em></h3>
<p>Return to <a title="GEMINI 2.3 home page" href="/gemini/40-gemini/1037-uk-gemini-standard-and-inspire-implementing-rules">GEMINI 2.3 home page</a></p>
<p><a title="Introduction" href="#Intro" rel="alternate">1. Introduction</a></p>
<p><a title="GEMINI2" href="#gemini" rel="alternate">2. GEMINI2</a></p>
<p style="padding-left: 30px;"><a title="2.1 Metadata elements" href="#2.1" rel="alternate">2.1 Metadata elements</a></p>
<p style="padding-left: 30px;"><a title="2.2 Additional metadata elements" href="#2.2" rel="alternate">2.2 Additional metadata elements</a></p>
<p style="padding-left: 30px;"><a title="2.3 Extension code lists" href="#2.3" rel="alternate">2.3 Extension code lists</a></p>
<p><a title="Possible metadata errors" href="#errors" rel="alternate">3. Possible metadata errors</a></p>
<p style="padding-left: 30px;"><a title="3.1 Impact of metadata errors" href="#3.1" rel="alternate">3.1 Impact of metadata errors</a></p>
<p style="padding-left: 30px;"><a title="3.2 Effect on searches" href="#3.2" rel="alternate">3.2 Effect on searches</a></p>
<p style="padding-left: 30px;"><a title="3.3 Prevention and correction of errors" href="#3.3" rel="alternate">3.3 Prevention and correction of errors</a></p>
<p style="padding-left: 30px;"><a title="3.4 Common errors" href="#3.4" rel="alternate">3.4 Common errors</a></p>
<p><a title="Guidance for individual metadata elements" href="#guidance" rel="alternate">4. Guidance for individual metadata elements</a></p>
<p style="padding-left: 30px;"> </p>
<h2>Preface</h2>
<p>This is the second part of a set of guidelines for metadata for geospatial data resources. These metadata guidelines are primarily concerned with geospatial data (i.e. that which references data to a location on the surface of the Earth), and which has a limited geographic extent (i.e. is restricted to a defined territory). The guidelines have been developed within the context of a UK Location Discovery metadata service meeting the requirements of the EU INSPIRE Directive and the UK GEMINI2 metadata standard. However, they are sufficiently broadly based to be applicable in a wider context of geospatial metadata creation and management.</p>
<p>The Guidelines are aimed at data managers and creators of metadata, providers of metadata services and general data users. They include guidance on quality management such that they could be used in the context of a national metadata service.</p>
<p><a title="Metadata Guidelines for Geospatial Data Resources - Part 1" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1052-metadata-guidelines-for-geospatial-data-resources-part-1" target="_blank" rel="alternate noopener noreferrer">Part 1 of the Guidelines </a>covers the basics of metadata and provides an introduction to the other two parts. It includes a glossary of terms and set of references. Part 3 [<a title="References" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1047-metadata-guidelines-for-geospatial-data-resources-part-3" target="_blank" rel="alternate noopener noreferrer">3</a>] deals with metadata quality and covers quality evaluation and quality management of metadata including guidance on establishing acceptable quality levels. This Part of the Guidelines provides a set of detailed guidelines for UK GEMINI2 metadata elements. It has been revised to correspond to version 2.3 of UK GEMINI.</p>
<p>Any comments on these guidelines or on the UK GEMINI2 metadata standard should be sent to <span id="cloak471d5cfa42bb10d384196fd525edb5c0">This email address is being protected from spambots. You need JavaScript enabled to view it.</span><script type='text/javascript'>
				document.getElementById('cloak471d5cfa42bb10d384196fd525edb5c0').innerHTML = '';
				var prefix = '&#109;a' + 'i&#108;' + '&#116;o';
				var path = 'hr' + 'ef' + '=';
				var addy471d5cfa42bb10d384196fd525edb5c0 = 'g&#101;m&#105;n&#105;' + '&#64;';
				addy471d5cfa42bb10d384196fd525edb5c0 = addy471d5cfa42bb10d384196fd525edb5c0 + '&#97;g&#105;' + '&#46;' + '&#111;rg' + '&#46;' + '&#117;k';
				var addy_text471d5cfa42bb10d384196fd525edb5c0 = 'g&#101;m&#105;n&#105;' + '&#64;' + '&#97;g&#105;' + '&#46;' + '&#111;rg' + '&#46;' + '&#117;k';document.getElementById('cloak471d5cfa42bb10d384196fd525edb5c0').innerHTML += '<a ' + path + '\'' + prefix + ':' + addy471d5cfa42bb10d384196fd525edb5c0 + '\'>'+addy_text471d5cfa42bb10d384196fd525edb5c0+'<\/a>';
		</script>.</p>
<h2><a id="intro"></a> 1. Introduction</h2>
<p>UK GEMINI2 defines a core set of metadata elements for discovery of data resources and other essential purposes. It provides details of what metadata should be collected for geospatial data resources and is designed for use in a geospatial discovery metadata service. The data resources may be datasets, dataset series, services delivering geographic data, or any other information resource with a geospatial content. This includes datasets that relate to a limited geographic area. The data resources may be graphical or textual (tabular or free text), hardcopy or digital.</p>
<p>This part of the <em>Metadata Guidelines for Geospatial Data Resources</em> provides detailed guidance for the application of UK GEMINI2. It is aimed at those creating metadata conforming to UK GEMINI2. This expands on existing guidance given in the UK GEMINI2 specification[<a title="References" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1047-metadata-guidelines-for-geospatial-data-resources-part-3" target="_blank" rel="alternate noopener noreferrer">4</a>]. It also describes possible errors that might occur in such metadata and suggests actions to guard against them. It explains how to expand the metadata elements in addition to those in UK GEMINI2 if required, and how to extend code lists of allowable values.</p>
<p>This Part should be read in conjunction with the other parts of these guidelines.</p>
<h2><a id="gemini"></a> 2. GEMINI2</h2>
<h3><strong><em><a id="2.1"></a>2.1 Metadata elements</em></strong></h3>
<p>UK GEMINI2 specifies a set of metadata elements for describing geospatial data resources. These resources may be a dataset, data set series (collection of datasets with a common specification) or data service. The type of resource is identified in the element Resource Type (39). The metadata elements are summarised in <a title="GEMINI element summary" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1250-element-summary">element summary</a>.</p>
<p>Detailed guidance on how to create each of these elements can be found here:</p>
<p><a title="GEMINI - Datasets and data series" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1027-citizens-as-sensors-a-solution-to-pollution" rel="alternate">GEMINI - Datasets and data series</a></p>
<p><a title="GEMINI - Services" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1028-new-agi-council-members-for-2017" rel="alternate">GEMINI - Services</a></p>
<h3><strong><em><a id="2.2"></a>2.2 Additional metadata elements</em></strong></h3>
<p>In many organisations, there is a need to record additional items of metadata to meet specific local requirements. This may be to incorporate particular characteristics of the data resources, or for particular applications. Additional metadata elements may be included in a metadata implementation. These elements should be taken from ISO 19115 <em>Geographic information - Metadata </em>[<a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1047-metadata-guidelines-for-geospatial-data-resources-part-3">18</a>], which includes a comprehensive collection of metadata elements for geographic information. An example would be Dataset character set and Metadata character set where non-standard characters are used.</p>
<h3><strong><em><a id="2.3"></a>2.3 Extension of code lists</em></strong></h3>
<p>Several of the metadata elements specified in UK GEMINI2 use enumerated code lists. These are pre-defined sets of values identified by codes. They are useful to standardise the entries to aid searches of metadata for specified values. The code lists included in UK GEMINI2 are taken from ISO 19115. In some cases, the explanations of the values have been modified to make them more appropriate to the UK context.</p>
<p>Some of these code lists will require extension. Additional codes may be created as follows:</p>
<ol>
<li>Identify the new value, which should be distinct from existing values;</li>
<li>Choose a name that encapsulates the essential concept;</li>
<li>Provide a definition that is understandable and concise;</li>
<li>Choose a new code that has not been used before for this element;</li>
<li>Document the new codes, and disseminate them to users.</li>
</ol>
<p>Such code extensions may be either specific to a metadata implementation in an organisation or sector, or for general usage. In the latter case, proposed new codes should be submitted (to <span id="cloakc7aa8b6999e1afdf768bfff301fd10ae">This email address is being protected from spambots. You need JavaScript enabled to view it.</span><script type='text/javascript'>
				document.getElementById('cloakc7aa8b6999e1afdf768bfff301fd10ae').innerHTML = '';
				var prefix = '&#109;a' + 'i&#108;' + '&#116;o';
				var path = 'hr' + 'ef' + '=';
				var addyc7aa8b6999e1afdf768bfff301fd10ae = 'st&#97;nd&#97;rds' + '&#64;';
				addyc7aa8b6999e1afdf768bfff301fd10ae = addyc7aa8b6999e1afdf768bfff301fd10ae + '&#97;g&#105;' + '&#46;' + '&#111;rg';
				var addy_textc7aa8b6999e1afdf768bfff301fd10ae = 'g&#101;m&#105;n&#105;' + '&#64;' + '&#97;g&#105;' + '&#46;' + '&#111;rg' + '&#46;' + '&#117;k';document.getElementById('cloakc7aa8b6999e1afdf768bfff301fd10ae').innerHTML += '<a ' + path + '\'' + prefix + ':' + addyc7aa8b6999e1afdf768bfff301fd10ae + '\'>'+addy_textc7aa8b6999e1afdf768bfff301fd10ae+'<\/a>';
		</script>) for inclusion in the next version of UK GEMINI2. It is expected that future editions of UK GEMINI will incorporate such modified code lists.</p>
<p><strong>Note that any new code values cannot be used in a national metadata service until incorporated in the Standard, neither will they be valid for the purposes of INSPIRE.</strong></p>
<h2><a id="errors"></a> 3. Possible metadata errors</h2>
<h3><strong><em><a id="3.1"></a>3.1 Impact of metadata errors</em></strong></h3>
<p>Errors having the greatest impact are likely to be those that affect searches based on:</p>
<ul>
<li><strong>Where?</strong> - geographical extent expressed in latitude and longitude or some named standard area (e.g. administrative area, postcode, country);</li>
<li><strong>What?</strong> - theme, subject or topic;</li>
<li><strong>When?</strong> - date when data resource was current.</li>
</ul>
<p>Errors in the metadata elements used by these searches will result in over- or under-selection of data resources and will degrade the quality of the discovery service that is providing the search facility. Inconsistencies in the capture or updating of metadata, such as the categorisation of data subject or topic, will further erode the quality of the discovery service.</p>
<h3><strong><em><a id="3.2"></a>3.2 Effect on searches</em></strong></h3>
<p>Having discovered a number of candidate data resources, the discovery service user then assesses the likelihood that any of these meet their requirements. They will need the information in the other metadata elements such as abstract, lineage, data format, and constraints to make their assessment. Inaccuracies, inconsistencies, or incompleteness will detract from the quality of the discovery service.</p>
<p>Information also needs to be topical or up-to-date. Discovery services are bedevilled by metadata containing information current at the inception of the service but never maintained since. The service user needs to have reliable information about where they can find out more about the data resource and how they can obtain that resource. It is not uncommon for this to be out-of-date or have incorrect URLs or contact details.</p>
<h3><strong><em><a id="3.3"></a>3.3 Prevention and correction of errors</em></strong></h3>
<p>Prevention and correction of these errors is usually a combination of:</p>
<ul>
<li>Understanding the nature of the errors;</li>
<li>Clear guidance on avoidance of errors at time of entry – metadata capture tools may help here in validating entries;</li>
<li>Staff trained in metadata capture who understand the nature of the data resources being documented;</li>
<li>Independent quality control with specified quality evaluation procedures, acceptable quality levels and procedures for dealing with metadata that fails;</li>
<li>Periodic reviews of existing metadata to check that all information is current;</li>
<li>Procedures for dealing with errors reported by service providers or users;</li>
<li>Overall quality assurance process which reviews procedures in the light of experience and aims to improve overall metadata quality.</li>
</ul>
<p>Further guidance on how to prevent and correct errors is given in Part 3 [<a title="References" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1047-metadata-guidelines-for-geospatial-data-resources-part-3" target="_blank" rel="alternate noopener noreferrer">3</a>] of these Guidelines.</p>
<h3><strong><em><a id="3.4"></a>3.4 Common errors</em></strong></h3>
<p>Some common errors that lead to inconsistent results when searching across metadatasets are:</p>
<ul>
<li>Documentation is too general;</li>
<li>Extent is over-generalised;</li>
<li>Subjects and topic categories are under-reported;</li>
<li>Incorrect or inconsistent date entries;</li>
<li>Different names are used for the same item in different places;</li>
<li>Missing values;</li>
<li>Data is not current.</li>
</ul>
<p>The nature and impact of these types of error are described in more detail below, together with suggested ways in which these errors can be prevented or corrected.</p>
<table border="1" width="919">
<thead>
<tr>
<td width="163">
<p><strong>Type of error</strong></p>
</td>
<td width="252">
<p><strong>Description and impact</strong></p>
</td>
<td width="252">
<p><strong>Examples of errors</strong></p>
</td>
<td width="252">
<p><strong>Prevention or correction</strong></p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td width="163">
<p>Documentation too general</p>
</td>
<td width="252">
<p>There are no absolute rules about how data resources should be “chunked” and individually documented. A metadata record can therefore refer to a dataset covering a single topic relating to a small area or major dataset series covering all or parts of UK containing many topics. This can lead to inconsistent search results with either over- or under-selection of data resources.  </p>
</td>
<td width="252">
<ol>
<li>Topographic mapping covering whole of GB at different scales to different specifications documented using one metadata record.</li>
<li>Reports produced by an organisation relating to a variety of locations and dates documented using one metadata record.</li>
</ol>
</td>
<td width="252">
<p>Have clear guidance on the “chunking” of data resources for individual documentation[See <a title="Part 1 of these Guidelines" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1052-metadata-guidelines-for-geospatial-data-resources-part-1" target="_blank" rel="alternate noopener noreferrer">Part 1 of these Guidelines</a>] based on:</p>
<ol style="list-style-type: lower-roman;">
<li>how the data is used (stand-alone or as part of wider set);  </li>
<li>continuity and extent of coverage;</li>
<li>date of capture or maintenance;</li>
<li>topics or subjects covered, and</li>
<li>uniformity of specification within data resource.</li>
</ol>
<p>Introduce checks to ensure consistency of approach across all metadata.</p>
</td>
</tr>
<tr>
<td width="163">
<p>Extent over-generalised</p>
</td>
<td width="252">
<p>This particularly applies when extent is described in terms of standard geographical areas such as postcode districts, counties, or countries. Inconsistencies in relating data resource coverage to these areas and the use of different extent names to refer to the same coverage results in either over- or under-selection of data resources.</p>
</td>
<td width="252">
<ol>
<li>Coverage given as UK or GB when restricted to England.</li>
<li>Coverage of UK referred to as GB.</li>
<li>Coverage given as England when restricted to Hampshire only.</li>
</ol>
</td>
<td width="252">
<p>Have clear rules and user guidance on the relating of named extents to the coverage of data resources and guidelines on the types of extents to be used. Where named extents form part of a nesting hierarchy (e.g. administrative areas) then any guidance should cover the possible need for inclusion of levels in the hierarchy.</p>
<p>Introduce checks to ensure consistency of approach across all metadata.</p>
</td>
</tr>
<tr>
<td width="163">
<p>Subjects and topic categories under-reported</p>
</td>
<td width="252">
<p>This particularly applies where there are enumerated lists of topics. Inconsistency in the inclusion of individual topics can lead to over- or under-selection of data resources.</p>
</td>
<td width="252">
<p>Metadata for topographic map series does not include boundaries, elevation, inland waters, structure, and transportation as topics.</p>

</td>
<td width="252">
<p>Use guidance on the recording of topics or themes to promote consistency.</p>
<p>Use closed lists wherever possible and discourage the use of free text.</p>
<p>Introduce checks to ensure consistency of approach across all metadata.</p>
</td>
</tr>
<tr>
<td width="163">
<p>Incorrect or inconsistent date entries</p>
</td>
<td width="252">
<p>There is often confusion between the date that the data was current, the date when the data was captured or last updated and the date when the data resource was released, published or made available.</p>
<p>There can be further inconsistencies between the frequency of update and the recorded currency of the data resource. This can lead to   false returns for searches based on dates.</p>
</td>
<td width="252">
<ol>
<li>Date of capture of data resource later than date of publication.</li>
<li>Update reported as continuous but date of last update reported as 10 years ago.</li>
</ol>
</td>
<td width="252">
<p>Use guidance on the recording of different dates to promote consistency.</p>
<p>Introduce checks, preferably by software, to ensure that the ordering of dates is consistent.</p>
</td>
</tr>
<tr>
<td width="163">
<p>Same item, different name</p>
</td>
<td width="252">
<p>This is particularly relevant where there is no closed list but a name or descriptor recurs which is common to many metadatasets. This may lead to inconsistent results or, more frequently misinterpretation of results.</p>
</td>
<td width="252">
<p>National Grid, British National Grid, National Grid of Great Britain.</p>
</td>
<td width="252">
<p>Include frequently used standard names in any internal guidance.</p>
<p>Introduce checks to ensure consistency of approach across all metadata.</p>
</td>
</tr>
<tr>
<td width="163">
<p>Missing values</p>
</td>
<td width="252">
<p>Omission of values relating to extent, date or topic will have great impact on searches since these are the usual criteria used.</p>
</td>
<td width="252">
<ol>
<li>Omission of geographical extent.</li>
<li>Omission of dataset reference date.</li>
<li>Missing topic categories.</li>
</ol>
</td>
<td width="252">
<p>Introduce checks, preferably software checks, to ensure that mandatory fields contain values.</p>
</td>
</tr>
<tr>
<td width="163">
<p>Information not current</p>
</td>
<td width="252">
<p>This can impact both on searches and the interpretation of search results since the metadata does not reflect the current information or only does so partially.</p>
</td>
<td width="252">
<ol>
<li>Content of data resource extended but no change to topic categories.</li>
<li>Abstract not updated to reflect change of specification.</li>
<li>Data resource updated but later date not entered in the metadata.</li>
</ol>
</td>
<td width="252">
<p>Introduce a regime of regular checks on all metadata to ensure that currency is assessed and updates made where needed.</p>
</td>
</tr>
</tbody>
</table>

<p>Other errors that may lead to misinterpretation of results are:</p>
<ul>
<li>Correct value, but for the wrong metadata element;</li>
<li>Values incorrect, incomplete or inaccurate;</li>
<li>Incomprehensible, misleading or uninformative entries.</li>
</ul>
<p>The nature and impact of these types of error are described in more detail below, together with suggested ways in which these errors can be prevented or corrected.</p>
<table border="1" width="919">
<tbody>
<tr>
<td width="163">
<p><strong>Type of error</strong></p>
</td>
<td width="252">
<p><strong>Description and impact</strong></p>
</td>
<td width="288">
<p><strong>Examples of errors</strong></p>
</td>
<td width="216">
<p><strong>Prevention or correction</strong></p>
</td>
</tr>
<tr>
<td width="163">
<p>Correct value, wrong metadata element</p>
</td>
<td width="252">
<p>Confusion between the definitions of metadata elements can lead to correct values entered against the wrong metadata element.</p>
</td>
<td width="288">
<ol>
<li>Lineage information given for abstract.</li>
<li>Limitations on public access given for use constraints.</li>
</ol>
</td>
<td width="216">
<p>Use guidance on the definition and use of the metadata elements especially those most commonly confused (see examples).</p>
<p>Introduce training and checks to ensure correct use of elements.</p>
</td>
</tr>
<tr>
<td width="163">
<p>Values incorrect, incomplete or inaccurate</p>
</td>
<td width="252">
<p>This can apply to both quantitative and non-quantitative entries and can impact on the way that results are interpreted and used.</p>
</td>
<td width="288">
<ol>
<li>URL given as additional information source incorrect and not accessible.</li>
<li>Contact details for obtaining data resource are incorrect.</li>
</ol>
</td>
<td width="216">
<p>Check values are correct as far as can be established e.g. independently check URLs, contact details.</p>
</td>
</tr>
<tr>
<td width="163">
<p>Incomprehensible, misleading or uninformative  entries</p>
</td>
<td width="252">
<p>Entries need to be understandable by the discovery service user who needs to interpret the search results. The impact can be that results are misinterpreted and candidate datasets ignored.</p>
</td>
<td width="288">
<ol>
<li>Where dataset does not have a recognised title, uninformative title given.</li>
<li>Abstract is uninformative with no information on content.</li>
<li>Lineage contains no information about sources or reasons for creation.</li>
<li>Use of terms and abbreviations unlikely to be understood by service user.</li>
</ol>
</td>
<td width="216">
<p>Use guidance and checklists for compiling entries e.g. abstracts.</p>
</td>
</tr>
</tbody>
</table>
<h2><a id="guidance"></a>4. Guidance for individual metadata elements</h2>
<p>Detailed guidance on how to create each of these elements can be found here:</p>
<p><a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1062-gemini-datasets-and-data-series" target="_blank" rel="noopener noreferrer">GEMINI - Datasets and data series</a></p>
<p><a title="GEMINI - Services" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1063-gemini-services" target="_blank" rel="alternate noopener noreferrer">GEMINI - Services</a></p>
<p>Each metadata element is listed separately, as described in <a href="/agi-groups/standards-committee/uk-gemini/40-gemini/1244-uk-gemini-introduction#4.3">UK GEMINI Introduction</a>.</p>
<p><em>Last updated: May 2018</em></p>
<p><a href="http://creativecommons.org/licenses/by/4.0/" rel="license"> <img style="border-width: 0;" src="https://i.creativecommons.org/l/by/4.0/88x31.png" alt="Creative Commons Licence" /> </a> <br />This work is licensed under a <a href="http://creativecommons.org/licenses/by/4.0/" rel="license">Creative Commons Attribution 4.0 International License</a></p> 	
	
	
		
		
	</div>

									</div>
				<div class="col-lg-3 col-md-3 col-sm-12 sidebar">
							<div class="module submenuver">
		<div>
							<h3>Main Submenu</h3>
							<ul class="nav menu">
<li class="item-145 deeper parent"><a href="/agi-groups/national-groups" >National Groups</a><ul><li class="item-150 deeper parent"><a href="/agi-groups/national-groups/agi-cymru" >AGI Cymru</a><ul><li class="item-153"><a href="/agi-groups/national-groups/agi-cymru/agi-cymru-committee" >AGI Cymru Committee</a></li><li class="item-365"><a href="/agi-groups/national-groups/agi-cymru/agi-geocymru-blogs" >AGI Cymru Blog</a></li></ul></li><li class="item-151 deeper parent"><a href="/agi-groups/national-groups/agi-northern-ireland" >AGI Northern Ireland</a><ul><li class="item-154"><a href="/agi-groups/national-groups/agi-northern-ireland/agi-northern-ireland-committee" >AGI Northern Ireland Committee</a></li><li class="item-368"><a href="/agi-groups/national-groups/agi-northern-ireland/agi-northern-ireland-blog" >AGI Northern Ireland Blog</a></li></ul></li><li class="item-152 deeper parent"><a href="/agi-groups/national-groups/agi-scotland" >AGI Scotland</a><ul><li class="item-158"><a href="/agi-groups/national-groups/agi-scotland/agi-scotland-committee" >AGI Scotland Committee</a></li><li class="item-302"><a href="/agi-groups/national-groups/agi-scotland/agi-scotland-blog" >AGI Scotland Blog</a></li><li class="item-366"><a href="/agi-groups/national-groups/agi-scotland/edinburgh-earth-observatory-eeo-seminars" >Edinburgh Earth Observatory (EEO) Seminars</a></li></ul></li></ul></li><li class="item-147 deeper parent"><a href="/agi-groups/special-interest-groups" >Special Interest Groups</a><ul><li class="item-285 deeper parent"><a href="/agi-groups/special-interest-groups/early-careers-network" >Early Careers Network</a><ul><li class="item-271"><a href="/agi-groups/special-interest-groups/early-careers-network/ecn-blog" >Early Careers Network Blog</a></li></ul></li></ul></li><li class="item-148 active deeper parent"><a href="/agi-groups/standards-committee" >Standards Committee</a><ul><li class="item-186"><a href="/agi-groups/standards-committee/the-importance-of-standards" >The Importance of Standards</a></li><li class="item-262"><a href="/agi-groups/standards-committee/standards-resources" >Standards Resources</a></li><li class="item-264 current active deeper parent"><a href="/agi-groups/standards-committee/uk-gemini" >UK GEMINI</a><ul><li class="item-363"><a href="/agi-groups/standards-committee/uk-gemini/agi-gemini-update" >AGI GEMINI Update</a></li></ul></li><li class="item-303"><a href="/agi-groups/standards-committee/bs7666-guidelines" >BS 7666 Guidelines</a></li><li class="item-305"><a href="/agi-groups/standards-committee/review-of-bs-7666" >Review of BS 7666</a></li><li class="item-357"><a href="/agi-groups/standards-committee/why-uk-gemini-why-not-just-have-the-inspire-technical-guidance" >Why UK GEMINI? Why not just have the INSPIRE Technical Guidance?</a></li></ul></li><li class="item-149 deeper parent"><a href="/agi-groups/action-working-groups" >Action Working Groups</a><ul><li class="item-188"><a href="/agi-groups/action-working-groups/events-awg" >Events AWG</a></li></ul></li></ul>
		</div>
		</div>

	
				</div>
				
							</div>
			
					</div>
	</section>

	
		<section class="bottom">
		<div class="container">
			<div class="row">
						<div class="module col-sm-4">
		<div>
							<ul class="nav menu">
<li class="item-254 alias-parent-active"><a href="/agi-groups" >AGI Groups</a></li><li class="item-193"><a href="/resources" >Resources</a></li><li class="item-191"><a href="/privacy-policy" >Privacy Policy</a></li><li class="item-192"><a href="/terms-and-conditions" >Terms &amp; Conditions</a></li></ul>
		</div>
		</div>

			<div class="module connect col-sm-4">
		<div>
							<h3>Connect</h3>
							<div>
	<a href="https://vimeo.com/geocommunity" class="vimeo" target="_blank"></a>
	<a href="https://twitter.com/geocommunity" class="twitter" target="_blank"></a>
	<a href="https://www.linkedin.com/groups/3744691/" class="linkedin" target="_blank"></a>
</div>
		</div>
		</div>

			<div class="module details col-sm-4 col-md-3 col-md-offset-1">
		<div>
							

<div>
	<p>Lancaster Court<br />8 Barnes Wallis Road<br />Fareham<br />Hampshire PO15 5TU</p>
<p>Tel: +44 (<span style="font-size: 16px;">0)1489 668 340</span><br />Email: <a href="mailto:info@agi.org.uk">info@agi.org.uk</a></p></div>
		</div>
		</div>

	
			</div>
		</div>
	</section>
		
	<footer>
		<div class="container">
			<div class="row">
				<div class="col-sm-6 wf">
					Website by <a href="https://www.web-foundry.co.uk" target="_blank">Web Foundry</a>
				</div>
				<div class="col-sm-6 copy">
					Copyright &copy; 2014 AGI. All rights reserved.
				</div>
			</div>
		</div>
	</footer>

	<script type="text/javascript" src="/templates/agi/js/bootstrap.min.js?v=1"></script>
	<script type="text/javascript" src="/templates/agi/js/template.js?v=3"></script>

	<script type="text/javascript">
		(function($){
		$(document).ready(function () {
		$.cookieCuttr(
		{
    	cookieOverlayEnabled: false,
    	cookieNotificationLocationBottom: false,
      	cookieAnalytics: false,	
		cookieCutter: true,
		cookieMessage: 'We use cookies for the proper functioning of this website. Read our <a href="/privacy-policy">Privacy Policy</a>.  ',
		cookiePolicyLink: '/privacy-policy',
		cookieDeclineButton: true,
		cookieDiscreetLink: false,
		cookieDiscreetPosition: 'topright',
        cookieAcceptButtonText: 'ACCEPT COOKIES',
        cookieDeclineButtonText: 'DECLINE COOKIES',
		cookieDisable: '#comments',
		cookieDomain: 'index.php/cookies-policy',
		cookieErrorMessage: 'This feature places cookies in your browser and has been disabled.To continue using this functionality, please ...',
		});
		});
		})(jQuery);
		</script>

</body>
</html>