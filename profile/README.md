## Repository Guide

### Digital Growth Charts (dGC)

The RCPCH has developed some digital versions of the paper child growth charts which have been in use for decades. To enable these charts to be work in a variety of use-cases, and to reduce development complexity, the dGC platform has been separated into a number of different repositories

#### Principal dGC repos

These repositories are key to the functioning of the dGC platform.

* [rcpchgrowth-python](https://github.com/rcpch/rcpchgrowth-python) houses the calculation functions of the growth charts in a Python package (which is also available on PyPi as a standalone python library)

* [digital-growth-charts-server](https://github.com/rcpch/digital-growth-charts-server) is the RCPCH Growth API server, which uses [rcpchgrowth-python](https://github.com/rcpch/rcpchgrowth-python) internally to perform these calculations, which it serves as a REST API.

* [digital-growth-charts-react-component-library](https://github.com/rcpch/digital-growth-charts-react-component-library) is a React.js library which 'knows' how to display the results from the REST API, as a familiar digital growth chart.

* [digital-growth-charts-hazard-log](https://github.com/rcpch/digital-growth-charts-hazard-log) contains the Hazard Log for our dGC clinical service - and is where we can discuss and mitigate all aspects of the risks associated with the clinical software and its deployment

#### Ancillary dGC repos

These repositories are support services or ancillary services and data collections.

* [upptime-rcpch-web-services](https://github.com/rcpch/upptime-rcpch-web-services) is a GitHub Actions-based uptime monitor to check the services are up, and display cumulative uptime.

* [growth-references](https://github.com/rcpch/growth-references) is a repository containing the raw data from the statistical references which are used to generate growth chart information. It is mainly of interest to academics and stats nerds.

* [digital-growth-charts-react-native-client](https://github.com/rcpch/digital-growth-charts-react-native-client) is a work in progress, pre-alpha React Native version of the charts display, which is designed to work better on smaller mobile screens. It was experimental and is not an official part of the project.

#### Deprecated dGC repos

* [digital-growth-charts-react-client-node-server](https://github.com/rcpch/digital-growth-charts-react-client-node-server) this Node.js server was briefly used to proxy requests between the demo site and the live server API, in order to allow us to securely inject API access credentials into the requests. Now no longer used because Gravitee.io API Management platform is much better than the old Azure one, so we don't need this.

* [digital-growth-charts-flask-client](https://github.com/rcpch/digital-growth-charts-flask-client) this was the original [Flask](https://flask.palletsprojects.com/) implementation of the Growth Chart API, which also at one stage included the display elements of the charts. We elected later to separate out the display from the API and also to replatform the API onto [FastAPI](https://fastapi.tiangolo.com/).

* [digital-growth-charts-react-chart-library](https://github.com/rcpch/digital-growth-charts-react-chart-library) was the first version of the React charts, which were superseded by [digital-growth-charts-react-component-library](https://github.com/rcpch/digital-growth-charts-react-component-library) which allowed the charts to be shipped as a standalone React Component.

## Epilepsy12 National Audit of Epilepsy Care

### RCPCH Audit Engine

The RCPCH Audit Engine is the data platform underlying the Epilepsy12 National Audit of Epilepsy Care

* [rcpch-audit-engine](https://github.com/rcpch/rcpch-audit-engine)
