# Project 7 - WordPress Pentesting

Time spent: **9** hours and half spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Vulnerability Name or ID
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [x] GIF Walkthrough:
  ![](./Question_1.gif)
  
  - [x] Steps to recreate: 
  
  Leave the following javascript line as a comment to the post
  
  <b onmouseover="alert('This is a vulnerability')">click!</b> 
  
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
2. (Required) Authenticated Stored Cross-Site Scripting via Image Filename
  - [x] Summary: this vulnerability allows attackers to create image files that will inject arbitrary web script.
  This abuses the insufficient validation of the file names of uploaded images.
  
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.6.1
  - [x] GIF Walkthrough:
   ![](./Question2.gif)
  
  
  - [x] Steps to recreate: Create a new media image file with the following format:
  
    filename<img src=a onerror=alert(1)>.png
  
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
    
3. (Required) 
  - [x] Summary: this vulnerability allows attackers to inject arbitrary web script via video URL embeds
  
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.7.2
  - [x] GIF Walkthrough:
  ![](./Question_1.gif)
  
  
  - [x] Steps to recreate: create a new page. And, then place the code below in the body of the page
  
  [embed src='https://youtube.com/embed/dark\x3csvg onload=alert(1)\x3e'][/embed]
  
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
# README
