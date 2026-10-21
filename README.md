# Knowledge Base Architecture

A repository for input and design documentation applicable to all Knowledge Base repositories

## Broad Overview

This architecture is aimed at management and curation of portfolio of interlinked knowledge bases, together forming a 'Body of RDMI Knowledge' (boRDMIk).

The architecture has the following components on a conceptual level (C1/C2):

 - Each Knowledge Base (KB) has a repository (GitHub or GitLab) where the following is maintained:
   - A schema or schemas, defining RDF classes and properties, as applicable;
   - A set of vocabularies, encoded as SKOS concept schemes;
   - A set of registries of important instances of classes that are not available in external registries;
   - One or more graph instances that link web-based resources or locally defined nodes via properties and vocabularies;
   - A folder of releases, these contain snapshots of vocabularies, registries, and graphs associated with a specific release of the KB.
   - Support documentation in markdown and image files.
   - Details of existing and envisaged KBs are available in 'List of Applicable Knowledge Bases'.
 - Each KB is managed via a curation UI that reads and writes directly to the relevant Git repository. See details below in 'Current Automated Curation Apps'.
 - Client applications: These knowledge bases enable several types of client/ UI applications that are generically similar:
   - An API that allows programmatic access to the vocabularies, schema and property definitions, and registries, as applicable;
   - A search and discovery application that indexes the graph, resolves vocabulary and registry URIs to human-readable labels, and links to detailed views of one or more resource classes available in the graph. There is a possibility of combining all graphs, since many nodes/ resources may be the same, but each KB classifies and links them differently.
   - Demonstrator applications that make use of the APIs to indicate how the knowledge bases and associated vocabularies can be used.
   - Compliance assessment applications - these create forms that allow manual and/ or automated assessment of compliance with KBs focused on compliance assessment;
   - Metadata capture and structured annotation forms - these capture a combination of free-text and vocabulary-driven information for a specific web resource that is either an existing node in a graph, or a new one to be added to a graph;
 - A browser Plug-In application: this application is a wrapper for one or more of the client applications, typically using the current web page/ resource as a primary context for annotation, metadata extraction and capture, licence and compliance verification, searches, or workflow invocations.
 - A range of workflows that can be invoked, processing data associated with a resource and optionally returning information to be included into one or more of the KBs. Each workflow can have an invocation/ result form.

## List of Applicable Knowledge Bases

- TRSP Working Group - a mature draft, available here: https://github.com/wimhugo/kb-attributes-eden-fidelis-trsp
- OpenREL Knowledge Base - a mature draft, available here: https://github.com/wimhugo/openrel
- Compliance Assessment Toolkit - a number of sub-KBs that will grow over time
  - CAT - mature - not yet deployed to GitHub  
  - EOSC PID Policy - mature - not yet deployed to GitHub
  - FAIR assessment - mature draft - not yet deployed to GitHub
  - AARC compliance - mature - not yet deployed to GitHub
  - DANS documentation - - to be created
  - FIDELIS Network - to be created
  - EOSC Node Acceptance - to be created
  - AI Act Conformance - to be created
- RDA KB - a mature draft - not yet deployed to GitHub
- AI Annotation - a concept - not yet deployed to GitHub

## Current Automated Curation Apps

There are, at the moment, two somewhat overlapping applications that manage existing KBs, and that have, to varioous degrees, been made configurable so that the functions can be applied to any KB. These are:

- KB Curation Platform - located at wimhugo/kb-curation-platform and https://app.base44.com/apps/69ef21e46d74e66459a1e538 - that is intended as the generic application that must be further refined and extended with functions available in the others. Currently focused on the TRSP WG KB.
- OpenREL - currently focused on the OpenREL Knowledge Base, and located at wimhugo/etl-pipeline-github-registry and https://app.base44.com/apps/69df36da0602728d38f7e05d/

## Current Client Applications

- OpenREL Demonstrator Application: assists with licence and policy compilation and publication
- A prototype set of example apps linked into a browser plugin: https://app.base44.com/apps/6a5c83fc96deb787faeec06b/ with a repository at wimhugo/plugin-framework


