<div align="center">

<!-- title -->

<!--lint ignore no-dead-urls-->

# Awesome InfoSec [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![lint](https://github.com/spekulatius/awesome-infosec/actions/workflows/lint.yaml/badge.svg)](https://github.com/spekulatius/awesome-infosec/actions/workflows/lint.yaml)

<!-- subtitle -->

Personal notes and awesome infosec stuff.

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

- [Image Libs: Converters, etc.](#image-libs-converters-etc)
- [`data:`-Attribute](#data-attribute)
- [XSS](#xss)
- [Request Smuggling](#request-smuggling)
- [Active Directory](#active-directory)

<!-- CONTENT -->

## Image Libs: Converters, etc.

- [ImageMagick: The hidden vulnerability behind your online images](https://www.metabaseq.com/imagemagick-zero-days/) - `2023-02-01`.
- [`CVE-2022-44268`](https://github.com/duc-nt/CVE-2022-44268-ImageMagick-Arbitrary-File-Read-PoC) - Arbitrary File Read over ImageMagick ([alternative](https://github.com/voidz0r/CVE-2022-44268)).
- [ImageMagick - Shell injection via PDF password](https://insert-script.blogspot.com/2020/11/imagemagick-shell-injection-via-pdf.html) - `2021-11-21`.
- [#1154542](https://hackerone.com/reports/1154542) - RCE in GitLab when removing metadata with ExifTool `2021-04-07`.
- [`CVE-2021-32802`](https://nvd.nist.gov/vuln/detail/CVE-2021-32802) - HEIC image preview can be used to invoke Imagick [#1261413](https://hackerone.com/reports/1261413) `2020-07-14`.
- [`CVE-2019-11932`](https://awakened1712.github.io/hacking/hacking-whatsapp-gif-rce/) - Double-free bug in WhatsApp turns to RCE ([BBRE](https://www.youtube.com/watch?v=lplExF6djQ4)) `2019-10-02`.
- [`CVE-2016-3714`](https://nvd.nist.gov/vuln/detail/CVE-2016-3714) - 'ImageTragick' Delegate Arbitrary Command Execution ([exploit-db.com/exploits/39791](https://www.exploit-db.com/exploits/39791)).

## `data:`-Attribute

- [#1444682](https://hackerone.com/reports/1444682) - XSS over data: at jamfpro.shopifycloud.com in outdated Swagger UI `2022-01-09`.
- [#1276742](https://hackerone.com/reports/1276742) - Stored XSS in SVG file as data: url in rich text editor `2021-07-24`.

## XSS

- [OWASP: XSS Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/XSS_Filter_Evasion_Cheat_Sheet.html) - Filter Evasion Cheat Sheet by OWASP.
- [Cross-site scripting (XSS) cheat sheet](https://portswigger.net/web-security/cross-site-scripting/cheat-sheet) - XSS Cheat Sheet by Portswigger.
- [AwesomeXSS](https://github.com/s0md3v/AwesomeXSS) - Awesome Page about XSS.
- [Cross-site scripting contexts](https://portswigger.net/web-security/cross-site-scripting/contexts) - Portswigger XSS context break outs.

## Request Smuggling

- [#771666](https://hackerone.com/reports/771666) - Stealing Zomato X-Access-Token: in Bulk using HTTP Request Smuggling on api.zomato.com `2020-01-10`.
- [HTTP Desync Attacks: Smashing into the Cell Next Door](https://www.youtube.com/watch?v=w-eJM2Pc0KI) - DEF CON 27 Conference talk by James Kettle (albinowax) of PortSwigger `2019-11-16`.
- [#737140](https://hackerone.com/reports/737140) - CL.TE-based request smuggling on Slack `2019-11-14`.
- [HTTP Desync Attacks: Request Smuggling Reborn](https://portswigger.net/research/http-desync-attacks-request-smuggling-reborn) - `2019-08-07`.

### Tools

- [defparam/smuggler](https://github.com/defparam/smuggler) - An HTTP Request Smuggling / Desync testing tool written in Python 3.

## Active Directory

### Tools

- [vletoux/pingcastle](https://github.com/vletoux/pingcastle) - Runs an initial scan and gives an high-level overview.
- [BloodHoundAD/BloodHound](https://github.com/BloodHoundAD/BloodHound) - Checks for attack vectors in AD.

<!-- END CONTENT -->
