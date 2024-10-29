<h3> Welcome!</h3><br>
<h1>Install software in a Linux distribution</h1 >
<br>
<p>October 29, 2024<br></p>


<p>Hey there, fellow lifelong learner! I´m <a href="https://www.linkedin.com/in/rosanafssantos/">Rosana</a>, and I’m genuinely excited to join you on this adventure.<br>
This practice is part of the <a href="https://www.coursera.org/professional-certificates/google-cybersecurity">Google Cybersecurity Professional Certificate</a> > Course 4: Tools of the Trade: Linux and SQL > Module X: ------------.<br><br>


Task 1 - Ensure that APT is installed
Task 2 - Install and uninstall the Suricata application
Task 3 - Install the tcpdump application
Task 4 - List the installed applications
Task 5 - Reinstall the Suricata application
<br>

<h2>Task 1 - Ensure that APT is installed</h2>
<br>
<p>First, you’ll check that the APT application is installed so that you can use it to manage applications. The simplest way to do this is to run the apt command in the Bash shell and check the response.<br>

The Bash shell is the command-line interpreter currently open on the left side of the screen. You’ll use the Bash shell by typing commands after the prompt. The prompt is represented by a dollar sign ($) followed by the input cursor.</p>

> Confirm that the APT package manager is installed in your Linux environment. To do this, type apt after the command-line prompt and press ENTER.
When installed, apt displays basic usage information when you run it. This includes the version information and a description of the tool:

![image](https://github.com/user-attachments/assets/7ae857bb-337c-4e89-820a-b6e22bef9586)

<p>I completed the task successfully!!!</p>

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
<br>
<p>In this task, you must install Suricata, a network analysis tool used for intrusion detection, and verify that it installed correctly. Then, you’ll uninstall the application.</p>
<p>Use the APT package manager to install the Suricata application.</p>
<p>Type <code>sudo apt install suricata</code> after the command-line prompt and press ENTER.</p>

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

<br>
<p><code>Note</code>: <em>The apt install and apt remove commands must be prefixed with the sudo command as elevated privileges are required to install and uninstall software in Linux.</em><br>
The Suricata application can take a few minutes to install.</p>
<br>
<p>When you install an application with APT, the output displays details of all the software to be installed. This may include additional applications that depend on the new software. These additional applications are called the dependencies of the software to be installed.<br>

When prompted to continue, press the <strong>ENTER</strong> key to respond with the default response. (In this case, the default response is <strong>Yes</strong>.)</p>

> Verify that Suricata is installed by running the newly installed application.

<p>Type <code>suricata</code> after the command-line prompt and press <strong>ENTER</strong>.

When Suricata is installed, version and usage information is listed:</p>

![image](https://github.com/user-attachments/assets/2892495e-ca6d-4e2c-93a1-f38bf83adda7)

<p>I completed the task successfully!!!</p>

<pre><code>analyst@7aee503cf643:~$ suricata 
Suricata 4.1.2
USAGE: suricata [OPTIONS] [BPF FILTER]

        -c <path>                            : path to configuration file
        -T                                   : test configuration file (use with -c)
        -i <dev or ip>                       : run in pcap live mode
        -F <bpf filter file>                 : bpf filter file
        -r <path>                            : run in pcap file/offline mode
        -q <qid>                             : run in inline nfqueue mode
        -s <path>                            : path to signature file loaded in addition to suricata.yaml settings (optional)
        ...
</code></pre>

> Use the <code>APT package manager</code> to uninstall Suricata.

<p>When prompted to continue, press the <strong>ENTER</strong> key to respond with the default response. (In this case, the default response is Yes.)</p>

<P>If you have uninstalled Suricata, the output is an error message:</P>

![image](https://github.com/user-attachments/assets/90d87566-f6ef-4381-b1be-89e776c4717a)

<p>This message indicates that Suricata can't be found anymore.</p>


<pre><code>sudo apt remove suricata
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following packages were automatically installed and are no longer required:
  geoip-database libauthen-sasl-perl libdata-dump-perl
  libencode-locale-perl libevent-2.1-6 libevent-core-2.1-6
  libevent-pthreads-2.1-6 libfile-listing-perl libfont-afm-perl
  libgeoip1 libhiredis0.14 libhtml-form-perl libhtml-format-perl
  libhtml-parser-perl libhtml-tagset-perl libhtml-tree-perl libhtp2
  libhttp-cookies-perl libhttp-daemon-perl libhttp-date-perl
  libhttp-message-perl libhttp-negotiate-perl libhyperscan5
  libio-html-perl libio-socket-ssl-perl libjanss
  ...
  0 upgraded, 0 newly installed, 2 to remove and 59 not upgraded.
After this operation, 5298 kB disk space will be freed.
Do you want to continue? [Y/n] Y
(Reading database ... 24795 files and directories currently installed.)
Removing suricata-oinkmaster (1:4.1.2-2+deb10u1) ...
Removing suricata (1:4.1.2-2+deb10u1) ...
invoke-rc.d: could not determine current runlevel
invoke-rc.d: policy-rc.d denied execution of stop.
Processing triggers for man-db (2.8.5-2+deb10u1) ...
</code></pre>

<p>I completed the task successfully!!!</p>

<pre><code>analyst@7aee503cf643:~$ suricata
-bash: /usr/bin/suricata: No such file or directory
</code></pre>

<h2>Task 3 - Install the tcpdumo application</h2>
<br>
<p>In this task, you must install the tcpdump application. This is a command-line tool that can be used to capture network traffic in a Linux Bash shell.</p>

<p>Use the <code>APT package manager</code>code> to install tcpdump.</p>

<p>Type <code>sudo apt install tcpdump</code>code> after the command-line prompt and press ENTER.</p>

<pre><code> sudo apt install tcpdump
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following packages were automatically installed and are no longer required:
geoip-database libauthen-sasl-perl libdata-dump-perl libencode-locale-perl libevent-2.1-6 libevent-core-2.1-6 libevent-pthreads-2.1-6 libfile-listing-perl libfont-afm-perl libgeoip1 libhiredis0.14
libhtml-form-perl libhtml-format-perl libhtml-parser-perl libhtml-tagset-perl libhtml-tree-perl libhtp2 libhttp-cookies-perl libhttp-daemon-perl libhttp-date-perl libhttp-message-perl libhttp-negotiate-perl
libhyperscan5 libio-html-perl libio-socket-ssl-perl libjansson4 libltdl7 libluajit-5.1-2 libluajit-5.1-common liblwp-mediatypes-perl liblwp-protocol-https-perl libmailtools-perl libnet-http-perl
...
The following NEW packages will be installed:
tcpdump
0 upgraded, 1 newly installed, 0 to remove and 59 not upgraded.
Need to get 400 kB of archives.
...
Preparing to unpack .../tcpdump_4.9.3-1~deb10u2_amd64.deb ...
Unpacking tcpdump (4.9.3-1~deb10u2) ......................................Setting up tcpdump (4.9.3-1~deb10u2) .....................................Processing triggers for man-db (2.8.5-2+deb10u1) ...###...................
analyst@7aee503cf643:~$ 
</code></pre>

<h2>Task 4 - List the installed applications</h2>
<br>
<p>Next, you need to confirm that you’ve installed the required applications. It's important to be able to validate that the correct applications are installed. Often you may want to check that the correct versions are installed as well.</p>

> Use the <code>APT package manager</code>code> to list all installed applications.</p>

<p>Type <code>apt list --installed</code>code> after the command-line prompt and press <strong>ENTER</strong>.

This produces a long list of applications because Linux has a lot of software installed by default.</p>

> Search through the list to find the tcpdump application you installed.

<p>The Suricata application is not listed because you installed and then uninstalled that application:</p>

![image](https://github.com/user-attachments/assets/1bc07236-8af6-48f8-9951-bbb19bd58b03)

<code>Note</code>: <em>The specific version of tcpdump that you see displayed may be different from what is shown above.</em>

<pre><code> apt list --installed
Listing... Done
adduser/oldoldstable,now 3.118 all [installed,automatic]
apt/oldoldstable,oldoldstable-updates,now 1.8.2.3 amd64 [installed,automatic]
base-files/oldoldstable,now 10.3+deb10u13 amd64 [installed,automatic]
base-passwd/oldoldstable,now 3.5.46 amd64 [installed,automatic]
bash/oldoldstable,now 5.0-4 amd64 [installed,automatic]
binutils-common/oldoldstable,now 2.31.1-16 amd64 [installed,automatic]
binutils-x86-64-linux-gnu/oldoldstable,now 2.31.1-16 amd64 [installed,automatic]
...
tar/oldoldstable,now 1.30+dfsg-6 amd64 [installed,upgradable to: 1.30+dfsg-6+deb10u1]
tcpdump/oldoldstable,now 4.9.3-1~deb10u2 amd64 [installed]
tree/oldoldstable,now 1.8.0-1 amd64 [installed]
tzdata/now 2021a-0+deb10u8 all [installed,upgradable to: 2024a-0+deb10u1]
ucf/oldoldstable,now 3.0038+nmu1 all [installed,automatic]
util-linux/oldoldstable,now 2.33.1-0.1 amd64 [installed,upgradable to: 2.33.1-0.1+deb10u1]
wget/oldoldstable,now 1.20.1-1.1 amd64 [installed]
xauth/oldoldstable,now 1:1.0.10-1 amd64 [installed,automatic]
xdg-user-dirs/oldoldstable,now 0.17-2 amd64 [installed,automatic]
xz-utils/oldoldstable,oldoldstable,now 5.2.4-1+deb10u1 amd64 [installed,automatic]
zlib1g/oldoldstable,now 1:1.2.11.dfsg-1+deb10u2 amd64 [installed,automatic]
</code></pre>

<p>I completed the task successfully!!!</p>

<h2>Task 5 -Reinstall the Suricata application</h2>
<br>
<p>Activity: Install software in a Linux distribution
experiment
Lab
schedule
1 hour
universal_currency_alt
No cost
show_chart
Introductory
info
This lab may incorporate AI tools to support your learning.
Lab instructions and tasks
Activity overview
Scenario
Start your lab
Task 1. Ensure that APT is installed
Task 2. Install and uninstall the Suricata application
Task 3. Install the tcpdump application
Task 4. List the installed applications
Task 5. Reinstall the Suricata application
Conclusion
End your lab
Activity overview
In this lab activity, you’ll use the Advanced Package Tool (APT) and sudo to install and uninstall applications in a Linux Bash shell.

While installing Linux applications can be a complex task, the APT package manager manages most of this complexity for you and allows you to quickly and reliably manage the applications in a Linux environment.

You'll use Suricata and tcpdump as an example. These are network security applications that can be used to capture and analyze network traffic.

The virtual machine you access in this lab has a Debian-based distribution of Linux running, and that works with the APT package manager. Using a virtual machine prevents damage to a system in the event its tools are used improperly. It also gives you the ability to revert to a previous state.

As a security analyst, it's likely you'll need to know how to install and manage applications on a Linux operating system. In this lab activity, you’ll learn how to do exactly that!

Scenario
Your role as a security analyst requires that you have the Suricata and tcpdump network security applications installed on your system.

In this scenario, you have to install, uninstall, and reinstall these applications on your Linux Bash shell. You also need to confirm that you’ve installed them correctly.

Here’s how you'll do this: First, you’ll confirm that APT is installed on your Linux Bash shell. Next, you’ll use APT to install the Suricata application and confirm that it is installed. Then, you’ll uninstall the Suricata application and confirm this as well. Next, you’ll install the tcpdump application and list the applications currently installed. Finally, you’ll reinstall the Suricata application and confirm that both applications are installed.

OK, it's time to learn how to install some applications!

Note: The lab starts with your user account, called analyst, already logged in to the Bash shell. This means you can start with the tasks as soon as you click the Start Lab button.
Disclaimer: For optimal performance and compatibility, it is recommended to use either Google Chrome or Mozilla Firefox browsers while accessing the labs.
Start your lab
You'll need to start the lab before you can access the materials. To do this, click the green “Start Lab” button at the top of the screen.

Lab Start button displayed.

After you click the Start Lab button, you will see a shell, where you will be performing further steps in the lab. You should have a shell like this:

Linux Terminal displayed. 

When you have completed all the tasks, refer to the End your Lab section that follows the tasks for information on how to end your lab.

Task 1. Ensure that APT is installed
First, you’ll check that the APT application is installed so that you can use it to manage applications. The simplest way to do this is to run the apt command in the Bash shell and check the response.

The Bash shell is the command-line interpreter currently open on the left side of the screen. You’ll use the Bash shell by typing commands after the prompt. The prompt is represented by a dollar sign ($) followed by the input cursor.

Confirm that the APT package manager is installed in your Linux environment. To do this, type apt after the command-line prompt and press ENTER.
When installed, apt displays basic usage information when you run it. This includes the version information and a description of the tool:

apt 1.8.2.3 (amd64)
Usage: apt [options] command

apt is a commandline package manager and provides commands for
searching and managing as well as querying information about packages.
It provides the same functionality as the specialized APT tools,
like apt-get and apt-cache, but enables options more suitable for
interactive use by default.
...
APT is already installed by default in the Linux Bash shell in this lab because this is a Debian-based system. APT is also the recommended package manager for Debian. If you’re using another distribution, a different package manager, such as YUM, may be available instead.

Click Check my progress to verify that you have completed this task correctly.

You have completed this task and confirmed that APT is installed.
Ensure that APT is installed

You have completed this task and confirmed that APT is installed.
Task 2. Install and uninstall the Suricata application
In this task, you must install Suricata, a network analysis tool used for intrusion detection, and verify that it installed correctly. Then, you’ll uninstall the application.

Use the APT package manager to install the Suricata application.
Type sudo apt install suricata after the command-line prompt and press ENTER.

Note: The apt install and apt remove commands must be prefixed with the sudo command as elevated privileges are required to install and uninstall software in Linux.

The Suricata application can take a few minutes to install.

When you install an application with APT, the output displays details of all the software to be installed. This may include additional applications that depend on the new software. These additional applications are called the dependencies of the software to be installed.

When prompted to continue, press the ENTER key to respond with the default response. (In this case, the default response is Yes.)

Verify that Suricata is installed by running the newly installed application.
Type suricata after the command-line prompt and press ENTER.

When Suricata is installed, version and usage information is listed:

Suricata 4.1.2
USAGE: suricata [OPTIONS] [BPF FILTER]

    -c   : path to configuration file
    -T         : test configuration file (use with -c)
...
Use the APT package manager to uninstall Suricata.
Type sudo apt remove suricata after the command-line prompt and press ENTER. Press ENTER (Yes) when prompted to continue.

When prompted to continue, press the ENTER key to respond with the default response. (In this case, the default response is Yes.)

Verify that Suricata has been uninstalled by running the application command again.
Type suricata after the command-line prompt and press ENTER.

If you have uninstalled Suricata, the output is an error message:

-bash: /usr/bin/suricata: No such file or directory
This message indicates that Suricata can't be found anymore.

Click Check my progress to verify that you have completed this task correctly.

You have completed this task and successfully installed and uninstalled the Suricata application.
Install and uninstall the Suricata application

You have completed this task and successfully installed and uninstalled the Suricata application.
Task 3. Install the tcpdump application
In this task, you must install the tcpdump application. This is a command-line tool that can be used to capture network traffic in a Linux Bash shell.

Use the APT package manager to install tcpdump.
Type sudo apt install tcpdump after the command-line prompt and press ENTER.

Click Check my progress to verify that you have completed this task correctly.

You have completed this task and installed the tcpdump application.
Install the tcpdump application

You have completed this task and installed the tcpdump application.
Task 4. List the installed applications
Next, you need to confirm that you’ve installed the required applications. It's important to be able to validate that the correct applications are installed. Often you may want to check that the correct versions are installed as well.

Use the APT package manager to list all installed applications.
Type apt list --installed after the command-line prompt and press ENTER.

This produces a long list of applications because Linux has a lot of software installed by default.

Search through the list to find the tcpdump application you installed.
The Suricata application is not listed because you installed and then uninstalled that application:

...
tcpdump/oldstable,now 4.9.3-1~deb10u2 amd64 [installed]
...
Note: The specific version of tcpdump that you see displayed may be different from what is shown above.
Click Check my progress to verify that you have completed this task correctly.

You have completed this task and displayed a list of installed applications.
List the installed applications

You have completed this task and displayed a list of installed applications.
Task 5. Reinstall the Suricata application
In this task, you must reinstall the Suricata application and verify that it has installed correctly.</p>

> Run the command to install the Suricata application.

<p>Type <code>sudo apt install suricata</code> after the command-line prompt and press <strong>ENTER</strong>.<br>

When prompted to continue, press the <strong>ENTER</strong> key to respond with the default response. (In this case, the default response is <strong>Yes</strong>.)</p>

> Use the APT package manager to list the installed applications.

<p>Type <code>apt list --installed</code> after the command-line prompt and press <strong>ENTER</strong>.</p>

<pre><code> sudo apt install suricata
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following additional packages will be installed:
  suricata-oinkmaster
Suggested packages:
  libtcmalloc-minimal4
The following NEW packages will be installed:
  suricata suricata-oinkmaster
0 upgraded, 2 newly installed, 0 to remove and 59 not upgraded.
Need to get 1698 kB of archives.
After this operation, 5298 kB of additional disk space will be used.
Do you want to continue? [Y/n] Y
  Get:1 http://deb.debian.org/debian buster/main amd64 suricata amd64 1:4.1.2-2+deb10u1 [1660 kB]
Get:2 http://deb.debian.org/debian buster/main amd64 suricata-oinkmaster all 1:4.1.2-2+deb10u1 [38.5 kB]
Fetched 1698 kB in 0s (16.7 MB/s)         
debconf: delaying package configuration, since apt-utils is not installed
Selecting previously unselected package suricata.
(Reading database ... 24774 files and directories currently installed.)
Preparing to unpack .../suricata_1%3a4.1.2-2+deb10u1_amd64.deb 
...
  
</code></pre>
