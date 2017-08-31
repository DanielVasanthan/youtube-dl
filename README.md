# youtube-dl
youtube-dl is not working in Ubuntu 16.04
magicvideo1@sharonu1:~/Videos$ youtube-dl "https://www.youtube.com/watch?v=-PFTaQJhLTY" --verbose 2>&1 | tee youtube-dl_bug_report1.txt
[debug] System config: []
[debug] User config: []
[debug] Command-line args: [u'https://www.youtube.com/watch?v=-PFTaQJhLTY', u'--verbose']
[debug] Encodings: locale UTF-8, fs UTF-8, out None, pref UTF-8
[debug] youtube-dl version 2016.02.22
[debug] Python version 2.7.12 - Linux-4.4.0-93-generic-x86_64-with-Ubuntu-16.04-xenial
[debug] exe versions: ffmpeg 2.8.11-0ubuntu0.16.04.1, ffprobe 2.8.11-0ubuntu0.16.04.1, rtmpdump 2.4
[debug] Proxy map: {}
[youtube] -PFTaQJhLTY: Downloading webpage
[youtube] -PFTaQJhLTY: Downloading video info webpage
[youtube] -PFTaQJhLTY: Extracting video information
WARNING: unable to extract uploader nickname
[youtube] {22} signature length 46.40, html5 player en_US-vfleWWlqf
[youtube] -PFTaQJhLTY: Downloading player /yts/jsbin/player-en_US-vfleWWlqf/base.js
ERROR: Signature extraction failed: Traceback (most recent call last):
  File "/usr/lib/python2.7/dist-packages/youtube_dl/extractor/youtube.py", line 905, in _decrypt_signature
    video_id, player_url, s
  File "/usr/lib/python2.7/dist-packages/youtube_dl/extractor/youtube.py", line 819, in _extract_signature_function
    errnote='Download of %s failed' % player_url)
  File "/usr/lib/python2.7/dist-packages/youtube_dl/extractor/common.py", line 468, in _download_webpage
    res = self._download_webpage_handle(url_or_request, video_id, note, errnote, fatal, encoding=encoding)
  File "/usr/lib/python2.7/dist-packages/youtube_dl/extractor/common.py", line 375, in _download_webpage_handle
    urlh = self._request_webpage(url_or_request, video_id, note, errnote, fatal)
  File "/usr/lib/python2.7/dist-packages/youtube_dl/extractor/common.py", line 355, in _request_webpage
    return self._downloader.urlopen(url_or_request)
  File "/usr/lib/python2.7/dist-packages/youtube_dl/YoutubeDL.py", line 1905, in urlopen
    return self._opener.open(req, timeout=self._socket_timeout)
  File "/usr/lib/python2.7/urllib2.py", line 421, in open
    protocol = req.get_type()
  File "/usr/lib/python2.7/urllib2.py", line 283, in get_type
    raise ValueError, "unknown url type: %s" % self.__original
ValueError: unknown url type: /yts/jsbin/player-en_US-vfleWWlqf/base.js
 (caused by ValueError(u'unknown url type: /yts/jsbin/player-en_US-vfleWWlqf/base.js',)); please report this issue on https://yt-dl.org/bug . Make sure you are using the latest version; see  https://yt-dl.org/update  on how to update. Be sure to call youtube-dl with the --verbose flag and include its complete output.
Traceback (most recent call last):
  File "/usr/lib/python2.7/dist-packages/youtube_dl/extractor/youtube.py", line 905, in _decrypt_signature
    video_id, player_url, s
  File "/usr/lib/python2.7/dist-packages/youtube_dl/extractor/youtube.py", line 819, in _extract_signature_function
    errnote='Download of %s failed' % player_url)
  File "/usr/lib/python2.7/dist-packages/youtube_dl/extractor/common.py", line 468, in _download_webpage
    res = self._download_webpage_handle(url_or_request, video_id, note, errnote, fatal, encoding=encoding)
  File "/usr/lib/python2.7/dist-packages/youtube_dl/extractor/common.py", line 375, in _download_webpage_handle
    urlh = self._request_webpage(url_or_request, video_id, note, errnote, fatal)
  File "/usr/lib/python2.7/dist-packages/youtube_dl/extractor/common.py", line 355, in _request_webpage
    return self._downloader.urlopen(url_or_request)
  File "/usr/lib/python2.7/dist-packages/youtube_dl/YoutubeDL.py", line 1905, in urlopen
    return self._opener.open(req, timeout=self._socket_timeout)
  File "/usr/lib/python2.7/urllib2.py", line 421, in open
    protocol = req.get_type()
  File "/usr/lib/python2.7/urllib2.py", line 283, in get_type
    raise ValueError, "unknown url type: %s" % self.__original
