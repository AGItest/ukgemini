---
title: "Technical Guidance"
linkTitle: "Technical Guidance"
weight: 5
description: >
  Familiar with UK GEMINI and require specific information about the requirements and guidance for the metadata elements. encoding UK GEMINI metadata in XML, then general guidance is supplemented with detailed guidance for each metadata element at datasets or series or for services
---

{{% pageinfo %}}
This is a placeholder page that shows you how to use this template site.
{{% /pageinfo %}}

<div class="row content">
								
				<div class="content col-lg-12">
										<div class="item-page">
		
		<div class="page-header">
	
		
					<h1>Influencing. Informing. Acting.</h1>
				
							</div>
	
		
	
	
		
							
	<h3>Technical guidance on the encoding of UK GEMINI</h3>
<p>Return to <a title="GEMINI 2.3 home page" href="/gemini/40-gemini/1037-uk-gemini-standard-and-inspire-implementing-rules">GEMINI 2.3 home page</a></p>
<p><a title="1. Introduction" href="#1" rel="alternate">1. Introduction</a></p>
<p style="padding-left: 30px;"><a title="1.1 Purpose of guidelines" href="#1.1" rel="alternate">1.1 Purpose of guidelines</a></p>
<p style="padding-left: 30px;"><a title="1.2 Scope" href="#1.2" rel="alternate">1.2 Scope</a></p>
<p style="padding-left: 30px;"><a title="1.3 Assumed knowledge" href="#1.3" rel="alternate">1.3 Assumed knowledge</a></p>
<p style="padding-left: 30px;"><a title="1.4 Terminology" href="#1.4" rel="alternate">1.4 Terminology</a></p>
<p style="padding-left: 30px;"><a title="1.5 Structure of document" href="#1.5" rel="alternate">1.5 Structure of document</a></p>
<p style="padding-left: 30px;"><a title="1.6 XML fragments" href="#1.6" rel="alternate">1.6 XML fragments</a></p>
<p><a title="2. Encoding Guidelines" href="#2" rel="alternate">2. Encoding Guidelines</a></p>
<p style="padding-left: 30px;"><a title="2.1 Schemas" href="#2.1" rel="alternate">2.1 Schemas</a></p>
<p style="padding-left: 30px;"><a title="2.2 Common concepts" href="#2.2" rel="alternate">2.2 Common concepts</a></p>
<p style="padding-left: 30px;"><a title="2.3 Metadata for datasets and dataset series" href="#2.3" rel="alternate">2.3 Metadata for datasets and dataset series</a></p>
<p style="padding-left: 30px;"><a title="2.4 Metadata for services" href="#2.4" rel="alternate">2.4 Metadata for services</a></p>
<p>Appendices</p>
<p style="padding-left: 30px;"><a title="XML Element Order" href="/40-gemini/1046-xml-element-order" rel="alternate">XML Element Order</a></p>
<p style="padding-left: 30px;"><a title="Dataset metadata instance example" href="/40-gemini/1044-dataset-metadata-instance-example" rel="alternate">Dataset metadata instance example</a></p>
<p style="padding-left: 30px;"><a title="Series metadata instance example" href="/40-gemini/1043-series-metadata-example-old" rel="alternate">Series metadata instance example</a></p>
<p style="padding-left: 30px;"><a title="Service metadata instance example" href="/40-gemini/1042-service-metadata-instance-example" rel="alternate">Service metadata instance example</a></p>
<h2><a id="1"></a>1. Introduction</h2>
<h3><a id="1.1"></a>1.1 Purpose of guidelines</h3>
<p>The purpose of these guidelines is to explain, with the aid of examples, how to encode UK GEMINI metadata using XSD schemas of ISO / TC 211. Examples are in the form of fragments of XML.</p>
<p>UK GEMINI metadata may be for a dataset, dataset series or a service. The encoding of all types is covered.</p>
<h3><a id="1.2"></a>1.2 Scope</h3>
<p>The scope of these guidelines is the encoding of UK GEMINI [<a title="References" href="/40-gemini/1047-metadata-guidelines-for-geospatial-data-resources-part-3" target="_blank" rel="alternate noopener noreferrer">4</a>]according to ISO 19139, ISO 19119 and ISO 19136, in a way that adheres to the INSPIRE technical guidelines [<a title="References" href="/40-gemini/1047-metadata-guidelines-for-geospatial-data-resources-part-3" target="_blank" rel="alternate noopener noreferrer">9</a>] for encoding metadata.</p>
<p>Outside the scope of this document is the description of GEMINI2 metadata items, their content, obligation and meaning. Readers seeking this information should consult the GEMINI2 standard [<a title="References" href="/40-gemini/1047-metadata-guidelines-for-geospatial-data-resources-part-3" target="_blank" rel="alternate noopener noreferrer">4</a>].</p>
<h3><a id="1.3"></a>1.3 Assumed knowledge</h3>
<p>It is assumed that readers will be familiar with XML. Readers who require background information are referred to the W3Schools introduction to XML:</p>
<ul>
<li>XML - <a href="http://www.w3schools.com/xml/xml_whatis.asp">http://www.w3schools.com/xml/xml_whatis.asp</a></li>
</ul>
<p>Readers requiring an introduction to XML Schemas are referred to the W3Schools XML Schema tutorial:</p>
<ul>
<li>XSD - <a title="http://www.w3schools.com/xml/xml_schema.asp" href="http://www.w3schools.com/xml/xml_schema.asp" target="_blank" rel="alternate noopener noreferrer">http://www.w3schools.com/xml/xml_schema.asp</a></li>
</ul>
<h3><a id="1.4"></a>1.4 Terminology</h3>
<p>A Glossary is provided <a title="Glossary" href="/40-gemini/1056-glossary" target="_blank" rel="alternate noopener noreferrer">here</a>.</p>
<h3><a id="1.5"></a>1.5 Structure of document</h3>
<p>The core section, Encoding Guidelines, is split into four principal sections</p>
<ul>
<li>The first section deals with the schemas</li>
<li>The second deals with concepts which are common to all kinds of GEMINI2 metadata instances.</li>
<li>The third explains the encoding of metadata for datasets and dataset series.</li>
<li>The fourth section explains the encoding of encoding metadata for services.</li>
</ul>
<p>There is some overlap, and therefore duplication, between the sections but it is felt that this approach is best in that it clearly indicates the requirements for each type of metadata.</p>
<p>The 'Metadata for datasets and dataset series' and 'Metadata for services' sections list metadata items from GEMINI2 in the order that they appear in GEMINI2. XML elements in an XML document must follow the <a title="XML Element Order" href="/40-gemini/1046-xml-element-order" target="_blank" rel="alternate noopener noreferrer">order </a>expressed in the XSD schema to which the XML document conforms. The order of XML element expressed by the XSD schema will not be the same as the order of metadata items in GEMINI2.</p>
<p>Examples are provided by way of XML fragments throughout the document. Full metadata instances are shown here:</p>
<p style="padding-left: 30px;"><a title="Dataset metadata instance example" href="/40-gemini/1044-dataset-metadata-instance-example" target="_blank" rel="alternate noopener noreferrer">Dataset metadata instance example</a></p>

<p>An example of a schema and Schematron valid dataset metadata instance is shown below.</p>
<p><code>&lt;?xml version="1.0" encoding="UTF-8"?&gt;</code></p>
<p><code>&lt;gmd:MD_Metadata xmlns:gmd="http://www.isotc211.org/2005/gmd"</code></p>
<p><code>                 xmlns:gsr="http://www.isotc211.org/2005/gsr"</code></p>
<p><code>                 xmlns:xlink="http://www.w3.org/1999/xlink"</code></p>
<p><code>                 xmlns:gss="http://www.isotc211.org/2005/gss"</code></p>
<p><code>                 xmlns:gts="http://www.isotc211.org/2005/gts"</code></p>
<p><code>                 xmlns:gml="http://www.opengis.net/gml/3.2"</code></p>
<p><code>                 xmlns:gmx="http://www.isotc211.org/2005/gmx"</code></p>
<p><code>                 xmlns:gco="http://www.isotc211.org/2005/gco"</code></p>
<p><code>                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"</code></p>
<p><code>                 xsi:schemaLocation="http://www.isotc211.org/2005/gmd http://inspire.ec.europa.eu/draft-schemas/inspire-md-schemas/apiso-inspire/apiso-inspire.xsd"&gt;</code></p>
<p><code>&lt;gmd:fileIdentifier&gt;</code></p>
<p><code>     &lt;gco:CharacterString&gt;ae0e855d-f0a2-438e-855c-6ef5400f4ef3&lt;/gco:CharacterString&gt;</code></p>
<p><code>&lt;/gmd:fileIdentifier&gt;</code></p>
<p><code>&lt;gmd:language&gt;</code></p>
<p><code>     &lt;gmd:LanguageCode codeList="http://www.loc.gov/standards/iso639-2/php/code_list.php" codeListValue="eng"&gt;eng&lt;/gmd:LanguageCode&gt;</code></p>
<p><code>&lt;/gmd:language&gt;</code></p>
<p><code>&lt;gmd:hierarchyLevel&gt;</code></p>
<p><code>     &lt;gmd:MD_ScopeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_ScopeCode" codeListValue="dataset"&gt;dataset&lt;/gmd:MD_ScopeCode&gt;</code></p>
<p><code>&lt;/gmd:hierarchyLevel&gt;</code></p>
<p><code>&lt;gmd:contact&gt;</code></p>
<p><code>     &lt;gmd:CI_ResponsibleParty&gt;</code></p>
<p><code>         &lt;gmd:organisationName&gt;</code></p>
<p><code>           &lt;gco:CharacterString&gt;Ordnance Survey, Great Britain&lt;/gco:CharacterString&gt;</code></p>
<p><code>         &lt;/gmd:organisationName&gt;</code></p>
<p><code>         &lt;gmd:positionName&gt;</code></p>
<p><code>           &lt;gco:CharacterString&gt;Customer Services&lt;/gco:CharacterString&gt;</code></p>
<p><code>         &lt;/gmd:positionName&gt;</code></p>
<p><code>         &lt;gmd:contactInfo&gt;</code></p>
<p><code>           &lt;gmd:CI_Contact&gt;</code></p>
<p><code>               &lt;gmd:phone&gt;</code></p>
<p><code>                 &lt;gmd:CI_Telephone&gt;</code></p>
<p><code>                     &lt;gmd:voice&gt;</code></p>
<p><code>                       &lt;gco:CharacterString&gt;+44 (0)8456 050505&lt;/gco:CharacterString&gt;</code></p>
<p><code>                     &lt;/gmd:voice&gt;</code></p>
<p><code>                 &lt;/gmd:CI_Telephone&gt;</code></p>
<p><code>               &lt;/gmd:phone&gt;</code></p>
<p><code>               &lt;gmd:address&gt;</code></p>
<p><code>                 &lt;gmd:CI_Address&gt;</code></p>
<p><code>                     &lt;gmd:deliveryPoint&gt;</code></p>
<p><code>                       &lt;gco:CharacterString&gt;Explorer House, Adanac Drive&lt;/gco:CharacterString&gt;</code></p>
<p><code>                     &lt;/gmd:deliveryPoint&gt;</code></p>
<p><code>                     &lt;gmd:city&gt;</code></p>
<p><code>                       &lt;gco:CharacterString&gt;Southampton&lt;/gco:CharacterString&gt;</code></p>
<p><code>                    &lt;/gmd:city&gt;</code></p>
<p><code>                     &lt;gmd:postalCode&gt;</code></p>
<p><code>                       &lt;gco:CharacterString&gt;SO16 0AS&lt;/gco:CharacterString&gt;</code></p>
<p><code>                     &lt;/gmd:postalCode&gt;</code></p>
<p><code>                     &lt;gmd:country&gt;</code></p>
<p><code>                       &lt;gco:CharacterString&gt;United Kingdom&lt;/gco:CharacterString&gt;</code></p>
<p><code>                     &lt;/gmd:country&gt;</code></p>
<p><code>                     &lt;gmd:electronicMailAddress&gt;</code></p>
<p><code>&lt;gco:CharacterString&gt;<span id="cloak39a744831ba8c974b27fd2eb61c01dd3">This email address is being protected from spambots. You need JavaScript enabled to view it.</span><script type='text/javascript'>
				document.getElementById('cloak39a744831ba8c974b27fd2eb61c01dd3').innerHTML = '';
				var prefix = '&#109;a' + 'i&#108;' + '&#116;o';
				var path = 'hr' + 'ef' + '=';
				var addy39a744831ba8c974b27fd2eb61c01dd3 = 'c&#117;st&#111;m&#101;rs&#101;rv&#105;c&#101;s' + '&#64;';
				addy39a744831ba8c974b27fd2eb61c01dd3 = addy39a744831ba8c974b27fd2eb61c01dd3 + '&#111;s' + '&#46;' + '&#117;k';
				var addy_text39a744831ba8c974b27fd2eb61c01dd3 = 'c&#117;st&#111;m&#101;rs&#101;rv&#105;c&#101;s' + '&#64;' + '&#111;s' + '&#46;' + '&#117;k';document.getElementById('cloak39a744831ba8c974b27fd2eb61c01dd3').innerHTML += '<a ' + path + '\'' + prefix + ':' + addy39a744831ba8c974b27fd2eb61c01dd3 + '\'>'+addy_text39a744831ba8c974b27fd2eb61c01dd3+'<\/a>';
		</script>&lt;/gco:CharacterString&gt;</code></p>
<p><code>                     &lt;/gmd:electronicMailAddress&gt;</code></p>
<p><code>                 &lt;/gmd:CI_Address&gt;</code></p>
<p><code>               &lt;/gmd:address&gt;</code></p>
<p><code>           &lt;/gmd:CI_Contact&gt;</code></p>
<p><code>         &lt;/gmd:contactInfo&gt;</code></p>
<p><code>         &lt;gmd:role&gt;</code></p>
<p><code>           &lt;gmd:CI_RoleCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_RoleCode"</code></p>
<p><code>codeListValue="pointOfContact"&gt;pointOfContact&lt;/gmd:CI_RoleCode&gt;</code></p>
<p><code>         &lt;/gmd:role&gt;</code></p>
<p><code>     &lt;/gmd:CI_ResponsibleParty&gt;</code></p>
<p><code>&lt;/gmd:contact&gt;</code></p>
<p><code>&lt;gmd:dateStamp&gt;</code></p>
<p><code>     &lt;gco:DateTime&gt;2010-12-02T11:39:34&lt;/gco:DateTime&gt;</code></p>
<p><code>&lt;/gmd:dateStamp&gt;</code></p>
<p><code>&lt;gmd:referenceSystemInfo&gt;</code></p>
<p><code>     &lt;gmd:MD_ReferenceSystem&gt;</code></p>
<p><code>         &lt;gmd:referenceSystemIdentifier&gt;</code></p>
<p><code>           &lt;gmd:RS_Identifier&gt;</code></p>
<p><code>               &lt;gmd:code&gt;</code></p>
<p><code>&lt;gco:CharacterString&gt; http://www.opengis.net/def/crs/EPSG/0/27700&lt;/gco:CharacterString&gt;</code></p>
<p><code>               &lt;/gmd:code&gt;</code></p>
<p><code>           &lt;/gmd:RS_Identifier&gt;</code></p>
<p><code>         &lt;/gmd:referenceSystemIdentifier&gt;</code></p>
<p><code>     &lt;/gmd:MD_ReferenceSystem&gt;</code></p>
<p><code>&lt;/gmd:referenceSystemInfo&gt;</code></p>
<p><code>&lt;gmd:identificationInfo&gt;</code></p>
<p><code>     &lt;gmd:MD_DataIdentification&gt;</code></p>
<p><code>         &lt;gmd:citation&gt;</code></p>
<p><code>           &lt;gmd:CI_Citation&gt;</code></p>
<p><code>               &lt;gmd:title&gt;</code></p>
<p><code>                 &lt;gco:CharacterString&gt;Boundary-Line™&lt;/gco:CharacterString&gt;</code></p>
<p><code>               &lt;/gmd:title&gt;</code></p>
<p><code>               &lt;gmd:date&gt;</code></p>
<p><code>                 &lt;gmd:CI_Date&gt;</code></p>
<p><code>                     &lt;gmd:date&gt;</code></p>
<p><code>                       &lt;gco:Date&gt;1996-04-01&lt;/gco:Date&gt;</code></p>
<p><code>                     &lt;/gmd:date&gt;</code></p>
<p><code>                     &lt;gmd:dateType&gt;</code></p>
<p><code>                       &lt;gmd:CI_DateTypeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_DateTypeCode"</code></p>
<p><code>codeListValue="creation"&gt;creation&lt;/gmd:CI_DateTypeCode&gt;</code></p>
<p><code>                     &lt;/gmd:dateType&gt;</code></p>
<p><code>                 &lt;/gmd:CI_Date&gt;</code></p>
<p><code>               &lt;/gmd:date&gt;</code></p>
<p><code>               &lt;gmd:identifier&gt;</code></p>
<p><code>                 &lt;gmd:RS_Identifier&gt;</code></p>
<p><code>                     &lt;gmd:code&gt;</code></p>
<p><code>                       &lt;gco:CharacterString&gt;Boundary-Line™&lt;/gco:CharacterString&gt;</code></p>
<p><code>                     &lt;/gmd:code&gt;</code></p>
<p><code>                 &lt;/gmd:RS_Identifier&gt;</code></p>
<p><code>               &lt;/gmd:identifier&gt;</code></p>
<p><code>           &lt;/gmd:CI_Citation&gt;</code></p>
<p><code>         &lt;/gmd:citation&gt;</code></p>
<p><code>         &lt;gmd:abstract&gt;</code></p>
<p><code>           &lt;gco:CharacterString&gt;Boundary-Line is a specialist 1:10 000 scale boundaries dataset. It contains all levels of electoral and administrative boundaries, from district, wards and civil parishes (or communities) up to parliamentary, assembly and European constituencies.</code></p>
<p><code> </code></p>
<p><code>The information is represented as vector digital data.  </code></p>
<p><code> </code></p>
<p><code>The boundary information is updated twice a year, in May and October. The May release contains the boundaries that have become live in the first week of May, in the year of release. The October release contains the May boundaries plus additional information. Customers can choose either May or October releases.</code></p>
<p><code> </code></p>
<p><code>    * County - The named  county, district, district ward, civil parish, county electoral division (ED).</code></p>
<p><code>    * European constituencies - The named European region.</code></p>
<p><code>    * Greater London Authority  - The Greater London Authority, Greater London Authority Assembly constituency, London borough, London borough ward.</code></p>
<p><code>    * Metropolitan districts - The named metropolitan district, metropolitan district ward, civil parish where appropriate.</code></p>
<p><code>    * Scottish parliamentary electoral region - The named Scottish Parliamentary electoral region, Scottish parliamentary constituency.</code></p>
<p><code>    * Unitary authorities- The named unitary authority, unitary authority ward or unitary authority ED as appropriate, civil parish where appropriate, together with community in Wales.</code></p>
<p><code>    * Welsh Assembly Electoral Region - The named Welsh Assembly electoral region, Welsh assembly constituency.</code></p>
<p><code>    * Westminster constituencies - The named Westminster constituency.</code></p>
<p><code>    * Extent of the realm -  Low water mark or seaward boundary extension.</code></p>
<p><code>    * High water mark</code></p>
<p><code>    * Unique identifiers -   For administrative areas, polygons and links.</code></p>
<p><code>    * Area measurements</code></p>
<p><code>    * Definitive names</code></p>
<p><code>    * Census codes&lt;/gco:CharacterString&gt;</code></p>
<p><code>         &lt;/gmd:abstract&gt;</code></p>
<p><code>         &lt;gmd:pointOfContact&gt;</code></p>
<p><code>           &lt;gmd:CI_ResponsibleParty&gt;</code></p>
<p><code>               &lt;gmd:organisationName&gt;</code></p>
<p><code>                 &lt;gco:CharacterString&gt;Ordnance Survey, Great Britain&lt;/gco:CharacterString&gt;</code></p>
<p><code>               &lt;/gmd:organisationName&gt;</code></p>
<p><code>               &lt;gmd:positionName&gt;</code></p>
<p><code>                 &lt;gco:CharacterString&gt;Customer Services&lt;/gco:CharacterString&gt;</code></p>
<p><code>               &lt;/gmd:positionName&gt;</code></p>
<p><code>               &lt;gmd:contactInfo&gt;</code></p>
<p><code>                 &lt;gmd:CI_Contact&gt;</code></p>
<p><code>                     &lt;gmd:phone&gt;</code></p>
<p><code>                       &lt;gmd:CI_Telephone&gt;</code></p>
<p><code>                           &lt;gmd:voice&gt;</code></p>
<p><code>                             &lt;gco:CharacterString&gt;+44 (0)8456 050505&lt;/gco:CharacterString&gt;</code></p>
<p><code>                           &lt;/gmd:voice&gt;</code></p>
<p><code>                       &lt;/gmd:CI_Telephone&gt;</code></p>
<p><code>                     &lt;/gmd:phone&gt;</code></p>
<p><code>                     &lt;gmd:address&gt;</code></p>
<p><code>                       &lt;gmd:CI_Address&gt;</code></p>
<p><code>                           &lt;gmd:deliveryPoint&gt;</code></p>
<p><code>                             &lt;gco:CharacterString&gt;Explorer House, Adanac Drive&lt;/gco:CharacterString&gt;</code></p>
<p><code>                          &lt;/gmd:deliveryPoint&gt;</code></p>
<p><code>                           &lt;gmd:city&gt;</code></p>
<p><code>                             &lt;gco:CharacterString&gt;Southampton&lt;/gco:CharacterString&gt;</code></p>
<p><code>                           &lt;/gmd:city&gt;</code></p>
<p><code>                           &lt;gmd:postalCode&gt;</code></p>
<p><code>                             &lt;gco:CharacterString&gt;SO16 0AS&lt;/gco:CharacterString&gt;</code></p>
<p><code>                           &lt;/gmd:postalCode&gt;</code></p>
<p><code>                           &lt;gmd:country&gt;</code></p>
<p><code>                             &lt;gco:CharacterString&gt;United Kingdom&lt;/gco:CharacterString&gt;</code></p>
<p><code>                           &lt;/gmd:country&gt;</code></p>
<p><code>                           &lt;gmd:electronicMailAddress&gt;</code></p>
<p><code>&lt;gco:CharacterString&gt;<span id="cloak1ab7c4803e7877895c4c7fd7ae0f1f15">This email address is being protected from spambots. You need JavaScript enabled to view it.</span><script type='text/javascript'>
				document.getElementById('cloak1ab7c4803e7877895c4c7fd7ae0f1f15').innerHTML = '';
				var prefix = '&#109;a' + 'i&#108;' + '&#116;o';
				var path = 'hr' + 'ef' + '=';
				var addy1ab7c4803e7877895c4c7fd7ae0f1f15 = 'c&#117;st&#111;m&#101;rs&#101;rv&#105;c&#101;s' + '&#64;';
				addy1ab7c4803e7877895c4c7fd7ae0f1f15 = addy1ab7c4803e7877895c4c7fd7ae0f1f15 + '&#111;s' + '&#46;' + '&#117;k';
				var addy_text1ab7c4803e7877895c4c7fd7ae0f1f15 = 'c&#117;st&#111;m&#101;rs&#101;rv&#105;c&#101;s' + '&#64;' + '&#111;s' + '&#46;' + '&#117;k';document.getElementById('cloak1ab7c4803e7877895c4c7fd7ae0f1f15').innerHTML += '<a ' + path + '\'' + prefix + ':' + addy1ab7c4803e7877895c4c7fd7ae0f1f15 + '\'>'+addy_text1ab7c4803e7877895c4c7fd7ae0f1f15+'<\/a>';
		</script>&lt;/gco:CharacterString&gt;</code></p>
