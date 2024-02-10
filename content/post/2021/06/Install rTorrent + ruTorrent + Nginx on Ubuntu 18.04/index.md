---
title: "Install rTorrent + ruTorrent + Nginx on Ubuntu 18.04"
date: 2021-06-24T00:30:13+07:00
description: "How to Install rTorrent + ruTorrent + Nginx on Ubuntu 18.04"
url: "install-rtorrent-rutorrent-nginx-on-ubuntu-18-04"
image: "ubuntu.svg"
categories: ["Linux", "Tutorial"]
tags: ["Linux", "Tutorial"]
keywords:
  [
    "Install rTorrent",
    "Install ruTorrent",
    "Install rTorrent + ruTorrent",
    "Install rTorrent Ubuntu 18.04",
    "Install rTorrent + ruTorrent Ubuntu 18.04",
    "Install rTorrent + ruTorrent + Nginx on Ubuntu 18.04",
  ]
description: 'Firefox 89.0 is the latest stable version of the Firefox web browser. Released on June 1, 2021, it ships with major interface changes, a new custom theme, and more.'
summary: 'Firefox 89.0 is the latest stable version of the Firefox web browser. Released on June 1, 2021, it ships with major interface changes, a new custom theme, and more.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi6l5tekXAR5aLIebY2y3-Iu_OdRt2Lv_qkemOHsvaOnY6_OtR_QjJPi6xbdQ6nXcppkpt2lY5Zyg2GzCpeZ8ciBKto2nXirMor6fwloSJ2-AFgIoZ-ZcXrmMdz_Y96ekt8XlScUF5htQ5JOMW361g5FZSzfcnwPpkxWUnE3BJwpcLm9gqPPO58fkjm8fCm/s80-rw/ubuntu-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi6l5tekXAR5aLIebY2y3-Iu_OdRt2Lv_qkemOHsvaOnY6_OtR_QjJPi6xbdQ6nXcppkpt2lY5Zyg2GzCpeZ8ciBKto2nXirMor6fwloSJ2-AFgIoZ-ZcXrmMdz_Y96ekt8XlScUF5htQ5JOMW361g5FZSzfcnwPpkxWUnE3BJwpcLm9gqPPO58fkjm8fCm/s0-rw/ubuntu-logo.png
---

{{% adsense %}}

rTorrent is a text-based BitTorrent client written in C++, based on the ncurses and libTorrent (not to be confused with libtorrent) libraries for Unix, whose author's goal is "a focus on high performance and good code". Source: [Wikipedia](https://en.wikipedia.org/wiki/RTorrent)

This tutorial will guide you through the installation of libtorrent 0.13.8, rTorrent 0.9.8, and the ruTorrent Web UI v3.10 on Ubuntu 18.04 system.

## Install some required dependencies
```python
sudo apt install libtools libxmlrpc-core-c3 libxmlrpc-c++8-dev libboost-tools-dev libboost-dev libboost-system-dev nginx php-fpm sox screen pcregrep libxmlrpc-core-c3 subversion -y
```
## Compile and Install libtorrent 0.13.8
1. Download libtorrent 0.13.8
```python
wget http://rtorrent.net/downloads/libtorrent-0.13.8.tar.gz
```
2. Extract libtorrent-0.13.8.tar.gz
```python
tar -xf libtorrent-0.13.8.tar.gz
cd libtorrent-0.13.8
```
3. Compile and Install libTorrent
```python
./autogen.sh
./configure
make
sudo make install
```

{{% adsense %}}

## Compile and Install rTorrent
1. Download rtorrent 0.98
```python
wget http://libtorrent.rakshasa.no/downloads/rtorrent-0.9.8.tar.gz
```
2. Extract rtorrent-0.9.8.tar.gz
```python
tar -xf rtorrent-0.9.8.tar.gz
cd rtorrent-0.9.8
```
3. Compile and Install rTorrent
```python
./autogen.sh
./configure --with-xmlrpc-c
make
sudo make install
sudo ldconfig
```

{{% adsense %}}