ValueError: unknown url type: /yts/jsbin/player-en_US-vfleWWlqf/base.js
Traceback (most recent call last):
  File "/usr/lib/python2.7/dist-packages/youtube_dl/YoutubeDL.py", line 666, in extract_info
    ie_result = ie.extract(url)
  File "/usr/lib/python2.7/dist-packages/youtube_dl/extractor/common.py", line 316, in extract
    return self._real_extract(url)
  File "/usr/lib/python2.7/dist-packages/youtube_dl/extractor/youtube.py", line 1407, in _real_extract
    encrypted_sig, video_id, player_url, age_gate)
  File "/usr/lib/python2.7/dist-packages/youtube_dl/extractor/youtube.py", line 915, in _decrypt_signature
    'Signature extraction failed: ' + tb, cause=e)
ExtractorError: Signature extraction failed: Traceback (most recent call last):
  File "/usr/lib/python2.7/dist-packages/youtube_dl/extractor/youtube.py", line 905, in _decrypt_signature
    video_id, player_url, s
  File "/usr/lib/python2.7/dist-packages/youtube_dl/extractor/youtube.py", line 819, in _extract_signature_function
    errnote='Download of %s failed' % player_url)
  File "/usr/lib/python2.7/dist-packages/youtube_dl/extractor/common.py", line 468, in _download_webpage
    res = self._download_webpage_handle(url_or_request, video_id, note, errnote, fatal, encoding=encoding)
  File "/usr/lib/python2.7/dist-packages/youtube_dl/extractor/common.py", line 375, in _download_webpage_handle
    urlh = self._request_webpage(url_or_request, video_id, note, errnote, fatal)
  File "/usr/lib/python2.7/dist-packages/youtube_dl/extractor/common.py", line 355, in _request_webpage
    return self._downloader.urlopen(url_or_request)
  File "/usr/lib/python2.7/dist-packages/youtube_dl/YoutubeDL.py", line 1905, in urlopen
    return self._opener.open(req, timeout=self._socket_timeout)
  File "/usr/lib/python2.7/urllib2.py", line 421, in open
    protocol = req.get_type()
  File "/usr/lib/python2.7/urllib2.py", line 283, in get_type
    raise ValueError, "unknown url type: %s" % self.__original
ValueError: unknown url type: /yts/jsbin/player-en_US-vfleWWlqf/base.js
 (caused by ValueError(u'unknown url type: /yts/jsbin/player-en_US-vfleWWlqf/base.js',)); please report this issue on https://yt-dl.org/bug . Make sure you are using the latest version; see  https://yt-dl.org/update  on how to update. Be sure to call youtube-dl with the --verbose flag and include its complete output.

magicvideo1@sharonu1:~/Videos$ uname -a 
Linux sharonu1 4.4.0-93-generic #116-Ubuntu SMP Fri Aug 11 21:17:51 UTC 2017 x86_64 x86_64 x86_64 GNU/Linux
magicvideo1@sharonu1:~/Videos$ cat /etc/release*
cat: '/etc/release*': No such file or directory
magicvideo1@sharonu1:~/Videos$ ls -l /etc/release*
ls: cannot access '/etc/release*': No such file or directory
magicvideo1@sharonu1:~/Videos$ ls -l /etc/*release*
-rw-r--r-- 1 root root 105 Jul 31 09:36 /etc/lsb-release
lrwxrwxrwx 1 root root  21 Jul 31 09:36 /etc/os-release -> ../usr/lib/os-release
magicvideo1@sharonu1:~/Videos$ cat /etc/os-release
NAME="Ubuntu"
VERSION="16.04.3 LTS (Xenial Xerus)"
ID=ubuntu
ID_LIKE=debian
PRETTY_NAME="Ubuntu 16.04.3 LTS"
VERSION_ID="16.04"
HOME_URL="http://www.ubuntu.com/"
SUPPORT_URL="http://help.ubuntu.com/"
BUG_REPORT_URL="http://bugs.launchpad.net/ubuntu/"
VERSION_CODENAME=xenial
UBUNTU_CODENAME=xenial
magicvideo1@sharonu1:~/Videos$ 
