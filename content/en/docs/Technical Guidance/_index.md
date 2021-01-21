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
<p style="padding-left: 30px;"><a title="Series metadata instance example" href="/40-gemini/1043-series-metadata-example-old" target="_blank" rel="alternate noopener noreferrer">Series metadata instance example</a></p>
<p style="padding-left: 30px;"><a title="Service metadata instance example" href="/40-gemini/1042-service-metadata-instance-example" target="_blank" rel="alternate noopener noreferrer">Service metadata instance example</a></p>
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
	