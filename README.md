```
var page = require('webpage').create();

page.onFilePicker = function(oldFile) {
    console.log('onFilePicker(' + oldFile + ') called');
    return 'master.zip';
}

page.onDownloadFinished = function(status) {
    console.log('onDownloadFinished(' + status + ')');
    phantom.exit(1);
}

page.onLoadFinished = function(status) {
    console.log('onLoadFinished(' + status + ')');
}

page.open('https://github.com/HedCET/TorrentAlert/archive/master.zip');
```
