# QuantumLeap

[![FIWARE Core Context Management](https://nexus.lab.fiware.org/static/badges/chapters/core.svg)](https://www.fiware.org/developers/catalogue/)
[![License: MIT](https://img.shields.io/github/license/orchestracities/ngsi-timeseries-api.svg)](https://opensource.org/licenses/MIT)
[![Docker Status](https://img.shields.io/docker/pulls/orchestracities/quantumleap.svg)](https://hub.docker.com/r/orchestracities/quantumleap/)
[![Support](https://img.shields.io/badge/support-ask-yellowgreen.svg)](https://ask.fiware.org/questions/)
<br/>
[![Documentation badge](https://img.shields.io/readthedocs/quantumleap.svg)](https://quantumleap.readthedocs.io/en/latest/)
[![CircleCI](https://circleci.com/gh/orchestracities/ngsi-timeseries-api.svg?style=shield)](https://circleci.com/gh/orchestracities/ngsi-timeseries-api)
[![Coverage Status](https://coveralls.io/repos/github/orchestracities/ngsi-timeseries-api/badge.svg?branch=master)](https://coveralls.io/github/orchestracities/ngsi-timeseries-api?branch=master)
![Status](https://nexus.lab.fiware.org/repository/raw/public/badges/statuses/full.svg)
[![Swagger Validator](https://img.shields.io/swagger/valid/2.0/https/raw.githubusercontent.com/OAI/OpenAPI-Specification/master/examples/v2.0/json/petstore-expanded.json.svg)](https://app.swaggerhub.com/apis/smartsdk/ngsi-tsdb)
[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/4394/badge)](https://bestpractices.coreinfrastructure.org/projects/4394)

QuantumLeap is the first implementation of
[an API](https://app.swaggerhub.com/apis/smartsdk/ngsi-tsdb)
that supports the storage of
[FIWARE NGSIv2](https://fiware.github.io/specifications/ngsiv2/stable/)
data into a
[time series database](https://en.wikipedia.org/wiki/Time_series_database).
It currently also experimentally supports the injection of
[NGSI-LD](https://www.etsi.org/deliver/etsi_gs/CIM/001_099/009/01.01.01_60/gs_CIM009v010101p.pdf)
in  a backward compatible way with NGSI-v2 API. I.e. you can retrieve NGSI-LD
stored data via NGSI v2 API and retrieve data will be describe following NGSI
v2 format.

QuantumLeap is not a
[real time](https://en.wikipedia.org/wiki/Real-time_computing)
API, its purpose is to process notifications received from the Context Broker
and to create temporal records for them. In general, the whole FIWARE stack,
being based on a micro-service architecture, cannot be regarded as real time
in case you have requirements on guaranteed delivery in a given amount of time.

However, even though hard real time may not be FIWARE's forte, in our experience
a properly tuned FIWARE stack can perform extremely well and
handle very demanding IoT workloads without a glitch - you just need to
configure your infrastructure to handle that :)

Want to know more? Refer to the
[docs](https://quantumleap.readthedocs.io/en/latest/)
or checkout the Extra Resources below.

This project is contributed to [FIWARE](https://www.fiware.org) by
[Martel Innovate](https://www.martel-innovate.com/) as part of its
[Orchestra Cities](https://www.orchestracities.com/)
platform.
You can find more FIWARE components in the
[FIWARE catalogue](https://catalogue.fiware.org).

|  :books: [Documentation](https://quantumleap.rtfd.io/) | :mortar_board: [Academy](https://fiware-academy.readthedocs.io/en/latest/core/quantum-leap) |  :whale: [Docker Hub](https://hub.docker.com/r/orchestracities/quantumleap/) | :dart: [Roadmap](https://github.com/orchestracities/ngsi-timeseries-api/blob/master/docs/roadmap.md) |
|---|---|---|---|

## Contents

- [Install](#install)
- [Usage](#usage)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [Extra resources](#extra-resources)
- [Adopters](#adopters)
- [Linked projects](#linked-projects)
- [License](#license)

## Install

Refer to the
[Installation Guide](https://quantumleap.readthedocs.io/en/latest/admin/).

QuantumLeap supports both Crate DB and Timescale as time-series DB
backends but please bear in mind that at the moment we only support
the following versions:

- Crate backend: Crate DB version `4.1.*`
- Timescale backend: Postgres version `10.*` or `11.*` +
  Timescale extension `1.3.*` + Postgis extension `2.5.*`.
  
PR [#373](https://github.com/orchestracities/ngsi-timeseries-api/pull/373)
introduced basic support for NGSI-LD. In short this means that using
the current endpoint you are able to store NGSI-LD payloads with few caveats
(see [#398](https://github.com/orchestracities/ngsi-timeseries-api/issue/398))

## Usage

Refer to the [User Manual](https://quantumleap.readthedocs.io/en/latest/user/).

## Troubleshooting

Refer to the
[Troubleshooting](https://quantumleap.readthedocs.io/en/latest/user/troubleshooting/)
section.

## Contributing

Refer to the
[Contributing](https://quantumleap.readthedocs.io/en/latest/user/contributing/)
section and to the [contribution guidelines](./CONTRIBUTING.md).

## Extra resources

The following is a collection of external guides and pages where you may find
additional documentation about QuantumLeap. Note that these guides could be
outdated (so could the official docs!), so we appreciate all efforts to keep
consistency.

- [FIWARE Step-by-step](https://fiware-tutorials.readthedocs.io/en/latest/time-series-data/index.html)
- [Orchestra Cities Helm Charts](https://github.com/orchestracities/charts)

## Adopters

[Orchestra Cities](https://www.orchestracities.com/) QuantumLeap is adopted
in the FIWARE community,
if you want to list it here, add your information on this
[issue](https://github.com/orchestracities/ngsi-timeseries-api/issues/436)
or create a PR to update the list.

| <a href="https://www.ekz.ch/"><img src="https://www.ekz.ch/content/ekz-internet/de/_jcr_content/configuration/logo/image.ekzImg.width_ekznative.png/1610370526582.png/logo.png" height="75" /></a> | <a href="https://www.stadtwerke-wolfsburg.de/"><img src="https://www.stadtwerke-wolfsburg.de/fileadmin/templates/Images/logo_stadtwerke.png" height="75" /></a> |   |  |
|---|---|---|---|

## Linked projects

The following projects are linked to
[Orchestra Cities](https://www.orchestracities.com/) QuantumLeap,
if you want to list it here, add your information on this
[issue](https://github.com/orchestracities/ngsi-timeseries-api/issues/436)
or create a PR to update the list.

| <a href="https://github.com/lets-fiware/ngsi-go"><img src="https://raw.githubusercontent.com/lets-fiware/ngsi-go/gh-pages/img/NGSI-Go.png" height="75" /> <br/> NGSI Go is a CLI supporting QL</a> |  |   |  |
|---|---|---|---|

## Enterprise Support

<a href="mailto:info@orchestracities.com?subject=[Orchestra
Cities]%20Enterprise%20Support">Contact us</a>
if you need Enterprise Support for your QuantumLeap installation.

---

## License

QuantumLeap is licensed under the [MIT](LICENSE) License

© 2017-2021 Martel Innovate
