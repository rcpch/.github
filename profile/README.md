## Repository Guide

As well as our essential work in education and career support for paediatricians, Royal College of Paediatrics and Child Health (RCPCH) staff and members work on a range of programmes to improve child health - from quality improvement to workforce studies, from research in the UK to global child health programmes. RCPCH have developed, maintain and host a growing number of digital projects with the aim of improving the health and experience of care of children and young people, as well as the education and working environment of paediatricians. Below are some of the key repositories developed by the RCPCH.

### Digital Growth Charts (dGC)

The RCPCH has developed some digital versions of the paper child growth charts which have been in use for decades. To enable these charts to be work in a variety of use-cases, and to reduce development complexity, the dGC platform has been separated into a number of different repositories

#### Principal dGC repos

These repositories are key to the functioning of the dGC platform.

* [rcpchgrowth-python](https://github.com/rcpch/rcpchgrowth-python) houses the calculation functions of the growth charts in a Python package (which is also available on PyPi as a standalone python library)<br/>
  ![PyPI - Version](https://img.shields.io/pypi/v/rcpchgrowth?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
  ![GitHub Issues or Pull Requests](https://img.shields.io/github/issues/rcpch/rcpchgrowth-python?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
  ![GitHub Issues or Pull Requests](https://img.shields.io/github/issues-pr/rcpch/rcpchgrowth-python?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
  ![GitHub Repo stars](https://img.shields.io/github/stars/RCPCH/rcpchgrowth-python?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)


* [digital-growth-charts-server](https://github.com/rcpch/digital-growth-charts-server) is the RCPCH Growth API server, which uses [rcpchgrowth-python](https://github.com/rcpch/rcpchgrowth-python) internally to perform these calculations, which it serves as a REST API.<br/>
![GitHub Release](https://img.shields.io/github/v/release/rcpch/digital-growth-charts-server?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues/rcpch/digital-growth-charts-server?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues-pr/rcpch/digital-growth-charts-server?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub Repo stars](https://img.shields.io/github/stars/RCPCH/digital-growth-charts-server?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)


* [digital-growth-charts-react-component-library](https://github.com/rcpch/digital-growth-charts-react-component-library) is a React 18.2 Typescript component library which 'knows' how to display the results from the REST API, as a familiar digital growth chart.<br/>
![NPM Version](https://img.shields.io/npm/v/%40rcpch%2Fdigital-growth-charts-react-component-library?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues/rcpch/digital-growth-charts-react-component-library?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues-pr/rcpch/digital-growth-charts-react-component-library?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/rcpch/digital-growth-charts-react-component-library?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub Repo stars](https://img.shields.io/github/stars/RCPCH/digital-growth-charts-react-component-library?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)

* [digital-growth-charts-react-client](https://github.com/rcpch/digital-growth-charts-react-client) is a React 18.2 JS demo client available [here](https://growth.rcpch.ac.uk). It has documentation for clinicians, implementers and developers.<br/>
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues/rcpch/digital-growth-charts-react-client?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues-pr/rcpch/digital-growth-charts-react-client?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/rcpch/digital-growth-charts-react-client?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub Repo stars](https://img.shields.io/github/stars/RCPCH/digital-growth-charts-react-client?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)


* [digital-growth-charts-hazard-log](https://github.com/rcpch/digital-growth-charts-hazard-log) contains the Hazard Log for our dGC clinical service - and is where we can discuss and mitigate all aspects of the risks associated with the clinical software and its deployment

#### Ancillary dGC repos

These repositories are support services or ancillary services and data collections.

* [upptime-rcpch-web-services](https://github.com/rcpch/upptime-rcpch-web-services) is a GitHub Actions-based uptime monitor to check the services are up, and display cumulative uptime.

* [growth-references](https://github.com/rcpch/growth-references) is a repository containing the raw data from the statistical references which are used to generate growth chart information. It is mainly of interest to academics and stats nerds.

* [digital-growth-charts-react-native-client](https://github.com/rcpch/digital-growth-charts-react-native-client) is a work in progress, pre-alpha React Native version of the charts display, which is designed to work better on smaller mobile screens. It was experimental and is not an official part of the project.

#### Deprecated dGC repos

These repositories are deprecated and no longer updated.

* [digital-growth-charts-react-client-node-server](https://github.com/rcpch/digital-growth-charts-react-client-node-server) this Node.js server was briefly used to proxy requests between the demo site and the live server API, in order to allow us to securely inject API access credentials into the requests. Now no longer used because Gravitee.io API Management platform is much better than the old Azure one, so we don't need this.

* [digital-growth-charts-flask-client](https://github.com/rcpch/digital-growth-charts-flask-client) this was the original [Flask](https://flask.palletsprojects.com/) implementation of the Growth Chart API, which also at one stage included the display elements of the charts. We elected later to separate out the display from the API and also to replatform the API onto [FastAPI](https://fastapi.tiangolo.com/).

* [digital-growth-charts-react-chart-library](https://github.com/rcpch/digital-growth-charts-react-chart-library) was the first version of the React charts, which were superseded by [digital-growth-charts-react-component-library](https://github.com/rcpch/digital-growth-charts-react-component-library) which allowed the charts to be shipped as a standalone React Component.

## National Audits

RCPCH now administer 2 national audit platforms on behalf of Healthcare Quality Improvement Partnership (HQIP)

### RCPCH Audit Engine

The RCPCH Audit Engine is the data platform underlying the Epilepsy12 National Audit of Epilepsy Care (Epilepsy12). In time the project will contain more applications.

* [rcpch-audit-engine](https://github.com/rcpch/rcpch-audit-engine) is a Django application which manages the Epilepsy12 audit.<br/>
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues/rcpch/rcpch-audit-engine?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues-pr/rcpch/rcpch-audit-engine?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub Repo stars](https://img.shields.io/github/stars/RCPCH/rcpch-audit-engine?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)

### National Paediatric Diabetes Audit (NPDA)

This is the data platform supporting the NPDA. It is currently in development and sits in its own project. In time it will included in the RCPCH Audit Engine
* [national-paediatric-diabetes-audit]([https://github.com/rcpch/](https://github.com/rcpch/national-paediatric-diabetes-audit)) is a Django application which manages the NPDA.<br/>
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues/rcpch/national-paediatric-diabetes-audit?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues-pr/rcpch/national-paediatric-diabetes-audit?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/rcpch/national-paediatric-diabetes-audit?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub Repo stars](https://img.shields.io/github/stars/RCPCH/national-paediatric-diabetes-audit?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)

## Other Services

There are 2 services that are open access and unmetered. These are used to support the audits, but will power other projects in time

* [rcpch-census-platform](https://github.com/rcpch/rcpch-census-platform) is a django rest framework project that holds data describing the lived environment of children and young people in the UK. Currently the main application returns indices of multiple deprivation scores and quantiles against a postcode. It holds some census data also about access to green space.<br/>
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues/rcpch/rcpch-census-platform?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues-pr/rcpch/rcpch-census-platform?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/rcpch/rcpch-census-platform?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub Repo stars](https://img.shields.io/github/stars/RCPCH/rcpch-census-platform?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
* [rcpch-nhs-organisations](https://github.com/rcpch/rcpch-nhs-organisations) is a django rest framework project that provides lists of organisations that care for children and young people across the UK, including their organisational geography and relationships.<br/>
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues/rcpch/rcpch-nhs-organisations?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues-pr/rcpch/rcpch-nhs-organisations?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/rcpch/rcpch-nhs-organisations?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)
![GitHub Repo stars](https://img.shields.io/github/stars/RCPCH/rcpch-nhs-organisations?style=flat-square&labelColor=%2311a7f2&color=%230d0d58)

### Getting involved

If you want to contribute to any of our projects, there is more information in our [playbook](https://playbook.rcpch.tech/)

---

![GitHub Org's stars](https://img.shields.io/github/stars/rcpch?style=for-the-badge&labelColor=%2311a7f2&color=%230d0d58)
![GitHub followers](https://img.shields.io/github/followers/rcpch?style=for-the-badge&labelColor=%2311a7f2&color=%230d0d58)