<p><code>                           &lt;/gmd:electronicMailAddress&gt;</code></p>
<p><code>                       &lt;/gmd:CI_Address&gt;</code></p>
<p><code>                     &lt;/gmd:address&gt;</code></p>
<p><code>                     &lt;gmd:onlineResource&gt;</code></p>
<p><code>                       &lt;gmd:CI_OnlineResource&gt;</code></p>
<p><code>                           &lt;gmd:linkage&gt;</code></p>
<p><code>                             &lt;gmd:URL&gt;https://os.uk/&lt;/gmd:URL&gt;</code></p>
<p><code>                           &lt;/gmd:linkage&gt;</code></p>
<p><code>                           &lt;gmd:description&gt;</code></p>
<p><code>                             &lt;gco:CharacterString&gt;Ordnance Survey, Great Britain top level website&lt;/gco:CharacterString&gt;</code></p>
<p><code>                           &lt;/gmd:description&gt;</code></p>
<p><code>                       &lt;/gmd:CI_OnlineResource&gt;</code></p>
<p><code>                     &lt;/gmd:onlineResource&gt;</code></p>
<p><code>                 &lt;/gmd:CI_Contact&gt;</code></p>
<p><code>               &lt;/gmd:contactInfo&gt;</code></p>
<p><code>               &lt;gmd:role&gt;</code></p>
<p><code>                 &lt;gmd:CI_RoleCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_RoleCode"</code></p>
<p><code>codeListValue="publisher"&gt;publisher&lt;/gmd:CI_RoleCode&gt;</code></p>
<p><code>               &lt;/gmd:role&gt;</code></p>
<p><code>           &lt;/gmd:CI_ResponsibleParty&gt;</code></p>
<p><code>         &lt;/gmd:pointOfContact&gt;</code></p>
<p><code>         &lt;gmd:resourceMaintenance&gt;</code></p>
<p><code>           &lt;gmd:MD_MaintenanceInformation&gt;</code></p>
<p><code>               &lt;gmd:maintenanceAndUpdateFrequency&gt;</code></p>
<p><code>                 &lt;gmd:MD_MaintenanceFrequencyCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_MaintenanceFrequencyCode"</code></p>
<p><code>codeListValue="biannually"&gt;biannually&lt;/gmd:MD_MaintenanceFrequencyCode&gt;</code></p>
<p><code>               &lt;/gmd:maintenanceAndUpdateFrequency&gt;</code></p>
<p><code>           &lt;/gmd:MD_MaintenanceInformation&gt;</code></p>
<p><code>         &lt;/gmd:resourceMaintenance&gt;</code></p>
<p><code>         &lt;gmd:graphicOverview&gt;</code></p>
<p><code>           &lt;gmd:MD_BrowseGraphic&gt;</code></p>
<p><code>               &lt;gmd:fileName&gt;</code></p>
<p><code>                 &lt;gco:CharacterString&gt;BoundaryLine_s.png&lt;/gco:CharacterString&gt;</code></p>
<p><code>               &lt;/gmd:fileName&gt;</code></p>
<p><code>               &lt;gmd:fileDescription&gt;</code></p>
<p><code>                 &lt;gco:CharacterString&gt;thumbnail&lt;/gco:CharacterString&gt;</code></p>
<p><code>               &lt;/gmd:fileDescription&gt;</code></p>
<p><code>               &lt;gmd:fileType&gt;</code></p>
<p><code>                 &lt;gco:CharacterString&gt;png&lt;/gco:CharacterString&gt;</code></p>
<p><code>               &lt;/gmd:fileType&gt;</code></p>
<p><code>           &lt;/gmd:MD_BrowseGraphic&gt;</code></p>
<p><code>         &lt;/gmd:graphicOverview&gt;</code></p>
<p><code>         &lt;gmd:descriptiveKeywords&gt;</code></p>
<p><code>           &lt;gmd:MD_Keywords&gt;</code></p>
<p><code>               &lt;gmd:keyword&gt;</code></p>
<p><code>                 &lt;gco:CharacterString&gt;Geographical names&lt;/gco:CharacterString&gt;</code></p>
<p><code>               &lt;/gmd:keyword&gt;</code></p>
<p><code>               &lt;gmd:thesaurusName&gt;</code></p>
<p><code>                 &lt;gmd:CI_Citation&gt;</code></p>
<p><code>                     &lt;gmd:title&gt;</code></p>
<p><code>                       &lt;gco:CharacterString&gt;GEMET - INSPIRE themes, version 1.0&lt;/gco:CharacterString&gt;</code></p>
<p><code>                     &lt;/gmd:title&gt;</code></p>
<p><code>                     &lt;gmd:date&gt;</code></p>
<p><code>                       &lt;gmd:CI_Date&gt;</code></p>
<p><code>                           &lt;gmd:date&gt;</code></p>
<p><code>                             &lt;gco:Date&gt;2008-06-01&lt;/gco:Date&gt;</code></p>
<p><code>                           &lt;/gmd:date&gt;</code></p>
<p><code>                           &lt;gmd:dateType&gt;</code></p>
<p><code>                             &lt;gmd:CI_DateTypeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_DateTypeCode"</code></p>
<p><code>codeListValue="publication"&gt;publication&lt;/gmd:CI_DateTypeCode&gt;</code></p>
<p><code>                           &lt;/gmd:dateType&gt;</code></p>
<p><code>                       &lt;/gmd:CI_Date&gt;</code></p>
<p><code>                     &lt;/gmd:date&gt;</code></p>
<p><code>                 &lt;/gmd:CI_Citation&gt;</code></p>
<p><code>               &lt;/gmd:thesaurusName&gt;</code></p>
<p><code>           &lt;/gmd:MD_Keywords&gt;</code></p>
<p><code>         &lt;/gmd:descriptiveKeywords&gt;</code></p>
<p><code>         &lt;gmd:descriptiveKeywords&gt;</code></p>
<p><code>           &lt;gmd:MD_Keywords&gt;</code></p>
<p><code>               &lt;gmd:keyword&gt;</code></p>
<p><code>                 &lt;gco:CharacterString&gt;Legal government boundaries&lt;/gco:CharacterString&gt;</code></p>
<p><code>               &lt;/gmd:keyword&gt;</code></p>
<p><code>               &lt;gmd:keyword&gt;</code></p>
<p><code>                 &lt;gco:CharacterString&gt;Mapping&lt;/gco:CharacterString&gt;</code></p>
<p><code>               &lt;/gmd:keyword&gt;</code></p>
<p><code>               &lt;gmd:keyword&gt;</code></p>
<p><code>                 &lt;gco:CharacterString&gt;Mid-Scales&lt;/gco:CharacterString&gt;</code></p>
<p><code>             &lt;/gmd:keyword&gt;</code></p>
<p><code>               &lt;gmd:keyword&gt;</code></p>
<p><code>                 &lt;gco:CharacterString&gt;Electorial Boundaries&lt;/gco:CharacterString&gt;</code></p>
<p><code>               &lt;/gmd:keyword&gt;</code></p>
<p><code>               &lt;gmd:keyword&gt;</code></p>
<p><code>                 &lt;gco:CharacterString&gt;administrative boundaries&lt;/gco:CharacterString&gt;</code></p>
<p><code>               &lt;/gmd:keyword&gt;</code></p>
<p><code>               &lt;gmd:keyword&gt;</code></p>
<p><code>                 &lt;gco:CharacterString&gt;GSS codes&lt;/gco:CharacterString&gt;</code></p>
<p><code>               &lt;/gmd:keyword&gt;</code></p>
<p><code>               &lt;gmd:keyword&gt;</code></p>
<p><code>                 &lt;gco:CharacterString&gt;Ordnance Survey&lt;/gco:CharacterString&gt;</code></p>
<p><code>               &lt;/gmd:keyword&gt;</code></p>
<p><code>               &lt;gmd:keyword&gt;</code></p>
<p><code>                 &lt;gco:CharacterString&gt;OS&lt;/gco:CharacterString&gt;</code></p>
<p><code>               &lt;/gmd:keyword&gt;</code></p>
<p><code>           &lt;/gmd:MD_Keywords&gt;</code></p>
<p><code>         &lt;/gmd:descriptiveKeywords&gt;</code></p>
<p><code>         &lt;gmd:resourceConstraints&gt;</code></p>
<p><code>           &lt;gmd:MD_LegalConstraints&gt;</code></p>
<p><code>               &lt;gmd:accessConstraints&gt;</code></p>
<p><code>                 &lt;gmd:MD_RestrictionCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_RestrictionCode"</code></p>
<p><code>codeListValue="otherRestrictions"&gt;otherRestrictions&lt;/gmd:MD_RestrictionCode&gt;</code></p>
<p><code>               &lt;/gmd:accessConstraints&gt;</code></p>
<p><code></code></p>
<p><code>               &lt;gmd:otherConstraints&gt;<br />                 &lt;gmx:Anchor xlink:href="http://inspire.ec.europa.eu/metadata-codelist/LimitationsOnPublicAccess/INSPIRE_Directive_Article13_1e"/&gt;<br />               &lt;/gmd:otherConstraints&gt;</code></p>
<p><code>               &lt;gmd:otherConstraints&gt;</code></p>
<p><code>                 &lt;gco:CharacterString&gt;For further details on licensing see http://www.ordnancesurvey.co.uk/oswebsite/business/licences/index.html&lt;/gco:CharacterString&gt;</code></p>
<p><code>               &lt;/gmd:otherConstraints&gt;</code></p>
<p><code>           &lt;/gmd:MD_LegalConstraints&gt;</code></p>
<p><code>         &lt;/gmd:resourceConstraints&gt;</code></p>
<p><code>         &lt;gmd:resourceConstraints&gt;</code></p>
<p><code> &lt;gmd:MD_LegalConstraints&gt;<br />  &lt;gmd:useConstraints&gt;<br />   &lt;gmd:MD_RestrictionCode<br />codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_RestrictionCode"<br /> codeListValue="otherRestrictions"&gt;otherRestrictions&lt;/gmd:MD_RestrictionCode&gt;<br />   &lt;/gmd:useConstraints&gt;<br />  &lt;gmd:otherConstraints&gt;<br />   &lt;gmx:Anchor xlink:href="https://os.uk/business/licences/index.html"&gt;Use limitation dependent upon licence&lt;/gmx:Anchor&gt;<br />  &lt;/gmd:otherConstraints&gt;<br /> &lt;/gmd:MD_LegalConstraints&gt;</code></p>
<p><code>         &lt;/gmd:resourceConstraints&gt;</code></p>
<p><code>         &lt;gmd:spatialResolution&gt;</code></p>
<p><code>           &lt;gmd:MD_Resolution&gt;</code></p>
<p><code>               &lt;gmd:equivalentScale&gt;</code></p>
<p><code>                 &lt;gmd:MD_RepresentativeFraction&gt;</code></p>
<p><code>                     &lt;gmd:denominator&gt;</code></p>
<p><code>                       &lt;gco:Integer&gt;10000&lt;/gco:Integer&gt;</code></p>
<p><code>                     &lt;/gmd:denominator&gt;</code></p>
<p><code>                 &lt;/gmd:MD_RepresentativeFraction&gt;</code></p>
<p><code>               &lt;/gmd:equivalentScale&gt;</code></p>
<p><code>           &lt;/gmd:MD_Resolution&gt;</code></p>
<p><code>         &lt;/gmd:spatialResolution&gt;</code></p>
<p><code>         &lt;gmd:language&gt;</code></p>
<p><code>           &lt;gmd:LanguageCode codeList="http://www.loc.gov/standards/iso639-2/php/code_list.php" codeListValue="eng"&gt;eng&lt;/gmd:LanguageCode&gt;</code></p>
<p><code>         &lt;/gmd:language&gt;</code></p>
<p><code>         &lt;gmd:topicCategory&gt;</code></p>
<p><code>           &lt;gmd:MD_TopicCategoryCode&gt;boundaries&lt;/gmd:MD_TopicCategoryCode&gt;</code></p>
<p><code>         &lt;/gmd:topicCategory&gt;</code></p>
<p><code>         &lt;gmd:extent&gt;</code></p>
<p><code>           &lt;gmd:EX_Extent&gt;</code></p>
<p><code>               &lt;gmd:geographicElement&gt;</code></p>
<p><code>                 &lt;gmd:EX_GeographicBoundingBox&gt;</code></p>
<p><code>                     &lt;gmd:westBoundLongitude&gt;</code></p>
<p><code>                       &lt;gco:Decimal&gt;-8.45&lt;/gco:Decimal&gt;</code></p>
<p><code>                     &lt;/gmd:westBoundLongitude&gt;</code></p>
<p><code>                     &lt;gmd:eastBoundLongitude&gt;</code></p>
<p><code>                       &lt;gco:Decimal&gt;1.78&lt;/gco:Decimal&gt;</code></p>
<p><code>                     &lt;/gmd:eastBoundLongitude&gt;</code></p>
<p><code>                     &lt;gmd:southBoundLatitude&gt;</code></p>
<p><code>                       &lt;gco:Decimal&gt;49.86&lt;/gco:Decimal&gt;</code></p>
<p><code>                     &lt;/gmd:southBoundLatitude&gt;</code></p>
<p><code>                     &lt;gmd:northBoundLatitude&gt;</code></p>
<p><code>                       &lt;gco:Decimal&gt;60.86&lt;/gco:Decimal&gt;</code></p>
<p><code>                     &lt;/gmd:northBoundLatitude&gt;</code></p>
<p><code>                 &lt;/gmd:EX_GeographicBoundingBox&gt;</code></p>
<p><code>               &lt;/gmd:geographicElement&gt;</code></p>
<p><code>               &lt;gmd:temporalElement&gt;</code></p>
<p><code>                 &lt;gmd:EX_TemporalExtent&gt;</code></p>
<p><code>                     &lt;gmd:extent&gt;</code></p>
<p><code>                       &lt;gml:TimePeriod gml:id="T1"&gt;</code></p>
<p><code>                           &lt;gml:beginPosition&gt;2010-06-01&lt;/gml:beginPosition&gt;</code></p>
<p><code>                           &lt;gml:endPosition&gt;2010-09-30&lt;/gml:endPosition&gt;</code></p>
<p><code>                       &lt;/gml:TimePeriod&gt;</code></p>
<p><code>                     &lt;/gmd:extent&gt;</code></p>
<p><code>                 &lt;/gmd:EX_TemporalExtent&gt;</code></p>
<p><code>               &lt;/gmd:temporalElement&gt;</code></p>
<p><code>           &lt;/gmd:EX_Extent&gt;</code></p>
<p><code>         &lt;/gmd:extent&gt;</code></p>
<p><code>     &lt;/gmd:MD_DataIdentification&gt;</code></p>
<p><code>&lt;/gmd:identificationInfo&gt;</code></p>
<p><code>&lt;gmd:distributionInfo&gt;</code></p>
<p><code>     &lt;gmd:MD_Distribution&gt;</code></p>
<p><code>         &lt;gmd:distributionFormat&gt;</code></p>
<p><code>           &lt;gmd:MD_Format&gt;</code></p>
<p><code>               &lt;gmd:name&gt;</code></p>
<p><code>                 &lt;gco:CharacterString&gt;ESRI® Spatial data format (Shapefile)&lt;/gco:CharacterString&gt;</code></p>
<p><code>               &lt;/gmd:name&gt;</code></p>
<p><code>               &lt;gmd:version&gt;</code></p>
<p><code>                  &lt;gco:CharacterString&gt;1.0&lt;/gco:CharacterString&gt;</code></p>
<p><code>               &lt;/gmd:version&gt;</code></p>
<p><code>           &lt;/gmd:MD_Format&gt;</code></p>
<p><code>         &lt;/gmd:distributionFormat&gt;</code></p>
<p><code>         &lt;gmd:transferOptions&gt;</code></p>
<p><code>           &lt;gmd:MD_DigitalTransferOptions&gt;</code></p>
<p><code>               &lt;gmd:onLine&gt;</code></p>
<p><code>                 &lt;gmd:CI_OnlineResource&gt;</code></p>
<p><code>                     &lt;gmd:linkage&gt;</code></p>
<p><code>&lt;gmd:URL&gt;https://os.uk/oswebsite/products/boundaryline/&lt;/gmd:URL&gt;</code></p>
<p><code>                     &lt;/gmd:linkage&gt;</code></p>
<p><code>                     &lt;gmd:function&gt;</code></p>
<p><code>                       &lt;gmd:CI_OnLineFunctionCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_OnLineFunctionCode"</code></p>
<p><code>codeListValue="information"&gt;information&lt;/gmd:CI_OnLineFunctionCode&gt;</code></p>
<p><code>                     &lt;/gmd:function&gt;</code></p>
<p><code>                 &lt;/gmd:CI_OnlineResource&gt;</code></p>
<p><code>               &lt;/gmd:onLine&gt;</code></p>
<p><code>           &lt;/gmd:MD_DigitalTransferOptions&gt;</code></p>
<p><code>         &lt;/gmd:transferOptions&gt;</code></p>
<p><code>     &lt;/gmd:MD_Distribution&gt;</code></p>
<p><code>&lt;/gmd:distributionInfo&gt;</code></p>
<p><code>&lt;gmd:dataQualityInfo&gt;</code></p>
<p><code>     &lt;gmd:DQ_DataQuality&gt;</code></p>
<p><code>         &lt;gmd:scope&gt;</code></p>
<p><code>           &lt;gmd:DQ_Scope&gt;</code></p>
<p><code>               &lt;gmd:level&gt;</code></p>
<p><code>                 &lt;gmd:MD_ScopeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_ScopeCode"</code></p>
<p><code>codeListValue="dataset"&gt;dataset&lt;/gmd:MD_ScopeCode&gt;</code></p>
<p><code>               &lt;/gmd:level&gt;</code></p>
<p><code>           &lt;/gmd:DQ_Scope&gt;</code></p>
<p><code>         &lt;/gmd:scope&gt;</code></p>
<p><code>         &lt;gmd:report&gt;<br />                &lt;gmd:DQ_DomainConsistency&gt;<br />                    &lt;gmd:result&gt;<br />                        &lt;gmd:DQ_ConformanceResult&gt;<br />                            &lt;gmd:specification&gt;<br />                                &lt;gmd:CI_Citation&gt;<br />                                    &lt;gmd:title&gt;<br />                                        &lt;gmx:Anchor xlink:href="http://data.europa.eu/eli/reg/2010/1089"&gt;Commission Regulation (EU) No 1089/2010 of 23 November 2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data sets and services&lt;/gmx:Anchor&gt;<br />                                    &lt;/gmd:title&gt;<br />                                    &lt;gmd:date&gt;<br />                                        &lt;gmd:CI_Date&gt;<br />                                            &lt;gmd:date&gt;<br />                                                &lt;gco:Date&gt;2010-12-08&lt;/gco:Date&gt;<br />                                            &lt;/gmd:date&gt;<br />                                            &lt;gmd:dateType&gt;<br />                                                &lt;gmd:CI_DateTypeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_DateTypeCode" codeListValue="publication"/&gt;<br />                                            &lt;/gmd:dateType&gt;<br />                                        &lt;/gmd:CI_Date&gt;<br />                                    &lt;/gmd:date&gt;<br />                                &lt;/gmd:CI_Citation&gt;<br />                            &lt;/gmd:specification&gt;<br />                            &lt;!-- Explanation is a required element but can be empty --&gt;<br />                            &lt;gmd:explanation gco:nilReason="inapplicable"/&gt;<br />                            &lt;!-- If not tested then --&gt;<br />                            &lt;gmd:pass gco:nilReason="unknown"/&gt;<br />                        &lt;/gmd:DQ_ConformanceResult&gt;<br />                    &lt;/gmd:result&gt;<br />                &lt;/gmd:DQ_DomainConsistency&gt;<br />           &lt;/gmd:report&gt;</code></p>
<p><code>         &lt;gmd:lineage&gt;</code></p>
<p><code>           &lt;gmd:LI_Lineage&gt;</code></p>
<p><code>               &lt;gmd:statement&gt;</code></p>
<p><code>                 &lt;gco:CharacterString&gt;Captured and maintained solely from legal boundary changes&lt;/gco:CharacterString&gt;</code></p>
<p><code>               &lt;/gmd:statement&gt;</code></p>
<p><code>           &lt;/gmd:LI_Lineage&gt;</code></p>
<p><code>         &lt;/gmd:lineage&gt;</code></p>
<p><code>     &lt;/gmd:DQ_DataQuality&gt;</code></p>
<p><code>  &lt;/gmd:dataQualityInfo&gt;</code></p>
<p><code>&lt;/gmd:MD_Metadata&gt;</code></p>

<p style="padding-left: 30px;"><a title="Series metadata instance example" href="/40-gemini/1043-series-metadata-example-old" target="_blank" rel="alternate noopener noreferrer">Series metadata instance example</a></p>

