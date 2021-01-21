---
title: "Metadata Guidelines for Geospatial Data Resources - Part 1"
linkTitle: "Part 1"
date: 2017-01-05
description: >
  New to metadata then follow this link to gain a general introduction to metadata for geographic information before going any further. Metadata Guidelines for Geospatial Data Resources - Part 1
---

{{% pageinfo %}}
Metadata Guidelines for Geospatial Data Resources - Part 1
{{% /pageinfo %}}
				
<h2>Introduction to Metadata</h2>
<h3>July 2018</h3>
<p>Return to <a title="GEMINI 2.3 home page" href="/gemini/40-gemini/1037-uk-gemini-standard-and-inspire-implementing-rules">GEMINI 2.3 home page</a></p>
<p><a href="#Intro">1. Introduction</a></p>
<p><a title="Fundamentals of Metadata" href="#fundamentals" rel="alternate">2. Fundamentals of Metadata</a></p>
<p style="padding-left: 30px;"><a title="2.1 The nature of metadata" href="#2.1" rel="alternate">2.1 The nature of metadata</a></p>
<p style="padding-left: 30px;"><a title="2.2 Metadata services" href="#2.2" rel="alternate">2.2 Metadata services</a></p>
<p style="padding-left: 30px;"><a title="2.3 Metadata as a business process" href="#2.3" rel="alternate">2.3 Metadata as a business process</a></p>
<p style="padding-left: 30px;"><a title="2.4 Metadata roles" href="#2.4" rel="alternate">2.4 Metadata roles</a></p>
<p style="padding-left: 30px;"><a title="2.5 Metadata standards" href="#2.5" rel="alternate">2.5 Metadata standards</a></p>
<p><a title="General principles of Metadata" href="#principles" rel="alternate">3. General principles of Metadata</a></p>
<p style="padding-left: 30px;"><a title="3.1 Introduction" href="#3.1" rel="alternate">3.1 Introduction</a></p>
<p style="padding-left: 30px;"><a title="3.2 Free text" href="#3.2" rel="alternate">3.2 Free text</a></p>
<p style="padding-left: 30px;"><a title="3.3 Obligation" href="#3.3" rel="alternate">3.3 Obligation</a></p>
<p style="padding-left: 30px;"><a title="3.4 Element domains" href="#3.4" rel="alternate">3.4 Element domains</a></p>
<p style="padding-left: 30px;"><a title="3.5 Spatial references" href="#3.5" rel="alternate">3.5 Spatial references</a></p>
<p style="padding-left: 30px;"><a title="3.6 Date fields" href="#3.6" rel="alternate">3.6 Date fields</a></p>
<p><a title="Data resources in Scope" href="#scope" rel="alternate">4. Data resources in Scope</a></p>
<p style="padding-left: 30px;"><a title="4.1 What is stated in UK GEMINI2" href="#4.1" rel="alternate">4.1 What is stated in UK GEMINI2</a></p>
<p style="padding-left: 30px;"><a title="4.2 Characteristics of data resources in scope" href="#4.2" rel="alternate">4.2 Characteristics of data resources in scope</a></p>
<p style="padding-left: 30px;"><a title="4.3 Applicability of UK GEMINI2" href="#4.3" rel="alternate">4.3 Applicability of UK GEMINI2</a></p>
<p style="padding-left: 30px;"><a title="4.4 Levels of data resources for documentation" href="#4.4" rel="alternate">4.4 Levels of data resources for documentation</a></p>
<h2>Preface</h2>
<p>These guidelines cover the basics of metadata for geospatial data resources and services. They are intended for general use in the UK geographic information environment and serve as a preamble to the more detailed and specific guidelines <a href="/gemini/40-gemini/1049-metadata-guidelines-for-geospatial-data-resources-part-2">Metadata Guidelines for Geospatial Data Resources - Part 2</a>. They are primarily concerned with geospatial data (i.e. that which references data to a location on the surface of the Earth), and which has a limited geographic extent (i.e. is restricted to a defined territory). Services which provide access to such data are also in scope. The Guidelines have been developed within the context of the capture and maintenance of metadata for INSPIRE using the UK’s interpretation of the INSPIRE implementing rules, referred to as UK GEMINI2. However, they are sufficiently broadly based to be applicable in a wider context of geospatial metadata creation and management.</p>
<p>The Guidelines are aimed at data managers and creators of metadata, providers of metadata services and general data users. They include some guidance on quality management such that they could be used in the context of a national metadata service. A UK discovery metadata service forms part of data.gov.uk. As well as the human usable portal, this has a machine readable OGC “Catalogue Services for the Web” interface (<a title="CSW Get Capabilities" href="http://csw.data.gov.uk/geonetwork/srv/en/csw?service=CSW&amp;version=2.0.2&amp;request=GetCapabilities">OGC Capabilities document link</a>).</p>
<p>The Guidelines have been revised during 2018 in the light of other developments, including revisions to UK GEMINI2. Any comments on these Guidelines or on UK GEMINI2 should be sent to <span id="cloakc4f0a2f39700a261b7a871c23abcbdad">This email address is being protected from spambots. You need JavaScript enabled to view it.</span><script type='text/javascript'>
		document.getElementById('cloakc4f0a2f39700a261b7a871c23abcbdad').innerHTML = '';
		var prefix = '&#109;a' + 'i&#108;' + '&#116;o';
		var path = 'hr' + 'ef' + '=';
		var addyc4f0a2f39700a261b7a871c23abcbdad = 'g&#101;m&#105;n&#105;' + '&#64;';
		addyc4f0a2f39700a261b7a871c23abcbdad = addyc4f0a2f39700a261b7a871c23abcbdad + '&#97;g&#105;' + '&#46;' + '&#111;rg' + '&#46;' + '&#117;k';
		var addy_textc4f0a2f39700a261b7a871c23abcbdad = 'g&#101;m&#105;n&#105;' + '&#64;' + '&#97;g&#105;' + '&#46;' + '&#111;rg' + '&#46;' + '&#117;k';document.getElementById('cloakc4f0a2f39700a261b7a871c23abcbdad').innerHTML += '<a ' + path + '\'' + prefix + ':' + addyc4f0a2f39700a261b7a871c23abcbdad + '\' rel="alternate">'+addy_textc4f0a2f39700a261b7a871c23abcbdad+'<\/a>';
