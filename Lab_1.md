<h3> Welcome!</h3><br>
<h1>Install software in a Linux distribution</h1 >
<br>
<p>October 29, 2024<br></p>


<p>Hey there, fellow lifelong learner! I´m <a href="https://www.linkedin.com/in/rosanafssantos/">Rosana</a>, and I’m genuinely excited to join you on this adventure.<br>
This practice is part of the <a href="https://www.coursera.org/professional-certificates/google-cybersecurity">Google Cybersecurity Professional Certificate</a> > Course 4: Tools of the Trade: Linux and SQL > Module X: ------------.<br><br>


Task 1 - Ensure that APT is installed
Task 2 - Install and uninstall the Suricata application

<h2>Task 1 - Ensure that APT is installed</h2>
<p>First, you’ll check that the APT application is installed so that you can use it to manage applications. The simplest way to do this is to run the apt command in the Bash shell and check the response.<br>

The Bash shell is the command-line interpreter currently open on the left side of the screen. You’ll use the Bash shell by typing commands after the prompt. The prompt is represented by a dollar sign ($) followed by the input cursor.</p>

> Confirm that the APT package manager is installed in your Linux environment. To do this, type apt after the command-line prompt and press ENTER.
When installed, apt displays basic usage information when you run it. This includes the version information and a description of the tool:


<pre><code>analyst@7aee503cf643:~$ apt
apt 1.8.2.3 (amd64)
Usage: apt [options] command

apt is a commandline package manager and provides commands for
searching and managing as well as querying information about packages.
It provides the same functionality as the specialized APT tools,
like apt-get and apt-cache, but enables options more suitable for
interactive use by default.

Most used commands:
  list - list packages based on package names
  search - search in package descriptions
  show - show package details
  install - install packages
  reinstall - reinstall packages
  remove - remove packages
  autoremove - Remove automatically all unused packages
  update - update list of available packages
  upgrade - upgrade the system by installing/upgrading packages
  full-upgrade - upgrade the system by removing/installing/upgrading packages
  edit-sources - edit the source information file

See apt(8) for more information about the available commands.
Configuration options and syntax is detailed in apt.conf(5).
Information about how to configure sources can be found in sources.list(5).
Package and version choices can be expressed via apt_preferences(5).
Security details are available in apt-secure(8).
                                        This APT has Super Cow Powers.
analyst@7aee503cf643:~$ 
</code></pre>

<p>APT is already installed by default in the Linux Bash shell in this lab because this is a Debian-based system. APT is also the recommended package manager for Debian. If you’re using another distribution, a different package manager, such as YUM, may be available instead.</p>

<h2>Task 2 - Install and uninstall the Suricata application</h2>

<p>In this task, you must install Suricata, a network analysis tool used for intrusion detection, and verify that it installed correctly. Then, you’ll uninstall the application.</p>
<p>Use the APT package manager to install the Suricata application.</p>
<p>Type <code>sudo apt installsuricata</code> after the command-line prompt and press ENTER.</p>
<br>
<p><code>Note</code>: <em>The apt install and apt remove commands must be prefixed with the sudo command as elevated privileges are required to install and uninstall software in Linux.</em><br>
The Suricata application can take a few minutes to install.</p>
<br>
<p>When you install an application with APT, the output displays details of all the software to be installed. This may include additional applications that depend on the new software. These additional applications are called the dependencies of the software to be installed.<br>

When prompted to continue, press the <strong>ENTER</strong> key to respond with the default response. (In this case, the default response is <strong>Yes</strong>.)</p>

> Verify that Suricata is installed by running the newly installed application.


<pre><code>analyst@7aee503cf643:~$ sudo apt install suricata
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following additional packages will be installed:
  geoip-database libauthen-sasl-perl libdata-dump-perl
  libencode-locale-perl libevent-2.1-6 libevent-core-2.1-6
  libevent-pthreads-2.1-6 libfile-listing-perl libfont-afm-perl
  libgeoip1 libhiredis0.14 libhtml-form-perl libhtml-format-perl
  libhtml-parser-perl libhtml-tagset-perl libhtml-tree-perl libhtp2
  libhttp-cookies-perl libhttp-daemon-perl libhttp-date-perl
  libhttp-message-perl libhttp-negotiate-perl libhyperscan5
  libio-html-perl libio-socket-ssl-perl libjansson4 libltdl7
  libluajit-5.1-2 libluajit-5.1-common liblwp-mediatypes-perl
  liblwp-protocol-https-perl libmailtools-perl libnet-http-perl
  libnet-smtp-ssl-perl libnet-ssleay-perl libnet1 libnetfilter-log1
  libnetfilter-queue1 libnfnetlink0 libnspr4 libnss3 libpcap0.8
  libprelude23 libpython-stdlib libpython2-stdlib libpython2.7-minimal
  libpython2.7-stdlib libtimedate-perl libtry-tiny-perl liburi-perl
  libwww-perl libwww-robotrules-perl libyaml-0-2 oinkmaster
  perl-openssl-defaults prelude-utils python python-minimal
  python-simplejson python2 python2-minimal python2.7
  python2.7-minimal snort-rules-default suricata-oinkmaster
  Suggested packages:
  libdigest-hmac-perl libgssapi-perl geoip-bin libcrypt-ssleay-perl
  libauthen-ntlm-perl python-doc python-tk python2-doc python2.7-doc
  binfmt-support snort | snort-pgsql | snort-mysql
  libtcmalloc-minimal4
  The following NEW packages will be installed:
  ...
  0 upgraded, 66 newly installed, 0 to remove and 59 not upgraded.
  Need to get 16.8 MB of archives.
  After this operation, 62.6 MB of additional disk space will be used.
  Do you want to continue? [Y/n] Y
  Get:1 http://deb.debian.org/debian-security buster/updates/main amd64 libpython2.7-minimal amd64 2.7.16-2+deb10u4 [396 kB]
  Get:2 http://deb.debian.org/debian-security buster/updates/main amd64 python2.7-minimal amd64 2.7.16-2+deb10u4 [1367 kB]
  ...
  Get:65 http://deb.debian.org/debian-security buster/updates/main amd64 snort-rules-default all 2.9.20-0+deb10u1 [374 kB]
  Get:66 http://deb.debian.org/debian buster/main amd64 suricata-oinkmaster all 1:4.1.2-2+deb10u1 [38.5 kB]
  Fetched 16.8 MB in 1s (33.2 MB/s)           
  debconf: delaying package configuration, since apt-utils is not installed
  analyst@7aee503cf643:~$ 
</code></pre>