<p>An example of a schema and Schematron valid metadata instance is shown below.</p>
<p><code>&lt;?xml version="1.0" encoding="utf-8"?&gt;</code></p>
<p><code>&lt;gmd:MD_Metadata xmlns:gsr="http://www.isotc211.org/2005/gsr"</code></p>
<p><code>                 xmlns:xlink="http://www.w3.org/1999/xlink" </code></p>
<p><code>                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"</code></p>
<p><code>                 xmlns:gss="http://www.isotc211.org/2005/gss"</code></p>
<p><code>                 xmlns:gts="http://www.isotc211.org/2005/gts"</code></p>
<p><code>                 xmlns:gml="http://www.opengis.net/gml/3.2"</code></p>
<p><code>                 xmlns:gmx="http://www.isotc211.org/2005/gmx"</code></p>
<p><code>                 xmlns:srv="http://www.isotc211.org/2005/srv"</code></p>
<p><code>                 xmlns:gco="http://www.isotc211.org/2005/gco"</code></p>
<p><code>                 xmlns:gmd="http://www.isotc211.org/2005/gmd"&gt;</code></p>
<p><code>&lt;gmd:fileIdentifier&gt;</code></p>
<p><code>    &lt;gco:CharacterString&gt;7928d609-e225-494c-ab79-99b92de8b5bb&lt;/gco:CharacterString&gt;</code></p>
<p><code>  &lt;/gmd:fileIdentifier&gt;</code></p>
<p><code>  &lt;gmd:language&gt;</code></p>
<p><code>    &lt;gmd:LanguageCode codeList="http://www.loc.gov/standards/iso639-2/php/code_list.php" codeListValue="eng"&gt;eng&lt;/gmd:LanguageCode&gt;</code></p>
<p><code>  &lt;/gmd:language&gt;</code></p>
<p><code>  &lt;gmd:hierarchyLevel&gt;</code></p>
<p><code>    &lt;gmd:MD_ScopeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_ScopeCode" codeListValue="series"&gt;series&lt;/gmd:MD_ScopeCode&gt;</code></p>
<p><code>  &lt;/gmd:hierarchyLevel&gt;</code></p>
<p><code>  &lt;gmd:hierarchyLevelName&gt;</code></p>
<p><code>    &lt;gco:CharacterString&gt;10k Raster&lt;/gco:CharacterString&gt;</code></p>
<p><code>  &lt;/gmd:hierarchyLevelName&gt;</code></p>
<p><code>  &lt;gmd:contact&gt;</code></p>
<p><code>    &lt;gmd:CI_ResponsibleParty&gt;</code></p>
<p><code>      &lt;gmd:organisationName&gt;</code></p>
<p><code>        &lt;gco:CharacterString&gt;Ordnance Survey&lt;/gco:CharacterString&gt;</code></p>
<p><code>     &lt;/gmd:organisationName&gt;</code></p>
<p><code>      &lt;gmd:contactInfo&gt;</code></p>
<p><code>        &lt;gmd:CI_Contact&gt;</code></p>
<p><code>          &lt;gmd:phone&gt;</code></p>
<p><code>            &lt;gmd:CI_Telephone&gt;</code></p>
<p><code>             &lt;gmd:voice&gt;</code></p>
<p><code>                &lt;gco:CharacterString&gt;+44 (0)8456 050505&lt;/gco:CharacterString&gt;</code></p>
<p><code>              &lt;/gmd:voice&gt;</code></p>
<p><code>              &lt;gmd:facsimile&gt;</code></p>
<p><code>                &lt;gco:CharacterString&gt;+44 (0)23 80792615&lt;/gco:CharacterString&gt;</code></p>
<p><code>              &lt;/gmd:facsimile&gt;</code></p>
<p><code>            &lt;/gmd:CI_Telephone&gt;</code></p>
<p><code>          &lt;/gmd:phone&gt;</code></p>
<p><code>          &lt;gmd:address&gt;</code></p>
<p><code>            &lt;gmd:CI_Address&gt;</code></p>
<p><code>              &lt;gmd:deliveryPoint&gt;</code></p>
<p><code>                &lt;gco:CharacterString&gt;Ordnance Survey&lt;/gco:CharacterString&gt;</code></p>
<p><code>              &lt;/gmd:deliveryPoint&gt;</code></p>
<p><code>              &lt;gmd:deliveryPoint&gt;</code></p>
<p><code>                &lt;gco:CharacterString&gt;Romsey Road&lt;/gco:CharacterString&gt;</code></p>
<p><code>              &lt;/gmd:deliveryPoint&gt;</code></p>
<p><code>              &lt;gmd:city&gt;</code></p>
<p><code>                &lt;gco:CharacterString&gt;Southampton&lt;/gco:CharacterString&gt;</code></p>
<p><code>              &lt;/gmd:city&gt;</code></p>
<p><code>              &lt;gmd:postalCode&gt;</code></p>
<p><code>                &lt;gco:CharacterString&gt;SO16 4GU&lt;/gco:CharacterString&gt;</code></p>
<p><code>             &lt;/gmd:postalCode&gt;</code></p>
<p><code>              &lt;gmd:electronicMailAddress&gt;</code></p>
<p><code>&lt;gco:CharacterString&gt;<span id="cloake23688d210e66ecfa9eacfb3d95c45b7">This email address is being protected from spambots. You need JavaScript enabled to view it.</span><script type='text/javascript'>
				document.getElementById('cloake23688d210e66ecfa9eacfb3d95c45b7').innerHTML = '';
				var prefix = '&#109;a' + 'i&#108;' + '&#116;o';
				var path = 'hr' + 'ef' + '=';
				var addye23688d210e66ecfa9eacfb3d95c45b7 = 'c&#117;st&#111;m&#101;rs&#101;rv&#105;c&#101;s' + '&#64;';
				addye23688d210e66ecfa9eacfb3d95c45b7 = addye23688d210e66ecfa9eacfb3d95c45b7 + '&#111;rdn&#97;nc&#101;s&#117;rv&#101;y' + '&#46;' + 'c&#111;' + '&#46;' + '&#117;k';
				var addy_texte23688d210e66ecfa9eacfb3d95c45b7 = 'c&#117;st&#111;m&#101;rs&#101;rv&#105;c&#101;s' + '&#64;' + '&#111;rdn&#97;nc&#101;s&#117;rv&#101;y' + '&#46;' + 'c&#111;' + '&#46;' + '&#117;k';document.getElementById('cloake23688d210e66ecfa9eacfb3d95c45b7').innerHTML += '<a ' + path + '\'' + prefix + ':' + addye23688d210e66ecfa9eacfb3d95c45b7 + '\'>'+addy_texte23688d210e66ecfa9eacfb3d95c45b7+'<\/a>';
		</script>&lt;/gco:CharacterString&gt;</code></p>
<p><code>             &lt;/gmd:electronicMailAddress&gt;</code></p>
<p><code>            &lt;/gmd:CI_Address&gt;</code></p>
<p><code>          &lt;/gmd:address&gt;</code></p>
<p><code>          &lt;gmd:onlineResource&gt;</code></p>
<p><code>            &lt;gmd:CI_OnlineResource&gt;</code></p>
<p><code>             &lt;gmd:linkage&gt;</code></p>
<p><code>                &lt;gmd:URL&gt;http://www.ordnancesurvey.co.uk&lt;/gmd:URL&gt;</code></p>
<p><code>              &lt;/gmd:linkage&gt;</code></p>
<p><code>            &lt;/gmd:CI_OnlineResource&gt;</code></p>
<p><code>          &lt;/gmd:onlineResource&gt;</code></p>
<p><code>        &lt;/gmd:CI_Contact&gt;</code></p>
<p><code>      &lt;/gmd:contactInfo&gt;</code></p>
<p><code>      &lt;gmd:role&gt;</code></p>
<p><code>        &lt;gmd:CI_RoleCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_RoleCode" codeListValue="pointOfContact"&gt;pointOfContact&lt;/gmd:CI_RoleCode&gt;</code></p>
<p><code>     &lt;/gmd:role&gt;</code></p>
<p><code>    &lt;/gmd:CI_ResponsibleParty&gt;</code></p>
<p><code>  &lt;/gmd:contact&gt;</code></p>
<p><code>  &lt;gmd:dateStamp&gt;</code></p>
<p><code>    &lt;gco:Date&gt;2010-09-09&lt;/gco:Date&gt;</code></p>
<p><code>  &lt;/gmd:dateStamp&gt;</code></p>
<p><code>&lt;gmd:referenceSystemInfo&gt;</code></p>
<p><code>    &lt;gmd:MD_ReferenceSystem&gt;</code></p>
<p><code>     &lt;gmd:referenceSystemIdentifier&gt;</code></p>
<p><code>        &lt;gmd:RS_Identifier&gt;</code></p>
<p><code>          &lt;gmd:code&gt;</code></p>
<p><code>&lt;gco:CharacterString&gt; http://www.opengis.net/def/crs/EPSG/0/27700&lt;/gco:CharacterString&gt;</code></p>
<p><code>         &lt;/gmd:code&gt;</code></p>
<p><code>        &lt;/gmd:RS_Identifier&gt;</code></p>
<p><code>      &lt;/gmd:referenceSystemIdentifier&gt;</code></p>
<p><code>    &lt;/gmd:MD_ReferenceSystem&gt;</code></p>
<p><code>  &lt;/gmd:referenceSystemInfo&gt;</code></p>
<p><code>  &lt;gmd:identificationInfo&gt;</code></p>
<p><code>    &lt;gmd:MD_DataIdentification&gt;</code></p>
<p><code>      &lt;gmd:citation&gt;</code></p>
<p><code>        &lt;gmd:CI_Citation&gt;</code></p>
<p><code>         &lt;gmd:title&gt;</code></p>
<p><code>            &lt;gco:CharacterString&gt;1:10 000 Scale Raster&lt;/gco:CharacterString&gt;</code></p>
<p><code>          &lt;/gmd:title&gt;</code></p>
<p><code>          &lt;gmd:alternateTitle&gt;</code></p>
<p><code>            &lt;gco:CharacterString&gt;10k Raster&lt;/gco:CharacterString&gt;</code></p>
<p><code>         &lt;/gmd:alternateTitle&gt;</code></p>
<p><code>          &lt;gmd:date&gt;</code></p>
<p><code>            &lt;gmd:CI_Date&gt;</code></p>
<p><code>              &lt;gmd:date&gt;</code></p>
<p><code>                &lt;gco:Date&gt;2010-05-12&lt;/gco:Date&gt;</code></p>
<p><code>              &lt;/gmd:date&gt;</code></p>
<p><code>              &lt;gmd:dateType&gt;</code></p>
<p><code>                &lt;gmd:CI_DateTypeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_DateTypeCode" codeListValue="revision"&gt;revision&lt;/gmd:CI_DateTypeCode&gt;</code></p>
<p><code>              &lt;/gmd:dateType&gt;</code></p>
<p><code>            &lt;/gmd:CI_Date&gt;</code></p>
<p><code>          &lt;/gmd:date&gt;</code></p>
<p><code>          &lt;gmd:identifier&gt;</code></p>
<p><code>            &lt;gmd:RS_Identifier&gt;</code></p>
<p><code>             &lt;gmd:code&gt;</code></p>
<p><code>                &lt;gco:CharacterString&gt;OS_10k_Raster&lt;/gco:CharacterString&gt;</code></p>
<p><code>             &lt;/gmd:code&gt;</code></p>
<p><code>              &lt;gmd:codeSpace&gt;</code></p>
<p><code>&lt;gco:CharacterString&gt;http://www.ordnancesurvey.co.uk&lt;/gco:CharacterString&gt;</code></p>
<p><code>              &lt;/gmd:codeSpace&gt;</code></p>
<p><code>            &lt;/gmd:RS_Identifier&gt;</code></p>
<p><code>          &lt;/gmd:identifier&gt;</code></p>
<p><code>        &lt;/gmd:CI_Citation&gt;</code></p>
<p><code>     &lt;/gmd:citation&gt;</code></p>
<p><code>      &lt;gmd:abstract&gt;</code></p>
<p><code>        &lt;gco:CharacterString&gt;Detailed raster mapping generated from 1:10 000 scale vector Landplan data. For overlay of information, particularly useful for site analysis, planning and marketing in urban areas.&lt;/gco:CharacterString&gt;</code></p>
<p><code>      &lt;/gmd:abstract&gt;</code></p>
<p><code>      &lt;gmd:pointOfContact&gt;</code></p>
<p><code>        &lt;gmd:CI_ResponsibleParty&gt;</code></p>
<p><code>          &lt;gmd:organisationName&gt;</code></p>
<p><code>            &lt;gco:CharacterString&gt;Ordnance Survey&lt;/gco:CharacterString&gt;</code></p>
<p><code>         &lt;/gmd:organisationName&gt;</code></p>
<p><code>          &lt;gmd:contactInfo&gt;</code></p>
<p><code>            &lt;gmd:CI_Contact&gt;</code></p>
<p><code>              &lt;gmd:phone&gt;</code></p>
<p><code>                &lt;gmd:CI_Telephone&gt;</code></p>
<p><code>                 &lt;gmd:voice&gt;</code></p>
<p><code>                    &lt;gco:CharacterString&gt;+44 (0)8456 050505&lt;/gco:CharacterString&gt;</code></p>
<p><code>                  &lt;/gmd:voice&gt;</code></p>
<p><code>                  &lt;gmd:facsimile&gt;</code></p>
<p><code>                    &lt;gco:CharacterString&gt;+44 (0)23 80792615&lt;/gco:CharacterString&gt;</code></p>
<p><code>                  &lt;/gmd:facsimile&gt;</code></p>
<p><code>                &lt;/gmd:CI_Telephone&gt;</code></p>
<p><code>              &lt;/gmd:phone&gt;</code></p>
<p><code>              &lt;gmd:address&gt;</code></p>
<p><code>                &lt;gmd:CI_Address&gt;</code></p>
<p><code>                  &lt;gmd:deliveryPoint&gt;</code></p>
<p><code>                    &lt;gco:CharacterString&gt;Ordnance Survey&lt;/gco:CharacterString&gt;</code></p>
<p><code>                  &lt;/gmd:deliveryPoint&gt;</code></p>
<p><code>                  &lt;gmd:deliveryPoint&gt;</code></p>
<p><code>                  &lt;gco:CharacterString&gt;Romsey Road&lt;/gco:CharacterString&gt;</code></p>
<p><code>                  &lt;/gmd:deliveryPoint&gt;</code></p>
<p><code>                  &lt;gmd:city&gt;</code></p>
<p><code>                    &lt;gco:CharacterString&gt;Southampton&lt;/gco:CharacterString&gt;</code></p>
<p><code>                  &lt;/gmd:city&gt;</code></p>
<p><code>                  &lt;gmd:postalCode&gt;</code></p>
<p><code>                    &lt;gco:CharacterString&gt;SO16 4GU&lt;/gco:CharacterString&gt;</code></p>
<p><code>                 &lt;/gmd:postalCode&gt;</code></p>
<p><code>                  &lt;gmd:electronicMailAddress&gt;</code></p>
<p><code>&lt;gco:CharacterString&gt;<span id="cloak8289287e7c10421577643a7aeb626abe">This email address is being protected from spambots. You need JavaScript enabled to view it.</span><script type='text/javascript'>
				document.getElementById('cloak8289287e7c10421577643a7aeb626abe').innerHTML = '';
				var prefix = '&#109;a' + 'i&#108;' + '&#116;o';
				var path = 'hr' + 'ef' + '=';
				var addy8289287e7c10421577643a7aeb626abe = 'c&#117;st&#111;m&#101;rs&#101;rv&#105;c&#101;s' + '&#64;';
				addy8289287e7c10421577643a7aeb626abe = addy8289287e7c10421577643a7aeb626abe + '&#111;rdn&#97;nc&#101;s&#117;rv&#101;y' + '&#46;' + 'c&#111;' + '&#46;' + '&#117;k';
				var addy_text8289287e7c10421577643a7aeb626abe = 'c&#117;st&#111;m&#101;rs&#101;rv&#105;c&#101;s' + '&#64;' + '&#111;rdn&#97;nc&#101;s&#117;rv&#101;y' + '&#46;' + 'c&#111;' + '&#46;' + '&#117;k';document.getElementById('cloak8289287e7c10421577643a7aeb626abe').innerHTML += '<a ' + path + '\'' + prefix + ':' + addy8289287e7c10421577643a7aeb626abe + '\'>'+addy_text8289287e7c10421577643a7aeb626abe+'<\/a>';
		</script>&lt;/gco:CharacterString&gt;</code></p>
<p><code>                 &lt;/gmd:electronicMailAddress&gt;</code></p>
<p><code>                &lt;/gmd:CI_Address&gt;</code></p>
<p><code>              &lt;/gmd:address&gt;</code></p>
<p><code>              &lt;gmd:onlineResource&gt;</code></p>
<p><code>                &lt;gmd:CI_OnlineResource&gt;</code></p>
<p><code>                 &lt;gmd:linkage&gt;</code></p>
<p><code>                    &lt;gmd:URL&gt;http://www.ordnancesurvey.co.uk/&lt;/gmd:URL&gt;</code></p>
<p><code>                  &lt;/gmd:linkage&gt;</code></p>
<p><code>                &lt;/gmd:CI_OnlineResource&gt;</code></p>
<p><code>              &lt;/gmd:onlineResource&gt;</code></p>
<p><code>            &lt;/gmd:CI_Contact&gt;</code></p>
<p><code>          &lt;/gmd:contactInfo&gt;</code></p>
<p><code>          &lt;gmd:role&gt;</code></p>
<p><code>            &lt;gmd:CI_RoleCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_RoleCode" codeListValue="originator"&gt;originator&lt;/gmd:CI_RoleCode&gt;</code></p>
<p><code>          &lt;/gmd:role&gt;</code></p>
<p><code>        &lt;/gmd:CI_ResponsibleParty&gt;</code></p>
<p><code>      &lt;/gmd:pointOfContact&gt;</code></p>
<p><code>      &lt;gmd:resourceMaintenance&gt;</code></p>
<p><code>        &lt;gmd:MD_MaintenanceInformation&gt;</code></p>
<p><code>          &lt;gmd:maintenanceAndUpdateFrequency&gt;</code></p>
<p><code>            &lt;gmd:MD_MaintenanceFrequencyCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_MaintenanceFrequencyCode" codeListValue="continual"&gt;continual&lt;/gmd:MD_MaintenanceFrequencyCode&gt;</code></p>
<p><code>         &lt;/gmd:maintenanceAndUpdateFrequency&gt;</code></p>
<p><code>        &lt;/gmd:MD_MaintenanceInformation&gt;</code></p>
<p><code>      &lt;/gmd:resourceMaintenance&gt;</code></p>
<p><code>      &lt;gmd:descriptiveKeywords&gt;</code></p>
<p><code>        &lt;gmd:MD_Keywords&gt;</code></p>
<p><code>          &lt;gmd:keyword&gt;</code></p>
<p><code>            &lt;gco:CharacterString&gt;raster&lt;/gco:CharacterString&gt;</code></p>
<p><code>          &lt;/gmd:keyword&gt;</code></p>
<p><code>          &lt;gmd:keyword&gt;</code></p>
<p><code>            &lt;gco:CharacterString&gt;map&lt;/gco:CharacterString&gt;</code></p>
<p><code>          &lt;/gmd:keyword&gt;</code></p>
<p><code>          &lt;gmd:thesaurusName&gt;</code></p>
<p><code>            &lt;gmd:CI_Citation&gt;</code></p>
<p><code>              &lt;gmd:title&gt;</code></p>
<p><code>                &lt;gco:CharacterString&gt;GEMET - Concepts, version 2.4&lt;/gco:CharacterString&gt;</code></p>
<p><code>              &lt;/gmd:title&gt;</code></p>
<p><code>              &lt;gmd:date&gt;</code></p>
<p><code>                &lt;gmd:CI_Date&gt;</code></p>
<p><code>                  &lt;gmd:date&gt;</code></p>
<p><code>                    &lt;gco:Date&gt;2010-01-13&lt;/gco:Date&gt;</code></p>
<p><code>                  &lt;/gmd:date&gt;</code></p>
<p><code>                  &lt;gmd:dateType&gt;</code></p>
<p><code>                    &lt;gmd:CI_DateTypeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_DateTypeCode" codeListValue="publication" /&gt;</code></p>
<p><code>                 &lt;/gmd:dateType&gt;</code></p>
<p><code>                &lt;/gmd:CI_Date&gt;</code></p>
<p><code>             &lt;/gmd:date&gt;</code></p>
<p><code>              &lt;gmd:edition&gt;</code></p>
<p><code>                &lt;gco:CharacterString&gt;version 2.4&lt;/gco:CharacterString&gt;</code></p>
<p><code>             &lt;/gmd:edition&gt;</code></p>
<p><code>            &lt;/gmd:CI_Citation&gt;</code></p>
<p><code>         &lt;/gmd:thesaurusName&gt;</code></p>
<p><code>        &lt;/gmd:MD_Keywords&gt;</code></p>
<p><code>      &lt;/gmd:descriptiveKeywords&gt;</code></p>
<p><code></code></p>
<pre><code>       &lt;gmd:resourceConstraints&gt;</code><br /><code>         &lt;gmd:MD_LegalConstraints&gt;</code><br /> &lt;gmd:accessConstraints&gt;<br /> &lt;gmd:MD_RestrictionCode<br />codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_RestrictionCode"<br /> codeListValue="otherRestrictions"&gt;otherRestrictions&lt;/gmd:MD_RestrictionCode&gt;<br /> &lt;/gmd:accessConstraints&gt;<br /> &lt;gmd:otherConstraints&gt;<br /> &lt;gmx:Anchor xlink:href="http://inspire.ec.europa.eu/metadata-codelist/LimitationsOnPublicAccess/noLimitations"&gt;no limitations&lt;/gmx:Anchor&gt;<br /> &lt;/gmd:otherConstraints&gt;<br /> &lt;/gmd:MD_LegalConstraints&gt;<br /> &lt;/gmd:resourceConstraints&gt;<br /> &lt;gmd:resourceConstraints&gt;<br /> &lt;gmd:MD_LegalConstraints&gt;<br /> &lt;gmd:useConstraints&gt;<br /> &lt;gmd:MD_RestrictionCode<br />codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_RestrictionCode"<br /> codeListValue="otherRestrictions"&gt;otherRestrictions&lt;/gmd:MD_RestrictionCode&gt;<br /> &lt;/gmd:useConstraints&gt;<br /><code>           &lt;gmd:otherConstraints&gt;</code><br /><code>             &lt;gco:CharacterString&gt;The 1:625k DiGMap data is made available for all uses - including commercial use, however the British Geological Survey (BGS) at all times retains the copyright in this material and you are not permitted, without an appropriate licence, to set up a service selling on this material. Your own use of any information provided by the British Geological Survey (BGS) is at your own risk. Neither BGS nor the Natural Environment Research Council (NERC) gives any warranty, condition or representation as to the quality, accuracy or completeness of the information or its suitability for any use or purpose. All implied conditions relating to the quality or suitability of the information, and all liabilities arising from the supply of the information (including any liability arising in negligence) are excluded to the fullest extent permitted by law.&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:otherConstraints&gt;</code><br /><code></code> &lt;gmd:otherConstraints&gt;<br /><code>            &lt;gco:CharacterString&gt;Ordnance Survey data licensing terms and conditions&lt;/gco:CharacterString&gt;</code><code><br />          &lt;/gmd:otherConstraints&gt;</code></pre>
<p><code>        &lt;/gmd:MD_LegalConstraints&gt;</code></p>
<p><code>      &lt;/gmd:resourceConstraints&gt;</code></p>
<p><code>      &lt;gmd:resourceConstraints&gt;</code></p>
<p><code>        &lt;gmd:MD_Constraints&gt;</code></p>
<p><code>          &lt;gmd:useLimitation&gt;</code></p>
<p><code>            &lt;gco:CharacterString&gt;Annual license fee for use of the data for internal business use including paper copies. Separate license fees and conditions for specific use to third parties&lt;/gco:CharacterString&gt;</code></p>
<p><code>          &lt;/gmd:useLimitation&gt;</code></p>
<p><code>        &lt;/gmd:MD_Constraints&gt;</code></p>
<p><code>      &lt;/gmd:resourceConstraints&gt;</code></p>
<p><code>      &lt;gmd:spatialResolution&gt;</code></p>
<p><code>        &lt;gmd:MD_Resolution&gt;</code></p>
<p><code>          &lt;gmd:equivalentScale&gt;</code></p>
<p><code>            &lt;gmd:MD_RepresentativeFraction&gt;</code></p>
<p><code>             &lt;gmd:denominator&gt;</code></p>
<p><code>               &lt;gco:Integer&gt;10000&lt;/gco:Integer&gt;</code></p>
<p><code>              &lt;/gmd:denominator&gt;</code></p>
<p><code>           &lt;/gmd:MD_RepresentativeFraction&gt;</code></p>
<p><code>          &lt;/gmd:equivalentScale&gt;</code></p>
<p><code>        &lt;/gmd:MD_Resolution&gt;</code></p>
<p><code>      &lt;/gmd:spatialResolution&gt;</code></p>
<p><code>      &lt;gmd:language&gt;</code></p>
<p><code>        &lt;gmd:LanguageCode codeList="http://www.loc.gov/standards/iso639-2/php/code_list.php" codeListValue="eng"&gt;eng&lt;/gmd:LanguageCode&gt;</code></p>
<p><code>      &lt;/gmd:language&gt;</code></p>
<p><code>      &lt;gmd:topicCategory&gt;</code></p>
<p><code>&lt;gmd:MD_TopicCategoryCode&gt;imageryBaseMapsEarthCover&lt;/gmd:MD_TopicCategoryCode&gt;</code></p>
<p><code>      &lt;/gmd:topicCategory&gt;</code></p>
<p><code>      &lt;gmd:extent&gt;</code></p>
<p><code>        &lt;gmd:EX_Extent&gt;</code></p>
<p><code>          &lt;gmd:geographicElement&gt;</code></p>
<p><code>            &lt;gmd:EX_GeographicBoundingBox&gt;</code></p>
<p><code>              &lt;gmd:westBoundLongitude&gt;</code></p>
<p><code>                &lt;gco:Decimal&gt;-8.45472&lt;/gco:Decimal&gt;</code></p>
<p><code>              &lt;/gmd:westBoundLongitude&gt;</code></p>
<p><code>              &lt;gmd:eastBoundLongitude&gt;</code></p>
<p><code>                &lt;gco:Decimal&gt;1.78024&lt;/gco:Decimal&gt;</code></p>
<p><code>              &lt;/gmd:eastBoundLongitude&gt;</code></p>
<p><code>              &lt;gmd:southBoundLatitude&gt;</code></p>
<p><code>              &lt;gco:Decimal&gt;49.8634&lt;/gco:Decimal&gt;</code></p>
<p><code>              &lt;/gmd:southBoundLatitude&gt;</code></p>
<p><code>              &lt;gmd:northBoundLatitude&gt;</code></p>
<p><code>                &lt;gco:Decimal&gt;60.8599&lt;/gco:Decimal&gt;</code></p>
<p><code>              &lt;/gmd:northBoundLatitude&gt;</code></p>
<p><code>            &lt;/gmd:EX_GeographicBoundingBox&gt;</code></p>
<p><code>         &lt;/gmd:geographicElement&gt;</code></p>
<p><code>          &lt;gmd:temporalElement&gt;</code></p>
<p><code>            &lt;gmd:EX_TemporalExtent&gt;</code></p>
<p><code>             &lt;gmd:extent&gt;</code></p>
<p><code>                &lt;gml:TimePeriod gml:id="_75c1e6a9-44ff-4aef-b923-c1b6f59d53a6"&gt;</code></p>
<p><code>                  &lt;gml:beginPosition&gt;2003-03-04&lt;/gml:beginPosition&gt;</code></p>
<p><code>                  &lt;gml:endPosition&gt;2010-05-12&lt;/gml:endPosition&gt;</code></p>
<p><code>                &lt;/gml:TimePeriod&gt;</code></p>
<p><code>             &lt;/gmd:extent&gt;</code></p>
<p><code>            &lt;/gmd:EX_TemporalExtent&gt;</code></p>
<p><code>          &lt;/gmd:temporalElement&gt;</code></p>
<p><code>        &lt;/gmd:EX_Extent&gt;</code></p>
<p><code>      &lt;/gmd:extent&gt;</code></p>
<p><code>      &lt;gmd:supplementalInformation&gt;</code></p>
<p><code>&lt;gco:CharacterString&gt;http://www.ordnancesurvey.co.uk/oswebsite/products/10kraster/&lt;/gco:CharacterString&gt;</code></p>
<p><code>      &lt;/gmd:supplementalInformation&gt;</code></p>
<p><code>    &lt;/gmd:MD_DataIdentification&gt;</code></p>
<p><code>&lt;/gmd:identificationInfo&gt;</code></p>
<p><code>  &lt;gmd:dataQualityInfo&gt;</code></p>
<p><code>    &lt;gmd:DQ_DataQuality&gt;</code></p>
<p><code>      &lt;gmd:scope&gt;</code></p>
<p><code>        &lt;gmd:DQ_Scope&gt;</code></p>
<p><code>          &lt;gmd:level&gt;</code></p>
<p><code>            &lt;gmd:MD_ScopeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_ScopeCode" codeListValue="series"&gt;series&lt;/gmd:MD_ScopeCode&gt;</code></p>
<p><code>          &lt;/gmd:level&gt;</code></p>
<p><code>        &lt;/gmd:DQ_Scope&gt;</code></p>
<p><code>      &lt;/gmd:scope&gt;</code></p>
<p><code>      &lt;gmd:lineage&gt;</code></p>
<p><code>        &lt;gmd:LI_Lineage&gt;</code></p>
<p><code>          &lt;gmd:statement&gt;</code></p>
<p><code>            &lt;gco:CharacterString&gt;Unknown&lt;/gco:CharacterString&gt;</code></p>
<p><code>          &lt;/gmd:statement&gt;</code></p>
<p><code>        &lt;/gmd:LI_Lineage&gt;</code></p>
<p><code>      &lt;/gmd:lineage&gt;</code></p>
<p><code>    &lt;/gmd:DQ_DataQuality&gt;</code></p>
<p><code>  &lt;/gmd:dataQualityInfo&gt;</code></p>
<p><code>&lt;/gmd:MD_Metadata&gt;</code></p>
<p><em>Last updated: April 2018</em><code></code></p>

