# DANS Documentation Knowledge Base

## Intent

Consolidate a large, partially complete documentation corpus currently held in Google Drive (documents, presentations, PDFs, and IcePanel architecture diagrams) into a mature collection with one canonical document per distinct topic, published as Word, PowerPoint, Excel and PDF copies accessible independently of Google Drive. The corpus is managed as the 'DANS documentation' Knowledge Base within the established boRDMIk architecture: a Git repository holds the RDF schema, SKOS vocabularies, registries of instances, graph instances and release snapshots, and this app is the curation UI that reads and writes that repository directly. The app also serves as the public search and discovery client over the graph: it indexes the graph, resolves vocabulary and registry URIs to human-readable labels, and provides detailed resource views. A later phase extends the corpus with papers and resources from the web (often Zenodo) and less-organised project-grouped supplementary documents.

## Audience and Roles

Four role groups. These have already been defined in one or more of the automated curation applications, and functionality is linked to the roles associated with each function.

- Public visitors (no login) browse, search, and download from the discovery interface, which indexes the graph and resolves SKOS vocabulary and registry URIs to readable labels.
- Contributors - authenticated users that contribute annotations, metadata, and other information in respect of resources, and register new resources.
- Curators - A small set of authenticated curators/editors that manage the corpus (graph and optionally resources) and the vocabularies. 
- Administrators - a few accounts that are authorised to configure the API based on the KB, and configure client apps to supplement the KB. They can modify and edit settings - such as the authentication key for access to GitHub repos, new project and KB definitions, and the like.

Curators in the case of the DANS Documentation corpus: likely will have automated or assisted functions to do one or more of: importing the Drive inventory, reviewing and classifying resources, marking placeholders and duplicates, designating canonical documents per topic, annotating with vocabulary keywords, and maintaining the SKOS concept schemes and registries in the KB repository. Curation screens are visible only to editors; discovery is fully public. The app follows the same repo-read/write curation pattern as the existing KB Curation Platform (TRSP) and OpenREL apps, so curators familiar with those tools find the same working model.

## Core Flows

These are specific to the general requirements and functions available from the existing automated curation applications.

Curator imports the Google Drive inventory (document list with metadata) into the app; each document becomes a resource node in the KB graph, written to the repository

2.

Curation review: curator inspects each resource, marks it as placeholder/duplicate/draft to discard, or promotes it as the canonical document for its topic; the decision is recorded in the graph

3.

Structure rule: requirements and specifications live in a canonical topic library; project-specific modifications live in annexes; each project has a summary document that links the requirements and specifications applicable to it

4.

Curator exports IcePanel architecture diagrams as PDFs, publishes them, and records them in the graph with diagram-for relations to the documents they illustrate

5.

Curator consolidates presentations into a smaller canonical subset using the same review-and-promote flow

6.

Publishing: canonical documents are made available as Word, PowerPoint, Excel and PDF copies stored independently of Google Drive (app file storage or Drive), with stable URLs recorded as properties of the graph nodes

7.

Curator annotates resources with keywords drawn from controlled vocabularies maintained as SKOS concept schemes and registries of instances (topics, projects) in the repository; edits to vocabularies and registries are written back to the repository

8.

Metadata graph: every resource is connected to topics, projects, keywords and other resources (relations such as supersedes, extends, annex-of, diagram-for), all persisted in the repository's graph instances

9.

Public discovery: visitor searches by free text or controlled keyword, browses by topic or project, and opens a resource detail page showing metadata, relationships and download/view links in all published formats, with URIs resolved to human-readable labels

10.

Release management: snapshots of vocabularies, registries and graphs can be taken into a releases folder in the repository, associated with a specific release of the KB

11.

Later phase: curator ingests web/Zenodo papers and less-organised project-grouped supplementary documents through the same annotation and classification flow, and the graph structure allows later combination with other boRDMIk knowledge bases since resources may be shared while each KB classifies them differently