</script>.</p>
<h2><a id="Intro"></a>1.  Introduction</h2>
<p>These guidelines for the creation, maintenance and quality management of metadata for geospatial data resources, including the services which provide access to the resources, provide a general introduction to the principles and concepts of metadata. They are aimed at data managers and creators of metadata, providers of metadata services and general data users.</p>
<p>The data resources may be datasets, dataset series, services delivering geographic data, or any other information resource with a geospatial content. This includes datasets that relate to a limited geographic area. The data resources may be graphical or textual (tabular or free text), hardcopy or digital. Geospatial data is data containing a positional or locational element relative to the Earth. Many data resources that at first sight do not appear to be geospatial nevertheless do have a geospatial component, in that they apply to a limited geographic area, for example statistics for a local authority area. Geospatial data contains spatial references which may take the form of coordinates, for example in latitude and longitude, or references to geographic place names, for example street data.</p>
<p>Metadata is data about data. It provides additional information about the data resource, to enable it to be better understood and used to good effect.</p>
<p>In an organisation, metadata is required for both internal and external purposes. It can add significantly to the value of an organisation’s data holdings, and failure to create it at the appropriate time can lead to greater hidden costs later. Lack of knowledge about available data can lead to costly duplication of effort.</p>
<p>Within an organisation, metadata is required to organise and maintain the internal investment in data. As staff change, institutional knowledge leaves the organisation. Undocumented data can lose its value. Subsequent staff may have little understanding of the contents and use of the data and may find that they cannot trust results generated using this data.</p>
<p>Externally, metadata is required to provide information about an organisation’s data holdings and data access services. Data resources are a major national asset, and information of what data resources exist within different organisations, particularly in the public sector, is required to improve efficiencies and reduce data duplication. Data catalogues and data discovery services enable potential users to find, evaluate and use that data, thereby increasing its value. In addition, data received from an external source requires further information, supplied by metadata, to process and interpret it.</p>
<p>The requirements for metadata for internal and external purposes are different. Metadata for external purposes will be at a general level, providing basic information about the data resources. Having this in a standardised form enables metadata services to be set up for widespread use. Standardisation of this aspect is thus important, and most metadata standards are designed for this purpose. Metadata for internal purposes will be much more detailed. Internal standards for metadata will generally be extensions of those required for external purposes, and often will contain items particular to the organisation or business sector. Whilst the details of these Guidelines relate to external metadata, and in particular the UK GEMINI2 metadata set designed for discovery metadata services, the principles are equally applicable to internal metadata.</p>
<p>A glossary of terms is provided in <a title="Glossary" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1056-glossary" target="_blank" rel="alternate noopener noreferrer">here</a>.</p>
<h2><a id="fundamentals"></a>2.  Fundamentals of metadata</h2>
<h3><strong><em><a id="2.1"></a>2.1 The nature of metadata</em></strong></h3>
<p>There are a range of uses for metadata, for discovery, for evaluation and for use:</p>
<ul>
<li><strong>discovery</strong>: the user aims to find out what resources are available and whether these are able to satisfy their requirements. This is typically what a search engine can process, using basic search criteria to identify the available resources corresponding to the user requirements, and providing to the user basic metadata (name, content description, geographic area of applicability etc.) about the candidate resources.</li>
<li><strong>evaluation</strong>: the user needs to go deeper in the metadata (e.g. looking at the quality of the information) to ascertain whether a candidate resource is fit for the intended purpose.</li>
<li><strong>use</strong>: the user has selected a candidate resource, but needs to access it and to configure a system or software to process it.</li>
</ul>
<h3><strong><em><a id="2.2"></a>2.2 Metadata services</em></strong></h3>
<p>Metadata services provide one of the fundamental parts of a Spatial Data Infrastructure (SDI). They are used within organisations as part of the information management facilities, and on a national basis for discovery purposes. Essentially, they work on the basis of a user defining parameters such as Topic Category and Extent, to carry out a search to discover data resources that might be suitable and return information about their source, content and availability.</p>
<h3><strong><em><a id="2.3"></a>2.3 Metadata as a business process</em></strong></h3>
<p>A simple process model is presented at Figure 1 and shows the flow from metadata creation through to metadata query with quality related processes built-in. It can represent the processes within one organisation or split between separate organisations. The flow is idealised and could relate to any discovery-level metadata service.</p>
<p>Although metadata creation and maintenance are shown as separate operations, it cannot be over-emphasised that they will be far more successful if they are fully integrated into the other business processes of an organisation. Thus, when a dataset or other form of data resource is produced, it should be routinely documented as metadata as part of the production or distribution process. Further, when the data resource is updated or subject to some form of change, the metadata should also be updated.</p>
<p><img src="/images/xslt/Model_metadata_creation.jpg" alt="Simple Process model for metadata creation, maintenance, service provision and use" width="1114" height="483" /></p>