<p style="padding-left: 30px;"><a title="Service metadata instance example" href="/40-gemini/1042-service-metadata-instance-example" target="_blank" rel="alternate noopener noreferrer">Service metadata instance example</a></p>

<p>An example of a schema and Schematron valid service metadata instance is shown below.</p>
<pre><code>&lt;?xml version="1.0" encoding="UTF-8"?&gt;</code><br /><code>&lt;gmd:MD_Metadata xmlns:gmd="http://www.isotc211.org/2005/gmd"</code><br /><code>                   xmlns:gco="http://www.isotc211.org/2005/gco"</code><br /><code>                   xmlns:gml="http://www.opengis.net/gml/3.2"</code><br /><code>                   xmlns:gmx="http://www.isotc211.org/2005/gmx"</code><br /><code>                   xmlns:gsr="http://www.isotc211.org/2005/gsr"</code><br /><code>                   xmlns:gss="http://www.isotc211.org/2005/gss"</code><br /><code>                   xmlns:gts="http://www.isotc211.org/2005/gts"</code><br /><code>                   xmlns:srv="http://www.isotc211.org/2005/srv"</code><br /><code>                   xmlns:xlink="http://www.w3.org/1999/xlink"&gt;</code><br /><code>   &lt;gmd:fileIdentifier&gt;</code><br /><code>     &lt;gco:CharacterString&gt;a0a82d76-657c-2a78-e044-0003ba9b0d98&lt;/gco:CharacterString&gt;</code><br /><code>   &lt;/gmd:fileIdentifier&gt;</code><br /><code>   &lt;gmd:language&gt;</code><br /><code>     &lt;gmd:LanguageCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/ML_gmxCodelists.xml#LanguageCode" codeListValue="eng"&gt;English&lt;/gmd:LanguageCode&gt;</code><br /><code>   &lt;/gmd:language&gt;</code><br /><code>   &lt;gmd:hierarchyLevel&gt;</code><br /><code>     &lt;gmd:MD_ScopeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_ScopeCode" codeListValue="service"&gt;service&lt;/gmd:MD_ScopeCode&gt;</code><br /><code>   &lt;/gmd:hierarchyLevel&gt;</code><br /><code>   &lt;gmd:hierarchyLevelName&gt;</code><br /><code>     &lt;gco:CharacterString&gt;service&lt;/gco:CharacterString&gt;</code><br /><code>   &lt;/gmd:hierarchyLevelName&gt;</code><br /><code>   &lt;gmd:contact&gt;</code><br /><code>     &lt;gmd:CI_ResponsibleParty&gt;</code><br /><code>       &lt;gmd:organisationName&gt;</code><br /><code>         &lt;gco:CharacterString&gt;British Geological Survey&lt;/gco:CharacterString&gt;</code><br /><code>       &lt;/gmd:organisationName&gt;</code><br /><code>       &lt;gmd:contactInfo&gt;</code><br /><code>         &lt;gmd:CI_Contact&gt;</code><br /><code>           &lt;gmd:phone&gt;</code><br /><code>             &lt;gmd:CI_Telephone&gt;</code><br /><code>               &lt;gmd:voice&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;+44 115 936 3100 Ex:3115&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:voice&gt;</code><br /><code>             &lt;/gmd:CI_Telephone&gt;</code><br /><code>           &lt;/gmd:phone&gt;</code><br /><code>           &lt;gmd:address&gt;</code><br /><code>             &lt;gmd:CI_Address&gt;</code><br /><code>               &lt;gmd:deliveryPoint&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;Murchison House, West Mains Road, Edinburgh, Lothian, United Kingdom, EH9 3LA, NG12 5GG&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:deliveryPoint&gt;</code><br /><code>               &lt;gmd:city&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;EDINBURGH&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:city&gt;</code><br /><code>               &lt;gmd:administrativeArea&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;LOTHIAN&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:administrativeArea&gt;</code><br /><code>               &lt;gmd:postalCode&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;EH9 3LA&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:postalCode&gt;</code><br /><code>               &lt;gmd:country&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;United Kingdom&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:country&gt;</code><br /><code>               &lt;gmd:electronicMailAddress&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;<span id="cloak99b1ae6b71a057239b1acb7aa3bdaa55">This email address is being protected from spambots. You need JavaScript enabled to view it.</span><script type='text/javascript'>
				document.getElementById('cloak99b1ae6b71a057239b1acb7aa3bdaa55').innerHTML = '';
				var prefix = '&#109;a' + 'i&#108;' + '&#116;o';
				var path = 'hr' + 'ef' + '=';
				var addy99b1ae6b71a057239b1acb7aa3bdaa55 = '&#101;nq&#117;&#105;r&#105;&#101;s' + '&#64;';
				addy99b1ae6b71a057239b1acb7aa3bdaa55 = addy99b1ae6b71a057239b1acb7aa3bdaa55 + 'bgs' + '&#46;' + '&#97;c' + '&#46;' + '&#117;k';
				var addy_text99b1ae6b71a057239b1acb7aa3bdaa55 = '&#101;nq&#117;&#105;r&#105;&#101;s' + '&#64;' + 'bgs' + '&#46;' + '&#97;c' + '&#46;' + '&#117;k';document.getElementById('cloak99b1ae6b71a057239b1acb7aa3bdaa55').innerHTML += '<a ' + path + '\'' + prefix + ':' + addy99b1ae6b71a057239b1acb7aa3bdaa55 + '\'>'+addy_text99b1ae6b71a057239b1acb7aa3bdaa55+'<\/a>';
		</script>&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:electronicMailAddress&gt;</code><br /><code>             &lt;/gmd:CI_Address&gt;</code><br /><code>           &lt;/gmd:address&gt;</code><br /><code>         &lt;/gmd:CI_Contact&gt;</code><br /><code>       &lt;/gmd:contactInfo&gt;</code><br /><code>       &lt;gmd:role&gt;</code><br /><code>         &lt;gmd:CI_RoleCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_RoleCode" codeListValue="pointOfContact"&gt;pointOfContact&lt;/gmd:CI_RoleCode&gt;</code><br /><code>       &lt;/gmd:role&gt;</code><br /><code>     &lt;/gmd:CI_ResponsibleParty&gt;</code><br /><code>   &lt;/gmd:contact&gt;</code><br /><code>   &lt;gmd:dateStamp&gt;</code><br /><code>     &lt;gco:Date&gt;2011-04-11&lt;/gco:Date&gt;</code><br /><code>   &lt;/gmd:dateStamp&gt;</code><br /><code>   &lt;gmd:metadataStandardName&gt;</code><br /><code>     &lt;gco:CharacterString&gt;ISO19115:2003(E)&lt;/gco:CharacterString&gt;</code><br /><code>   &lt;/gmd:metadataStandardName&gt;</code><br /><code>   &lt;gmd:metadataStandardVersion&gt;</code><br /><code>     &lt;gco:CharacterString&gt;GEMINI:2&lt;/gco:CharacterString&gt;</code><br /><code>   &lt;/gmd:metadataStandardVersion&gt;</code><br /><code>   &lt;gmd:referenceSystemInfo&gt;</code><br /><code>     &lt;gmd:MD_ReferenceSystem&gt;</code><br /><code>       &lt;gmd:referenceSystemIdentifier&gt;</code><br /><code>         &lt;gmd:RS_Identifier&gt;</code><br /><code>           &lt;gmd:authority&gt;</code><br /><code>             &lt;gmd:CI_Citation&gt;</code><br /><code>               &lt;gmd:title&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;www.epsg.org&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:title&gt;</code><br /><code>               &lt;gmd:date&gt;</code><br /><code>                 &lt;gmd:CI_Date&gt;</code><br /><code>                   &lt;gmd:date&gt;</code><br /><code>                     &lt;gco:Date&gt;2005&lt;/gco:Date&gt;</code><br /><code>                   &lt;/gmd:date&gt;</code><br /><code>                   &lt;gmd:dateType&gt;</code><br /><code>                     &lt;gmd:CI_DateTypeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_DateTypeCode" codeListValue="revision"&gt;revision&lt;/gmd:CI_DateTypeCode&gt;</code><br /><code>                   &lt;/gmd:dateType&gt;</code><br /><code>                 &lt;/gmd:CI_Date&gt;</code><br /><code>               &lt;/gmd:date&gt;</code><br /><code>             &lt;/gmd:CI_Citation&gt;</code><br /><code>           &lt;/gmd:authority&gt;</code><br /><code>           &lt;gmd:code&gt;</code><br /><code>             &lt;gmx:Anchor xlink:href="http://www.opengis.net/def/crs/EPSG/0/4258"&gt;ETRS89-GRS80&lt;/gmx:Anchor&gt;</code><br /><code>           &lt;/gmd:code&gt;</code><br /><code>         </code><code>&lt;/gmd:RS_Identifier&gt;</code><br /><code>       &lt;/gmd:referenceSystemIdentifier&gt;</code><br /><code>     &lt;/gmd:MD_ReferenceSystem&gt;</code><br /><code>   &lt;/gmd:referenceSystemInfo&gt;</code><br /><code>   &lt;gmd:identificationInfo&gt;</code><br /><code>     &lt;srv:SV_ServiceIdentification&gt;</code><br /><code>       &lt;gmd:citation&gt;</code><br /><code>         &lt;gmd:CI_Citation&gt;</code><br /><code>           &lt;gmd:title&gt;</code><br /><code>             &lt;gco:CharacterString&gt;BGS Surface geology (OGC WxS INSPIRE IOC)&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:title&gt;</code><br /><code>           &lt;gmd:date&gt;</code><br /><code>             &lt;gmd:CI_Date&gt;</code><br /><code>               &lt;gmd:date&gt;</code><br /><code>                 &lt;gco:Date&gt;1995&lt;/gco:Date&gt;</code><br /><code>               &lt;/gmd:date&gt;</code><br /><code>               &lt;gmd:dateType&gt;</code><br /><code>                  &lt;gmd:CI_DateTypeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_DateTypeCode" codeListValue="publication"&gt;publication&lt;/gmd:CI_DateTypeCode&gt;</code><br /><code>               &lt;/gmd:dateType&gt;</code><br /><code>             &lt;/gmd:CI_Date&gt;</code><br /><code>           &lt;/gmd:date&gt;</code><br /><code>           &lt;gmd:identifier&gt;</code><br /><code>             &lt;gmd:MD_Identifier&gt;</code><br /><code>               &lt;gmd:code&gt;</code><br /><code>                 &lt;gmx:Anchor xlink:href="http://data.bgs.ac.uk/id/dataHolding/13605559"&gt;BGS Surface geology&lt;/gmx:Anchor&gt;                 </code><br /><code>               &lt;/gmd:code&gt;</code><br /><code>             &lt;</code><code>/gmd:MD_Identifier&gt;</code><br /><code>           &lt;/gmd:identifier&gt;</code><br /><code>         &lt;/gmd:CI_Citation&gt;</code><br /><code>       &lt;/gmd:citation&gt;</code><br /><code>       &lt;gmd:abstract&gt;</code><br /><code>         &lt;gco:CharacterString&gt;Data from the DiGMap covering the whole of the United Kingdom at a scale of 1:625 000 is available in this OGC WMS service for personal, non-commercial use only. The service is a contribution to the OneGeology-Europe initiative. The layers can be displayed either by age or by lithology. For more information about the digital maps available from the British Geological Survey, please visit http://www.bgs.ac.uk/products/digitalmaps/digmapgb.html.&lt;/gco:CharacterString&gt;</code><br /><code>       &lt;/gmd:abstract&gt;</code><br /><code>       &lt;gmd:pointOfContact&gt;</code><br /><code>         &lt;gmd:CI_ResponsibleParty&gt;</code><br /><code>           &lt;gmd:individualName&gt;</code><br /><code>             &lt;gco:CharacterString&gt;Westhead,Keith Robert&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:individualName&gt;</code><br /><code>           &lt;gmd:organisationName&gt;</code><br /><code>             &lt;gco:CharacterString&gt;British Geological Survey&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:organisationName&gt;</code><br /><code>           &lt;gmd:positionName&gt;</code><br /><code>             &lt;gco:CharacterString&gt;HoS - Information Delivery&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:positionName&gt;</code><br /><code>           &lt;gmd:contactInfo&gt;</code><br /><code>             &lt;gmd:CI_Contact&gt;</code><br /><code>               &lt;gmd:phone&gt;</code><br /><code>                 &lt;gmd:CI_Telephone&gt;</code><br /><code>                   &lt;gmd:voice&gt;</code><br /><code>                     &lt;gco:CharacterString&gt;+44 131 667 1000 Ex:364&lt;/gco:CharacterString&gt;</code><br /><code>                   &lt;/gmd:voice&gt;</code><br /><code>                 &lt;/gmd:CI_Telephone&gt;</code><br /><code>               &lt;/gmd:phone&gt;</code><br /><code>               &lt;gmd:address&gt;</code><br /><code>                 &lt;gmd:CI_Address&gt;</code><br /><code>                   &lt;gmd:deliveryPoint&gt;</code><br /><code>                     &lt;gco:CharacterString&gt;Murchison House, West Mains Road, Edinburgh, Lothian, United Kingdom, EH9 3LA, NG12 5GG&lt;/gco:CharacterString&gt;</code><br /><code>                   &lt;/gmd:deliveryPoint&gt;</code><br /><code>                   &lt;gmd:city&gt;</code><br /><code>                     &lt;gco:CharacterString&gt;EDINBURGH&lt;/gco:CharacterString&gt;</code><br /><code>                   &lt;/gmd:city&gt;</code><br /><code>                   &lt;gmd:administrativeArea&gt;</code><br /><code>                     &lt;gco:CharacterString&gt;LOTHIAN&lt;/gco:CharacterString&gt;</code><br /><code>                   &lt;/gmd:administrativeArea&gt;</code><br /><code>                   &lt;gmd:postalCode&gt;</code><br /><code>                     &lt;gco:CharacterString&gt;EH9 3LA&lt;/gco:CharacterString&gt;</code><br /><code>                   &lt;/gmd:postalCode&gt;</code><br /><code>                   &lt;gmd:country&gt;</code><br /><code>                     &lt;gco:CharacterString&gt;United Kingdom&lt;/gco:CharacterString&gt;</code><br /><code>                   &lt;/gmd:country&gt;</code><br /><code>                   &lt;gmd:electronicMailAddress&gt;</code><br /><code>                     &lt;gco:CharacterString&gt;<span id="cloakf9aa22ce08524f7e844e0b630bfba924">This email address is being protected from spambots. You need JavaScript enabled to view it.</span><script type='text/javascript'>
				document.getElementById('cloakf9aa22ce08524f7e844e0b630bfba924').innerHTML = '';
				var prefix = '&#109;a' + 'i&#108;' + '&#116;o';
				var path = 'hr' + 'ef' + '=';
				var addyf9aa22ce08524f7e844e0b630bfba924 = '&#101;nq&#117;&#105;r&#105;&#101;s' + '&#64;';
				addyf9aa22ce08524f7e844e0b630bfba924 = addyf9aa22ce08524f7e844e0b630bfba924 + 'bgs' + '&#46;' + '&#97;c' + '&#46;' + '&#117;k';
				var addy_textf9aa22ce08524f7e844e0b630bfba924 = '&#101;nq&#117;&#105;r&#105;&#101;s' + '&#64;' + 'bgs' + '&#46;' + '&#97;c' + '&#46;' + '&#117;k';document.getElementById('cloakf9aa22ce08524f7e844e0b630bfba924').innerHTML += '<a ' + path + '\'' + prefix + ':' + addyf9aa22ce08524f7e844e0b630bfba924 + '\'>'+addy_textf9aa22ce08524f7e844e0b630bfba924+'<\/a>';
		</script>&lt;/gco:CharacterString&gt;</code><br /><code>                   &lt;/gmd:electronicMailAddress&gt;</code><br /><code>                 &lt;/gmd:CI_Address&gt;</code><br /><code>               &lt;/gmd:address&gt;</code><br /><code>             &lt;/gmd:CI_Contact&gt;</code><br /><code>           &lt;/gmd:contactInfo&gt;</code><br /><code>           &lt;gmd:role&gt;</code><br /><code>             &lt;gmd:CI_RoleCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_RoleCode" codeListValue="distributor"&gt;distributor&lt;/gmd:CI_RoleCode&gt;</code><br /><code>           &lt;/gmd:role&gt;</code><br /><code>         &lt;/gmd:CI_ResponsibleParty&gt;</code><br /><code>       &lt;/gmd:pointOfContact&gt;</code><br /><code>       &lt;gmd:resourceMaintenance&gt;</code><br /><code>         &lt;gmd:MD_MaintenanceInformation&gt;</code><br /><code>           &lt;gmd:maintenanceAndUpdateFrequency&gt;</code><br /><code>             &lt;gmd:MD_MaintenanceFrequencyCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_MaintenanceFrequencyCode" codeListValue="asNeeded"&gt;asNeeded&lt;/gmd:MD_MaintenanceFrequencyCode&gt;</code><br /><code>           &lt;/gmd:maintenanceAndUpdateFrequency&gt;</code><br /><code>         &lt;/gmd:MD_MaintenanceInformation&gt;</code><br /><code>       &lt;/gmd:resourceMaintenance&gt;</code><br /><code>       &lt;gmd:descriptiveKeywords&gt;</code><br /><code>         &lt;gmd:MD_Keywords&gt;</code><br /><code>           &lt;gmd:keyword&gt;</code><br /><code>             &lt;gco:CharacterString&gt;Geology&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:keyword&gt;</code><br /><code>           &lt;gmd:thesaurusName&gt;</code><br /><code>             &lt;gmd:CI_Citation&gt;</code><br /><code>               &lt;gmd:title&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;GEMET Thesaurus version 1.0&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:title&gt;</code><br /><code>               &lt;gmd:date&gt;</code><br /><code>                 &lt;gmd:CI_Date&gt;</code><br /><code>                   &lt;gmd:date&gt;</code><br /><code>                     &lt;gco:Date&gt;2009-06-30&lt;/gco:Date&gt;</code><br /><code>                   &lt;/gmd:date&gt;</code><br /><code>                   &lt;gmd:dateType&gt;</code><br /><code>                     &lt;gmd:CI_DateTypeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_DateTypeCode" codeListValue="publication"&gt;publication&lt;/gmd:CI_DateTypeCode&gt;</code><br /><code>                   &lt;/gmd:dateType&gt;</code><br /><code>                 &lt;/gmd:CI_Date&gt;</code><br /><code>               &lt;/gmd:date&gt;</code><br /><code>             &lt;/gmd:CI_Citation&gt;</code><br /><code>           &lt;/gmd:thesaurusName&gt;</code><br /><code>         &lt;/gmd:MD_Keywords&gt;</code><br /><code>       &lt;/gmd:descriptiveKeywords&gt;</code><br /><code>       &lt;gmd:descriptiveKeywords&gt;</code><br /><code>         &lt;gmd:MD_Keywords&gt;</code><br /><code>           &lt;gmd:keyword&gt;</code><br /><code>             &lt;gco:CharacterString&gt;Maps&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:keyword&gt;</code><br /><code>           &lt;gmd:keyword&gt;</code><br /><code>             &lt;gco:CharacterString&gt;Digital maps&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:keyword&gt;</code><br /><code>           &lt;gmd:keyword&gt;</code><br /><code>             &lt;gco:CharacterString&gt;Spatial data&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:keyword&gt;</code><br /><code>           &lt;gmd:keyword&gt;</code><br /><code>             &lt;gco:CharacterString&gt;Geology&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:keyword&gt;</code><br /><code>           &lt;gmd:keyword&gt;</code><br /><code>             &lt;gco:CharacterString&gt;Data&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:keyword&gt;</code><br /><code>           &lt;gmd:thesaurusName&gt;</code><br /><code>             &lt;gmd:CI_Citation&gt;</code><br /><code>               &lt;gmd:title&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;BGS Thesaurus of Geosciences&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:title&gt;</code><br /><code>               &lt;gmd:date&gt;</code><br /><code>                 &lt;gmd:CI_Date&gt;</code><br /><code>                   &lt;gmd:date&gt;</code><br /><code>                     &lt;gco:Date&gt;2009&lt;/gco:Date&gt;</code><br /><code>                   &lt;/gmd:date&gt;</code><br /><code>                   &lt;gmd:dateType&gt;</code><br /><code>                     &lt;gmd:CI_DateTypeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_DateTypeCode" codeListValue="revision"&gt;revision&lt;/gmd:CI_DateTypeCode&gt;</code><br /><code>                   &lt;/gmd:dateType&gt;</code><br /><code>                 &lt;/gmd:CI_Date&gt;</code><br /><code>               &lt;/gmd:date&gt;</code><br /><code>             &lt;/gmd:CI_Citation&gt;</code><br /><code>           &lt;/gmd:thesaurusName&gt;</code><br /><code>          &lt;/gmd:MD_Keywords&gt;</code><br /><code>       &lt;/gmd:descriptiveKeywords&gt;</code><br /><code>       &lt;gmd:descriptiveKeywords&gt;</code><br /><code>         &lt;gmd:MD_Keywords&gt;</code><br /><code>           &lt;gmd:keyword&gt;</code><br /><code>             &lt;gco:CharacterString&gt;infoMapAccessService&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:keyword&gt;</code><br /><code>           &lt;gmd:thesaurusName&gt;</code><br /><code>             &lt;gmd:CI_Citation&gt;</code><br /><code>               &lt;gmd:title&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;ISO 19119:2005&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:title&gt;</code><br /><code>               &lt;gmd:date&gt;</code><br /><code>                 &lt;gmd:CI_Date&gt;</code><br /><code>                   &lt;gmd:date&gt;</code><br /><code>                     &lt;gco:Date&gt;2008-04-16&lt;/gco:Date&gt;</code><br /><code>                   &lt;/gmd:date&gt;</code><br /><code>                   &lt;gmd:dateType&gt;</code><br /><code>                     &lt;gmd:CI_DateTypeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_DateTypeCode" codeListValue="revision"&gt;revision&lt;/gmd:CI_DateTypeCode&gt;</code><br /><code>                   &lt;/gmd:dateType&gt;</code><br /><code>                 &lt;/gmd:CI_Date&gt;</code><br /><code>                &lt;/gmd:date&gt;</code><br /><code>             &lt;/gmd:CI_Citation&gt;</code><br /><code>           &lt;/gmd:thesaurusName&gt;</code><br /><code>         &lt;/gmd:MD_Keywords&gt;</code><br /><code>       &lt;/gmd:descriptiveKeywords&gt;</code><br /><code>       &lt;gmd:descriptiveKeywords&gt;</code><br /><code>         &lt;gmd:MD_Keywords&gt;</code><br /><code>           &lt;gmd:keyword&gt;</code><br /><code>             &lt;gco:CharacterString&gt;NERC_DDC&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:keyword&gt;</code><br /><code>         &lt;/gmd:MD_Keywords&gt;</code><br /><code>       &lt;/gmd:descriptiveKeywords&gt;</code><br /><code>       &lt;gmd:resourceConstraints&gt;</code><br /><code>         &lt;gmd:MD_LegalConstraints&gt;</code><br /> &lt;gmd:accessConstraints&gt;<br /> &lt;gmd:MD_RestrictionCode<br />codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_RestrictionCode"<br /> codeListValue="otherRestrictions"&gt;otherRestrictions&lt;/gmd:MD_RestrictionCode&gt;<br /> &lt;/gmd:accessConstraints&gt;<br /> &lt;gmd:otherConstraints&gt;<br /> &lt;gmx:Anchor xlink:href="http://inspire.ec.europa.eu/metadata-codelist/LimitationsOnPublicAccess/noLimitations"&gt;no limitations&lt;/gmx:Anchor&gt;<br /> &lt;/gmd:otherConstraints&gt;<br /> &lt;/gmd:MD_LegalConstraints&gt;<br /> &lt;/gmd:resourceConstraints&gt;<br /> &lt;gmd:resourceConstraints&gt;<br /> &lt;gmd:MD_LegalConstraints&gt;<br /> &lt;gmd:useConstraints&gt;<br /> &lt;gmd:MD_RestrictionCode<br />codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_RestrictionCode"<br /> codeListValue="otherRestrictions"&gt;otherRestrictions&lt;/gmd:MD_RestrictionCode&gt;<br /> &lt;/gmd:useConstraints&gt;<br /><code>          &lt;gmd:otherConstraints&gt;</code><br /><code>            &lt;gco:CharacterString&gt;The 1:625k DiGMap data is made available for all uses - including commercial use, however the British Geological Survey (BGS) at all times retains the copyright in this material and you are not permitted, without an appropriate licence, to set up a service selling on this material. Your own use of any information provided by the British Geological Survey (BGS) is at your own risk. Neither BGS nor the Natural Environment Research Council (NERC) gives any warranty, condition or representation as to the quality, accuracy or completeness of the information or its suitability for any use or purpose. All implied conditions relating to the quality or suitability of the information, and all liabilities arising from the supply of the information (including any liability arising in negligence) are excluded to the fullest extent permitted by law.&lt;/gco:CharacterString&gt;</code><br /><code>          &lt;/gmd:otherConstraints&gt;</code><br /><code>        &lt;/gmd:MD_LegalConstraints&gt;</code><br /><code>      &lt;/gmd:resourceConstraints&gt;</code><br /><code>      &lt;srv:serviceType&gt;</code><br /><code>         &lt;gco:LocalName codeSpace="INSPIRE"&gt;view&lt;/gco:LocalName&gt;</code><br /><code>      &lt;/srv:serviceType&gt;</code><br /><code>      &lt;srv:extent&gt;</code><br /><code>         &lt;gmd:EX_Extent&gt;</code><br /><code>           &lt;gmd:geographicElement&gt;</code><br /><code>             &lt;gmd:EX_GeographicDescription&gt;</code><br /><code>               &lt;gmd:geographicIdentifier&gt;</code><br /><code>                 &lt;gmd:MD_Identifier&gt;</code><br /><code>                   &lt;gmd:authority&gt;</code><br /><code>                     &lt;gmd:CI_Citation&gt;</code><br /><code>                       &lt;gmd:title&gt;</code><br /><code>                         &lt;gco:CharacterString&gt;ISO 3166_2&lt;/gco:CharacterString&gt;</code><br /><code>                       &lt;/gmd:title&gt;</code><br /><code>                       &lt;gmd:date&gt;</code><br /><code>                         &lt;gmd:CI_Date&gt;</code><br /><code>                           &lt;gmd:date&gt;</code><br /><code>                             &lt;gco:Date&gt;2009-01-07&lt;/gco:Date&gt;</code><br /><code>                           &lt;/gmd:date&gt;</code><br /><code>                           &lt;gmd:dateType&gt;</code><br /><code>                             &lt;gmd:CI_DateTypeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_DateTypeCode" codeListValue="revision"&gt;revision&lt;/gmd:CI_DateTypeCode&gt;</code><br /><code>                           &lt;/gmd:dateType&gt;</code><br /><code>                         &lt;/gmd:CI_Date&gt;</code><br /><code>                       &lt;/gmd:date&gt;</code><br /><code>                     &lt;/gmd:CI_Citation&gt;</code><br /><code>                  &lt;/gmd:authority&gt;</code><br /><code>                   &lt;gmd:code&gt;</code><br /><code>                     &lt;gco:CharacterString&gt;UKM&lt;/gco:CharacterString&gt;</code><br /><code>                   &lt;/gmd:code&gt;</code><br /><code>                 &lt;/gmd:MD_Identifier&gt;</code><br /><code>               &lt;/gmd:geographicIdentifier&gt;</code><br /><code>             &lt;/gmd:EX_GeographicDescription&gt;</code><br /><code>           &lt;/gmd:geographicElement&gt;</code><br /><code>           &lt;gmd:geographicElement&gt;</code><br /><code>             &lt;gmd:EX_GeographicDescription&gt;</code><br /><code>               &lt;gmd:geographicIdentifier&gt;</code><br /><code>                 &lt;gmd:MD_Identifier&gt;</code><br /><code>                    &lt;gmd:authority&gt;</code><br /><code>                     &lt;gmd:CI_Citation&gt;</code><br /><code>                       &lt;gmd:title&gt;</code><br /><code>                         &lt;gco:CharacterString&gt;ISO 3166_1&lt;/gco:CharacterString&gt;</code><br /><code>                       &lt;/gmd:title&gt;</code><br /><code>                       &lt;gmd:date&gt;</code><br /><code>                         &lt;gmd:CI_Date&gt;</code><br /><code>                           &lt;gmd:date&gt;</code><br /><code>                             &lt;gco:Date&gt;2009-01-07&lt;/gco:Date&gt;</code><br /><code>                           &lt;/gmd:date&gt;</code><br /><code>                           &lt;gmd:dateType&gt;</code><br /><code>                             &lt;gmd:CI_DateTypeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_DateTypeCode" codeListValue="revision"&gt;revision&lt;/gmd:CI_DateTypeCode&gt;</code><br /><code>                           &lt;/gmd:dateType&gt;</code><br /><code>                         &lt;/gmd:CI_Date&gt;</code><br /><code>                       &lt;/gmd:date&gt;</code><br /><code>                     &lt;/gmd:CI_Citation&gt;</code><br /><code>                   &lt;/gmd:authority&gt;</code><br /><code>                   &lt;gmd:code&gt;</code><br /><code>                     &lt;gco:CharacterString&gt;GB&lt;/gco:CharacterString&gt;</code><br /><code>                   &lt;/gmd:code&gt;</code><br /><code>                 &lt;/gmd:MD_Identifier&gt;</code><br /><code>               &lt;/gmd:geographicIdentifier&gt;</code><br /><code>             &lt;/gmd:EX_GeographicDescription&gt;</code><br /><code>           &lt;/gmd:geographicElement&gt;</code><br /><code>           &lt;gmd:geographicElement&gt;</code><br /><code>             &lt;gmd:EX_GeographicBoundingBox&gt;</code><br /><code>               &lt;gmd:westBoundLongitude&gt;</code><br /><code>                 &lt;gco:Decimal&gt;-6.8647&lt;/gco:Decimal&gt;</code><br /><code>               &lt;/gmd:westBoundLongitude&gt;</code><br /><code>               &lt;gmd:eastBoundLongitude&gt;</code><br /><code>                 &lt;gco:Decimal&gt;2.9603&lt;/gco:Decimal&gt;</code><br /><code>               &lt;/gmd:eastBoundLongitude&gt;</code><br /><code>               &lt;gmd:southBoundLatitude&gt;</code><br /><code>                 &lt;gco:Decimal&gt;49.7974&lt;/gco:Decimal&gt;</code><br /><code>               &lt;/gmd:southBoundLatitude&gt;</code><br /><code>               &lt;gmd:northBoundLatitude&gt;</code><br /><code>                 &lt;gco:Decimal&gt;60.7719&lt;/gco:Decimal&gt;</code><br /><code>               &lt;/gmd:northBoundLatitude&gt;</code><br /><code>             &lt;/gmd:EX_GeographicBoundingBox&gt;</code><br /><code>           &lt;/gmd:geographicElement&gt;</code><br /><code>           &lt;gmd:temporalElement&gt;</code><br /><code>             &lt;gmd:EX_TemporalExtent&gt;</code><br /><code>               &lt;gmd:extent&gt;</code><br /><code>                &lt;gml:TimePeriod gml:id="ID1"&gt;</code><br /><code>                   &lt;gml:beginPosition&gt;1995&lt;/gml:beginPosition&gt;</code><br /><code>                   &lt;gml:endPosition&gt;1995&lt;/gml:endPosition&gt;</code><br /><code>                 &lt;/gml:TimePeriod&gt;</code><br /><code>               &lt;/gmd:extent&gt;</code><br /><code>             &lt;/gmd:EX_TemporalExtent&gt;</code><br /><code>           &lt;/gmd:temporalElement&gt;</code><br /><code>         &lt;/gmd:EX_Extent&gt;</code><br /><code>       &lt;/srv:extent&gt;</code><br /><code>       &lt;srv:couplingType&gt;</code><br /><code>         &lt;srv:SV_CouplingType codeListValue="tight" codeList="http://www.isotc211.org/2005/iso19119/resources/codelist/gmxCodelists.xml#SV_CouplingType" /&gt;</code><br /><code>       &lt;/srv:couplingType&gt;</code><br /><code>       &lt;srv:containsOperations gco:nilReason="missing" /&gt;</code><br /><code>       &lt;srv:operatesOn xlink:title="BGS.1M.surface.GeologicUnit" xlink:href="http://ogcdev.bgs.ac.uk/geonetwork/srv/en/csw?SERVICE=CSW&amp;amp;amp;REQUEST=GetRecordById&amp;amp;amp;ID=9df8df52-d788-37a8-e044-0003ba9b0d98&amp;amp;amp;elementSetName=full&amp;amp;amp;OutputSchema=http://www.isotc211.org/2005/gmd&amp;amp;amp;" uuidref="9df8df52-d788-37a8-e044-0003ba9b0d98" /&gt;</code><br /><code>       &lt;srv:operatesOn xlink:title="BGS.1M.surface.GeologicUnit.age" xlink:href="http://ogcdev.bgs.ac.uk/geonetwork/srv/en/csw?SERVICE=CSW&amp;amp;amp;REQUEST=GetRecordById&amp;amp;amp;ID=9df8df52-d788-37a8-e044-0003ba9b0d98&amp;amp;amp;elementSetName=full&amp;amp;amp;OutputSchema=http://www.isotc211.org/2005/gmd&amp;amp;amp;" uuidref="9df8df52-d788-37a8-e044-0003ba9b0d98" /&gt;</code><br /><code>     &lt;/srv:SV_ServiceIdentification&gt;</code><br /><code>   &lt;/gmd:identificationInfo&gt;</code><br /><code>   &lt;gmd:distributionInfo&gt;</code><br /><code>     &lt;gmd:MD_Distribution&gt;</code><br /><code>       &lt;gmd:distributionFormat&gt;</code><br /><code>         &lt;gmd:MD_Format&gt;</code><br /><code>           &lt;gmd:name&gt;</code><br /><code>             &lt;gco:CharacterString&gt;image/gif&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:name&gt;</code><br /><code>           &lt;gmd:version&gt;</code><br /><code>             &lt;gco:CharacterString&gt;NotApplicable&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:version&gt;</code><br /><code>         &lt;/gmd:MD_Format&gt;</code><br /><code>       &lt;/gmd:distributionFormat&gt;</code><br /><code>       &lt;gmd:distributionFormat&gt;</code><br /><code>         &lt;gmd:MD_Format&gt;</code><br /><code>           &lt;gmd:name&gt;</code><br /><code>             &lt;gco:CharacterString&gt;image/png; mode=24bit&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:name&gt;</code><br /><code>           &lt;gmd:version&gt;</code><br /><code>             &lt;gco:CharacterString&gt;NotApplicable&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:version&gt;</code><br /><code>         &lt;/gmd:MD_Format&gt;</code><br /><code>       &lt;/gmd:distributionFormat&gt;</code><br /><code>       &lt;gmd:distributionFormat&gt;</code><br /><code>         &lt;gmd:MD_Format&gt;</code><br /><code>           &lt;gmd:name&gt;</code><br /><code>             &lt;gco:CharacterString&gt;image/jpeg&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:name&gt;</code><br /><code>           &lt;gmd:version&gt;</code><br /><code>             &lt;gco:CharacterString&gt;NotApplicable&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:version&gt;</code><br /><code>         &lt;/gmd:MD_Format&gt;</code><br /><code>       &lt;/gmd:distributionFormat&gt;</code><br /><code>       &lt;gmd:distributionFormat&gt;</code><br /><code>         &lt;gmd:MD_Format&gt;</code><br /><code>           &lt;gmd:name&gt;</code><br /><code>             &lt;gco:CharacterString&gt;image/png&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:name&gt;</code><br /><code>           &lt;gmd:version&gt;</code><br /><code>             &lt;gco:CharacterString&gt;NotApplicable&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:version&gt;</code><br /><code>         &lt;/gmd:MD_Format&gt;</code><br /><code>       &lt;/gmd:distributionFormat&gt;</code><br /><code>       &lt;gmd:distributionFormat&gt;</code><br /><code>         &lt;gmd:MD_Format&gt;</code><br /><code>           &lt;gmd:name&gt;</code><br /><code>             &lt;gco:CharacterString&gt;image/vnd.wap.wbmp&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:name&gt;</code><br /><code>           &lt;gmd:version&gt;</code><br /><code>             &lt;gco:CharacterString&gt;NotApplicable&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:version&gt;</code><br /><code>         &lt;/gmd:MD_Format&gt;</code><br /><code>       &lt;/gmd:distributionFormat&gt;</code><br /><code>       &lt;gmd:distributionFormat&gt;</code><br /><code>         &lt;gmd:MD_Format&gt;</code><br /><code>           &lt;gmd:name&gt;</code><br /><code>             &lt;gco:CharacterString&gt;image/tiff&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:name&gt;</code><br /><code>           &lt;gmd:version&gt;</code><br /><code>             &lt;gco:CharacterString&gt;NotApplicable&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:version&gt;</code><br /><code>         &lt;/gmd:MD_Format&gt;</code><br /><code>       &lt;/gmd:distributionFormat&gt;</code><br /><code>       &lt;gmd:distributionFormat&gt;</code><br /><code>         &lt;gmd:MD_Format&gt;</code><br /><code>           &lt;gmd:name&gt;</code><br /><code>             &lt;gco:CharacterString&gt;image/svg+xml&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:name&gt;</code><br /><code>           &lt;gmd:version&gt;</code><br /><code>             &lt;gco:CharacterString&gt;NotApplicable&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:version&gt;</code><br /><code>         &lt;/gmd:MD_Format&gt;</code><br /><code>       &lt;/gmd:distributionFormat&gt;</code><br /><code>       &lt;gmd:distributionFormat&gt;</code><br /><code>         &lt;gmd:MD_Format&gt;</code><br /><code>           &lt;gmd:name&gt;</code><br /><code>             &lt;gco:CharacterString&gt;text/xml; subtype=gml/3.1.1&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:name&gt;</code><br /><code>           &lt;gmd:version&gt;</code><br /><code>             &lt;gco:CharacterString&gt;3.1.1&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:version&gt;</code><br /><code>         &lt;/gmd:MD_Format&gt;</code><br /><code>       &lt;/gmd:distributionFormat&gt;</code><br /><code>       &lt;gmd:distributionFormat&gt;</code><br /><code>         &lt;gmd:MD_Format&gt;</code><br /><code>           &lt;gmd:name&gt;</code><br /><code>             &lt;gco:CharacterString&gt;GeoSciML&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:name&gt;</code><br /><code>           &lt;gmd:version&gt;</code><br /><code>             &lt;gco:CharacterString&gt;2&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:version&gt;</code><br /><code>         &lt;/gmd:MD_Format&gt;</code><br /><code>       &lt;/gmd:distributionFormat&gt;</code><br /><code>       &lt;gmd:distributionFormat&gt;</code><br /><code>         &lt;gmd:MD_Format&gt;</code><br /><code>           &lt;gmd:name&gt;</code><br /><code>             &lt;gco:CharacterString&gt;text/plain&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:name&gt;</code><br /><code>           &lt;gmd:version gco:nilReason="inapplicable" /&gt;</code><br /><code>         &lt;/gmd:MD_Format&gt;</code><br /><code>       &lt;/gmd:distributionFormat&gt;</code><br /><code>       &lt;gmd:distributionFormat&gt;</code><br /><code>         &lt;gmd:MD_Format&gt;</code><br /><code>           &lt;gmd:name&gt;</code><br /><code>             &lt;gco:CharacterString&gt;text/html&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:name&gt;</code><br /><code>           &lt;gmd:version gco:nilReason="inapplicable" /&gt;</code><br /><code>         &lt;/gmd:MD_Format&gt;</code><br /><code>       &lt;/gmd:distributionFormat&gt;</code><br /><code>       &lt;gmd:distributionFormat&gt;</code><br /><code>         &lt;gmd:MD_Format&gt;</code><br /><code>           &lt;gmd:name&gt;</code><br /><code>             &lt;gco:CharacterString&gt;application/vnd.ogc.gml&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:name&gt;</code><br /><code>           &lt;gmd:version gco:nilReason="inapplicable" /&gt;</code><br /><code>         &lt;/gmd:MD_Format&gt;</code><br /><code>       &lt;/gmd:distributionFormat&gt;</code><br /><code>       &lt;gmd:distributionFormat&gt;</code><br /><code>         &lt;gmd:MD_Format&gt;</code><br /><code>           &lt;gmd:name&gt;</code><br /><code>             &lt;gco:CharacterString&gt;text/xml&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:name&gt;</code><br /><code>           &lt;gmd:version gco:nilReason="unknown" /&gt;</code><br /><code>         </code><code>&lt;/gmd:MD_Format&gt;</code><br /><code>       &lt;/gmd:distributionFormat&gt;</code><br /><code>       &lt;gmd:distributor&gt;</code><br /><code>         &lt;gmd:MD_Distributor&gt;</code><br /><code>           &lt;gmd:distributorContact&gt;</code><br /><code>             &lt;gmd:CI_ResponsibleParty&gt;</code><br /><code>               &lt;gmd:organisationName&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;British Geological Survey&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:organisationName&gt;</code><br /><code>               &lt;gmd:contactInfo&gt;</code><br /><code>                 &lt;gmd:CI_Contact&gt;</code><br /><code>                   &lt;gmd:phone&gt;</code><br /><code>                     &lt;gmd:CI_Telephone&gt;</code><br /><code>                       &lt;gmd:voice&gt;</code><br /><code>                         &lt;gco:CharacterString&gt;+44 131 667 1000 Ex:364&lt;/gco:CharacterString&gt;</code><br /><code>                     &lt;/gmd:voice&gt;</code><br /><code>                     &lt;/gmd:CI_Telephone&gt;</code><br /><code>                   &lt;/gmd:phone&gt;</code><br /><code>                   &lt;gmd:address&gt;</code><br /><code>                     &lt;gmd:CI_Address&gt;</code><br /><code>                       &lt;gmd:deliveryPoint&gt;</code><br /><code>                         &lt;gco:CharacterString&gt;Murchison House, West Mains Road, Edinburgh, Lothian, United Kingdom, EH9 3LA, NG12 5GG&lt;/gco:CharacterString&gt;</code><br /><code>                       &lt;/gmd:deliveryPoint&gt;</code><br /><code>                       &lt;gmd:city&gt;</code><br /><code>                         &lt;gco:CharacterString&gt;EDINBURGH&lt;/gco:CharacterString&gt;</code><br /><code>                       &lt;/gmd:city&gt;</code><br /><code>                       &lt;gmd:administrativeArea&gt;</code><br /><code>                         &lt;gco:CharacterString&gt;LOTHIAN&lt;/gco:CharacterString&gt;</code><br /><code>                       &lt;/gmd:administrativeArea&gt;</code><br /><code>                       &lt;gmd:postalCode&gt;</code><br /><code>                         &lt;gco:CharacterString&gt;EH9 3LA&lt;/gco:CharacterString&gt;</code><br /><code>                       &lt;/gmd:postalCode&gt;</code><br /><code>                       &lt;gmd:country&gt;</code><br /><code>                         &lt;gco:CharacterString&gt;United Kingdom&lt;/gco:CharacterString&gt;</code><br /><code>                       &lt;/gmd:country&gt;</code><br /><code>                       &lt;gmd:electronicMailAddress&gt;</code><br /><code>&lt;gco:CharacterString&gt;<span id="cloak282858164f3b365ce985f7fdb3ef122a">This email address is being protected from spambots. You need JavaScript enabled to view it.</span><script type='text/javascript'>
				document.getElementById('cloak282858164f3b365ce985f7fdb3ef122a').innerHTML = '';
				var prefix = '&#109;a' + 'i&#108;' + '&#116;o';
				var path = 'hr' + 'ef' + '=';
				var addy282858164f3b365ce985f7fdb3ef122a = '&#101;nq&#117;&#105;r&#105;&#101;s' + '&#64;';
				addy282858164f3b365ce985f7fdb3ef122a = addy282858164f3b365ce985f7fdb3ef122a + 'bgs' + '&#46;' + '&#97;c' + '&#46;' + '&#117;k';
				var addy_text282858164f3b365ce985f7fdb3ef122a = '&#101;nq&#117;&#105;r&#105;&#101;s' + '&#64;' + 'bgs' + '&#46;' + '&#97;c' + '&#46;' + '&#117;k';document.getElementById('cloak282858164f3b365ce985f7fdb3ef122a').innerHTML += '<a ' + path + '\'' + prefix + ':' + addy282858164f3b365ce985f7fdb3ef122a + '\'>'+addy_text282858164f3b365ce985f7fdb3ef122a+'<\/a>';
		</script>&lt;/gco:CharacterString&gt;</code><br /><code>                       &lt;/gmd:electronicMailAddress&gt;</code><br /><code>                     &lt;/gmd:CI_Address&gt;</code><br /><code>                   &lt;/gmd:address&gt;</code><br /><code>                 &lt;/gmd:CI_Contact&gt;</code><br /><code>               &lt;/gmd:contactInfo&gt;</code><br /><code>               &lt;gmd:role&gt;</code><br /><code>                 &lt;gmd:CI_RoleCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_RoleCode" codeListValue="distributor"&gt;distributor&lt;/gmd:CI_RoleCode&gt;</code><br /><code>               &lt;/gmd:role&gt;</code><br /><code>             &lt;/gmd:CI_ResponsibleParty&gt;</code><br /><code>           &lt;/gmd:distributorContact&gt;</code><br /><code>         &lt;/gmd:MD_Distributor&gt;</code><br /><code>       &lt;/gmd:distributor&gt;</code><br /><code>       &lt;gmd:transferOptions&gt;</code><br /><code>         &lt;gmd:MD_DigitalTransferOptions&gt;</code><br /><code>           &lt;gmd:onLine&gt;</code><br /><code>             &lt;gmd:CI_OnlineResource&gt;</code><br /><code>               &lt;gmd:linkage&gt;</code><br /><code>&lt;gmd:URL&gt;http://ogc.bgs.ac.uk/BGS_Bedrock_and_Surface_Geology/wms.php?SERVICE=WMS&amp;amp;REQUEST=getCapabilities&amp;amp;&lt;/gmd:URL&gt;</code><br /><code>               &lt;/gmd:linkage&gt;</code><br /><code>               &lt;gmd:protocol&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;OGC:WMS-1.3.0-http-get-capabilities&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:protocol&gt;</code><br /><code>               &lt;gmd:name&gt;</code><br /><code>&lt;gco:CharacterString&gt;BGS.Bedrock.and.Surface.Geology&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:name&gt;</code><br /><code>               &lt;gmd:description&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;BGS Bedrock and Surface geology&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:description&gt;</code><br /><code>               &lt;gmd:function&gt;</code><br /><code>                 &lt;gmd:CI_OnLineFunctionCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_OnLineFunctionCode" codeListValue="download"&gt;download&lt;/gmd:CI_OnLineFunctionCode&gt;</code><br /><code>               &lt;/gmd:function&gt;</code><br /><code>             &lt;/gmd:CI_OnlineResource&gt;</code><br /><code>           &lt;/gmd:onLine&gt;</code><br /><code>         &lt;/gmd:MD_DigitalTransferOptions&gt;</code><br /><code>       &lt;/gmd:transferOptions&gt;</code><br /><code>       &lt;gmd:transferOptions&gt;</code><br /><code>         &lt;gmd:MD_DigitalTransferOptions&gt;</code><br /><code>           &lt;gmd:onLine&gt;</code><br /><code>             &lt;gmd:CI_OnlineResource&gt;</code><br /><code>               &lt;gmd:linkage&gt;</code><br /><code>&lt;gmd:URL&gt;http://ogc.bgs.ac.uk/BGS_Bedrock_and_Surface_Geology/wms.php&lt;/gmd:URL&gt;</code><br /><code>               &lt;/gmd:linkage&gt;</code><br /><code>               &lt;gmd:protocol&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;OGC:WMS-1.3.0-http-get-map&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:protocol&gt;</code><br /><code>               &lt;gmd:name&gt;</code><br /><code>&lt;gco:CharacterString&gt;BGS.1M.surface.GeologicUnit.age&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:name&gt;</code><br /><code>               &lt;gmd:description&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;BGS 1M surface Geologic Unit Age. The layer shows the rocks and superficial deposits present at the land surface, clasified by Geological age&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:description&gt;</code><br /><code>               &lt;gmd:function&gt;</code><br /><code>                 &lt;gmd:CI_OnLineFunctionCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_OnLineFunctionCode" codeListValue="download"&gt;download&lt;/gmd:CI_OnLineFunctionCode&gt;</code><br /><code>               &lt;/gmd:function&gt;</code><br /><code>             &lt;/gmd:CI_OnlineResource&gt;</code><br /><code>           &lt;/gmd:onLine&gt;</code><br /><code>         &lt;/gmd:MD_DigitalTransferOptions&gt;</code><br /><code>       &lt;/gmd:transferOptions&gt;</code><br /><code>       &lt;gmd:transferOptions&gt;</code><br /><code>         &lt;gmd:MD_DigitalTransferOptions&gt;</code><br /><code>           &lt;gmd:onLine&gt;</code><br /><code>             &lt;gmd:CI_OnlineResource&gt;</code><br /><code>               &lt;gmd:linkage&gt;</code><br /><code>&lt;gmd:URL&gt;http://ogc.bgs.ac.uk/BGS_Bedrock_and_Surface_Geology/wms.php&lt;/gmd:URL&gt;</code><br /><code>               &lt;/gmd:linkage&gt;</code><br /><code>               &lt;gmd:protocol&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;OGC:WMS-1.3.0-http-get-map&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:protocol&gt;</code><br /><code>               &lt;gmd:name&gt;</code><br /><code>&lt;gco:CharacterString&gt;BGS.1M.surface.GeologicUnit&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:name&gt;</code><br /><code>               &lt;gmd:description&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;BGS 1M surface Geologic Unit. The layer shows the rocks and superficial deposits present at the land surface, clasified by lithology&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:description&gt;</code><br /><code>               &lt;gmd:function&gt;</code><br /><code>                 &lt;gmd:CI_OnLineFunctionCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_OnLineFunctionCode" codeListValue="download"&gt;download&lt;/gmd:CI_OnLineFunctionCode&gt;</code><br /><code>               &lt;/gmd:function&gt;</code><br /><code>             &lt;/gmd:CI_OnlineResource&gt;</code><br /><code>           &lt;/gmd:onLine&gt;</code><br /><code>         &lt;/gmd:MD_DigitalTransferOptions&gt;</code><br /><code>       &lt;/gmd:transferOptions&gt;</code><br /><code>     &lt;/gmd:MD_Distribution&gt;</code><br /><code>   &lt;/gmd:distributionInfo&gt;</code><br /><code>   &lt;gmd:dataQualityInfo&gt;</code><br /><code>     &lt;gmd:DQ_DataQuality&gt;</code><br /><code>       &lt;gmd:scope&gt;</code><br /><code>         &lt;gmd:DQ_Scope&gt;</code><br /><code>           &lt;gmd:level&gt;</code><br /><code>             &lt;gmd:MD_ScopeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_ScopeCode" codeListValue="service"&gt;service&lt;/gmd:MD_ScopeCode&gt;</code><br /><code>           &lt;/gmd:level&gt;</code><br /><code>           &lt;gmd:levelDescription&gt;</code><br /><code>             &lt;gmd:MD_ScopeDescription&gt;</code><br /><code>               &lt;gmd:other&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;service&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:other&gt;</code><br /><code>             &lt;/gmd:MD_ScopeDescription&gt;</code><br /><code>           &lt;/gmd:levelDescription&gt;</code><br /><code>         &lt;/gmd:DQ_Scope&gt;</code><br /><code>       &lt;/gmd:scope&gt;</code><br /><code>       &lt;gmd:report&gt;</code><br /><code>         &lt;gmd:DQ_DomainConsistency&gt;</code><br /><code>           &lt;gmd:result&gt;</code><br /><code>             &lt;gmd:DQ_ConformanceResult&gt;</code><br /><code>               &lt;gmd:specification&gt;</code><br /><code>                 &lt;gmd:CI_Citation&gt;</code><br /><code>                   &lt;gmd:title&gt;</code><br /><code>                     &lt;gco:CharacterString&gt;Commission Regulation (EU) No 1089/2010 of 23 November 2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data sets and services&lt;/gco:CharacterString&gt;</code><br /><code>                   &lt;/gmd:title&gt;</code><br /><code>                   &lt;gmd:date&gt;</code><br /><code>                     &lt;gmd:CI_Date&gt;</code><br /><code>                       &lt;gmd:date&gt;</code><br /><code>                         &lt;gco:Date&gt;2010-12-08&lt;/gco:Date&gt;</code><br /><code>                       &lt;/gmd:date&gt;</code><br /><code>                       &lt;gmd:dateType&gt;</code><br /><code>                         &lt;gmd:CI_DateTypeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/ML_gmx                                                    Codelists.xml#CI_DateTypeCode" codeListValue="publication"&gt;publication&lt;/gmd:CI_DateTypeCode&gt;</code><br /><code>                       &lt;/gmd:dateType&gt;</code><br /><code>                     &lt;/gmd:CI_Date&gt;</code><br /><code>                   &lt;/gmd:date&gt;</code><br /><code>                 &lt;/gmd:CI_Citation&gt;</code><br /><code>               &lt;/gmd:specification&gt;</code><br /><code>               &lt;gmd:explanation&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;See http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:323:0011:0102:EN:PDF&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:explanation&gt;</code><br /><code>               &lt;gmd:pass&gt;</code><br /><code>                 &lt;gco:Boolean&gt;true&lt;/gco:Boolean&gt;</code><br /><code>               &lt;/gmd:pass&gt;</code><br /><code>             &lt;/gmd:DQ_ConformanceResult&gt;</code><br /><code>           &lt;/gmd:result&gt;</code><br /><code>           &lt;gmd:result&gt;</code><br /><code>             &lt;gmd:DQ_ConformanceResult&gt;</code><br /><code>               &lt;gmd:specification&gt;</code><br /><code>                 &lt;gmd:CI_Citation&gt;</code><br /><code>                   &lt;gmd:title&gt;</code><br /><code>                     &lt;gco:CharacterString&gt;Technical Guidance for the implementation of INSPIRE View Services Version 3.0&lt;/gco:CharacterString&gt;</code><br /><code>                  &lt;/gmd:title&gt;</code><br /><code>                   &lt;gmd:date&gt;</code><br /><code>                     &lt;gmd:CI_Date&gt;</code><br /><code>                       &lt;gmd:date&gt;</code><br /><code>                         &lt;gco:Date&gt;2011-03-21&lt;/gco:Date&gt;</code><br /><code>                       &lt;/gmd:date&gt;</code><br /><code>                       &lt;gmd:dateType&gt;</code><br /><code>                         &lt;gmd:CI_DateTypeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/ML_gmx                                                     Codelists.xml#CI_DateTypeCode" codeListValue="publication"&gt;publication&lt;/gmd:CI_DateTypeCode&gt;</code><br /><code>                       &lt;/gmd:dateType&gt;</code><br /><code>                     &lt;/gmd:CI_Date&gt;</code><br /><code>                   &lt;/gmd:date&gt;</code><br /><code>                 &lt;/gmd:CI_Citation&gt;</code><br /><code>               &lt;/gmd:specification&gt;</code><br /><code>               &lt;gmd:explanation&gt;</code><br /><code>                 &lt;gco:CharacterString&gt;See the referenced specification at http://inspire.jrc.ec.europa.eu/documents/Network_Services/TechnicalGuidance_ViewServices_v3.0.pdf&lt;/gco:CharacterString&gt;</code><br /><code>               &lt;/gmd:explanation&gt;</code><br /><code>               &lt;gmd:pass&gt;</code><br /><code>                 &lt;gco:Boolean&gt;true&lt;/gco:Boolean&gt;</code><br /><code>               &lt;/gmd:pass&gt;</code><br /><code>             &lt;/gmd:DQ_ConformanceResult&gt;</code><br /><code>           &lt;/gmd:result&gt;</code><br /><code>         &lt;/gmd:DQ_DomainConsistency&gt;</code><br /><code>       &lt;/gmd:report&gt;</code><br /><code>      &lt;gmd:lineage&gt;</code><br /><code>         &lt;gmd:LI_Lineage&gt;</code><br /><code>           &lt;gmd:statement&gt;</code><br /><code>             &lt;gco:CharacterString&gt;For lineage of datasets served by this service please refer to the metadata for those data&lt;/gco:CharacterString&gt;</code><br /><code>           &lt;/gmd:statement&gt;</code><br /><code>         &lt;/gmd:LI_Lineage&gt;</code><br /><code>       &lt;/gmd:lineage&gt;</code><br /><code>     &lt;/gmd:DQ_DataQuality&gt;</code><br /><code>   &lt;/gmd:dataQualityInfo&gt;</code><br /><code>&lt;/gmd:MD_Metadata&gt;</code><br /><em><br />Last updated: June 2018</em><code></code></pre>


