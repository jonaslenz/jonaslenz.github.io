---
layout: post
title: Description of the Pilot
description: Proposed solution to data-challenge
image: assets/images/soilpulse_scheme.png
nav-menu: true
---

### What we want to achieve?
We would like to develop a Python package with capability to process files and other data and metadata packages to make their contents understandable for both humans and machines. By gathering available data
Interoperability of existing and new datasets will be ensured by mapping their structure to a metadata standard, guided by the SoilPulse metadata generator. Curation overhead for researchers is minimized as they can maintain their established data structures and reuse mapping templates. The metadata standard will build upon existing standards and extend it for functional soil process analyses, in which we consider the experience from NFDI4Earth Pilot "Interoperability and Reusability of Geoscientific Lab Data" in semantic mapping. Interoperability and reusability of the data will be demonstrated with automated tests, which implies that datasets can be standardized linked to earth system models.

### What is the technological backbone you rely upon?
SoilPulse assists metadata generation and API-assisted upload for new and existing datasets through an open R/python-package and with a web app frontend, strongly extending current MetaEditors. It will be publicly documented and hosted on GitHub. To improve findability of interoperable SoilPulse datasets, they will be listed by DOIs in the GitHub repo. A metadata-tag in the dataset linking to SoilPulse is foreseen. Defined FAIR MI tests and the automatic generation of human-readable reports will test data set interoperability and reusability.

### Which are the standards and interoperability approaches used in the pilot’s context?
The semantically interoperable SoilPulse metadata standard will build upon existing standards (e.g. BONARES; ISCN, building on INSPIRE and Dublin Core), vocabularies (e.g. AGROVOC, upcoming GAIA Data GO FAIR) and data harmonization approaches (e.g. SoDaH; ESIP).

### Which improvements are made compared to the status quo?
Interoperability of data repositories will be ensured by mapping their individual data structures to common vocabulary and metadata standards. Automated reusability tests will be developed. Data curation effort for individual researchers will be reduced through guided metadata generation and the ability to retain their established data structure and workflows.
