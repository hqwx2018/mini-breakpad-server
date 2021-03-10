# mini-breakpad-server

Minimum collecting server for crash reports sent by
[google-breakpad](https://code.google.com/p/google-breakpad/).


## Features

* No requirement for setting up databases or web servers.
* Collecting crash reports with minidump files.
* Simple web interface for viewing translated crash reports.

## Run

* `npm install .`
* `grunt`
* Put your breakpad symbols under `pool/symbols/PRODUCT_NAME`
* `node lib/app.js`


### Notice
win10下运行mini-breakpad-server

1.nvm use 6.9.2 (node version 6.9.2)

2.minidump 0.11.0

Linux下运行mini-breakpad-server

1.nvm use 8.10.0 (node version 8.10.0)

2.minidump 0.3.0

3.上传文件

curl -F upload_file_minidump=@filename.dmp -F ver="4.7.0.0" -F prod=programName localhost:1127/post