<h3><a id="1.6"></a>1.6 XML Fragments</h3>
<p>This document contains examples of XML encoding. The examples are considered fragments in that they are not complete XML documents. The following conventions are used:</p>
<ul>
<li>The root element will generally be shown and it shall be gmd:MD_Metadata</li>
<li>XML element tags will generally be shown on a single line</li>
<li>XML will be tabbed in where possible to aid reading</li>
<li>Where an XML element, including the start tag, end tag and content, is too long to show on a single line, it shall break across more than one line automatically (i.e. under the control of browser justification and text wrapping)</li>
<li>Missing XML content, removed while forming the fragment, shall be represented by an ellipsis (...)</li>
</ul>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 1 – XML fragment – tabbing</strong></h5>
<br /><code>&lt;gmd:MD_Metadata&gt;</code><br /> <code>   &lt;gmd:fileIdentifier&gt;</code><br /> <code>     &lt;gco:CharacterString&gt;98e25be5-388d-4be3-bc5f-ba07ef6009b2&lt;/gco:CharacterString&gt;</code><br /> <code>   &lt;/gmd:fileIdentifier&gt;</code><br /> <code>   ...</code><br /> <code>&lt;/gmd:MD_Metadata&gt;</code></div>
<p>Figure 1 shows an example of an XML fragment. Note that it starts with the XML element gmd:MD_Metadata. The next XML element in order is gmd:fileIdentifier and its start-tag is on the next line and is tabbed in. The following line is the content of gmd:fileIdentifier.</p>
<p>An ellipsis follows the end tag of the XML element gmd:fileIdentifier indicating that other content is missing</p>
<p>Also deliberately omitted from XML fragments is:</p>
<ul>
<li>The XML declaration</li>
<li>XML namespace identifiers</li>
</ul>
<p>In the example in Figure 1 CharacterString is an XML element in the namespace gco. It has the start-tag <code>&lt;gco:CharacterString&gt;</code> and the end-tag <code>&lt;/gco:CharacterString&gt;.</code> The string <em>98e25be5-388d-4be3-bc5f-ba07ef6009b2</em> is the element’s content. The CharacterString element forms the content of another element: fileIdentifier. Its start-tag is <code>&lt;gmd:fileIdentifier&gt;</code> and its end-tag is <code>&lt;/gmd:fileIdentifier&gt;</code>.  In the example below <code>gml:id</code> and <code>codeSpace</code> are XML attributes. XML attributes are encoded in the start-tag of an element with the form <code>[namespace]:[attributeName]="[content]"</code>.</p>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 2 - XML attributes </strong></h5>
<code>...</code><br /> <code>&lt;gmx:CodeDefinition gml:id="MD_ScopeCode_dataset"&gt;</code><br /> <code>   &lt;gml:description&gt;information applies to the dataset&lt;/gml:description&gt;</code><br /> <code>   &lt;gml:identifier codeSpace="ISOTC211/19115"&gt;dataset&lt;/gml:identifier&gt;</code><br /> <code>&lt;/gmx:CodeDefinition&gt;</code><br /> <code>...</code></div>
<p>Note that there is no reason in practice to tab in XML and to present each XML element on a new line other than to aid humans in reading raw XML. XML parsers, on the other hand, would have no problem reading the XML were it encoded without carriage returns as shown in Figure 3.</p>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 3 - XML fragment - no tabbing </strong></h5>
<code>&lt;gmd:MD_Metadata&gt;&lt;gmd:fileIdentifier&gt;&lt;gco:CharacterString&gt;98e25be5-388d-4be3-bc5f-ba07ef6009b2&lt;/gco:CharacterString&gt;&lt;/gmd:fileIdentifier&gt;&lt;/gmd:MD_Metadata&gt;</code></div>
<p>The UK Location Information Infrastructure will accept any valid XML document that conforms to these guidelines. This includes canonical XML encodings [<a title="References" href="/40-gemini/1047-metadata-guidelines-for-geospatial-data-resources-part-3" rel="alternate">5</a>] and files laid out with additional white space for human readability, and other variants in between. Similarly, XML attribute values could be delimited using single or double quotes.</p>
<h2><a id="2"></a>2. Encoding Guidelines</h2>
<h3><a id="2.1"></a>2.1 Schemas</h3>
<p>The schemas defining the structure of GEMINI2 metadata instances must implement:</p>
<ul>
<li>ISO 19139:2007 – for a physical implementation of ISO 19115:2003</li>
<li>ISO 19119:2005 – for service metadata</li>
<li>ISO 19136:2007 – for GML</li>
</ul>
<p>Several schema sets have been identified as meeting these requirements:</p>
<ol>
<li style="text-align: left;"><a href="http://schemas.opengis.net/csw/2.0.2/profiles/apiso/1.0.0/apiso.xsd">http://schemas.opengis.net/csw/2.0.2/profiles/apiso/1.0.0/apiso.xsd</a>, provided by OGC</li>
<li><a href="http://inspire.ec.europa.eu/draft-schemas/inspire-md-schemas/apiso-inspire/apiso-inspire.xsd">http://inspire.ec.europa.eu/draft-schemas/inspire-md-schemas/apiso-inspire/apiso-inspire.xsd</a>, provided by JRC</li>
<li><a href="http://schemas.opengis.net/iso/19139/20070417">http://schemas.opengis.net/iso/19139/20070417</a>, provided by OGC.</li>
</ol>
<p>Both 1 &amp; 2 import the same dataset schemas, which are authoritatively at the ISO TC211 resource site: <a href="https://schemas.isotc211.org/schemas/19139/">https://schemas.isotc211.org/schemas/19139/</a>. Note: this is a human browsable site; if you want to validate correctly against this set of schemas, you can 'deep link' to e.g. <a href="https://schemas.isotc211.org/schemas/19139/-/gmx/1.0/gmx.xsd"><span style="font-weight: 400;">https://schemas.isotc211.org/schemas/19139/-/gmx/1.0/gmx.xsd</span></a></p>
<p>The schema files that shall be used for validating GEMINI2 metadata instances are:</p>
<ul>
<li>gmx.xsd (Datasets and dataset series metadata)</li>
<li>gmx.xsd and srv.xsd (Service metadata)</li>
</ul>
<p>The AP-ISO schema files given above import both of these, so a validator does not need to determine what type of record it is validating.</p>
<p>With schema set 3, the dataset and service schemas have separate entry points: gmx/gmx.xsd and srv/srv.xsd</p>
<p>Notes:</p>
<ol>
<li>the schemas provided by ISO TC211 do not include anything for ISO 19119 service metadata, but could be used directly to validate dataset metadata</li>
<li>the older draft schemas published at <a href="http://schemas.opengis.net/iso/19139/20060504/">http://schemas.opengis.net/iso/19139/20060504/</a> import GML version 3.1 instead of GML 3.2, so records that validate with one will not validate with the other.</li>
<li>the UK GEMINI schema that was published on GI Gateway [service withdrawn in 2012] encodes GEMINI1, not GEMINI2. Also, it does not conform with INSPIRE technical guidance. Therefore, it cannot be used to encode GEMINI2 and shall not be used for metadata instances within UK Location.</li>
</ol>
<p><strong>Schema Validation</strong></p>
<p>The XML schemaLocation property officially provides only a ‘hint’ to the validator, but many validators do use the schemas at that location.</p>
<p>The INSPIRE Validator available through <a href="https://inspire.ec.europa.eu/validator/about/">https://inspire.ec.europa.eu/validator/about/</a> includes metadata validation.</p>
<h3><a id="2.2"></a>2.2 Common concepts</h3>
<h4>2.2.1 XML declaration</h4>
<p>Metadata instances are XML documents. XML documents should, but do not have to, begin with an XML declaration. If a metadata instance has an XML declaration then it must be the first line in the document. It must not be preceded by anything else, other than an invisible Unicode byte-order mark.</p>
<p>Figure 4 shows an XML declaration. The version attribute must always have the value 1.0. The encoding attribute is optional. Its value specifies which character set is in use in the document. By default (i.e. if the encoding attribute is omitted) XML documents are assumed to be encoded in the UTF-8 encoding of the Unicode character set. Care should be taken when using text editing software to edit XML, or writing XML using bespoke software code, that the XML’s actual physical encoding conforms with the encoding stated with this attribute. It is expected that the UTF-8 character set will be sufficient in nearly all cases.</p>
<p>An XML declaration may include a “standalone” attribute. However, this attribute is only relevant if an XML document is using a DTD. Metadata instances of GEMINI2 shall not use a DTD so it is out of scope.</p>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 4 - XML declaration </strong></h5>
<code>&lt;?xml version="1.0" encoding="utf-8"?&gt;</code></div>
<h4>2.2.2 Root element</h4>
<p>The root element of a GEMINI2 metadata instance shall be gmd:MD_Metadata. The root element shall contain namespace references to, at least, gmd, gco, gml and xlink. Metadata for services shall, in addition, contain a namespace reference to srv. In addition reference may be made to the gmx namespace if XML elements such as gmx:Anchor are used.</p>
<p>An example is shown in Figure 5. Subsequent examples omit the namespace references for brevity. An ellipsis is used to indicate that required content has been omitted.</p>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure  5 - Root Element</strong></h5>
<code>&lt;?xml version="1.0" encoding="utf-8"?&gt;</code><br /> <code>&lt;gmd:MD_Metadata xmlns:gmd="http://www.isotc211.org/2005/gmd"</code><br /> <code>                 xmlns:gco="http://www.isotc211.org/2005/gco"</code><br /> <code>                 xmlns:srv="http://www.isotc211.org/2005/srv"</code><br /> <code>                 xmlns:gml="http://www.opengis.net/gml/3.2"</code><br /> <code>                 xmlns:xlink="http://www.w3.org/1999/xlink"&gt;</code><br /> <code>  ...</code><br /> <code>&lt;/gmd:MD_Metadata&gt;</code></div>
<p>The namespace identifier for gmd shall be: http://www.isotc211.org/2005/gmd</p>
<p>The namespace identifier for gco shall be: http://www.isotc211.org/2005/gco</p>
<p>The namespace identifier for srv shall be: http://www.isotc211.org/2005/srv</p>
<p>The namespace identifier for gmx shall be: http://www.isotc211.org/2005/gmx</p>
<p>The namespace identifier for xlink shall be: http://www.w3.org/1999/xlink</p>
<p>The namespace identifier for gml shall be: http://www.opengis.net/gml/3.2</p>
<p>Note that  http://www.opengis.net/gml/3.2 refers to GML version 3.2.1 <strong>not</strong> GML version 3.2.0.</p>
<p>The root element, and in fact any element in an XML instance, may have an attribute called xsi:schemaLocation which contains a value or set of values <strong>hinting </strong>at the physical location of schemas which may be used for validation. Since this attribute provides only a hint, validating parsers are allowed to ignore it and use other means of locating the relevant schemas.</p>
<p>Figure 6 shows a root element containing an xsi:schemaLocation attribute. Here the schemas referenced are in the INSPIRE Metadata XSD repository.</p>
<p>Since the xsi:schemaLocation attribute exists in the xsi namespace, this namespace must be referenced. The xsi:schemaLocation attribute contains a pair of space separated values when one schema is identified. The first value specifies the namespace and the second value specifies the schema to use to validate elements in that namespace. When more than one schema is identified, as would be the case for validating a service metadata instance, the attribute contains a space separated sequence of namespace / schema pairs. The xsi:schemaLocation attribute is not required in a GEMINI2 metadata instance.</p>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 6 - Using the xsi:schemaLocation attribute</strong></h5>
<code>&lt;?xml version="1.0" encoding="utf-8"?&gt;</code><br /> <code>&lt;gmd:MD_Metadata xmlns:gmx="http://www.isotc211.org/2005/gmx"</code><br /><code>    xmlns:gmd="http://www.isotc211.org/2005/gmd"</code><br /> <code>    xmlns:gco="http://www.isotc211.org/2005/gco"</code><br /> <code>    xmlns:srv="http://www.isotc211.org/2005/srv"</code><br /> <code>    xmlns:gml="http://www.opengis.net/gml/3.2"</code><br /> <code>    xmlns:xlink="http://www.w3.org/1999/xlink"</code><br /> <code>    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"</code><br /> <code>    xsi:schemaLocation="http://www.isotc211.org/2005/gmx</code><br /> <code>        https://schemas.isotc211.org/schemas/19139/-/gmx/1.0/gmx.xsd</code><br /> <code>        http://www.isotc211.org/2005/srv</code><br /> <code>        http://inspire.ec.europa.eu/draft-schemas/inspire-md-schemas/srv/1.0/srv.xsd"&gt;</code><br /> <code>  ...</code><br /> <code>&lt;/gmd:MD_Metadata&gt;</code></div>
<h4><a id="2.2.3"></a>2.2.3 Dates and Times</h4>
<p>Dates and date-time shall be expressed in the Gregorian calendar and UTC as per ISO 8601. The formatting shall be as follows, in order of increasing precision:</p>
<ul>
<li>yyyy (e.g. 1995)</li>
<li>yyyy-MM (e.g. 1995-01)</li>
<li>yyyy-MM-dd (e.g. 1995-01-25)</li>
<li>yyyy-MM-ddThh:mm:ss (e.g. 1995-01-25T12:01:55)</li>
</ul>
<p>The ISO 8601 encoding also allows negative dates to represent BC. However, gco:Date and gco:DateTime XML elements do not accept negative values.</p>
<p>The GEMINI2 standard states that temporal extents may be given with as coarse a granularity as century (e.g. yy or 19). However, unfortunately this cannot be encoded in ISO 19139 XML and will result in a schema validation error. The lowest level of granularity allowable is the year.</p>
<h4>2.2.4 Element order</h4>
<p>XML elements in a metadata instance must follow the order in which the elements are defined in an XSD schema. Failure to do so will result in schema validation errors. The order of XML elements and their corresponding GEMINI2 metadata items is shown <a title="example" href="/40-gemini/1046-xml-element-order" target="_blank" rel="alternate noopener noreferrer">here</a>.</p>
<h4>2.2.5 Patterns for multiple instances</h4>
<p>Some metadata items, such as alternative title, have cardinalities for more than one. This means that more than one instance of the item can be encoded in metadata instances. The general approach in ISO 19139 XML is that an XML element expressing the property, in Figure7 gmd:alternateTitle, contains an XML element which expresses the data type and contains the value, in this case gco:CharacterString. Note that more than one alternative title is expressed by repeating the gmd:alternateTitle XML element, not the gco:CharacterString XML element (shown in an invalid example in Figure 8). This pattern is followed throughout ISO 19139 XML including for XML elements that have complex content, such as gmd:identificationInfo (Figure 9).</p>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 7 - Multiple alternative title elements</strong></h5>
  <code>...</code><br /> <code>&lt;gmd:alternateTitle&gt;</code><br /> <code>  &lt;gco:CharacterString&gt;Digital Geological Map Data of Great Britain - 625k&lt;/gco:CharacterString&gt;</code><br /> <code>&lt;/gmd:alternateTitle&gt;</code><br /> <code>&lt;gmd:alternateTitle&gt;</code><br /> <code>  &lt;gco:CharacterString&gt;DiGMapGB-625&lt;/gco:CharacterString&gt;</code><br /> <code>&lt;/gmd:alternateTitle&gt;</code><br /> <code>...</code></div>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 8 - Multiple alternative title elements - invalid encoding</strong></h5>
