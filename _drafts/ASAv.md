---
layout: post
title: "ASAv"
description: ""
category:
tags: [asav, network]
--

ASAV Notes
- Release notes of version attempted http://www.cisco.com/c/en/us/td/docs/security/asa/asa94/release/notes/asarn94.html

## Using VirtualBox
1. Downloaded Adaptive Security Virtual Appliance (ASAv) - 9.4.1.200        (asav941-202.zip )
2. Extracted the .zip file
3. Attempted import of ovi file into VirtualBox
4. Error with below of manifest file
![Alt text](/img/asav-vbox-error.png)
 - [x] Research Error
     - https://davejsteele.wordpress.com/2012/08/12/virtualbox-ovf-import-error-verr_manifest_file_mismatch-failed-to-import-appliance/
     - Fixed by renaming *.mf to *.manifest and reimporting file.
     - specifically: $ mv asav-vi.mf asav-vi.manifest