## rTorrent Configuration File
rTorrent requires a configuration file (**.rtorrent.rc**) to be added to the home directory of user running the application.\
You can find this default configuration in [Github](https://github.com/rtakshasa/rtorrent/blob/master/doc/rtorrent.rc). This will require you to configure it manually.\
But you can copy and paste my configuration and save it on **.rtorrent.rc** in your home directory\
**NOTE: Edit this line**
 - `directory.default.set`  This for default directory to save the downloaded torrents.
    - Example `directory.default.set = /home/rmdhnreza/Downloads` 
 - `session.path.set` Default session directory.
    - Example `session.path.set = /home/rmdhnreza/.session`
 - `network.scgi.open_port` = "127.0.0.1:6000"
    - Port default is 5000, but I change to 6000 because I set nginx port to 5000

{{< spoiler text="Click to Show Configuration" >}}
```nginx
#############################################################################
# This is an (old) example resource file for rTorrent.
# Copy to ~/.rtorrent.rc and enable/modify the options as needed.
# Remember to uncomment the options you wish to enable.
#
# See 'rtorrent.rc-example' for a newer, basic configuration.
#
#   Sample: https://github.com/rakshasa/rtorrent/wiki/CONFIG-Template
# Complete: https://rtorrent-docs.readthedocs.io/en/latest/cmd-ref.html
#   Useful: https://rtorrent-docs.readthedocs.io/en/latest/use-cases.html
#   Manual: https://rtorrent-docs.readthedocs.io/en/latest/
#  Convert: https://github.com/rakshasa/rtorrent/wiki/rTorrent-0.9-Comprehensive-Command-list-(WIP)
# Handbook: https://media.readthedocs.org/pdf/rtorrent-docs/latest/rtorrent-docs.pdf
#     File: https://github.com/rakshasa/rtorrent/blob/master/doc/rtorrent.rc
#############################################################################

# Maximum and minimum number of peers to connect to per torrent.
#
throttle.min_peers.normal.set = 40
throttle.max_peers.normal.set = 500

# Same as above but for seeding completed torrents.
# "-1" = same as downloading.
#
throttle.min_peers.seed.set = 10
throttle.max_peers.seed.set = 500

# Maximum number of simultaneous uploads per torrent.
#
#throttle.max_uploads.set = 15

# Global upload and download rate in KiB.
# "0" for unlimited.
#
#throttle.global_down.max_rate.set_kb = 0
#throttle.global_up.max_rate.set_kb = 0

# Default directory to save the downloaded torrents.
#
directory.default.set = /home/USER/Downloads ## CHANGE THIS

# Default session directory. Make sure you don't run multiple instance
# of rTorrent using the same session directory. Perhaps using a
# relative path?
#
session.path.set = /home/USER/.session ## CHANGE THIS

# Watch a directory for new torrents, and stop those that have been
# deleted.
#
#schedule2 = watch_directory,5,5,load.start=./watch/*.torrent

# Close torrents when disk-space is low.
#
#schedule2 = low_diskspace,5,60,close_low_diskspace=100M

# The IP address reported to the tracker.
#
#network.local_address.set = 127.0.0.1
#network.local_address.set = rakshasa.no

# The IP address the listening socket and outgoing connections is
# bound to.
#
#network.bind_address.set = 127.0.0.1
#network.bind_address.set = rakshasa.no

# Port range to use for listening.
#
network.port_range.set = 6890-6999

# Start opening ports at a random position within the port range.
#
network.port_random.set = no

# Check hash for finished torrents. Might be useful until the bug is
# fixed that causes lack of disk-space not to be properly reported.
#
pieces.hash.on_completion.set = no

# Set whether the client should try to connect to UDP trackers.
#
trackers.use_udp.set = yes

# Alternative calls to bind and IP that should handle dynamic IP's.
#
#schedule2 = ip_tick,0,1800,ip=rakshasa
#schedule2 = bind_tick,0,1800,bind=rakshasa

# Encryption options, set to none (default) or any combination of the following:
# allow_incoming, try_outgoing, require, require_RC4, enable_retry, prefer_plaintext
#
# The example value allows incoming encrypted connections, starts unencrypted
# outgoing connections but retries with encryption if they fail, preferring
# plain-text to RC4 encryption after the encrypted handshake.
#
# protocol.encryption.set = allow_incoming,enable_retry,prefer_plaintext

# Enable DHT support for trackerless torrents or when all trackers are down.
# May be set to "disable" (completely disable DHT), "off" (do not start DHT),
# "auto" (start and stop DHT as needed), or "on" (start DHT immediately).
# The default is "off". For DHT to work, a session directory must be defined.
#
dht.mode.set = on

# UDP port to use for DHT.
#
dht.port.set = 6881

# Enable peer exchange (for torrents not marked private).
#
# protocol.pex.set = yes

# Set download list layout style ("full", "compact").
#
#ui.torrent_list.layout.set = "full"

# Run rTorrent as a daemon, controlled via XMLRPC.
#
#system.daemon.set = false

# SCGI Connectivity (for alternative rtorrent interfaces, XMLRPC)
# Use a IP socket with scgi_port, or a Unix socket with scgi_local.
# schedule can be used to set permissions on the unix socket.
#
network.scgi.open_port = "127.0.0.1:6000"
#network.scgi.open_local = (cat,(session.path),/rpc.sock)
#schedule2 = socket_chmod, 0, 0, "execute.nothrow=chmod,770,(cat,(session.path),/rpc.sock)"
```
{{< /spoiler >}}


After all configuration has been set up, you can run command `rtorrent`, if no error, this will look like this.\
Hit `CTRL + Q` for kill rtorrent

![rTorrent](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjBO22IHaBMBnEaDCQK3beVkO_2xFTzg4MOTqJBBJd3L-tCUys69tX1vFUP66YyrBh50BMCbzsqqeFD_LdVw4xWXh_vQ_8bvQ6NsML0hd5tdQFVpEYkDjhEL89gECkz0zDTc9yGjUkPrxRPB6XMgJamNcLUIOHNG5ne1PzakzOri2kCVIYMYSe9X_IMxWYx/s0-rw/rmdhnreza.my.id.install.rutorrent.1.jpeg)

## Configuration Nginx and PHP
1. You can use favorite editor for edit this configuration, You can find it on `/etc/nginx/sites-available/default`\
**This configuration use port 5000 and php-fpm7.2**, but you can change it if you want
  - Server
    - listen 5000 default_server
    - listen [::]:5000 default_server
  - PHP
    - fastcgi_pass unix:/run/php/php7.2-fpm.sock; <- change with your php-fpm version


{{< spoiler text="Click to Show Configuration" >}}
```nginx
##
# You should look at the following URL's in order to grasp a solid understanding
# of Nginx configuration files in order to fully unleash the power of Nginx.
# http://wiki.nginx.org/Pitfalls
# http://wiki.nginx.org/QuickStart
# http://wiki.nginx.org/Configuration
#
# Generally, you will want to move this file somewhere, and start with a clean
# file but keep this around for reference. Or just disable in sites-enabled.
#
# Please see /usr/share/doc/nginx-doc/examples/ for more detailed examples.
##

# Default server configuration
#
server {
  listen 5000 default_server;
  listen [::]:5000 default_server;

  # SSL configuration
  #
  # listen 443 ssl default_server;
  # listen [::]:443 ssl default_server;
  #
  # Note: You should disable gzip for SSL traffic.
  # See: https://bugs.debian.org/773332
  #
  # Read up on ssl_ciphers to ensure a secure configuration.
  # See: https://bugs.debian.org/765782
  #
  # Self signed certs generated by the ssl-cert package
  # Don't use them in a production server!
  #
  # include snippets/snakeoil.conf;

  root /var/www/html;

  # Add index.php to the list if you are using PHP
  index index.php index.html index.htm index.nginx-debian.html;

  server_name _;

  location / {
  # First attempt to serve request as file, then
  # as directory, then fall back to displaying a 404.
  try_files $uri $uri/ =404;
  # proxy_pass http://localhost:8080;
  # proxy_http_version 1.1;
  # proxy_set_header Upgrade $http_upgrade;
  # proxy_set_header Connection 'upgrade';
  # proxy_set_header Host $host;
  # proxy_cache_bypass $http_upgrade;
  }

  # pass the PHP scripts to FastCGI server listening on 127.0.0.1:9000
  #
  location ~ \.php$ {
    include snippets/fastcgi-php.conf;
  #
  # # With php7.0-cgi alone:
  # fastcgi_pass 127.0.0.1:9000;
  # # With php7.0-fpm:
    fastcgi_pass unix:/run/php/php7.2-fpm.sock;
  }

  # deny access to .htaccess files, if Apache's document root
  # concurs with nginx's one
  #
  #location ~ /\.ht {
  # deny all;
  #}
}


# Virtual Host configuration for example.com
#
# You can move that to a different file under sites-available/ and symlink that
# to sites-enabled/ to enable it.
#
#server {
# listen 80;
# listen [::]:80;
#
# server_name example.com;
#
# root /var/www/example.com;
# index index.html;
#
# location / {
#   try_files $uri $uri/ =404;
# }
#}

```
{{< /spoiler >}}

2. Save configuration
3. Start php-fpm and Nginx
```bash
sudo service php7.2-fpm start  
sudo service nginx start 
```
4. Try open in browser `localhost:5000`

![Nginx](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg2D1T8CnbtpVr7g7ewxjKiSVWXr_icQ_sfAgnSPep3JhQja2mzEqFJ9nUFXrfP_coXKkTpUkQ84X27EKNfOFjZ5E9qgzkzls8KpG-FkMOrwD9TapK3X-wzZ-jcDnLqSEa-NA6_SQfqafYAfKNFhkwlV-5jB5jPznmzMr9zmr5skA0NaYdK1oxfAmSRBDFY/s0-rw/rmdhnreza.my.id.install.rutorrent.2.jpeg)

{{% adsense %}}

## Configuration ruTorrent WebUI v3.10
1. Download ruTorrent WebUI v3.10 [github releases](https://github.com/Novik/ruTorrent/archive/refs/tags/v3.10.zip)
```bash
wget https://github.com/Novik/ruTorrent/archive/refs/tags/v3.10.zip
```
2. Extract zip file with command
```bash
unzip v3.10.zip
```
3. Open ruTorrent configuration at `ruTorrent-3.10/conf/config.php`

{{< spoiler text="Click to Show Configuration" >}}
```php
<?php
  // configuration parameters

  // for snoopy client
  @define('HTTP_USER_AGENT', 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.87 Safari/537.36', true);
  @define('HTTP_TIME_OUT', 30, true); // in seconds
  @define('HTTP_USE_GZIP', true, true);
  $httpIP = null;       // IP string. Or null for any.
  $httpProxy = array
  (
    'use'   => false,
    'proto' => 'http',    // 'http' or 'https'
    'host'  => 'PROXY_HOST_HERE',
    'port'  => 3128
  );

  @define('RPC_TIME_OUT', 5, true); // in seconds

  @define('LOG_RPC_CALLS', false, true);
  @define('LOG_RPC_FAULTS', true, true);

  // for php
  @define('PHP_USE_GZIP', false, true);
  @define('PHP_GZIP_LEVEL', 2, true);

  $schedule_rand = 10;      // rand for schedulers start, +0..X seconds

  $do_diagnostic = true;
  $log_file = '/tmp/errors.log';    // path to log file (comment or leave blank to disable logging)

  $saveUploadedTorrents = true;   // Save uploaded torrents to profile/torrents directory or not
  $overwriteUploadedTorrents = false;     // Overwrite existing uploaded torrents in profile/torrents directory or make unique name

  $topDirectory = '/';      // Upper available directory. Absolute path with trail slash.
  $forbidUserSettings = false;

  $scgi_port = 6000;
  $scgi_host = "localhost";

  // For web->rtorrent link through unix domain socket 
  // (scgi_local in rtorrent conf file), change variables 
  // above to something like this:
  //
  // $scgi_port = 0;
  // $scgi_host = "unix:///tmp/rpc.socket";

  $XMLRPCMountPoint = "/RPC2";    // DO NOT DELETE THIS LINE!!! DO NOT COMMENT THIS LINE!!!

  $pathToExternals = array(
    "python"  => '/usr/bin/python3',  // Something like /usr/bin/python3. If empty, will be found in PATH.
    "php"     => '/usr/bin/php',      // Something like /usr/bin/php. If empty, will be found in PATH.
    "curl"    => '/usr/bin/curl',     // Something like /usr/bin/curl. If empty, will be found in PATH.
    "gzip"    => '/usr/bin/gzip',     // Something like /usr/bin/gzip. If empty, will be found in PATH.
    "id"      => '/usr/bin/id',       // Something like /usr/bin/id. If empty, will be found in PATH.
    "stat"    => '/usr/bin/stat',     // Something like /usr/bin/stat. If empty, will be found in PATH.
    "pgrep"   => '/usr/bin/pgrep',    // Something like /usr/bin/pgrep. If empty, will be found in PATH.
    "sox"     => '/usr/bin/sox',      // Something like /usr/bin/sox. If empty, will be found in PATH.
  );

  $localhosts = array(      // list of local interfaces
    "127.0.0.1",
    "localhost",
  );

  $profilePath = '../share';    // Path to user profiles
  $profileMask = 0777;      // Mask for files and directory creation in user profiles.
            // Both Webserver and rtorrent users must have read-write access to it.
            // For example, if Webserver and rtorrent users are in the same group then the value may be 0770.

  $tempDirectory = null;      // Temp directory. Absolute path with trail slash. If null, then autodetect will be used.

  $canUseXSendFile = false;   // If true then use X-Sendfile feature if it exist

  $locale = "UTF8";

```
{{< /spoiler >}}

As you can see, my `$scgi_port = 6000;` this port must be same with `network.scgi.open_port` in **.rtorrent.rc**

4. Create folder html under /var/www
```bash
mkdir -p /var/www/html/
```
5. Copy ruTorrent-3.10 to /var/www/html
```bash
mv ruTorrent-3.10 /var/www/html/ruTorrent
```
6. Change owner of /var/www/html/ruTorrent
```bash
sudo chown -R $USER:www-data /var/www/html/ruTorrent
```

## Start rTorrent
1. First you can try run command `rtorrent`
2. Open in web browser `localhost:5000/ruTorrent`
3. If no error reported, `CTRL + Q` for kill rtorrent
4. Start rtorrent in background with screen
```bash
screen -d -m -S rtorrent rtorrent
```
5. For kill rtorrent, just kill screen
```bash
pkill -9 screen
```

![ruTorrent](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi8N00xf6niniCn5jLmVTifXaf_JZWx9Cg2xZpsmf8ekbwzwDRZusOYq1jppJb8s27KmAwlt9qYyxDo6UFlDejvhc-KRqhSS5da7obs7RGkcoqqlvWaMQtmWmEjFP_qt1ag3MCpbDjohA54rjmwQFgwUTC4VfZK2Dcy8yduRYPPTeSDldX4v_hM-N4C5wTP/s0-rw/rmdhnreza.my.id.install.rutorrent.3.jpeg) | ![ruTorrent](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhLeT0z6TqMdGOTxLor42fkjWJsonSkFcAoH0dPLt_F2U55Fsgxg7oji8eBD0vKGbtZph7UQ7ff4uADlpQQ-vN68sEcqYDWEDTp5B92Ev2NLOj34mEVTbaTT00IKpIkiLTSTvyQibTxfe8T0Q1mUT8L2VT18Ps7embVIHBDTJAbXu9nqO7VlXbqG348itqF/s0-rw/rmdhnreza.my.id.install.rutorrent.4.jpeg) 

![ruTorrent](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjEQ1LuEvvPzmAxVvrueaQkzVZQKj5euvMadiZEHOKzLHiLt5dugpSWPHceCV_Le5YXNj3ekZvD6TyurS74Aq78zQ5xUvAuk9GbCus2Npty8Szmvuoz_XxWm4JFus89e4bOXrt7e2vNZ5BSX58wklcZ4v2DF1BrL6ZrOf8Zi9PjFeYQlymUeWzau8nlomlo/s0-rw/rmdhnreza.my.id.install.rutorrent.5.jpeg)

{{% adsense %}}