<code>...</code><br /> <code>&lt;gmd:alternateTitle&gt;</code><br /> <code>  &lt;gco:CharacterString&gt;Digital Geological Map Data of Great Britain - 625k&lt;/gco:CharacterString&gt;</code><br /> <code>  &lt;gco:CharacterString&gt;DiGMapGB-625&lt;/gco:CharacterString&gt;</code><br /> <code>&lt;/gmd:alternateTitle&gt;</code><br /> <code>...</code></div>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 9 - Multiple identification information elements </strong></h5>
<code>&lt;gmd:MD_Metadata&gt;</code><br /> <code>  ...</code><br /> <code>  &lt;gmd:identificationInfo&gt;</code><br /> <code>   &lt;gmd:MD_DataIdentification id="_local-id1"&gt;</code><br /> <code>     ...</code><br /> <code>  &lt;/gmd:MD_DataIdentification&gt;</code><br /> <code>&lt;/gmd:identificationInfo&gt;</code><br /> <code>  &lt;gmd:identificationInfo&gt;</code><br /> <code>    &lt;gmd:MD_DataIdentification id="_local-id2"&gt;</code><br /> <code>     ...</code><br /> <code>    &lt;/gmd:MD_DataIdentification&gt;</code><br /> <code>  &lt;/gmd:identificationInfo&gt;</code><br /> <code>  ...</code><br /> <code>&lt;/gmd:MD_Metadata&gt; </code></div>
<h4><a id="2.2.6"></a>2.2.6 File identifier</h4>
<p>The first XML child element of any GEMINI2 metadata instance shall be gmd:fileIdentifier. The content of this XML element is the identifier of the metadata instance.   File identifier is not to be confused with the metadata item <a title="Resource Identifier" href="/component/content/article?id=1062#36" rel="alternate">Resource Identifier</a>.</p>
<p>The content of the XML element shall be a unique managed identifier, such as a system generated UUID. Once the identifier has been set for a metadata instance it shall not change.</p>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 10 - File Identifier</strong></h5>
<code>&lt;gmd:MD_Metadata&gt;</code><br /><code>  &lt;gmd:fileIdentifier&gt;</code><br /><code>    &lt;gco:CharacterString&gt;98e25be5-388d-4be3-bc5f-ba07ef6009b2&lt;/gco:CharacterString&gt;</code><br /><code>  &lt;/gmd:fileIdentifier&gt;</code><br /><code>  ...</code><br /><code>&lt;/gmd:MD_Metadata&gt; </code></div>
<h4>2.2.7 Citation</h4>
<p>External resources, such as publications, controlled vocabularies, are expressed using the ISO 19115 class CI_Citation and its XML element instance, gmd:CI_Citation. This is a common structure that is used to encode:</p>
<ul>
<li>Resource reference information about datasets and series</li>
<li>Resource reference information about services</li>
<li>Information about the originating controlled vocabulary of keywords</li>
<li>The specification for conformance statements</li>
<li>The authority of Spatial Reference System</li>
<li>The authority of Extent</li>
</ul>
<p>A citation must include at least a title, a date and a date type. Figure 11 shows the citation structure used to encode information about the GEMET Concepts dictionary.</p>
<p>In any one citation there may be more than one date. However, there shall be only one date with a date type of ‘creation’ and there shall be only one date with type 'revision'.</p>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 11 - CI_Citation structure</strong></h5>
<code>...</code><br /><code>&lt;gmd:CI_Citation&gt;</code><br /><code>  &lt;gmd:title&gt;</code><br /><code>    &lt;gco:CharacterString&gt;GEMET - Concepts, version 2.4&lt;/gco:CharacterString&gt;</code><br /><code>  &lt;/gmd:title&gt;</code><br /><code>  &lt;gmd:date&gt;</code><br /><code>    &lt;gmd:CI_Date&gt;</code><br /><code>      &lt;gmd:date&gt;</code><br /><code>        &lt;gco:Date&gt;2010-01-13&lt;/gco:Date&gt;</code><br /><code>      &lt;/gmd:date&gt;</code><br /><code>      &lt;gmd:dateType&gt;</code><br /><code><code>        &lt;gmd:CI_DateTypeCode codeList="</code></code><code>https://schemas.isotc211.org/schemas/19139/resources/gmxCodelists.xml</code><code>#CI_DateTypeCode" codeListValue="revision"&gt;revision&lt;/gmd:CI_DateTypeCode&gt;</code><br /><code>      &lt;/gmd:dateType&gt;</code><br /><code>    &lt;/gmd:CI_Date&gt;</code><br /><code>  &lt;/gmd:date&gt;</code><br /><code>&lt;/gmd:CI_Citation&gt;</code><br /><code>...</code></div>
<h4> <a id="2.2.8"></a>2.2.8 Responsible party</h4>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 12 - CI_ResponsibleParty structure </strong></h5>
 <code>...</code><br /><code>&lt;gmd:CI_ResponsibleParty&gt;</code><br /><code>  &lt;gmd:organisationName&gt;</code><br /><code>    &lt;gco:CharacterString&gt;SeaZone Solutions&lt;/gco:CharacterString&gt;</code><br /><code>  &lt;/gmd:organisationName&gt;</code><br /><code>  &lt;gmd:positionName&gt;</code><br /><code>    &lt;gco:CharacterString&gt;Data Product Manager&lt;/gco:CharacterString&gt;</code><br /><code>  &lt;/gmd:positionName&gt;</code><br /><code>  &lt;gmd:contactInfo&gt;</code><br /><code>    &lt;gmd:CI_Contact&gt;</code><br /><code>      &lt;gmd:phone&gt;</code><br /><code>        &lt;gmd:CI_Telephone&gt;</code><br /><code>          &lt;gmd:voice&gt;</code><br /><code>            &lt;gco:CharacterString&gt;+44 (0) 870 013 0607&lt;/gco:CharacterString&gt;</code><br /><code>          &lt;/gmd:voice&gt;</code><br /><code>          &lt;gmd:facsimile&gt;</code><br /><code>            &lt;gco:CharacterString&gt;+44 (0) 870 013 0608&lt;/gco:CharacterString&gt;</code><br /><code>          &lt;/gmd:facsimile&gt;</code><br /><code>        &lt;/gmd:CI_Telephone&gt;</code><br /><code>      &lt;/gmd:phone&gt;</code><br /><code>      &lt;gmd:address&gt;</code><br /><code>        &lt;gmd:CI_Address&gt;</code><br /><code>          &lt;gmd:deliveryPoint&gt;</code><br /><code>            &lt;gco:CharacterString&gt;Red Lion House&lt;/gco:CharacterString&gt;</code><br /><code>          &lt;/gmd:deliveryPoint&gt;</code><br /><code>          &lt;gmd:deliveryPoint&gt;</code><br /><code>            &lt;gco:CharacterString&gt;Bentley&lt;/gco:CharacterString&gt;</code><br /><code>          &lt;/gmd:deliveryPoint&gt;</code><br /><code>          &lt;gmd:administrativeArea&gt;</code><br /><code>            &lt;gco:CharacterString&gt;Hampshire&lt;/gco:CharacterString&gt;</code><br /><code>          &lt;/gmd:administrativeArea&gt;</code><br /><code>          &lt;gmd:postalCode&gt;</code><br /><code>            &lt;gco:CharacterString&gt;GU10 5HY&lt;/gco:CharacterString&gt;</code><br /><code>          &lt;/gmd:postalCode&gt;</code><br /><code>          &lt;gmd:electronicMailAddress&gt;</code><br /><code>            &lt;gco:CharacterString&gt;<span id="cloakdd5151d9d540c7fa216a246653103a1d">This email address is being protected from spambots. You need JavaScript enabled to view it.</span><script type='text/javascript'>
				document.getElementById('cloakdd5151d9d540c7fa216a246653103a1d').innerHTML = '';
				var prefix = '&#109;a' + 'i&#108;' + '&#116;o';
				var path = 'hr' + 'ef' + '=';
				var addydd5151d9d540c7fa216a246653103a1d = '&#105;nf&#111;' + '&#64;';
				addydd5151d9d540c7fa216a246653103a1d = addydd5151d9d540c7fa216a246653103a1d + 's&#101;&#97;z&#111;n&#101;' + '&#46;' + 'c&#111;m';
				var addy_textdd5151d9d540c7fa216a246653103a1d = '&#105;nf&#111;' + '&#64;' + 's&#101;&#97;z&#111;n&#101;' + '&#46;' + 'c&#111;m';document.getElementById('cloakdd5151d9d540c7fa216a246653103a1d').innerHTML += '<a ' + path + '\'' + prefix + ':' + addydd5151d9d540c7fa216a246653103a1d + '\'>'+addy_textdd5151d9d540c7fa216a246653103a1d+'<\/a>';
		</script>&lt;/gco:CharacterString&gt;</code><br /><code>          &lt;/gmd:electronicMailAddress&gt;</code><br /><code>        &lt;/gmd:CI_Address&gt;</code><br /><code>      &lt;/gmd:address&gt;</code><br /><code>      &lt;gmd:onlineResource&gt;</code><br /><code>        &lt;gmd:CI_OnlineResource&gt;</code><br /><code>          &lt;gmd:linkage&gt;</code><br /><code>            &lt;gmd:URL&gt;http://www.seazone.com/index.php&lt;/gmd:URL&gt;</code><br /><code>          &lt;/gmd:linkage&gt;</code><br /><code>        &lt;/gmd:CI_OnlineResource&gt;</code><br /><code>      &lt;/gmd:onlineResource&gt;</code><br /><code>    &lt;/gmd:CI_Contact&gt;</code><br /><code>  &lt;/gmd:contactInfo&gt;</code><br /><code>  &lt;gmd:role&gt;</code><br /><code><code>    &lt;gmd:CI_RoleCode codeList="</code></code><code>https://schemas.isotc211.org/schemas/19139/resources/gmxCodelists.xml</code><code>#CI_RoleCode" codeListValue="author"&gt;author&lt;/gmd:CI_RoleCode&gt;</code><br /><code>  &lt;/gmd:role&gt;</code><br /><code>&lt;/gmd:CI_ResponsibleParty&gt;</code><br /><code>...</code></div>