<p>If the main purpose of creating metadata is to document and enable discovery of an organisation’s own data resources and the exposure of all or part of that metadata to some external service is secondary, then there will be far greater chance of support and resources for metadata in the business.</p>
<p>However, if metadata is seen as an additional activity to support some external service, it is likely to be ignored or forgotten. When it is finally picked up, it may well be assigned to someone who has no knowledge of the data resource and no interest in the quality of the metadata.</p>
<h3><strong><em><a id="2.4"></a>2.4 Metadata roles</em></strong></h3>
<p>Three generic roles in the metadata process can be recognised, these are illustrated above:</p>
<ul>
<li><strong>Metadata creator</strong> – responsible for creating and maintaining the metadata and for its quality. Although the metadata creator is usually the data producer or distributor, this is not always so.</li>
<li><strong>Service provider </strong>– runs the metadata service, and may be part of the same organisation as the metadata creator or quite separate. A broad view of the role is taken here which may be made up of several actual roles in the real world - for example:
<ul>
<li>a contractor hosting the service and providing IT support who is contracted to</li>
<li>a service owner who is ultimately responsible for the quality of the service and has service level agreements (SLAs) with the contractor and metadata creators.</li>
</ul>
</li>
</ul>
<ul>
<li><strong>Service user </strong>- the consumer of the service who selects the search criteria matching their requirements, performs the searches and finds data resources meeting their requirements or, at least, meriting further investigation.</li>
</ul>
<h3><strong><em><a id="2.5"></a>2.5 Metadata standards</em></strong></h3>
<p>There are many metadata standards in existence. These have been produced at different times by different bodies for different purposes. The main ones that are relevant to geospatial data resources are:</p>
<ul>
<li><b><strong>ISO 19115</strong></b></li>
</ul>
<p style="padding-left: 30px;">This describes all aspects of geospatial metadata and provides a comprehensive set of metadata elements. It is designed for electronic metadata services, and the elements are designed to be searchable wherever possible. It is widely used as the basis for geospatial metadata services. However, because of the large number of metadata elements and the complexity of its data model, it is difficult to implement.</p>
<ul>
<li><b><strong>INSPIRE</strong></b></li>
</ul>
<p style="padding-left: 30px;">The INSPIRE metadata Implementing Rules defines the minimum set of metadata elements necessary to comply with the INSPIRE Directive. In essence it is a profile of ISO 19115 for discovery purposes. It allows a variety of possible implementations.</p>
<ul>
<li><b><strong>UK</strong><strong> GEMINI</strong></b></li>
</ul>
<p style="padding-left: 30px;">The UK Geospatial Metadata Interoperability Initiative (GEMINI) was produced originally through a collaboration between the Association for Geographic Information (AGI), the e-Government Unit (eGU) and the UK Data Archive. In a subsequent revision, it was made compatible with the core elements of ISO 19115. In its current version it is conformant with the INSPIRE Implementing Rules and Technical Guidance for metadata, and designed to meet the requirements of INSPIRE in a UK context. This latest revision has been sponsored by Defra and managed by AGI. UK GEMINI remains an AGI publication.</p>
<p style="padding-left: 30px;">In common with INSPIRE, UK GEMINI remains an implementation of ISO 19115:2005, not the more recent version ISO 19115-1:2014.</p>
<ul>
<li><b><strong>Dublin</strong><strong> Core</strong></b></li>
</ul>
<p style="padding-left: 30px;">This was originally developed by librarians for cataloguing information resources. It uses free-text fields, which makes automatic searching difficult. Consequently, it not ideally suited for discovery purposes using electronic data services. It is severely limited in its ability to handle the geospatial aspects of data, and also in how it handles the geographic extent of non-geographic data, e.g. data that applies to one country or region rather than another.</p>
<p style="padding-left: 30px;">However, Dublin Core provides the basic vocabulary used in W3C’s Data Catalogue Vocabulary (DCAT), on which the European Commission has based their GeoDCAT Application Profile.</p>
<p style="padding-left: 30px;">At present, GEMINI makes no direct use of DCAT or GeoDCAT, but it does share some of the Dublin Core vocabulary.</p>
<p>Formal references for these standards and implementing rules are given in the <a title="References" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1047-metadata-guidelines-for-geospatial-data-resources-part-3" target="_blank" rel="alternate noopener noreferrer">Bibliography</a>.</p>
<h2><a id="principles"></a>3.  General principles of metadata</h2>
<h3><strong><em><a id="3.1"></a>3.1 Introduction</em></strong></h3>
<p>This section describes some general high-level rules that apply to the creation of metadata. Whilst primarily applying to UK GEMINI2, they are also relevant to other metadata specifications.</p>
<h3><strong><em><a id="3.2"></a>3.2 Free text</em></strong></h3>
<p>The aim of a discovery metadata such as specified in UK GEMINI2 is to define metadata in a form that provides easily understood information for potential users of the data resource, and is searchable in a computerised discovery metadata service such as the <a title="INSPIRE Geoportal" href="http://inspire-geoportal.ec.europa.eu/">INSPIRE Geoportal</a>. It is difficult to carry out searches on free text, since the same thing can be written in different ways, for example “OS”, “Ordnance Survey”, “The Ordnance Survey of Great Britain”, “OSGB”. Hence, free text entries are discouraged where the metadata is searchable. Where only a limited number of options is available, code lists are specified. For some metadata elements, such as Topic, these may not correspond exactly to the theme of the dataset, and the nearest option should be chosen. Where code lists are used, input and output facilities in a metadata service should identify the corresponding element value.</p>
<h3><strong><em><a id="3.3"></a>3.3 Obligation</em></strong></h3>
<p>As with other data specifications, elements in UK GEMINI2 are given as mandatory, conditional or optional. Mandatory elements must be completed, and most software tools do not allow the metadata to be published if any mandatory elements are missing. Conditional elements have a condition associated with them, and should be supplied when that condition is fulfilled. Such conditions usually define the applicability of the element. Optional elements need not always be completed. This can be for several reasons, for example if the element is not relevant or its value is not known. In practice, optional elements are conditional, and there is a set of circumstances in which a value should be given, roughly corresponding to “is it relevant?” and “is its value known?” Optional elements should not be ignored.</p>
<h3><strong><em><a id="3.4"></a>3.4 Element domains</em></strong></h3>
<p>Each metadata element has a range of allowable values, called its domain. These may be values in a given range (e.g. positive integers) or a set of code values chosen from a list. Specifying the domain helps with both the initial creation of data and quality checking [For further details on quality checking, see <a title="References" href="/agi-groups/standards-committee/uk-gemini/40-gemini/1047-metadata-guidelines-for-geospatial-data-resources-part-3" target="_blank" rel="alternate noopener noreferrer">Part 3 </a>of these Guidelines]. In some cases, default values may be used, for example for elements relating to the metadata itself.</p>
<h3><strong><em><a id="3.5"></a>3.5 Spatial references</em></strong></h3>
<p>By definition, geographic data contains some form of spatial reference. The spatial reference identifies the position of the object of interest in the real world. Spatial references can be given in a number of forms, not just as Grid References. They can take the form of the name or identifier of a geographic location which can be described in a gazetteer. Examples are property addresses, postcodes and census areas. These spatial references are a key means of searching the data by location, not only within the data resource, but also positioning the data resource in the world (e.g. data for Scotland). A consistent set of spatial references enables spatial searches to be made for datasets in a metadata service.</p>
<h3><strong><em><a id="3.6"></a>3.6 Date fields</em></strong></h3>
<p>Metadata can contain a multitude of dates identifying the different stages in the life cycle of the data. Key dates are included in metadata. To enable searches to be carried out (e.g. date relating to the period 1990 to 1999), these dates need to be recorded in standardised form. Unfortunately, different standards are used in different places. Here it is recommended that the extended format defined in <a title="ISO date and time format" href="https://www.iso.org/iso-8601-date-and-time-format.html">ISO 8601</a> (YYYY-MM-DD) is used.</p>
<h2><a id="scope"></a>4.  Data resources in scope</h2>
<h3><strong><em><a id="4.1"></a>4.1 What is stated in </em></strong><strong><em>UK GEMINI2</em></strong></h3>
<p>The purpose of this section is to provide guidance on</p>
<p style="padding-left: 30px;">(i) what types of geospatial data can be documented using UK GEMINI2,</p>
<p style="padding-left: 30px;">(ii) the applicability of UK GEMINI2 and</p>
<p style="padding-left: 30px;">(iii) how to find an appropriate level for the individual documentation of data resources.</p>
<p>UK GEMINI2 “specifies a set of metadata elements for describing geographic data resources” but provides no other information about what types of data or services are in or out of scope.</p>
<p>In practice it can be difficult to decide what data or service resources are in scope and how they should be documented. For example, what constitutes a suitable body of data for individual documentation? Should it be an individual map or the whole map series?</p>
<p>There is no simple answer to these questions; it is likely to be a compromise. However, some general guidance can be given.</p>
<h3><strong><em><a id="4.2"></a>4.2 Characteristics of data resources in scope</em></strong></h3>
<p>The general nature of geospatial data and access services is described in the Introduction. As is emphasised there, many data resources that at first sight do not appear to be geospatial nevertheless have a geospatial component. They are geographically constrained in some way, in that the data only refers to certain areas or locations on the surface of the Earth, whether on land or sea. The way that these locations are referenced can take many forms such as coordinates (e.g. latitude and longitude, National Grid), or geographic place names (e.g. street, locality, town, administrative area).</p>
<p>Although it is common to think of geospatial data as being synonymous with maps, this is far from the case. Geospatial data can equally well be textual - whether tabular or free text – or images taken from the air or from the ground. The data can be as hardcopy or in digital or even video form.</p>
<p>All these types can be documented using UK GEMINI2.</p>
<h3><strong><em><a id="4.3"></a>4.3 Applicability of </em></strong><strong><em>UK GEMINI2</em></strong></h3>
<p>The primary purpose of UK GEMINI2 is to provide the requirements for documenting data resources within the United Kingdom that conforms with the INSPIRE Metadata Implementing Rules.</p>
<h3><strong><em><a id="4.4"></a>4.4 Levels of data resources for documentation</em></strong></h3>
<p>There are no absolute rules for deciding on an appropriate level for the individual documentation of a data resource. The overriding consideration is that the data resource has been documented with sufficient granularity to yield a useful result if discovered using a metadata service. Too coarse a granularity will result in too generalised a result, too fine a granularity is likely to overwhelm the user (and the metadata creator!). The granularity can relate to geographical extent, temporal extent or subject.  </p>
<p>There are some questions that can be posed which may help the metadata creator to find an answer.</p>
<ul>
<li>How is the data resource used and how is it made available? Is it a product, dataset, document that may be used and combined with other datasets or is it an integral part of a larger data resource?</li>
<li>Has the data resource been captured using a single data specification? Are there other data resources captured using the same data specification?</li>
<li>Is the data resource part of a time series? Is the data resource covering the same extent periodically updated to the same specification?</li>
<li>Does the data resource relate to, or reference, a continuous area or contiguous areas, or does it reference specific locations?</li>
<li>Does the data resource relate to one or many subjects, topics or themes?</li>
</ul>
<p>An approach to resolving these questions is found in the table below.</p>
<p>The key points are:</p>
<ul>
<li>Finding the appropriate level will be a compromise between what appears to be fit for purpose for the user and the granularity which can be supported by the metadata creator.</li>
<li>If the metadata creator has to aggregate what is documented for practical reasons then they should ensure that the resource is adequately documented in terms of Extent, Dataset reference date and Topic category. There should also an Additional Information Source included so that the service user can understand the finer granularity lying behind the single entry.</li>
</ul>
<table style="height: 600px;" border="1" width="1079">
<tbody>
<tr>
<td width="235">
<p><strong>Nature of data resource</strong></p>
</td>
<td width="432">
<p><strong>How to document</strong></p>
</td>
<td width="278">
<p><strong>Examples</strong></p>
</td>
</tr>
<tr>
<td width="235">
<p><strong>Stand-alone product or identifiable dataset or document </strong></p>
<ol style="list-style-type: lower-alpha;">
<li>not part of a series produced to the same specification; and</li>
<li>not part of a time series.</li>
</ol>

