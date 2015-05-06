#Snapshot Crawler
##Snapshot Crawler can be used to make a HTML Snapshot of an AJAX Web Site for Example if build with GWT.

Usage: java -jar snapshotCrawler.jar [OPTION]... [SITEMAP-LINK]... [POST-LINK]

Example 1: Creates a HTML snapshot of a single page<br>
java -jar snapshotCrawler.jar --url ht<span>tp://</span>www.url-to-ajax-page.com --outpath /home/user/path-to-save-snapshots/ --log out.html --concurrent 10

Example 2: Creates a HTML snapshot of all links found insight the XML sitemap. The format used is the <a href="https://support.google.com/webmasters/answer/183668?hl=en">Google Webmaster Tools sitemap</a>.<br>
java -jar snapshotCrawler.jar --sitemap http&#58;//www\.url-to-xml-sitemap.com --outpath /home/user/path-to-save-snapshots/ --log out.html --concurrent 10

Example 3: Creates a HTML snapshot and posts the Result to your web server:<br>
java -jar snapshotCrawler.jar --sitemap http&#58;//www\.url-to-xml-sitemap.com --posturl http://www\.your-server-servlet.com/ --concurrent 10



OPTIONS:

| Option               | Description  |
| ---------------------|--------------|
| --help               | Display this help  |
| --sitemap            | http URL to an XML Sitemap  |
| --url                | http URL to make a HTML shapshot  |
| --outpath            | Path, where the snapshots are saved |
| --posturl            | Followed by the path where the HTML Snapshot is POSTED<br>$_POST[link] contains the retreived Website<br>$_POST[html] the HTML Snapshot itself--outdir<br>Followed by the folder, where the snapshots are saved locally |
| --log                | HTML Log File, where log about work is saved  |
| --compress           | Removes White Spaces in HTML Snapshot  |
| --concurrent         | Number of Threads running contemporarily calculating the HTML Snapshots. default 1 |
| --waitchange         | Time to wait where JS execution is not changing the snapshot anymore. default 30s.  |
| --deadline           | Deadline for Snapshot Thread in seconds. Default 120s.Retreiving Sitemap:   |