<p>Addresses are expressed using the ISO 19115 class CI_ResponsibleParty and its XML element instance, gmd:CI_ResponsibleParty. This is a common structure that is used to encode:</p>
<ul>
<li>Metadata contact</li>
<li>Responsible organisation</li>
</ul>
<p>In the context of GEMINI2 a responsible party set shall include at least the organisation name (encoded using gmd:organisationName), an email address (encoded using gmd:electronicMailAddress) and a role (encoded using gmd:role).</p>
<p>The XML element role takes values from the ISO 19115 codelist CI_RoleCode. Any value in the code list may be chosen.</p>
<p>Additionally, the contact position (encoded using gmd:positionName), the postal address (encoded using a combination of gmd:deliveryPoint, gmd:city, gmd:administrativeArea, gmd:postalCode and gmd:country), telephone number (encoded using gmd:voice) and facsimile number (encoded using gmd:facsimile) may be provided.</p>
<h4><a id="2.2.9"></a>2.2.9 Code lists</h4>
<p>Where a sub-item takes its value from a code list, which may or may not be expressed in ISO 19115, the source code list catalogue and code list value shall be expressed using the attributes gmd:codeList and gmd:codeListValue respectively.</p>
<p>Figure 13 shows the encoding where a code list is specified in ISO 19115. The value of the codeList attribute should be the URL for the ISO 19115 code list catalogue that is published on the ISO website:</p>
<p style="padding-left: 60px;"><a title="https://schemas.isotc211.org/schemas/19139/resources/gmxCodelists.xml" href="https://schemas.isotc211.org/schemas/19139/resources/gmxCodelists.xml" target="_blank" rel="alternate noopener noreferrer">https://schemas.isotc211.org/schemas/19139/resources/gmxCodelists.xml</a></p>
<p>Plus a hash character acting as a delimiter, and then the identifier of the code list, in this case ‘MD_ScopeCode’, that contains the code list value that is used. This information could be used to validate the code list value and ensure that it is a member of the code list.</p>
<p>The value of the code list value attribute (gmd:codeListValue) shall be a valid entry from the specified code list dictionary.</p>
<p>The element value (i.e. in Figure 13  <code>&lt;gmd:MD_ScopeCode ...&gt;<strong>dataset</strong>&lt;/gmd:MD_ScopeCode&gt;</code>) is human readable text. It can be omitted or given a value different from that of the attribute codeListValue (e.g. Dataset).  Developers of GEMINI aware applications should note that reliance should not be placed on the element value of code list elements but rather on the value of the attribute gmd:codeListValue.</p>
<div style="width: 63em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 13 - Code list</strong></h5>
<code>&lt;gmd:MD_ScopeCode codeList="<a href="https://schemas.isotc211.org/schemas/19139/resources/gmxCodelists.xml">https://schemas.isotc211.org/schemas/19139/resources/gmxCodelists.xml</a></code><code>#MD_ScopeCode" </code><br /><code>  codeListValue="dataset"&gt;dataset&lt;/gmd:MD_ScopeCode&gt;</code></div>
<p>Figure 14 shows a fragment of the code list catalogue with the entries of MD_ScopeCode that are relevant to GEMINI2 metadata.</p>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 14 - Fragment of the code list catalogue</strong></h5>
<code>&lt;CT_CodelistCatalogue xmlns="http://www.isotc211.org/2005/gmx" </code><br /><code>                      xmlns:gco="http://www.isotc211.org/2005/gco" </code><br /><code>                      xmlns:gml="http://www.opengis.net/gml/3.2" </code><br /><code>                      xmlns:xlink="http://www.w3.org/1999/xlink" </code><br /><code>                      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"&gt;</code><br /><code>  ...</code><br /><code>  &lt;!--=== MD_ScopeCode ===--&gt;</code><br /><code>  &lt;codelistItem&gt;</code><br /><code>    &lt;CodeListDictionary gml:id="MD_ScopeCode"&gt;</code><br /><code>      &lt;gml:description&gt;class of information to which the referencing entity applies&lt;/gml:description&gt;</code><br /><code>      &lt;gml:identifier codeSpace="ISOTC211/19115"&gt;MD_ScopeCode&lt;/gml:identifier&gt;</code><br /><code>      ...</code><br /><code>      &lt;codeEntry&gt;</code><br /><code>        &lt;CodeDefinition gml:id="MD_ScopeCode_dataset"&gt;</code><br /><code>          &lt;gml:description&gt;information applies to the dataset&lt;/gml:description&gt;</code><br /><code>          &lt;gml:identifier codeSpace="ISOTC211/19115"&gt;dataset&lt;/gml:identifier&gt;</code><br /><code>        &lt;/CodeDefinition&gt;</code><br /><code>      &lt;/codeEntry&gt;</code><br /><code>      &lt;codeEntry&gt;</code><br /><code>        &lt;CodeDefinition gml:id="MD_ScopeCode_series"&gt;</code><br /><code>          &lt;gml:description&gt;information applies to the series&lt;/gml:description&gt;</code><br /><code>          &lt;gml:identifier codeSpace="ISOTC211/19115"&gt;series&lt;/gml:identifier&gt;</code><br /><code>        &lt;/CodeDefinition&gt;</code><br /><code>      &lt;/codeEntry&gt;</code><br /><code>      ...</code><br /><code>      &lt;codeEntry&gt;</code><br /><code>        &lt;CodeDefinition gml:id="MD_ScopeCode_service"&gt;</code><br /><code>          &lt;gml:description&gt;information applies to a capability which a service provider entity makes available to a service user entity through a set of interfaces that define a behaviour, such as a use case&lt;/gml:description&gt;</code><br /><code>          &lt;gml:identifier codeSpace="ISOTC211/19115"&gt;service&lt;/gml:identifier&gt;</code><br /><code>        &lt;/CodeDefinition&gt;</code><br /><code>      &lt;/codeEntry&gt;</code><br /><code>      ...</code><br /><code>    &lt;/CodeListDictionary&gt;</code><br /><code>  &lt;/codelistItem&gt;</code><br /><code>&lt;/CT_CodelistCatalogue&gt; </code></div>
<h4>2.2.10 Null Values</h4>
<p>The ISO 19139 XML schemas provide a means for indicating that the contents of an element may be unknown or withheld, through the use of the gco:nilReason attribute. This attribute can be added to any element in the gmd namespace. It can take the following values:</p>
<ul>
<li>inapplicable</li>
<li>missing</li>
<li>template</li>
<li>unknown</li>
<li>withheld</li>
<li>other:[any text]</li>
</ul>
<p>Empty XML elements (see Figure 15) are not permitted in ISO 19139 metadata instances. Although this is not checked by the “Table A” schematron rules in use in UK Location, those creating metadata records should avoid creating empty XML elements if at all possible. If an optional element is not required, don’t include it; if a mandatory element is not available use gco:nilReason.</p>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 15 - Examples of empty elements not permitted in GEMINI metadata instances</strong></h5>
<p><code>&lt;gco:CharacterString/&gt;</code></p>
<p><code>&lt;gco:CharacterString&gt;&lt;/gco:CharacterString&gt;</code></p>
<p><code>&lt;gmx:Anchor /&gt;</code></p>
<p><code>&lt;gmx:Anchor&gt;&lt;/gmx:Anchor&gt;</code></p>
</div>
<p>The following metadata items shall not be nillable:</p>
<ul>
<li>Title</li>
<li>Abstract</li>
<li>Bounding box (west, east, south and north coordinates)</li>
<li>Unique resource identifier</li>
<li>Responsible organization</li>
<li>Metadata point of contact</li>
<li>Topic category</li>
<li>Originating controlled vocabulary title</li>
<li>File identifier</li>
</ul>
<h4>2.2.11 By Value or By Reference</h4>
<p>The content of a metadata instance may be expressed <em>by value</em> or <em>by reference</em>. <em>By value</em> means that the metadata instance carries all the necessary information. <em>By reference</em> means that a metadata instance indicates that content is to be found in an external repository or another place within the same instance. The <em>by reference</em> case is supported by the object reference (gco:ObjectReference) attribute group. This provides two mechanisms for referencing remote resources:</p>
<ul>
<li>XLink, primarily using the xlink:href attribute</li>
<li>By UUID using the uuidref attribute</li>
</ul>
<p>Figure 16 shows the use of the XLink href attribute to specify a vertical CRS by reference to the EPSG Geodetic parameter dataset while Figure 17 shows the same information encoded by value (note however, that in this case the domain of validity (gml:domainOfValidity), vertical coordinate system (gml:verticalCS) and vertical datum (gml:verticalDatum) are themselves encoded <em>by reference</em>).</p>
<p>Encoding information <em>by reference</em> is clearly advantageous in the sense that it is more efficient (in terms of file size but also avoiding data duplication) than by value. However, it presupposes that an XML software application will ‘know’ how to dereference the reference. Dereferencing is the act of obtaining the externally referenced information. It is also important that the referenced information is universally available in a structured machine readable form so that it can be incorporated by value. In the case of the examples below the EPSG web service endpoint can be used to dereference the EPSG URN to return the GML encoded vertical CRS. The GML can be directly incorporated in an XML metadata instance, where the metadata element accepts a GML value (noting that there will be a difference in the GML namespace identifier – EPSG returning GML 3.1.1 while metadata instances shall identify the GML 3.2.1 namespace – in the case of the CRS XML elements of GML there is no difference between these versions of GML).</p>
<p>Typically, <em>by reference</em> shall be used for identifying the vertical CRS of a vertical extent and the implementation of coupled resource (following INSPIRE guidelines) alone. The XLink mechanism shall be used (see Figure 16 for vertical CRS and Figure 18 for coupled resource). Note that in encoding coupled resource by referencing the uuidref attribute may also be used, in addition to XLink. All other metadata items shall be implemented <em>by value</em>.</p>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 16 - Vertical CRS by reference</strong></h5>
<code>&lt;gmd:verticalCRS xlink:href="http://www.opengis.net/def/crs/EPSG/0/5701"/&gt;</code></div>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 17 - Vertical CRS by value</strong></h5>
<code>...</code><br /><code>&lt;gmd:verticalCRS&gt;</code><br /><code>  &lt;gml:VerticalCRS gml:id="epsg-crs-5701"&gt;</code><br /><code>    &lt;gml:identifier codeSpace="OGP"&gt;<a href="http://www.opengis.net/def/crs/EPSG/0/5701/">http://www.opengis.net/def/crs/EPSG/0/5701/</a>&lt;/gml:identifier&gt;</code><br /><code>    &lt;gml:name&gt;ODN height&lt;/gml:name&gt;</code><br /><code>    &lt;gml:domainOfValidity xlink:href="<a href="http://www.opengis.net/def/crs/EPSG/0/2792/">http://www.opengis.net/def/crs/EPSG/0/2792/</a>"/&gt;</code><br /><code>    &lt;gml:scope&gt;Geodetic and engineering surveying.&lt;/gml:scope&gt;</code><br /><code>    &lt;gml:verticalCS xlink:href="<a href="http://www.opengis.net/def/crs/EPSG/0/649/9">http://www.opengis.net/def/crs/EPSG/0/6499/</a>"/&gt;</code><br /><code>    &lt;gml:verticalDatum xlink:href="<a href="/&quot;http:/www.opengis.net/def/crs/EPSG/0/5101/">http://www.opengis.net/def/crs/EPSG/0/5101/</a>"&gt;</code><br /><code>  &lt;/gml:VerticalCRS&gt;</code><br /><code>&lt;/gmd:verticalCRS&gt;</code><br /><code>... </code></div>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 18 - Coupled resource by reference</strong></h5>
<code>&lt;srv:operatesOn xlink:title="Digital Geological Map Data of Great Britain - 625k (DiGMapGB-625) 2008" </code><br /><code>xlink:href="http://metadata.bgs.ac.uk/geonetwork/srv/en/csw?SERVICE=CSW&amp;REQUEST=GetRecordById</code><br /><code>&amp;ID=9df8df52-d788-37a8-e044-0003ba9b0d98&amp;OutputSchema=http://www.isotc211.org/2005/gmd&amp;elementSetName=full#BGS-13480426&amp;" uuidref="9df8df52-d788-37a8-e044-0003ba9b0d98" /&gt;</code></div>
<h4><a id="2.2.12"></a>2.2.12 Identifiers</h4>
<p>GML XML elements which are used in metadata have an optional gml:id attribute. The value domain of the identifier is referred to as <em>XML name</em>. XML names have certain restrictions. They may contain any alphanumeric character, non-English alphanumeric characters, ideograms and the underscore, hyphen and period. They may not contain any other punctuation characters. The colon is allowed, but its use is reserved for namespaces, so it cannot appear in an identifier. XML names may not include any whitespace including spaces and carriage returns. All names beginning with the letters XML (in uppercase, lowercase or any mixture thereof) are reserved (see [<a title="References" href="/40-gemini/1047-metadata-guidelines-for-geospatial-data-resources-part-3" target="_blank" rel="alternate noopener noreferrer">11</a>] pages 18 and 19).</p>
<p>XML names may only start with letters, ideograms and the underscore character. Consequently, care must be taken when using the value of a UUID as the value of an identifier because these can begin with numeric characters.  If using UUIDs as the basis of such an identifier best practice is to prefix the UUIDs with an underscore.</p>
<p>An identifier must be unique within the scope of any XML document (i.e. there shall not be more than one id type attribute with a particular identifier value) that the metadata record might occur in, such as a result set from a CSW query and not just the metadata document itself. </p>
<p>If an id type attribute contains an illegally formed XML name the result will be a schema validation error.</p>
<h4>2.2.13 Free text</h4>
<p>In GEMINI2 there are two ways of encoding free text.  The basic element for providing text of unrestricted length with no internal XML structure is gco:CharacterString. This element is appropriate when the text does not refer to a specific external resource or registry.  When the  provided text is a term or code referring to an externally defined explanation or registry value, gmx:Anchor element is <strong>recommended</strong> over gco:CharacterString. gmx:Anchor contains an additional attribute group enabling linking the provided piece of text with an external describing resource. The most important of these attributes in this context is xlink:href, which contains the actual reference in Uniform Resource Identifier (URI) format.</p>
<p>For example the encoding of an identifier/code value should be done with gmx:Anchor as in Figure 19, rather than gco:CharacterString (Figure 20), when the unique resource identifier is referenceable,</p>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 19 - Non-empty free text, with gmx:Anchor</strong></h5>
<pre>&lt;gmd:identifier&gt;
  &lt;gmd:MD_Identifier&gt;
    &lt;gmd:code&gt;
      &lt;gmx:Anchor xlink:href="http://data.bgs.ac.uk/id/dataHolding/13480180"&gt;
       World Mineral Statistics Dataset
      &lt;/gmx:Anchor&gt;
    &lt;/gmd:code&gt;
  &lt;/gmd:MD_Identifier&gt;