</td>
<td width="432">
<p>Individually with one metadata record.</p>
<p><strong>Notes: </strong></p>
<ul>
<li>If the data resource references a number of separate locations then at least ensure that this is reflected in a multiple entry for Extent.</li>
<li>If the data resource covers a number of topics or subjects then ensure that each of these is reflected, using multiple entries for Topic category and Keyword.</li>
</ul>
</td>
<td width="278">
<ul>
<li>Stand-alone soil map of the New Forest.</li>
<li>One-off report on a Site of Special Scientific Interest.</li>
<li>Historical index of streets in Cambridge.</li>
<li>One-off table of statistics for Oxfordshire.</li>
</ul>
</td>
</tr>
<tr>
<td width="235">
<p><strong>Products or identifiable datasets or documents forming a series with a common specification</strong>;</p>
<ol style="list-style-type: lower-alpha;">
<li>referencing one location or contiguous area; and</li>
<li>may be part of a time series.</li>
</ol>
</td>
<td width="432">
<p>Together with one metadata record.</p>
<p><strong>Notes: </strong></p>
<ul>
<li>If the time series is not regular with periodic updates, consider documenting by individual dates or durations referring to particular periods of update.</li>
<li>If the data resource covers a number of topics or subjects then ensure that each of these is reflected, using multiple entries for Topic category and Keyword.</li>
</ul>
</td>
<td width="278">
<ul>
<li>Unrevised geological map series of all of Scotland.</li>
<li>Topographic map series covering all of GB updated periodically.</li>
<li>Series of statistical reports on the crime by ward in Surrey for 1973.</li>
<li>Street gazetteer of Hampshire.</li>
</ul>
</td>
</tr>
<tr>
<td width="235">
<p><strong>Products or identifiable datasets or documents forming a series with a common specification</strong>;</p>
<ol style="list-style-type: lower-alpha;">
<li>referencing more than one discrete location or contiguous area; and</li>
<li>may be part of a time series.</li>
</ol>

</td>
<td width="432">
<p>Each location or area individually with a metadata record.</p>
<p><strong>Notes: </strong></p>
<ul>
<li>If the time series is not regular with periodic updates, consider documenting by individual dates or durations referring to a particular period of update.</li>
<li>If the data resource covers a number of topics or subjects then ensure that each of these is reflected, using multiple entries for Topic category and Keyword.</li>
<li>If it is not feasible to individually document each location or contiguous area, e.g. borehole records or Sites of Special Scientific Interest, then at least ensure that is reflected in a multiple entry for Extent. Also include Additional Information Source.</li>
</ul>
</td>
<td width="278">
<ul>
<li>Geological map series of different parts of Great Britain – document each part separately.</li>
<li>Topographic maps of National Parks – document each Park separately.</li>
<li>Aerial photography of parts of Devon, Cornwall and Somerset taken in 1957 and not re-flown to same specification – document each part separately.</li>
<li>Statistical tables for metropolitan areas in UK – document separately if feasible.</li>
</ul>
</td>
</tr>
</tbody>
</table>
