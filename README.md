# Born2beroot
<a href="https://github.com/JaeSeoKim/badge42"><img src="https://badge42.vercel.app/api/v2/cl4qxms4g001609l49j835g66/project/2574154" alt="joslopez's 42 Born2beroot Score" /><a/n>
<b>General guidelines</b>
<p>• The use of VirtualBox (or UTM if you can’t use VirtualBox) is mandatory.</p>
<p>• You only have to turn in a signature.txt file at the root of your repository. You
must paste in it the signature of your machine’s virtual disk. Go to Submission and
peer-evaluation for more information.<p/n>
<b>Mandatory part</b>
<p>This project consists of having you set up your first server by following specific rules.</p>
<p>You must choose as an operating system either the latest stable version of Debian (no
testing/unstable), or the latest stable version of Rocky. Debian is highly recommended
if you are new to system administration.</p>
<p>You must create at least 2 encrypted partitions using LVM.</p>
<p>A SSH service will be running on port 4242 only. For security reasons, it must not be
possible to connect using SSH as root.</p>
<p>You have to configure your operating system with the UFW (or firewalld for Rocky)
firewall and thus leave only port 4242 open.</p>
<p>• The hostname of your virtual machine must be your login ending with 42 (e.g.,
wil42). You will have to modify this hostname during your evaluation.</p>
<p>• You have to implement a strong password policy.</p>
<p>• You have to install and configure sudo following strict rules.</p>
<p>• In addition to the root user, a user with your login as username has to be present.</p>
<p>• This user has to belong to the user42 and sudo groups</p>
<p>To set up a strong password policy, you have to comply with the following requirements:</p>
<p>• Your password has to expire every 30 days.</p>
<p>• The minimum number of days allowed before the modification of a password will
be set to 2.</p>
<p>• The user has to receive a warning message 7 days before their password expires.</p>
<p>• Your password must be at least 10 characters long. It must contain an uppercase
letter, a lowercase letter, and a number. Also, it must not contain more than 3
consecutive identical characters.</p>
<p>• The password must not include the name of the user.</p>
<p>• The following rule does not apply to the root password: The password must have
at least 7 characters that are not part of the former password.</p>
<p>• Of course, your root password has to comply with this policy.</p>
To set up a strong configuration for your sudo group, you have to comply with the
following requirements:</p>
<p>• Authentication using sudo has to be limited to 3 attempts in the event of an incorrect password.</p>
<p>• A custom message of your choice has to be displayed if an error due to a wrong
password occurs when using sudo.</p>
<p>• Each action using sudo has to be archived, both inputs and outputs. The log file
has to be saved in the /var/log/sudo/ folder.</p>
<p>• The TTY mode has to be enabled for security reasons.</p>
<p>• For security reasons too, the paths that can be used by sudo must be restricted.</p>
<p>Example:</p>
<p>/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin</p>
<p>Finally, you have to create a simple script called monitoring.sh. It must be developed in bash.</p>
<p>At server startup, the script will display some information (listed below) on all terminals every 10 minutes (take a look at wall). The banner is optional. No error must be visible.</p>
<p>Your script must always be able to display the following information:</p>
<p>• The architecture of your operating system and its kernel version.</p>
<p>• The number of physical processors.</p>
<p>• The number of virtual processors.</p>
<p>• The current available RAM on your server and its utilization rate as a percentage.</p>
<p>• The current available memory on your server and its utilization rate as a percentage.</p>
<p>• The current utilization rate of your processors as a percentage.</p>
<p>• The date and time of the last reboot.</p>
<p>• Whether LVM is active or not.</p>
<p>• The number of active connections.</p>
<p>• The number of users using the server.</p>
<p>• The IPv4 address of your server and its MAC (Media Access Control) address.</p>
<p>• The number of commands executed with the sudo program.<p/n>
<b>Bonus list:</b>
<p>• Set up partitions correctly.</p>
<p>• Set up a functional WordPress website with the following services: lighttpd, MariaDB, and PHP.</p>
<p>• Set up a service of your choice that you think is useful (NGINX / Apache2 excluded!). During the defense, you will have to justify your choice.</p>
