# CodePath-Week7
# Project 7 - WordPress Pentesting

Time spent: **6** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Vulnerability Name or ID: User Enumeration
  - [x] Summary:
    - Vulnerability types: User Enumeration
    - Tested in version: 4.2
    - Fixed in version: 4.6.1
  - [x] GIF Walkthrough:
      <img src='https://github.com/andywang219/CodePath-Week7/blob/master/Challenge1/ue.gif' title='User Enumeration' width='800' alt='UE' />
  - [x] Steps to recreate: Sign in with username admin, but no password. Then sign in with username admin and a random password. Lastly, sign in with a random username and a random password.
  - [x] Affected source code:
    - [Link 1](https://wordpress.org/plugins/stop-user-enumeration/#description)
    <hr/>
2. (Required) Vulnerability Name or ID: Cross Site Scripting
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.6.1
  - [x] GIF Walkthrough: 
      <img src='https://github.com/andywang219/CodePath-Week7/blob/master/Challenge2/xss.gif' title='XSS' width='800' alt='xss' />
  - [x] Steps to recreate: First, create a new post. Second, insert the code: ```<a onmouseover= "alert('Hello')" >Say Hello</a>```. Third, click on "Preview" and as you hover over the text, there'll be a alert.
  - [x] Affected source code:
    - [Link 2](https://core.trac.wordpress.org/browser/branches/4.2/src/wp-includes/class-wp-editor.php?rev=33361)
    <hr/>
3. (Required) Vulnerability Name or ID: Authenticated Stored Cross-Site Scripting via Image Filename
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: Later Versions
  - [x] GIF Walkthrough: 
       <img src='https://github.com/andywang219/CodePath-Week7/blob/master/Challenge3/mediaXSS.gif' title='FXSS' width='800' alt='fxss' />
  - [x] Steps to recreate: First, create a new media page and upload an image from your computer. Second, click on the image and insert the following code into the image's title: ```filename<img src=a onerror=alert(1)>.png```.
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
    <hr/>
4. (Optional) Vulnerability Name or ID: Stored XSS through embedded URL
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: Later Version
  - [x] GIF Walkthrough: 
      <img src='https://github.com/andywang219/CodePath-Week7/blob/master/Challenge4/link.gif' title='LXSS' width='800' alt='lxss' />
  - [x] Steps to recreate: First, create a new post. Second, insert a malicious link like this one: ```[embed src='https://youtube.com/embed/123\x3csvg onload=alert("Hacked")\x3e'][/embed]```
  - [x] Affected source code:
    - [Link 4](https://blog.sucuri.net/2017/03/stored-xss-in-wordpress-core.html)

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2018] [Andy Wang]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
