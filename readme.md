<div align="center">

<!-- title -->

<!--lint ignore no-dead-urls-->

# Awesome InfoSec [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![lint](https://github.com/spekulatius/awesome-infosec/actions/workflows/lint.yaml/badge.svg)](https://github.com/spekulatius/awesome-infosec/actions/workflows/lint.yaml)

<!-- subtitle -->

Personal notes and awesome infosec stuff for a bash-focused workflow. Highly subjective selection by nature.

<!-- image -->

<!--
<a href="" target="_blank" rel="noopener noreferrer">
  <img src="" />
</a>
-->

<!-- description -->

</div>

<!-- TOC -->

## Contents

- [Image Libs: Converters, Resizers, etc. pp](#image-libs-converters-resizers-etc-pp)
- [Archives: ZipSlip, TarSlip, etc. pp](#archives-zipslip-tarslip-etc-pp)
- [WYSIWYG Editors](#wysiwyg-editors)
- [`data:`-Attribute](#data-attribute)
- [XSS](#xss)
- [Request Smuggling](#request-smuggling)
- [Open Redirects](#open-redirects)
- [SQLi](#sqli)
- [PHP](#php)
- [Python](#python)
- [Docker](#docker)
- [Active Directory](#active-directory)

<!-- CONTENT -->

## Image Libs: Converters, Resizers, etc. pp

- [ImageMagick: The hidden vulnerability behind your online images](https://www.metabaseq.com/imagemagick-zero-days/) - `2023-02-01`.
- [`CVE-2022-44268`](https://github.com/duc-nt/CVE-2022-44268-ImageMagick-Arbitrary-File-Read-PoC) - Arbitrary File Read over ImageMagick [`#1858574`](https://hackerone.com/reports/1858574) [alternative](https://github.com/voidz0r/CVE-2022-44268).
- [ImageMagick - Shell injection via PDF password](https://insert-script.blogspot.com/2020/11/imagemagick-shell-injection-via-pdf.html) - `2021-11-21`.
- [#1154542](https://hackerone.com/reports/1154542) - RCE in GitLab when removing metadata with ExifTool `2021-04-07`.
- [`CVE-2021-32802`](https://nvd.nist.gov/vuln/detail/CVE-2021-32802) - HEIC image preview can be used to invoke Imagick [#1261413](https://hackerone.com/reports/1261413) `2020-07-14`.
- [`CVE-2019-11932`](https://awakened1712.github.io/hacking/hacking-whatsapp-gif-rce/) - Double-free bug in WhatsApp turns to RCE ([BBRE](https://www.youtube.com/watch?v=lplExF6djQ4)) `2019-10-02`.
- [`CVE-2016-3714`](https://nvd.nist.gov/vuln/detail/CVE-2016-3714) - 'ImageTragick' Delegate Arbitrary Command Execution ([Exploit-DB](https://www.exploit-db.com/exploits/39791)).

## Archives: ZipSlip, TarSlip, etc. pp

- [#1914118](https://hackerone.com/reports/1914118) - [`PR`](https://github.com/github/securitylab/issues/728), [`Video`](https://www.youtube.com/watch?v=F95U912u7OQ) `2023-03-21`.
- [`CVE-2022-3607`](https://huntr.dev/bounties/2d1db3c9-93e8-4902-a55b-5ea53c22aa11/) - ZipSlip Symlink variant allows to read any file within OctoPrint Box in [octoprint/octoprint](https://github.com/OctoPrint/OctoPrint) [`Commit`](https://github.com/octoprint/octoprint/commit/3cca3a43f3d085e9bbe5a5840c8255bb1b5d052e) `2022-08-24`.

## WYSIWYG Editors

- [`CVE-2023-30943`](https://nvd.nist.gov/vuln/detail/CVE-2023-30943) - Moodle vulnerability allowing a remote user to send a specially crafted HTTP request and create arbitrary folders on the system using TinyMCE loaders `2023-05-11`.
- [`CVE-2011-4906`](https://nvd.nist.gov/vuln/detail/CVE-2011-4906) - Joomla 1.5.12 TinyMCE vulnerability leading to RCE (via Arbitrary File Upload) [#778629](https://hackerone.com/reports/778629) [Exploit-DB](https://www.exploit-db.com/exploits/10183).

## `data:`-Attribute

- [#1444682](https://hackerone.com/reports/1444682) - XSS over data: at jamfpro.shopifycloud.com in outdated Swagger UI `2022-01-09`.
- [#1276742](https://hackerone.com/reports/1276742) - Stored XSS in SVG file as data: url in rich text editor `2021-07-24`.

## XSS

- [OWASP: XSS Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/XSS_Filter_Evasion_Cheat_Sheet.html) - Filter Evasion Cheat Sheet by OWASP.
- [Cross-site scripting (XSS) cheat sheet](https://portswigger.net/web-security/cross-site-scripting/cheat-sheet) - XSS Cheat Sheet by Portswigger.
- [AwesomeXSS](https://github.com/s0md3v/AwesomeXSS) - Awesome Page about XSS.
- [Cross-site scripting contexts](https://portswigger.net/web-security/cross-site-scripting/contexts) - Portswigger XSS context break outs.
- [Breaking XSS mitigations via Script Gadgets](https://www.blackhat.com/docs/us-17/thursday/us-17-Lekies-Dont-Trust-The-DOM-Bypassing-XSS-Mitigations-Via-Script-Gadgets.pdf) - Conference talk from 2017 explaining various CSP bypasses using Script Gadgets.

## Request Smuggling

- [#771666](https://hackerone.com/reports/771666) - Stealing Zomato X-Access-Token: in Bulk using HTTP Request Smuggling on api.zomato.com `2020-01-10`.
- [HTTP Desync Attacks: Smashing into the Cell Next Door](https://www.youtube.com/watch?v=w-eJM2Pc0KI) - DEF CON 27 Conference talk by James Kettle (albinowax) of PortSwigger `2019-11-16`.
- [#737140](https://hackerone.com/reports/737140) - CL.TE-based request smuggling on Slack `2019-11-14`.
- [HTTP Desync Attacks: Request Smuggling Reborn](https://portswigger.net/research/http-desync-attacks-request-smuggling-reborn) - `2019-08-07`.

### Tools

- [defparam/smuggler](https://github.com/defparam/smuggler) - An HTTP Request Smuggling / Desync testing tool written in Python 3.

## Open Redirects

- [#1032610](https://hackerone.com/reports/1032610) - Chaining requests to bypass a blacklist `2020-11-12`.

## SQLi

- [payloadbox/sql-injection-payload-list](https://github.com/payloadbox/sql-injection-payload-list) - SQL Injection Payload List.

## PHP

- [PHP Magic Tricks: Type Juggling](https://owasp.org/www-pdf-archive/PHPMagicTricks-TypeJuggling.pdf) - `2015`.

## Python

- [Prototype Pollution in Python](https://blog.abdulrah33m.com/prototype-pollution-in-python/) - `2023-01-04`.

## Docker

- [Finding leaked secrets in your Docker image with a scanner](https://pythonspeed.com/articles/docker-secret-scanner/) - `2022-02-01`.
- [Security scanners for Python and Docker: from code to dependencies](https://pythonspeed.com/articles/docker-python-security-scan/) - `2020-05-20`.

## Active Directory

### Tools

- [vletoux/pingcastle](https://github.com/vletoux/pingcastle) - Runs an initial scan and gives an high-level overview.
- [BloodHoundAD/BloodHound](https://github.com/BloodHoundAD/BloodHound) - Checks for attack vectors in AD.

<!-- END CONTENT -->