&lt;/gmd:identifier&gt;
</pre>
</div>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 20 - Non-empty free text, with gco:CharacterString</strong></h5>
<pre>&lt;gmd:identifier&gt;
  &lt;gmd:MD_Identifier&gt;
    &lt;gmd:code&gt;
      &lt;gco:CharacterString&gt;
        http://data.bgs.ac.uk/id/dataHolding/13605835
      &lt;/gco:CharacterString&gt;
    &lt;/gmd:code&gt;
  &lt;/gmd:MD_Identifier&gt;
&lt;/gmd:identifier&gt;</pre>
</div>
<h4><a id="2.2.14"></a>2.2.14 Limitations, conditions, and licences</h4>
<p>GEMINI contains two elements, 25 <em>Limitations on public access</em> and 26 <em>Use constraints</em>. These represent the two INSPIRE elements <em>Limitations on public access</em> and <em>Conditions applying to access and use</em>, and are therefore both encoded with ISO 19115 MD_LegalConstraints elements. INSPIRE requires that they are encoded in separate MD_LegalConstraints elements. This means that a GEMINI metadata record must contain at least two MD_LegalConstraints elements.</p>
<p>INSPIRE requires that both of these elements use MD_RestrictionCode = otherRestrictions. Because GEMINI element 26 is for <strong>use</strong> constraints, it makes sense for both elements to place this inside a useConstraints element. Having specified <em>otherRestrictions</em>, each shall then use one or more <em>otherConstraints</em> elements to specify the actual constraints.</p>
<p>For <em>Limitations on public access</em>, at least one of the <em>otherConstraints </em>elements shall use gmx:Anchor to indicate the kind of constraint, by reference to the appropriate entry in the INSPIRE registry (http://inspire.ec.europa.eu/metadata-codelist/LimitationsOnPublicAccess). The free text within the anchor can provide human readable detail.</p>
<p>For <em>Use constraints</em>, if there are no conditions, or the conditions are unknown, then use gmx:Anchor to reference the appropriate entry in the INSPIRE registry (http://inspire.ec.europa.eu/metadata-codelist/ConditionsApplyingToAccessAndUse). Similarly, if the conditions are documented in a license, use gmx:Anchor to reference the full license text. The free text within the anchor can provide a human readable summary. If the conditions are not available at a URL, they can be entered as plain text; see FIgure 22b.</p>
<p>Three examples:</p>
<p>Figure 21 describes a commercial product, not available to the public for IPR reasons, and with a web page describing licences</p>
<div style="border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 21 - OS licence</strong></h5>
<pre>&lt;!-- INSPIRE C.17; GEMINI 25 Limitations on public access --&gt; <br />&lt;gmd:resourceConstraints&gt;<br /> &lt;gmd:MD_LegalConstraints&gt;<br />  &lt;gmd:accessConstraints&gt;<br />   &lt;gmd:MD_RestrictionCode<br />codeList="<code>https://schemas.isotc211.org/schemas/19139/resources/gmxCodelists.xml</code>#MD_RestrictionCode"<br /> codeListValue="otherRestrictions"&gt;otherRestrictions&lt;/gmd:MD_RestrictionCode&gt;<br />   &lt;/gmd:accessConstraints&gt;<br />  &lt;gmd:otherConstraints&gt;<br />   &lt;gmx:Anchor xlink:href="http://inspire.ec.europa.eu/metadata-codelist/LimitationsOnPublicAccess/INSPIRE_Directive_Article13_1e"/&gt;<br />  &lt;/gmd:otherConstraints&gt;<br /> &lt;/gmd:MD_LegalConstraints&gt;<br />&lt;/gmd:resourceConstraints&gt;<br /><br /> &lt;!-- INSPIRE C.18; GEMINI 26 use constraints --&gt; <br />&lt;gmd:resourceConstraints&gt;<br /> &lt;gmd:MD_LegalConstraints&gt;<br />  &lt;gmd:useConstraints&gt;<br />   &lt;gmd:MD_RestrictionCode<br />codeList="<code>https://schemas.isotc211.org/schemas/19139/resources/gmxCodelists.xml</code>#MD_RestrictionCode"<br /> codeListValue="otherRestrictions"&gt;otherRestrictions&lt;/gmd:MD_RestrictionCode&gt;<br />   &lt;/gmd:useConstraints&gt;<br />  &lt;gmd:otherConstraints&gt;<br />   &lt;gmx:Anchor xlink:href="https://os.uk/business/licences/index.html"&gt;Use limitation dependent upon licence&lt;/gmx:Anchor&gt;<br />  &lt;/gmd:otherConstraints&gt;<br /> &lt;/gmd:MD_LegalConstraints&gt;<br />&lt;/gmd:resourceConstraints&gt;</pre>
</div>
<p>Figure 22a describes an open data product, with no limitations on public access, the Open Government Licence referenced, and summarised in plain text.</p>
<div style="border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 22a - INSPIRE no limitations; OGL</strong></h5>
<pre>&lt;!-- INSPIRE C.17; GEMINI 25 Limitations on public access --&gt; <br />&lt;gmd:resourceConstraints&gt;<br /> &lt;gmd:MD_LegalConstraints&gt;<br />  &lt;gmd:accessConstraints&gt;<br />   &lt;gmd:MD_RestrictionCode<br />codeList="<code>https://schemas.isotc211.org/schemas/19139/resources/gmxCodelists.xml</code>#MD_RestrictionCode"<br /> codeListValue="otherRestrictions"&gt;otherRestrictions&lt;/gmd:MD_RestrictionCode&gt;<br />   &lt;/gmd:accessConstraints&gt;<br />  &lt;gmd:otherConstraints&gt;<br />   &lt;gmx:Anchor xlink:href="http://inspire.ec.europa.eu/metadata-codelist/LimitationsOnPublicAccess/noLimitations"&gt;no limitations&lt;/gmx:Anchor&gt;<br />  &lt;/gmd:otherConstraints&gt;<br /> &lt;/gmd:MD_LegalConstraints&gt;<br />&lt;/gmd:resourceConstraints&gt;<br /><br /> &lt;!-- INSPIRE C.18; GEMINI 26 use constraints --&gt; <br />&lt;gmd:resourceConstraints&gt;<br /> &lt;gmd:MD_LegalConstraints&gt; &lt;!-- change existing example here, was MD_Constraints --&gt;<br />  &lt;gmd:useConstraints&gt;<br />   &lt;gmd:MD_RestrictionCode<br />codeList="<code>https://schemas.isotc211.org/schemas/19139/resources/gmxCodelists.xml</code>#MD_RestrictionCode"<br /> codeListValue="otherRestrictions"&gt;otherRestrictions&lt;/gmd:MD_RestrictionCode&gt;<br />   &lt;/gmd:useConstraints&gt;<br />  &lt;gmd:otherConstraints&gt;<br />   &lt;gmx:Anchor xlink:href="http://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/"&gt;Attribution required&lt;/gmx:Anchor&gt;<br />  &lt;/gmd:otherConstraints&gt;<br /> &lt;/gmd:MD_LegalConstraints&gt;<br />&lt;/gmd:resourceConstraints&gt;</pre>
</div>
<p>Figure 22b describes an open data product, with no limitations on public access, but plain text conditions of use.</p>
<div style="border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 22b - INSPIRE no limitations on access; constraint on use</strong></h5>
<pre>&lt;!-- INSPIRE C.17; GEMINI 25 Limitations on public access --&gt; <br />&lt;gmd:resourceConstraints&gt;<br /> &lt;gmd:MD_LegalConstraints&gt;<br />  &lt;gmd:accessConstraints&gt;<br />   &lt;gmd:MD_RestrictionCode<br />codeList="<code>https://schemas.isotc211.org/schemas/19139/resources/gmxCodelists.xml</code>#MD_RestrictionCode"<br /> codeListValue="otherRestrictions"&gt;otherRestrictions&lt;/gmd:MD_RestrictionCode&gt;<br /> &lt;/gmd:accessConstraints&gt;<br /> &lt;gmd:otherConstraints&gt;<br /> &lt;gmx:Anchor xlink:href="http://inspire.ec.europa.eu/metadata-codelist/LimitationsOnPublicAccess/noLimitations"&gt;no limitations&lt;/gmx:Anchor&gt;<br /> &lt;/gmd:otherConstraints&gt;<br /> &lt;/gmd:MD_LegalConstraints&gt;<br />&lt;/gmd:resourceConstraints&gt;<br /><br /> &lt;!-- INSPIRE C.18; GEMINI 26 use constraints --&gt; <br />&lt;gmd:resourceConstraints&gt;<br /> &lt;gmd:MD_LegalConstraints&gt; &lt;!-- change existing example here, was MD_Constraints --&gt;<br /> &lt;gmd:useConstraints&gt;<br /> &lt;gmd:MD_RestrictionCode<br />codeList="<code>https://schemas.isotc211.org/schemas/19139/resources/gmxCodelists.xml</code>#MD_RestrictionCode"<br /> codeListValue="otherRestrictions"&gt;otherRestrictions&lt;/gmd:MD_RestrictionCode&gt;<br /> &lt;/gmd:useConstraints&gt;<br /> &lt;gmd:otherConstraints&gt;<br /> &lt;gco:CharacterString&gt;Not to be used for navigation&lt;/gco:CharacterString&gt;<br /> &lt;/gmd:otherConstraints&gt;<br /> &lt;/gmd:MD_LegalConstraints&gt;<br />&lt;/gmd:resourceConstraints&gt;</pre>
</div>
<h3><a id="2.3"></a>2.3 Metadata for datasets and dataset series</h3>
<h4>2.3.1 Data identification</h4>
<p>XML elements for encoding metadata for datasets and series of datasets are drawn, primarily, from the gmd and gco namespaces and also the gml and xlink namespaces. Identification information is encoded using the gmd:MD_DataIdentification type (Figure 23).</p>
<p>Metadata instances may include more than one gmd:identificationInfo XML element. The first gmd:identificationInfo XML element in a GEMINI metadata instance for datasets or series shall have as its first and only child XML element gmd:MD_DataIdentification. The ISO 19115 hierarchyLevel element shall be set to “dataset” or “series”. For a series, ISO 19115 hierarchyLevelName element must also be set, to "dataset" or "series" as appropriate.</p>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 23 - Metadata for datasets using the gmd:MD_DataIdentification type </strong></h5>
<code>&lt;gmd:MD_Metadata&gt;</code><br /><code>  ...</code><br /><code>  &lt;gmd:hierarchyLevel&gt;</code><br /><code><code>    &lt;gmd:MD_ScopeCode codeList="</code></code><code>https://schemas.isotc211.org/schemas/19139/resources/gmxCodelists.xml</code><code>#MD_ScopeCode" codeListValue="dataset"&gt;dataset&lt;/gmd:MD_ScopeCode&gt;</code><br /><code>  &lt;/gmd:hierarchyLevel&gt;</code><br /><code>  ...</code><br /><code>  &lt;gmd:identificationInfo&gt;</code><br /><code>    &lt;gmd:MD_DataIdentification&gt;</code><br /><code>      ...</code><br /><code>    &lt;/gmd:MD_DataIdentification&gt;</code><br /><code>  &lt;/gmd:identificationInfo&gt;</code><br /><code>  ...</code><br /><code>&lt;/gmd:MD_Metadata&gt;</code></div>
<h3><a id="2.3.2"></a>2.3.2 Detailed guidance for each metadata element</h3>
<ul>
<li><a title="Detailed guidance – datasets and series" href="/40-gemini/1062-gemini-datasets-and-data-series" rel="alternate">Datasets and series</a></li>
</ul>
<h3><a id="2.4"></a>2.4 Metadata for services</h3>
<h4>2.4.1 Service identification</h4>
<p>XML elements for encoding metadata for services are drawn from the gmd, gco, gml, xlink and srv namespaces. Identification information is encoded using the srv:SV_ServiceIdentification type (Figure 24).</p>
<p>Metadata may include more than one gmd:identificationInfo XML element. The first gmd:identificationInfo XML element in a GEMINI metadata instance for services shall have as its first child XML element srv:SV_ServiceIdentification. The ISO 19115 hierarchyLevel element shall be set to “service”, ISO 19115 hierarchyLevelName element must also be set, to "service".</p>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 24 - Metadata for services using the srv:SV_ServiceIdentification type</strong></h5>
<code>&lt;gmd:MD_Metadata&gt;</code><br /><code>  ...</code><br /><code>  &lt;gmd:hierarchyLevel&gt;</code><br /><code>    &lt;gmd:MD_ScopeCode </code><br /><code><code>      codeList="</code></code><code>https://schemas.isotc211.org/schemas/19139/r</code><code>esources/codelist/gmxCodelists.xml#MD_ScopeCode" </code><br /><code>      codeListValue="service"&gt;service</code><br /><code>    &lt;/gmd:MD_ScopeCode&gt;</code><br /><code>  &lt;/gmd:hierarchyLevel&gt;</code><br /><code>  &lt;gmd:hierarchyLevelName&gt;</code><br /><code>    &lt;gco:CharacterString&gt;service&lt;/gco:CharacterString&gt;</code><br /><code>  &lt;/gmd:hierarchyLevelName&gt;</code><br /><code>  ...</code><br /><code>  &lt;gmd:identificationInfo&gt;</code><br /><code>    &lt;srv:SV_ServiceIdentification&gt;</code><br /><code>      ...</code><br /><code>    &lt;/srv:SV_ServiceIdentification&gt;</code><br /><code>  &lt;/gmd:identificationInfo&gt;</code></div>
<h4>2.4.2 Service metadata null values</h4>
<p>The ISO 19119 class SV_ServiceIdentification includes two mandatory properties that are out of scope of GEMINI2 metadata. These are srv:couplingType and srv:containsOperations. Both shall be implemented with null values with the nil reason being missing (Figure 23).</p>
<div style="width: 60em; border-style: solid; border-width: thin; margin: 2ex 2em 6ex 5em; padding: 1em;">
<h5><strong>Figure 25 – Coupling Type and Contains Operations – Null values</strong></h5>
<code>&lt;gmd:MD_Metadata&gt;</code><br /><code>  ...</code><br /><code>  &lt;gmd:identificationInfo&gt;</code><br /><code>    &lt;srv:SV_ServiceIdentification&gt;</code><br /><code>      ...</code><br /><code>      &lt;srv:couplingType gco:nilReason="missing"/&gt;</code><br /><code>      &lt;srv:containsOperations gco:nilReason="missing"/&gt;</code><br /><code>      ...</code><br /><code>    &lt;/srv:SV_ServiceIdentification&gt;</code><br /><code>  &lt;/gmd:identificationInfo&gt;</code><br /><code>  ...</code><br /><code>&lt;/gmd:MD_Metadata&gt;</code></div>
<h3><a id="2.4.3"></a>2.4.3 Detailed guidance for each metadata element</h3>
<ul>
<li><a title="Detailed guidance – services" href="/40-gemini/1063-gemini-services" rel="alternate">Services</a></li>
</ul>
<p><em>Last technical update: March 2019</em></p>
<p><a href="http://creativecommons.org/licenses/by/4.0/" rel="license"> <img style="border-width: 0;" src="https://i.creativecommons.org/l/by/4.0/88x31.png" alt="Creative Commons Licence" /> </a> <br />This work is licensed under a <a href="http://creativecommons.org/licenses/by/4.0/" rel="license">Creative Commons Attribution 4.0 International License</a></p> 	
	
