# Project 7 - WordPress Pentesting

Time spent: 5 hours spent in total

> Objective: Find, analyze, recreate, and document **three vulnerabilities** affecting an old version of WordPress.

## Pentesting Report

1. XSS: Through Image Filename
  - [ ] Summary: 
    - Vulnerability types: Cross-Site Scripting (XSS) Vulnerability
    - Tested in version: 4.2
    - Fixed in version: 4.2.10
  - [ ] GIF Walkthrough: https://github.com/jiayiw6/Week-7-CodePath-Web-Security/blob/master/gif1.gif
  - [ ] Steps to recreate:
    - Step 1: Create a file with the following name: File_Name<JS_Code>; JS_Code is the Javascript code to execute.
    - Step 2: Make the size of the file to be at least 2MB.
    - Step 3: Create a new media file and upload the file and "update".
    - Step 4: JS_Code executes as the size of the image is too large and an error message pops up. 
  
2. XSS: Through Embeded Link
  - [ ] Summary: 
    - Vulnerability types: Cross-Site Scripting (XSS) Vulnerability
    - Tested in version: 4.2
    - Fixed in version: 4.2.13
  - [ ] GIF Walkthrough: https://github.com/jiayiw6/Week-7-CodePath-Web-Security/blob/master/gif2.gif
  - [ ] Steps to recreate: 
    - Step 1: Embed a youtube link (with JavaScript) in "edit a post" in Text View.
    - Step 2: Switch to Visual View and the JavaScript code should execute.
    
3. XSS: Mouse Over Link
  - [ ] Summary: 
    - Vulnerability types: Cross-Site Scripting (XSS) Vulnerability
    - Tested in version: 4.2
    - Fixed in version: 4.2.3
  - [ ] GIF Walkthrough: https://github.com/jiayiw6/Week-7-CodePath-Web-Security/blob/master/gif3.gif
  - [ ] Steps to recreate: 
    - Step 1: Create a post with ancher that has JavaScript code in Text View. (For instance: \<a href\="[caption code=">]\</a\>\<a title\=\" onmouseover\=alert\(\'666\'\) \"\>link\<\/a>\)
    - Step 2: In Page View, when hover over the link, the JavaScript code will be executed.

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

The greatest challenge during my work process is to get the time machine working. 

## License

    Copyright [2018] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
