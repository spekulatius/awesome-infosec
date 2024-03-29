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

- [Orientation](#orientation)
- [Bugs](#bugs)
  - [Archives: ZipSlip/TarSlip and others](#archives-zipsliptarslip-and-others)
  - [CLI Applications](#cli-applications)
  - [Image Libs: Converters, Resizers, etc. pp](#image-libs-converters-resizers-etc-pp)
  - [Request Smuggling](#request-smuggling)
  - [Deserialization](#deserialization)
  - [SQLi](#sqli)
  - [URL Parsers](#url-parsers)
  - [WYSIWYG Editors](#wysiwyg-editors)
  - [XSS](#xss)
  - [XSS via `data:`-Attribute](#xss-via-data-attribute)
- [Bug Chains](#bug-chains)
- [Language-Level](#language-level)
  - [PHP](#php)
  - [Python](#python)
- [Secret Scanning](#secret-scanning)
  - [Docker](#docker)

<!-- CONTENT -->

## Orientation

- [roadmap.sh](https://roadmap.sh/cyber-security) - Cyber-Security Roadmap.

## Bugs

### Archives: ZipSlip/TarSlip and others

- [`CVE-2023-40477`](https://www.zerodayinitiative.com/advisories/ZDI-23-1152/) - code execution via crafted .rar in vulnerable WinRAR versions prior to 6.23 [`PoC (unverified)`](https://github.com/b1tg/CVE-2023-38831-winrar-exploit) `2023-08-17`.
- [`CVE-2023-32981`](https://nvd.nist.gov/vuln/detail/CVE-2023-32981) - Arbitrary file write vulnerability in Jenkins Pipeline Utility Steps Plugin 2.15.2 and earlier using crafted archives as parameters [`GitHub Security Lab`](https://securitylab.github.com/advisories/GHSL-2023-058_GHSL-2023-059_Pipeline_Utility_Steps_Plugin/) `2023-05-16`.
- [`#1914118`](https://hackerone.com/reports/1914118) - [`PR`](https://github.com/github/securitylab/issues/728), [`Video`](https://www.youtube.com/watch?v=F95U912u7OQ) `2023-03-21`.
- [`CVE-2022-3607`](https://huntr.dev/bounties/2d1db3c9-93e8-4902-a55b-5ea53c22aa11) - ZipSlip Symlink variant allows to read any file within OctoPrint Box in [octoprint/octoprint](https://github.com/OctoPrint/OctoPrint) [`Fix`](https://github.com/octoprint/octoprint/commit/3cca3a43f3d085e9bbe5a5840c8255bb1b5d052e) `2022-08-24`.

### CLI Applications

- [Terminally Owned - 60 Years of Escaping](https://www.youtube.com/watch?v=Y4A7KMQEmfo) -  DEF CON 31 talk by David Leadbeater `2023`.
- [Weaponizing Plain Text ANSI Escape Sequences as a Forensic Nightmare](https://www.youtube.com/watch?v=3T2Al3jdY38) - DEF CON 31  talk by STÖK `2023`.
- [Plain Text? Really?](https://www.youtube.com/watch?v=_mZBa3sqTrI) - NDC Oslo 2021 talk by Dylan Beattie `2021`.

### Image Libs: Converters, Resizers, etc. pp

- [`CVE-2023-34153`](https://nvd.nist.gov/vuln/detail/CVE-2023-34153) - Command injection via `video:vsync` or `video:pixel-format` [`Fix`](https://github.com/ImageMagick/ImageMagick/issues/6338) `2023-05-30`.
- [ImageMagick: The hidden vulnerability behind your online images](https://www.metabaseq.com/imagemagick-zero-days/) - `2023-02-01`.
- [`CVE-2022-44268`](https://github.com/duc-nt/CVE-2022-44268-ImageMagick-Arbitrary-File-Read-PoC) - Arbitrary File Read over ImageMagick [`#1858574`](https://hackerone.com/reports/1858574) [`alternative`](https://github.com/voidz0r/CVE-2022-44268).
- [ImageMagick - Shell injection via PDF password](https://insert-script.blogspot.com/2020/11/imagemagick-shell-injection-via-pdf.html) - `2021-11-21`.
- [`#1154542`](https://hackerone.com/reports/1154542) - RCE in GitLab when removing metadata with ExifTool [Video](https://www.youtube.com/watch?v=PZ-H099IaWo) `2021-04-07`.
- [`CVE-2021-32802`](https://nvd.nist.gov/vuln/detail/CVE-2021-32802) - HEIC image preview can be used to invoke Imagick [`#1261413`](https://hackerone.com/reports/1261413) `2020-07-14`.
- [`CVE-2019-11932`](https://awakened1712.github.io/hacking/hacking-whatsapp-gif-rce/) - Double-free bug in WhatsApp turns to RCE [`BBRE`](https://www.youtube.com/watch?v=lplExF6djQ4) `2019-10-02`.
- [`CVE-2016-3714`](https://nvd.nist.gov/vuln/detail/CVE-2016-3714) - "ImageTragick" Delegate Arbitrary Command Execution [`Exploit-DB`](https://www.exploit-db.com/exploits/39791).

### Request Smuggling

- [`#771666`](https://hackerone.com/reports/771666) - Stealing Zomato X-Access-Token: in Bulk using HTTP Request Smuggling on `api.zomato.com` `2020-01-10`.
- [HTTP Desync Attacks: Smashing into the Cell Next Door](https://www.youtube.com/watch?v=w-eJM2Pc0KI) - DEF CON 27 Conference talk by James Kettle ([@albinowax](https://twitter.com/albinowax)) of PortSwigger `2019-11-16`.
- [`#737140`](https://hackerone.com/reports/737140) - CL.TE-based request smuggling on Slack `2019-11-14`.
- [HTTP Desync Attacks: Request Smuggling Reborn](https://portswigger.net/research/http-desync-attacks-request-smuggling-reborn) - `2019-08-07`.

#### Tools

- [defparam/smuggler](https://github.com/defparam/smuggler) - An HTTP Request Smuggling / Desync testing tool `Python 3`.

### Deserialization

#### PHP

- [ambionics/phpggc](https://github.com/ambionics/phpggc) - PHPGGC is a library of PHP `unserialize()`-payloads along with a tool to generate them, from command line or programmatically.
- [Finding a POP chain on a common Symfony bundle](https://www.synacktiv.com/en/publications/finding-a-pop-chain-on-a-common-symfony-bundle-part-1) - Detailed, step-by-step bash-driven analysis of a Symfony bundle [`Part 2`](https://www.synacktiv.com/en/publications/finding-a-pop-chain-on-a-common-symfony-bundle-part-2) `2023-09-12`.
- [Code Reuse Attacks in PHP: Automated POP Chain Generation](https://ia803205.us.archive.org/15/items/ARMArchitectureReferenceManual/CodeReuseAttacksInPHPAutomatedPOPChainGeneration.pdf) - Using static analytics to automatically identify POP chains in various PHP frameworks.

#### Python

- [Insecure Deserialization Detection in Python](https://scholarworks.sjsu.edu/etd_projects/1270?utm_source=scholarworks.sjsu.edu%2Fetd_projects%2F1270) - Project work by Aneesh Verma discussing deserialization issues `2023-05`.

#### Java

- [frohoff/ysoserial](https://github.com/frohoff/ysoserial) - A proof-of-concept tool for generating payloads that exploit unsafe Java object deserialization.

#### Ruby

- [Universal Deserialisation Gadget for Ruby 2.x-3.x](https://devcraft.io/2021/01/07/universal-deserialisation-gadget-for-ruby-2-x-3-x.html) - `2021-01-07`.
- [Ruby Deserialization](https://www.elttam.com/blog/ruby-deserialization/#content) - Ruby 2.x Universal RCE Deserialization Gadget Chain `2018-11-08`.

### SQLi

- [payloadbox/sql-injection-payload-list](https://github.com/payloadbox/sql-injection-payload-list) - SQL Injection Payload List.

### URL Parsers

- [`RFC 3986`](https://www.rfc-editor.org/rfc/rfc3986) - Official RFC Uniform Resource Identifier (URI) `2005-01`.
- [What Is a URL?](https://azeemba.com/posts/what-is-a-url.html) - Dangers of inconsistent parsing of URLs `2023-04-30`.
- [http-http-http-http-http-http-http](https://daniel.haxx.se/blog/2022/09/08/http-http-http-http-http-http-http/) - Daniel Stenberg, the author of curl, discusses URLs validation with examples `2022-09-08`.
- [A New Era of SSRF - Exploiting URL Parser in Trending Programming Languages!](https://www.youtube.com/watch?v=voTHFdL9S2k) - BlackHat talk by Orange Tsai discussing how different libs parse URLs [`Slides`](https://www.blackhat.com/docs/us-17/thursday/us-17-Tsai-A-New-Era-Of-SSRF-Exploiting-URL-Parser-In-Trending-Programming-Languages.pdf) `2017`.

### WYSIWYG Editors

- [`CVE-2023-30943`](https://nvd.nist.gov/vuln/detail/CVE-2023-30943) - Moodle vulnerability allowing a remote user to send a specially crafted HTTP request and create arbitrary folders on the system using TinyMCE loaders `2023-05-11`.
- [`CVE-2011-4906`](https://nvd.nist.gov/vuln/detail/CVE-2011-4906) - Joomla 1.5.12 TinyMCE vulnerability leading to RCE (via Arbitrary File Upload) [`#778629`](https://hackerone.com/reports/778629) [`Exploit-DB`](https://www.exploit-db.com/exploits/10183).

### XSS

- [OWASP: XSS Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/XSS_Filter_Evasion_Cheat_Sheet.html) - Filter Evasion Cheat Sheet by OWASP.
- [Cross-site scripting (XSS) cheat sheet](https://portswigger.net/web-security/cross-site-scripting/cheat-sheet) - XSS Cheat Sheet by Portswigger.
- [AwesomeXSS](https://github.com/s0md3v/AwesomeXSS) - Awesome Page about XSS.
- [Cross-site scripting contexts](https://portswigger.net/web-security/cross-site-scripting/contexts) - Portswigger XSS context breakouts.
- [Breaking XSS mitigations via Script Gadgets](https://www.blackhat.com/docs/us-17/thursday/us-17-Lekies-Dont-Trust-The-DOM-Bypassing-XSS-Mitigations-Via-Script-Gadgets.pdf) - Conference talk from 2017 explaining various CSP bypasses using Script Gadgets `2017`.

### XSS via `data:`-Attribute

- [`#1444682`](https://hackerone.com/reports/1444682) - XSS over data: at `jamfpro.shopifycloud.com` in outdated Swagger UI `2022-01-09`.
- [`#1276742`](https://hackerone.com/reports/1276742) - Stored XSS in SVG file as `data:` url in rich text editor `2021-07-24`.

## Bug Chains

Multiple single vulnerabilities combined to create a more significant one.

- [`#2089042`](https://hackerone.com/reports/2089042) - ATO via self-XSS and cookie bridge (to switch to local domains: here `yelp.com` to `yelp.dk`). Includes setting additional cookies to break the cookie bridge. `2023-07-28`.
- [CVE-2023-36844 and Friends: RCE in Juniper Devices](https://labs.watchtowr.com/cve-2023-36844-and-friends-rce-in-juniper-firewalls/) - Utilising two bugs that would be near-useless in isolation and combining them to unauthenticated RCE [ComputerWeekly](https://www.computerweekly.com/news/366550532/Threat-actors-exploiting-unpatched-Juniper-Networks-devices) [`CVE-2023-36846`](https://nvd.nist.gov/vuln/detail/CVE-2023-36846) [`CVE-2023-36845`](https://nvd.nist.gov/vuln/detail/CVE-2023-36845) [`PoC`](https://github.com/watchtowrlabs/juniper-rce_cve-2023-36844).
- [Two XSS Vulnerabilities in Azure with Embedded postMessage IFrames](https://orca.security/resources/blog/examining-two-xss-vulnerabilities-in-azure-services/) - iframe, postMessage and XSS `2023-06-14`.
- [A smorgasbord of a bug chain: postMessage, JSONP, WAF bypass, DOM-based XSS, CORS, CSRF…](https://jub0bs.com/posts/2023-05-05-smorgasbord-of-a-bug-chain/) - a complex bug chain consisting of an insecure message event listener, a shoddy JSONP endpoint, a WAF bypass, DOM-based XSS on an out-of-scope subdomain, and a permissive CORS configuration `2023-05-05`.
- [`#1032610`](https://hackerone.com/reports/1032610) - Chaining requests to bypass a blacklist `2020-11-12`.
- [WordPress Transposh: Exploiting a Blind SQL Injection via XSS](https://www.rcesecurity.com/2022/07/WordPress-Transposh-Exploiting-a-Blind-SQL-Injection-via-XSS/) - combining three CVEs using weak default config, using stored XSS, and blind SQL `2022-07-22`. 
- [XXE-scape through the front door: circumventing the firewall with HTTP request smuggling](https://honoki.net/2020/03/18/xxe-scape-through-the-front-door-circumventing-the-firewall-with-http-request-smuggling/) - XML External Entity injection (XXE) vulnerability combined with request smuggling `2020-03-18`.


## Language-Level

### PHP

- [Type Juggling](https://www.php.net/manual/en/language.types.type-juggling.php) - Official PHP page.
- [PHP Magic Tricks: Type Juggling](https://owasp.org/www-pdf-archive/PHPMagicTricks-TypeJuggling.pdf) - `2015`.
- [PHP filters chain](https://www.synacktiv.com/en/publications/php-filters-chain-what-is-it-and-how-to-use-it) - What is it and how to use it `2022`.

### Python

- [Prototype Pollution in Python](https://blog.abdulrah33m.com/prototype-pollution-in-python/) - `2023-01-04`.


## Secret Scanning

### Docker

- [Finding leaked secrets in your Docker image with a scanner](https://pythonspeed.com/articles/docker-secret-scanner/) - `2022-02-01`.
- [Security scanners for Python and Docker: from code to dependencies](https://pythonspeed.com/articles/docker-python-security-scan/) - `2020-05-20`.

<!-- END CONTENT -->
