<p align="center">
    <img src="./sysadmin_preview.png" alt="sysadmin logo">
</p>

<br>

<p align="center">:star:</p>

<p align="center">"<i>A great Admin doesn't need to know everything, but they should be able to come up with amazing solutions to impossible projects.</i>" - cwheeler33 (ServerFault)</p>

<p align="center">:star:</p>

<p align="center">"<i>Systems Administration... [is about] acting as a force multiplier to optimize the effectiveness of other employees.</i>" <br>- Unknown</p>

<br>

<p align="center">
  <a href="https://github.com/dfuentes87/test-your-sysadmin-skills/pulls">
    <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?longCache=true" alt="Pull Requests">
  </a>
  <a href="LICENSE.md">
    <img src="https://img.shields.io/badge/License-MIT-lightgrey.svg?longCache=true" alt="MIT License">
  </a>
</p>

<div align="center">
  <sub>Forked from <a href="https://github.com/trimstray/test-your-sysadmin-skills">trimstray</a>; Brought back to life and updated by <a href="https://github.com/dfuentes87/linux-sysadmin-questions">dfuentes87</a></sub>
</div>

<br>

****

<br>

:information_source: This project contains almost **200** questions and answers that can be used to test your general knowledge as a **Linux System Administrator**, or to ask someone interviewing for such a position.

These questions are not meant to be a list of arbitrary facts, such as port numbers that you'll maybe deal with once a year, situations or commands that are rarely encountered, or issues specific to a certain application. Instead, these are geared towards real world situations that are common and good to know in general, however not knowing all these do not mean you are not a good Linux SysAdmin.

:heavy_check_mark: The answers are only **examples** and do not exhaust the whole topic. Most of them contains **useful resources** for a deeper understanding.

:warning: Questions marked **`***`** don't have answer yet or answer the is incomplete - **make a pull request to add them**!

:traffic_light: If you find something which doesn't make sense, or something doesn't seem right, **please make a pull request** and please add valid and well-reasoned explanations about your changes or comments.

<br>

### Contributing

If you would like to answer questions, or you found an error - fork the repo, add your fixes, and submit a pull request.

#### Using the issue tracker

* Please **do not** use the issue tracker for personal tech support requests.

* Please **do not** derail or troll issues. Keep the discussion on topic and
  respect the opinions of others.

#### Pull requests

When creating a pull request, please heed the following:

* For new answers: try to give an objective, clear, and concise response, including an example if appropriate.
* For changes to answers: explain why you believe the current answer is incorrect and a better response and/or solution.

<br>

****

<br>

## Table of Contents

| <b><u>The type of chapter</u></b>    | <b><u>Short description</u></b> |
| :---         | :---         |
| <b>[General Knowledge](#general-knowledge)</b> ||
| :small_orange_diamond: [Junior SysAdmin](#junior-sysadmin) | Reasonably simple questions based on basic knowledge. |
| :small_orange_diamond: [Proficient SysAdmin](#proficient-sysadmin) | Mid-level questions that you will probably come across during your first 5 years. |
| :small_orange_diamond: [Senior SysAdmin](#senior-sysadmin) | Advanced questions which may be open-ended, require actual experience to<br> fully understand, or are unique scenarios. |
| <b>[Extra Knowledge](#extra-knowledge)</b> ||

<br>

## <a name="general-knowledge">General Knowledge</a>

### :diamond_shape_with_a_dot_inside: <a name="junior-sysadmin">Junior Sysadmin</a>

#### System Questions

<details>
<summary><b>Give some examples of Unix or Linux distributions. Describe what makes them unique.</b></summary>

* Red Hat Enterprise Linux

* AlmaLinux

* Debian

* Ubuntu

* Arch

* Kali

* OpenBSD

**AlmaLinux** is a free and open-source, community-driven enterprise Linux distribution. It is a downstream rebuild of Red Hat Enterprise Linux (RHEL), designed to be binary-compatible with it. AlmaLinux emerged as a replacement for CentOS after its shift to CentOS Stream. Its key strengths are long-term support, enterprise stability, and predictable release cycles.

**Kali Linux** is a Debian-based Linux distribution aimed at advanced Penetration Testing and Security Auditing. Kali contains several hundred tools which are geared towards various information security tasks, such as Penetration Testing, Security research, Computer Forensics and Reverse Engineering.

**OpenBSD** is a security-focused OS which emphasizes adherence to strictly open source licensing, sane initial settings, and excellent documentation for everything. It is known for its superior packet filter firewall and much of the OpenSSH codebase.

Useful resources:

* [List of Linux distributions](https://en.wikipedia.org/wiki/List_of_Linux_distributions)
* [Distro Watch](https://distrowatch.com/)

</details>

<details>
<summary><b>In SQL, what is a Primary key? What implicit constraint does it have?</b></summary>

A primary key is a combination of fields which uniquely specify a row. A Unique key constraint uniquely identified each record in the database. This provides uniqueness for the column or set of columns. This is a special kind of unique key, and it has implicit NOT NULL constraint. It means, Primary key values cannot be NULL.

</details>

<details>
<summary><b>What is BASH?</b></summary>

A command-line interface for interacting with the operating system. It allows users to execute commands, manage files, and perform a variety of other tasks including scripting.
It is the default shell on most Linux distributions

Useful resources:

* [Comparison of command shells](https://en.wikipedia.org/wiki/Comparison_of_command_shells)

</details>

<details>
<summary><b>How do you get help on the command line?</b></summary><br>

* `man` [commandname] can be used to see a description of a command (ex.: `man less`, `man cat`)

* `-h` or `--help` some programs will implement printing instructions when passed this parameter (ex.: `python -h` and `python --help`)

</details>

<details>
<summary><b>What do the fields in <code>ls -al</code> output mean?</b></summary><br>

In the order of output:

```bash
-rwxrw-r--    1    root   root 2048    Jan 13 07:11 db.dump
```

* file permissions,
* number of links,
* owner name,
* owner group,
* file size,
* time of last modification,
* file/directory name

File permissions is displayed as following:

* first character is `-` or `l` or `d`, `d` indicates a directory, a `-` represents a file, `l` is a symlink (or soft link) - special type of file
* three sets of characters, three times, indicating permissions for owner, group and other:
  * `r` = readable
  * `w` = writable
  * `x` = executable

In your example `-rwxrw-r--`, this means the line displayed is:

* a regular file (displayed as `-`)
* readable, writable and executable by owner (`rwx`)
* readable, writable, but not executable by group (`rw-`)
* readable but not writable or executable by other (`r--`)

Useful resources:

* [What do the fields in ls -al output mean? (original)](https://unix.stackexchange.com/questions/103114/what-do-the-fields-in-ls-al-output-mean)

</details>

<details>
<summary><b>In SQL, how do you restrict your query to a certain number of rows, aside from using specific <code>where</code> clauses?</b></summary>

You can use "LIMIT" which limits the number of rows returned:

<code>SELECT column_name(s) FROM table_name LIMIT number_of_rows;</code>

</details>

<details>
<summary><b>What is the advantage of executing a process in the background? How can you do that?</b></summary><br>

The advantage of executing processes in the background is that you can do any other task simultaneously. You can do this by adding the special character `&` at the end of the command.

Generally applications that take too long to execute and doesn't require user interaction are sent to background so that we can continue our work in terminal.

For example if you want to download something in background, you can:

```bash
wget https://url-to-download.com/download.tar.gz &
```

When you run the above command you get the following output:

```bash
[1] 2203
```

Here 1 is the serial number of job and 2203 is PID of the job.

You can see the jobs running in background using the following command:

```bash
jobs
```

When you execute job in background it give you a PID of job, you can kill the job running in background using the following command:

```bash
kill PID
```

Replace the PID with the PID of the job. If you have only one job running you can bring it to foreground using:

```bash
fg
```

If you have multiple jobs running in background you can bring any job in foreground using:

```bash
fg %#
```

Replace the `#` with serial number of the job.

Useful resources:

* [How do I run a Unix process in the background?](https://kb.iu.edu/d/afnz)
* [Job Control Commands](http://tldp.org/LDP/abs/html/x9644.html)
* [What is/are the advantage(s) of running applications in background?](https://unix.stackexchange.com/questions/162186/what-is-are-the-advantages-of-running-applications-in-backgound)

</details>

<details>
<summary><b>How can you reduce load time of a dynamic website?</b></summary><br>

* website optimization
* compressed files
* Apache/Nginx tuning
* server-side "caching" (Squid, Varnish, Redis)
* external caching (e.g. Cloudflare)

</details>

<details>
<summary><b>Is running processes as root a good or bad practice?</b></summary><br>

Running (everything) as root is bad practice because:

* Nothing prevents you from making a careless mistake. If you try to change the system in any potentially harmful way, you need to use sudo, which ensures a pause (while you're entering the password) to ensure that you aren't about to make a mistake.

* Processes running as root have unrestricted access to the system's resources. It can make changes to anything and if
the process is exploited or hacked, that 3rd party will have root by proxy.

Useful resources:

* [Why is it bad to log in as root? (original)](https://askubuntu.com/questions/16178/why-is-it-bad-to-log-in-as-root)
* [What's wrong with always being root?](https://serverfault.com/questions/57962/whats-wrong-with-always-being-root)

</details>

<details>
<summary><b>How can you check memory and CPU resource usage?</b></summary><br>

* **top:** This command displays a real-time view of the system's processes, including their CPU usage and memory consumption. The output is updated every few seconds and can be sorted by various parameters, such as process ID, CPU usage, or memory usage.
* **ps:** This command displays a snapshot of the current processes running on the system, along with their process ID (PID), CPU usage, and memory usage. The ps command can be combined with other Unix commands, such as grep, to filter the output and show only processes that meet certain criteria.
* **vmstat:** This command displays system statistics, including CPU usage, memory usage, and I/O activity. The vmstat command provides a summary of system resource usage since the last reboot, as well as real-time updates on resource usage.
* **free:** This command displays information about the system's memory usage, including the total amount of memory, the amount of memory used, and the amount of memory available. The free command can be used to check if the system is running low on memory and if any memory-intensive processes need to be optimized or terminated.

Useful resources:

* [How do I Find Out Linux CPU Utilization?](https://www.cyberciti.biz/tips/how-do-i-find-out-linux-cpu-utilization.html)

</details>

<details>
<summary><b>What is load average?</b></summary><br>

Linux **load averages** are "system load averages" that show the running thread (task) demand on the system as an average number of running plus waiting threads. This measures demand, which can be greater than what the system is currently processing. Most tools show three averages, for 1, 5, and 15 minutes.

These 3 numbers are not the numbers for the different CPUs. These numbers are mean values of the load number for a given period of time (of the last 1, 5 and 15 minutes).

**Load average** is usually described as "average length of run queue". So few CPU-consuming processes or threads can raise **load average** above 1. There is no problem if **load average** is less than total number of CPU cores. But if it gets higher than number of CPUs, this means some threads/processes will stay in queue, ready to run, but waiting for free CPU.

It is meant to give you an idea of the state of the system, averaged over several periods of time. Since it is averaged, it takes time for it to go back to 0 after a heavy load was placed on the system.

Some interpretations:

* if the averages are 0.0, then your system is idle
* if the 1-minute average is higher than the 5 or 15 minute averages, then load is increasing
* if the 1-minute average is lower than the 5 or 15 minute averages, then load is decreasing
* if they are higher than your CPU count, then you _might_ have a performance problem

Useful resources:

* [Linux Load Averages: Solving the Mystery (original)](http://www.brendangregg.com/blog/2017-08-08/linux-load-averages.html)
* [How CPU load averages work (and using them to triage webserver performance!)](https://jvns.ca/blog/2016/02/07/cpu-load-averages/)

</details>

<details>
<summary><b>Where are user passwords stored on Linux/Unix systems?</b></summary><br>

The passwords are not stored anywhere on the system at all. What is stored in `/etc/shadow` are so-called hashes of the passwords.

A hash of some text is created by performing a so-called one way function on the text (password), thus creating a string to check against. By design, it is "impossible" (computationally infeasible) to reverse that process.

Older Unix variants stored the encrypted passwords in `/etc/passwd` along with other information about each account.

Newer ones simply have a `*` in the relevant field in `/etc/passwd` and use `/etc/shadow` to store the password, in part to ensure nobody gets read access to the passwords when they only need the other stuff (`shadow` is usually protected more strongly than `passwd`).

For more info consult `man crypt`, `man shadow`, `man passwd`.

Useful resources:

* [Where is my password stored on Linux?](https://security.stackexchange.com/questions/37050/where-is-my-password-stored-on-linux)
* [Where are the passwords of the users located in Linux?](https://www.cyberciti.biz/faq/where-are-the-passwords-of-the-users-located-in-linux/)
* [Linux Password & Shadow File Formats](https://www.tldp.org/LDP/lame/LAME/linux-admin-made-easy/shadow-file-formats.html)

</details>

<details>
<summary><b>You type <code>CTRL + C</code> but your script still running. How do you stop it?</b></summary><br>

Use the kill command to terminate the script: First, find the process ID (PID) of the running script using the ps command. Once you have the PID, you can use the kill command to send a termination signal to the process.

Useful resources:

* [How to kill a script running in terminal, without closing terminal (Ctrl + C doesn't work)? (original)](https://askubuntu.com/questions/520107/how-to-kill-a-script-running-in-terminal-without-closing-terminal-ctrl-c-doe)
* [What's the difference between ^C and ^D for Unix/Mac OS X terminal?](https://superuser.com/questions/169051/whats-the-difference-between-c-and-d-for-unix-mac-os-x-terminal)

</details>

<details>
<summary><b>What is <code>grep</code> command? How do you match multiple strings in the same line?</b></summary><br>

The `grep` utilities are a family of Unix tools, including `egrep` and `fgrep`.

`grep` searches file patterns. If you are looking for a specific pattern in the output of another command, `grep` highlights the relevant lines. Use this grep command for searching log files, specific processes, and more.

For match multiple strings:

```bash
grep -E "string1|string2" filename
```

or

```bash
grep -e "string1" -e "string2" filename
```

Useful resources:

* [What is grep, and how do I use it? (original)](https://kb.iu.edu/d/afiy)

</details>

<details>
<summary><b>Explain a few commands to read files without editing them.</b></summary><br>

* `head`: to check the starting of a file.
* `tail`: to check the ending of the file. It is the reverse of head command.
* `cat`: used to view, create, concatenate the files.
* `tac`: same as `cat` but the contents are shown starting from the bottom
* `more`: used to display the text in the terminal window in pager form.
* `less`: used to view the text in the backward direction and also provides single line movement.

Useful resources:

* [5 Commands to View the Content of a File in Linux Command Line](https://linuxhandbook.com/view-file-linux/)

</details>

<details>
<summary><b>Explain the SIGHUP, SIGINT, SIGKILL, and SIGTERM signals.</b></summary><br>

* **SIGHUP** - is sent to a process when its controlling terminal is closed. It was originally designed to notify the process of a serial line drop (a hangup). Many daemons will reload their configuration files and reopen their logfiles instead of exiting when receiving this signal.
* **SIGINT** - is sent to a process by its controlling terminal when a user wishes to interrupt the process. This is typically initiated by pressing `Ctrl+C`, but on some systems, the "delete" character or "break" key can be used.
* **SIGKILL** - is sent to a process to cause it to terminate immediately (kill). In contrast to **SIGTERM** and **SIGINT**, this signal cannot be caught or ignored, and the receiving process cannot perform any clean-up upon receiving this signal.
* **SIGTERM** - is sent to a process to request its termination. Unlike the **SIGKILL** signal, it can be caught and interpreted or ignored by the process. This allows the process to perform nice termination releasing resources and saving state if appropriate. **SIGINT** is nearly identical to **SIGTERM**.

Useful resources:

* [A list of signals and what they mean](https://www-uxsup.csx.cam.ac.uk/courses/moved.Building/signals.pdf)

</details>

<details>
<summary><b>What does <code>kill</code> command do?</b></summary><br>

In Unix and Unix-like operating systems, `kill` is a command used to send a signal to a process. By default, the message sent is the termination signal, which requests that the process exit. But `kill` is something of a misnomer; the signal sent may have nothing to do with process killing.

Useful resources:

* [Mastering the "Kill" Command in Linux](https://www.maketecheasier.com/kill-command-in-linux/)

</details>

<details>
<summary><b>When would you want to use <code>-f</code> for <code>rm</code>?</b></summary><br>

* Removing large numbers of files: If you are trying to delete a large number of files at once, using the -f option can save you time by skipping the confirmation prompt for each file.
* Removing write-protected files: If you have a write-protected file that you need to delete, using the -f option can force its removal without changing its permissions.
* Removing files owned by other users: If you have permission to delete a file, but it is owned by another user, using the -f option can force its removal without prompting for confirmation.

</details>

<details>
<summary><b>How can I chmod files using the <code>find</code> command?</b></summary><br>

You can use the -exec option with the find command to execute the chmod command on each matching file. For example:

<code>find . -name "*.txt" -exec chmod 644 "{}" \;</code>

The <code>\;</code> sequence is used to indicate the end of the command that should be executed on each file. The backslash before the semicolon is used to escape it and prevent the shell from interpreting it as a command terminator.

Useful resources:

* [How to Use the find Command With exec](https://linuxhandbook.com/find-exec-command/)
* [How to Use the Powerful Xargs Command in Linux](https://linuxhandbook.com/xargs-command/)

</details>

<details>
<summary><b>Combine multiple shell commands in one line.</b></summary><br>

If you want to execute each command only if the previous one succeeded, then combine them using the `&&` operator:

```bash
cd /my_folder && rm *.jar && svn co path to repo && mvn compile package install
```

If one of the commands fails, then all other commands following it won't be executed.

If you want to execute all commands regardless of whether the previous ones failed or not, separate them with semicolons:

```bash
cd /my_folder; rm *.jar; svn co path to repo; mvn compile package install
```

In your case, I think you want the first case where execution of the next command depends on the success of the previous one.

You can also put all commands in a script and execute that instead:

```bash
#! /bin/sh
cd /my_folder \
&& rm *.jar \
&& svn co path to repo \
&& mvn compile package install
```

Useful resources:

* [Execute combine multiple linux commands in one line (original)](https://stackoverflow.com/questions/13077241/execute-combine-multiple-linux-commands-in-one-line)

</details>

<details>
<summary><b>What symbolic representation can you pass to <code>chmod</code> to give all users execute access to a file without affecting other permissions?</b></summary><br>

```bash
chmod a+x /path/to/file
```

* `a` - for all users
* `x` - for execution permission
* `r` - for read permission
* `w` - for write permission

Useful resources:

* [How to Set File Permissions Using chmod](https://www.washington.edu/computing/unix/permissions.html)
* [What does "chmod +x your_file_name" do and how do I use it?](https://askubuntu.com/questions/443789/what-does-chmod-x-filename-do-and-how-do-i-use-it)

</details>

<details>
<summary><b>How can you mirror the contents of two directories?</b></summary><br>

To sync the contents of **dir1** to **dir2** on the same system, type:

```bash
rsync -av --progress --delete dir1/ dir2
```

* `-a`, `--archive` - archive mode
* `--delete` - delete extraneous files from dest dirs
* `-v`, `--verbose` - verbose mode (increase verbosity)
* `--progress` - show progress during transfer

Useful resources:

* [How can I sync two local directories? (original](https://unix.stackexchange.com/questions/392536/how-can-i-sync-two-local-directories)
* [Synchronizing folders with rsync](https://www.jveweb.net/en/archives/2010/11/synchronizing-folders-with-rsync.html)

</details>

<details>
<summary><b>Many basic maintenance or troubleshooting tasks require you to edit config files. Explain ways to undo the changes you make.</b></summary><br>

* Manually make a copy of the file by using `cp` or copy the line and comment out the original.
* For more permanent changes, the best solution is to use version control such as git to keep track of changes

Useful resources:

* [Backup file with .bak before filename extension](https://unix.stackexchange.com/questions/66376/backup-file-with-bak-before-filename-extension)
* [Is it a good idea to use git for configuration file version controlling?](https://superuser.com/questions/1037211/is-it-a-good-idea-to-use-git-for-configuration-file-version-controlling)

</details>

<details>
<summary><b>You have to find all files larger than 20MB. How do you do it?</b></summary><br>

```bash
find / -type f -size +20M
```

Useful resources:

* [How can I find files that are bigger/smaller than x bytes?](https://superuser.com/questions/204564/how-can-i-find-files-that-are-bigger-smaller-than-x-bytes)

</details>

<details>
<summary><b>Why do we use <code>sudo su -</code> and not just <code>sudo su</code>?</b></summary><br>

`su` switches the user providing a normal shell with an environment nearly the same as with the user invoking the command.

`su -` invokes a login shell after switching the user. A login shell resets most environment variables, providing a clean base. This is a safer method because it prevents a malicious enviornment from being brought to the new user during the temporary session. It also allows the use of the new enviornment variables.

Useful resources:

* [su vs sudo -s vs sudo -i vs sudo bash](https://unix.stackexchange.com/questions/35338/su-vs-sudo-s-vs-sudo-i-vs-sudo-bash)
* [Why do we use su - and not just su? (original)](https://unix.stackexchange.com/questions/7013/why-do-we-use-su-and-not-just-su)

</details>

<details>
<summary><b>What are the main reasons for keeping old log files?</b></summary><br>

They are essential to investigate issues on the system. **Log management** is absolutely critical for IT security.

Servers, firewalls, and other IT equipment keep log files that record important events and transactions. This information can provide important clues about hostile activity affecting your network from within and without.
Log data can also provide information for identifying and troubleshooting equipment problems including configuration problems and hardware failure.

It’s your server’s record of who has accessed your site or server, when, and exactly what they looked at.

* Origin (IP, location)
* Browser (agent) being used
* Files accessed/modified
* Actions taken

Factors to consider:

* Legal requirements for retention or destruction
* Company policies for retention and destruction
* How long the logs are useful
* What questions you're hoping to answer from the logs
* How much space they take up

By collecting and analyzing logs, you can understand what transpires within your network. Each log file contains many pieces of information that can be invaluable, especially if you know how to read them and analyze them.

Useful resources:

* [How long do you keep log files?](https://serverfault.com/questions/135365/how-long-do-you-keep-log-files)

</details>

<details>
<summary><b>What is an incremental backup?</b></summary><br>

An incremental backup is a type of backup that only copies files that have changed since the previous backup.

Useful resources:

* [What Is Incremental Backup?](https://www.nakivo.com/blog/what-is-incremental-backup/)

</details>

<details>
<summary><b>What is RAID? What is RAID0, RAID1, RAID5, RAID10? </b></summary><br>

A **RAID** (Redundant Array of Inexpensive Disks) is a technology that is used to increase the performance and/or reliability of data storage.

* **RAID0**: Also known as disk **striping**, is a technique that breaks up a file and spreads the data across all the disk drives in a RAID group. There are no safeguards against failure
* **RAID1**: A popular disk subsystem that increases safety by writing the same data on two drives. Called "**mirroring**," RAID 1 does not increase write performance, but read performance may equal up to the sum of each disks' performance. However, if one drive fails, the second drive is used, and the failed drive is manually replaced. After replacement, the RAID controller duplicates the contents of the working drive onto the new one
* **RAID5**: It is disk subsystem that increases safety by computing parity data and increasing speed by interleaving data across three or more drives (**striping**). Upon failure of a single drive, subsequent reads can be calculated from the distributed parity such that no data is lost
* **RAID10**: Also known as **RAID 1+0**, is a RAID configuration that combines disk mirroring and disk striping to protect data. It requires a minimum of four disks, and stripes data across mirrored pairs. As long as one disk in each mirrored pair is functional, data can be retrieved. If two disks in the same mirrored pair fail, all data will be lost because there is no parity in the striped sets

Useful resources:

* [RAID](https://www.prepressure.com/library/technology/raid)

</details>

<details>
<summary><b>Why would you want to mount servers in a rack?</b></summary><br>

* Protecting Hardware
* Proper Cooling
* Organized Workspace
* Better Power Management
* Cleaner Environment

Useful resources:

* [5 Reasons to Rackmount Your PC](https://www.racksolutions.com/news/blog/5-reasons-to-rackmount-pc/)

</details>

#### Network Questions

<details>
<summary><b>Describe the steps for a successful DHCP handshake process.</b></summary><br>

1. Discover - The DHCP client broadcasts a DHCPDISCOVER message on the network subnet using the destination address 255.255.255.255 (limited broadcast) or the specific subnet broadcast address (directed broadcast). A DHCP client may also request its last known IP address.

2. Offer - When a DHCP server receives a DHCPDISCOVER message from a client, the DHCP server reserves an IP address for the client and makes a lease offer by sending a DHCPOFFER message to the client.

3. Request - In response to the DHCP offer, the client replies with a DHCPREQUEST message, broadcast to the server, requesting the offered address. Before claiming an IP address, the client will broadcast an ARP request, in order to find if there is another host present in the network with the proposed IP address. If there is no reply, this address does not conflict with that of another host, so it is free to be used.

4. Acknowledge - The DHCP server sends a DHCPACK packet to the client. This packet includes the lease duration and any other configuration information that the client might have requested. At this point, the IP configuration process is completed.

Useful resources:

* [DHCP Operation](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol#Operation)

</details>

<details>
<summary><b>What are the most important things to understand about the OSI model?</b></summary><br>

The most important things to understand about the **OSI** model are:

* we can divide up protocols into layers
* layers provide encapsulation
* layers provide abstraction
* layers decouple functions from others

Useful resources:

* [OSI Model and Networking Protocols Relationship](https://networkengineering.stackexchange.com/questions/6380/osi-model-and-networking-protocols-relationship)

</details>

<details>
<summary><b>What is the difference between TCP and UDP?</b></summary><br>

| TCP | UDP |
| :--- | :--- |
| TCP stands for Transmission Control Protocol | UDP is stands for User Datagram Protocol or Universal Datagram Protocol |
| Once the connection is setup, data can be sent bi-directional, i.e. TCP is a connection oriented protocol | UDP is connectionless, simple protocol. Using UDP, messages are sent as packets |
| TCP is slower than UDP | UDP is faster compared to TCP |
| TCP is used for applications where time is not critical part of data transmission | UDP is suitable for the applications which require fast transmission of data and time is crucial in this case. |
| TCP transmission occurs in a sequential manner | UDP does not guarantee data is received in the same order when it reaches the destination |
| TCP tracks the data sent to ensure no data loss during data transmission | UDP does not ensure whether receiver receives packets are not. If packets are misses then they are just lost |

</details>

<details>
<summary><b>What is a Proxy Server?</b></summary><br>

A proxy server is a server that acts as an intermediary between clients (such as web browsers) and other servers on the internet.
When a client sends a request to access a resource (such as a website or file) on the internet, the request is first sent to the proxy server, which then forwards the request to the appropriate server. The response from the server is then returned to the proxy server, which in turn sends the response back to the client.

Proxy servers can be used for several purposes, including:

* Improving performance: Proxy servers can cache frequently accessed resources, such as web pages or files, so that subsequent requests can be served faster from the cache instead of retrieving the resource again from the original server.
* Filtering content: Proxy servers can be used to filter content, such as blocking access to certain websites or restricting access to certain types of content based on policy or user preferences.
* Increasing security: Proxy servers can provide an additional layer of security by acting as a gateway between clients and servers, blocking malicious traffic, and providing anonymity for clients by hiding their IP addresses.
* Controlling access: Proxy servers can be used to control access to resources based on policies, such as restricting access to certain resources to specific users or groups.

</details>

<details>
<summary><b>How do you check default route and routing table?</b></summary><br>

Using the commands `netstat -nr`, `route -n` or `ip route show` we can see the default route and routing tables.

</details>

<details>
<summary><b>What are 127.0.0.1 and localhost?</b></summary><br>

127.0.0.1 is the loopback connection on your network interface card (NIC); pinging this address will see if it is responding. If the ping is successful, then the hardware is good. If the ping isn't successful, the NIC may have issues.

127.0.0.1 and localhost mean the same thing in most cases, but can be treated differently in some situations. The main difference is that you still have to do an actual lookup of localhost somewhere. If you use `127.0.0.1`, the request is directly against the IP address. Otherwise, the name has to be resolved.

Useful resources:

* [What is the difference between 127.0.0.1 and localhost?](https://stackoverflow.com/questions/7382602/what-is-the-difference-between-127-0-0-1-and-localhost)
* [localhost vs. 127.0.0.1](https://stackoverflow.com/questions/3715925/localhost-vs-127-0-0-1)

</details>

<details>
<summary><b>Server A can't talk to Server B. Describe possible reasons in a few steps.</b></summary><br>

To troubleshoot communication problems between servers, it is better to ideally follow the TCP/IP stack:

1. **Application Layer**: are the services up and running on both servers? Are they correctly configured (e.g. bind the correct IP and correct port)? Do application and system logs show meaningful errors?

2. **Transport Layer**: are the ports used by the application open? Is it possible to ping the server?

3. **Network Layer**: is there a firewall on the network or on the OS correctly configured? Is the IP stack correctly configured (IP, routes, dns, etc.)? Are switches and routers working (check the ARP table!)?

4. **Physical Layer**: are the servers connected to a network? Are packets being lost?

</details>

<details>
<summary><b>How can you resolve a domain name, using external dns, with CLI? Can IPs be resolved to domain names?</b></summary><br>

Examples to a resolve an IP address from a domain name:

```bash
# with host command:
host domain.com 8.8.8.8

# with dig command:
dig @1.1.1.1 google.com

# with nslookup command:
nslookup domain.com 8.8.8.8
```

You can resolve an IP Address back to a hostname if the IP Address is stored in a **PTR** DNS record.

```bash
dig -x 1.2.3.4
```

To look up the IPv6 address for a host:

```bash
dig AAAA domain.com
```

Useful resources:

* [How can I resolve a hostname to an IP address in a Bash script?](https://unix.stackexchange.com/questions/20784/how-can-i-resolve-a-hostname-to-an-ip-address-in-a-bash-script)
* [How To Resolve IP Addresses To Domain Names?](https://superuser.com/questions/315687/how-to-resolve-ip-addresses-to-domain-names)

</details>

<details>
<summary><b>How do you test port connectivity with <code>nc</code>?</b></summary><br>

```bash
# with nc (netcat) command:
nc -vz code42.example.com 5432
```

</details>

<details>
<summary><b>What are the ports used for FTP and SFTP, and how is each used?</b></summary><br>

FTP uses two ports: port 21 for control commands and port 20 for data transfers. The control connection is used to send commands such as login credentials and directory listings, while the data connection is used to transfer the actual files.

SFTP, on the other hand, uses a single port for both control commands and data transfers: port 22. SFTP is a secure file transfer protocol that uses SSH (Secure Shell) to encrypt all data in transit. This makes SFTP more secure than FTP and suitable for transferring sensitive data.

</details>

<details>
<summary><b>What is the difference between Hub, Switch, and Router?</b></summary><br>

A hub is the simplest of the three devices, and it operates at the physical layer of the OSI model. A hub connects multiple devices on a network, and it sends all incoming data to every device on the network. This means that any device connected to the hub can receive data sent by any other device, but it also means that data collisions can occur if multiple devices try to send data at the same time. Hubs are not commonly used in modern networks due to their limited functionality and lack of security features.

A switch is a more advanced device that operates at the data link layer of the OSI model. Like a hub, a switch connects multiple devices on a network, but it is capable of selectively sending data to only the device for which it is intended. This means that data collisions are less likely to occur, and the network can operate more efficiently. Switches are commonly used in modern networks and are essential for creating local area networks (LANs).

A router is a device that operates at the network layer of the OSI model. A router connects multiple networks, such as LANs or wide area networks (WANs), and it is capable of directing traffic between them. Routers use routing tables to determine the most efficient path for data to take between networks. They can also provide security features such as firewalls, which filter incoming and outgoing traffic to protect the network from attacks.

</details>

<details>
<summary><b>What is SSH and how does it work?</b></summary><br>

**SSH** stands for **Secure Shell**. It is a protocol that lets you access another machine through a shell session.

An **SSH** connection to be established, the remote machine (server A) must be running an **SSH** daemon and the user's computer must have an **SSH** client.

The **SSH** daemon and **SSH** client listen for connections on a specific network port (default 22), authenticates connection requests, and spawns the appropriate environment if the user provides the correct credentials.

Useful resources:

* [Understanding the SSH Encryption and Connection Process](https://www.digitalocean.com/community/tutorials/understanding-the-ssh-encryption-and-connection-process)

</details>

<details>
<summary><b>What are IP classes? How are they different from CIDR (classless)?</b></summary><br>

The classful IP addressing system was an early method that divided the IPv4 address space into specific classes based on the leading bits of an address.

CIDR was introduced to improve the scalability of IP addressing and overcome the limitations of the classful system, especially given the rapid growth of the internet.
CIDR doesn't rely on fixed classes. Instead, it allows for flexible division of IP space.

</details>

<details>
<summary><b>Explain the function of each of the following DNS records: SOA, PTR, A, MX, and CNAME.</b></summary><br>

**DNS records** are basically mapping files that tell the DNS server which IP address each domain is associated with, and how to handle requests sent to each domain. Some **DNS records** syntax that are commonly used in nearly all DNS record configurations are `A`, `AAAA`, `CNAME`, `MX`, `PTR`, `NS`, and `TXT`.

* **A** - Address Mapping records
* **AAAA** - IP Version 6 Address records
* **CNAME** - Canonical Name records
* **MX** - Mail exchanger record
* **NS** - Name Server records
* **PTR** - Reverse-lookup Pointer records

Useful resources:

* [List of DNS record types](https://en.wikipedia.org/wiki/List_of_DNS_record_types)

</details>

<details>
<summary><b>What is a MAC address and how is it determined?</b></summary><br>

A Media Access Control (MAC) address is a unique identifier assigned to a network interface controller (NIC) for use as a network address in communications within a network segment. It is used to uniquely identify devices on a network at the data link layer of the networking stack.

MAC addresses are typically assigned by the manufacturer of the network interface card and are stored in its hardware. The MAC address is a 48-bit number (12 hexadecimal digits) that is globally unique and permanently assigned to the NIC by the manufacturer. The first half of the MAC address represents the vendor, while the second half represents the device itself.

MAC addresses are used in various network protocols to identify the source and destination of network traffic. They are also used in security protocols, such as MAC filtering, to restrict network access based on the MAC address of a device.

* [How is the MAC address on a computer determined?](https://superuser.com/questions/504770/how-is-the-mac-address-on-a-computer-determined)

</details>

<details>
<summary><b>What is the smallest IPv4 subnet that can be applied to a network containing up to 200 devices?</b></summary><br>

The smallest IPv4 subnet that can be applied to a network containing up to 200 devices is /24 or 255.255.255.0. This allows for a maximum of 254 usable IP addresses on the network (excluding the network address and broadcast address), which is sufficient for a network with 200 devices.

Useful resources:

* [How do you calculate the prefix, network, subnet, and host numbers?](https://networkengineering.stackexchange.com/questions/7106/how-do-you-calculate-the-prefix-network-subnet-and-host-numbers)
* [The slash after an IP Address - CIDR Notation](https://networkengineering.stackexchange.com/questions/3697/the-slash-after-an-ip-address-cidr-notation)
* [IP Calculator](http://jodies.de/ipcalc)

</details>

<details>
<summary><b>What are some common HTTP status codes?</b></summary><br>

* **1xx** - Informational responses - communicates transfer protocol-level information
* **2xx** - Success - indicates that the client’s request was accepted successfully
* **3xx** - Redirection - indicates that the client must take some additional action in order to complete their request
* **4xx** - Client side error - this category of error status codes points the finger at clients
* **5xx** - Server side error - the server takes responsibility for these error status codes

Useful resources:

* [HTTP Status Codes](https://httpstatuses.com/)

</details>

#### DevOps Questions

<details>
<summary><b>What is DevOps?</b></summary><br>

**DevOps** is a cohesive team that engages in both Development and Operations tasks, or its individual Operations and Development teams that work very closely together. It's more of a "way" of working collaboratively with other departments to achieve common goals.

</details>

<details>
<summary><b>What is a version control? What are atomic commits?</b></summary><br>

It is a system that records changes to a file or set of files over time so that you can recall specific versions later. Version control systems consist of a central shared repository where teammates can commit changes to a file or set of file. Then you can mention the uses of version control.

Version control allows you to:

* Track Changes: Every change, along with its author and a descriptive message, is recorded. This aids in understanding the evolution of a project.
* Collaboration: Multiple developers can work on the same project simultaneously without overwriting each other's changes. The version control system assists in merging concurrent modifications.
* Backup and Restore: All changes and historical versions of files are stored. If mistakes are made, it's easy to revert back to a previous state.
* Branching and Merging: Developers can create branches to isolate feature development or experimental changes, then merge these branches back into the main project line once the changes are stable.
* Accountability: By logging every change with its associated author, it's clear who made each change, ensuring accountability.

Atomic commits are about making small, focused changes that can be easily understood and, if necessary, independently reverted. This practice promotes better code history, simplifies debugging, and improves collaboration.

* Single Purpose: Each commit should address a single, clear objective. For example, fixing one bug or adding one feature.
* Consistency: An atomic commit should never leave the codebase in a broken state. If a commit is applied, the system should still function correctly. If it's reverted, the system should revert to its previous working state without any residual side effects.
* Comprehensibility: Atomic commits make the history more understandable. When reviewing history, it's easier to understand and reason about changes when each commit represents a single, isolated piece of work.
* Ease of Reversion: If a specific change introduces an issue, atomic commits make it easier to revert just that change without affecting other unrelated changes.

Useful resources:

* [Getting Started - About Version Control (original)](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)

</details>

<details>
<summary><b>Explain some basic <code>git</code> commands.</b></summary><br>

* `git init` - create a new local repository
* `git commit -m "message"` - commit changes to head
* `git status` - list the files you've added with `git add` and also commit any files you've changed since then
* `git push origin master` - send changes to the master branch of your remote repository

</details>

<details>
<summary><b>Explain a simple Continuous Integration pipeline.</b></summary><br>

* clone repository
* deploy stage (QA)
* testing environment (QA)
* deploy stage (PROD)

</details>

<details>
<summary><b>Explain some basic Docker commands.</b></summary><br>

* `docker ps` - show running containers
* `docker ps -a` - show all containers
* `docker images` - show docker images
* `docker logs <container-id|container-name>` - get logs from container
* `docker network ls` - show all docker networks
* `docker volumes ls` - show all docker volumes
* `docker exec -it <container-id|container-name> bash` - execute bash in container with interactive shell

</details>

#### Cybersecurity Questions

<details>
<summary><b>What makes a password very strong?</b></summary><br>

Password length is more important than complexity when it comes to creating a strong password.

A password that is long and complex can be difficult to remember, and users may be more likely to write it down or reuse it across multiple accounts, which can increase the risk of a security breach. In contrast, a longer password that is easy to remember but not easily guessable can provide strong security.

It is generally recommended to use a password that is at least 16 characters long, and that does not contain easily guessable information such as names, birthdays, or common phrases. It is also important to use unique passwords for each account to prevent a security breach from affecting multiple accounts. To help remember long passwords, users can use password managers, which securely store passwords and generate random, complex passwords for each account.

Useful resources:

* [Password Strength](https://xkcd.com/936/)
* [Short complex password, or long dictionary passphrase?](https://security.stackexchange.com/questions/6095/xkcd-936-short-complex-password-or-long-dictionary-passphrase)

</details>

<details>
<summary><b>What is a Security Misconfiguration?</b></summary><br>

**Security misconfiguration** is a vulnerability when a device/application/network is configured in a way which can be exploited by an attacker to take advantage of it. This can be as simple as leaving the default username/password unchanged or too simple for device accounts etc.

</details>

<details>
<summary><b>Most tutorials suggest using SSH key authentication rather than password authentication. Why is it considered more secure?</b></summary><br>

An **SSH key** is an access credential in the SSH protocol. Its function is similar to that of usernames and passwords, but the keys are primarily used for automated processes and for implementing single sign-on by system administrators and power users.

Instead of requiring a user's password, it is possible to confirm the client's identity by using asymmetric cryptography algorithms, with public and private keys.

If your SSH service only allows public-key authentication, an attacker needs a copy of a private key corresponding to a public key stored on the server.

If your SSH service allows password based authentication, then your Internet connected SSH server will be hammered day and night by bot-nets trying to guess user-names and passwords. The bot net needs no information, it can just try popular names and popular passwords. Apart from anything else this clogs your logs.

Useful resources:

* [Key-Based Authentication (Public Key Authentication)](http://www.crypto-it.net/eng/tools/key-based-authentication.html)
* [SSH password vs. key authentication](https://security.stackexchange.com/questions/33381/ssh-password-vs-key-authentication)

</details>

<details>
<summary><b>Define the three major terms in cybersecurity (Confidentiality, Integrity, and Availability).</b></summary><br>

Confidentiality, integrity, and availability are three fundamental principles of information security and cybersecurity. They are commonly referred to as the CIA triad.

* Confidentiality: Confidentiality is the principle that ensures that information is only accessible to authorized individuals or entities. It involves protecting sensitive information from unauthorized access, disclosure, or theft. Confidentiality is often achieved through the use of encryption, access controls, and other security measures.
* Integrity: Integrity is the principle that ensures that information is accurate, complete, and trustworthy. It involves protecting information from unauthorized modification or destruction, and ensuring that it remains consistent and reliable over time. Integrity is often achieved through the use of data backups, checksums, and other data validation techniques.
* Availability: Availability is the principle that ensures that information and resources are accessible to authorized individuals or entities when needed. It involves ensuring that systems and applications are always operational and that resources are available to support business operations. Availability is often achieved through the use of redundancy, disaster recovery, and backup systems.

Together, confidentiality, integrity, and availability provide a framework for securing information and systems against a wide range of threats.

Useful resources:

* [Confidentiality, Integrity, and Availability: The CIA Triad](https://informationsecurity.wustl.edu/items/confidentiality-integrity-and-availability-the-cia-triad/)

</details>

<details>
<summary><b>What is the difference between threats, vulnerabilities, and attacks?</b></summary><br>

A threat is a potential danger that could exploit a vulnerability in a system or application. Threats can come in various forms, including natural disasters, human errors, or malicious attacks.

A vulnerability is a weakness or flaw in a system or application that can be exploited by a threat. Vulnerabilities can be caused by software bugs, misconfigurations, or human error, among other things.

An attack is an intentional action that is taken to exploit a vulnerability in a system or application. An attack can be carried out by a human, a bot, or a malware, and can have various objectives, such as stealing data, disrupting service, or gaining unauthorized access.

To illustrate the differences between these concepts, consider the example of a bank's online banking system. The system may have a vulnerability, such as a weak password policy, which can be exploited by a threat, such as a hacker. The hacker may launch an attack, such as a brute force attack, to try to guess users' passwords and gain unauthorized access to their accounts.

</details>

<details>
<summary><b>Describe Threat Modeling.</b></summary><br>

Threat modeling is a process that is used to identify, prioritize, and mitigate potential security threats to a system or application. It is a systematic approach to analyzing potential threats and vulnerabilities in order to identify the most effective strategies for mitigating those risks.

The process of threat modeling typically involves several steps, including:

* Defining the scope of the model: This involves identifying the system or application to be analyzed, as well as any external dependencies or interfaces that may be relevant to the analysis.
* Creating a data flow diagram: This diagram is used to identify the data flows within the system or application, as well as any entry points and exit points where data can enter or leave the system.
* Identifying potential threats: This involves brainstorming potential threats that could affect the system or application, such as malware, data breaches, or social engineering attacks.
* Analyzing the risks: This step involves assessing the potential impact and likelihood of each identified threat, and prioritizing them based on their risk level.
* Mitigating the risks: Once the risks have been prioritized, strategies can be developed to mitigate those risks. This may involve implementing technical controls, such as firewalls or encryption, or non-technical controls, such as training or policies and procedures.
* Re-evaluating the model: Threat modeling is an ongoing process, and it is important to periodically re-evaluate the model to ensure that it is up-to-date and effective.

</details>

<br>

### :diamond_shape_with_a_dot_inside: <a name="proficient-sysadmin">Proficient Sysadmin</a>

#### System Questions

<details>
<summary><b>Explain briefly how Linux allows most of its software to be updated without needing to reboot? Is it possible to update the kernel without rebooting?</b></summary><br>

* Shared Libraries: Linux uses shared libraries (.so files) extensively. When software is updated, new versions of shared libraries are typically placed alongside the old ones. Running applications will continue to use the old libraries they were started with until they are restarted. New or restarted applications will use the updated libraries.
* Process Management: In Linux, you can restart individual services or processes without affecting others. So, if you update a service, you generally only need to restart that specific service to start using the updated version, rather than rebooting the entire system.
* File System Implementation: Linux file systems allow files to be replaced even while they're being used by the system. When a file is replaced (or deleted), any process that still has the file open continues to see the old version until it closes the file. New accesses to the file see the new version. This is possible because the inode of the file (data structure storing file metadata) remains valid as long as there are references to it, even if the directory entry is removed or replaced.

Traditionally, updating the Linux kernel required a reboot to switch to the new kernel. However, there are methods and technologies developed to enable live kernel patching, which allows kernel updates without rebooting:

* kpatch: A tool developed by Red Hat, kpatch allows you to patch a Linux kernel without rebooting the system. It works by building dynamic kernel modules that can replace existing code in the running kernel.
* kGraft: Developed by SUSE, kGraft is another approach to live kernel patching. Like kpatch, it allows for real-time patching of a running kernel.
* KernelCare: This is a commercial solution that offers rebootless kernel updates. It's automated and works with various Linux distributions.
* Livepatch: Offered by Canonical for Ubuntu, Livepatch provides kernel updates without the need for a reboot.

Useful resources:

* [How does Linux update without a reboot? - Quora](https://www.quora.com/How-does-Linux-update-without-a-reboot)

</details>

<details>
<summary><b>Difference between <code>nohup</code>, <code>disown</code>, and <code>&</code>. What happens when using all together?</b></summary><br>

* `&` puts the job in the background, that is, makes it block on attempting to read input, and makes the shell not wait for its completion
* `disown` removes the process from the shell's job control, but it still leaves it connected to the terminal. One of the results is that the shell won't send it a **SIGHUP**. Obviously, it can only be applied to background jobs, because you cannot enter it when a foreground job is running
* `nohup` disconnects the process from the terminal, redirects its output to `nohup.out` and shields it from **SIGHUP**. One of the effects (the naming one) is that the process won't receive any sent **SIGHUP**. It is completely independent of job control and could in principle be used also for foreground jobs (although that's not very useful)

If you use all three together, the process is running in the background, is removed from the shell's job control and is effectively disconnected from the terminal.

Useful resources:

* [Difference between nohup, disown and & (original)](https://unix.stackexchange.com/questions/3886/difference-between-nohup-disown-and)

</details>

<details>
<summary><b>Pick two different computer languages. Describe when you would use one over the other.</b></summary><br>

Python is a high-level, interpreted language that is known for its simplicity, ease of use, and flexibility. It is commonly used for data science, machine learning, web development, scripting, and automation tasks. Python has a large and active community that creates and maintains numerous libraries and frameworks, making it an excellent choice for rapid prototyping, experimentation, and development of proof-of-concept applications.

C++ is a lower-level, compiled language that is known for its speed, efficiency, and power. It is commonly used for systems programming, operating systems, embedded systems, games, and other applications that require high performance, low-level control, and minimal runtime overhead. C++ allows for greater memory control and more efficient use of system resources, making it a better choice for applications that require high levels of optimization.

When deciding between Python and C++, it's important to consider the requirements and constraints of the project at hand. If the project requires high-level abstraction and rapid development, Python may be the better choice. However, if the project requires fine-tuned control over system resources and high-performance execution, C++ may be a better option. Ultimately, the choice of language will depend on the specific requirements of the project and the skills and preferences of the development team.

</details>

<details>
<summary><b>Why is the <code>mktemp</code> command useful? Present an example of use.</b></summary><br>

<code>mktemp</code> randomizes the name. It is very important from the security point of view.

Just imagine that you do something like:

```bash
echo "random_string" > /tmp/temp-file
```

in your root-running script. And someone (who has read your script) does

```bash
ln -s /etc/passwd /tmp/temp-file
```

The <code>mktemp</code> command could help you in this situation:

```bash
TEMP=$(mktemp /tmp/temp-file.XXXXXXXX)
echo "random_string" > ${TEMP}
```

Now this <code>ln /etc/passwd</code> attack will not work.

</details>

<details>
<summary><b>In what circumstance can <code>df</code> and <code>du</code> disagree on available disk space? How do you solve it?</b></summary><br>

`du` checks usage of directories, but `df` checks free'd inodes, and files can be held open and take space after they're deleted.

**Solution 1**

Check for files on located under mount points. Frequently if you mount a directory (say a sambafs) onto a filesystem that already had a file or directories under it, you lose the ability to see those files, but they're still consuming space on the underlying disk.

I've had file copies while in single user mode dump files into directories that I couldn't see except in single usermode (due to other directory systems being mounted on top of them).

**Solution 2**

On the other hand `df -h` and `du -sh` could disagree by about 50% of the hard disk size. This was caused by e.g. Apache (httpd) keeping large log files in memory which had been deleted from disk.

This was tracked down by running `lsof | grep "/var" | grep deleted` where `/var` was the partition I needed to clean up.

The output showed lines like this:

```plaintext
httpd     32617    nobody  106w      REG        9,4 1835222944     688166 /var/log/apache/awstats_log (deleted)
```

The situation was then resolved by restarting Apache (`service httpd restart`) and cleared of disk space, by allowing the locks on deleted files to be cleared.

Useful resources:

* [Why du and df display different values in Linux and Unix](https://linuxshellaccount.blogspot.com/2008/12/why-du-and-df-display-different-values.html)

</details>

<details>
<summary><b>Every command fails with <code>command not found</code>. How can you trace the source of the error and resolve it?</b></summary><br>

It looks that at one point or another are overwriting the default `PATH` environment variable. The type of errors you have, indicates that `PATH` does not contain e.g. `/bin`, where the commands (including bash) reside.

One way to begin debugging your bash script or command would be to start a subshell with the `-x` option:

```bash
bash --login -x
```

This will show you every command, and its arguments, which is executed when starting that shell.

Also very helpful is show `PATH` variable values:

```bash
echo $PATH
```

If you run this:

```bash
PATH=/bin:/sbin:/usr/bin:/usr/sbin
```

most commands should start working - and then you can edit `~/.bash_profile` instead of `~/.bashrc` and fix whatever is resetting `PATH` there. Default `PATH` variable values for **root** and other users is in `/etc/profile` file.

Useful resource:

* [How to correctly add a path to PATH?](https://unix.stackexchange.com/questions/26047/how-to-correctly-add-a-path-to-path)

</details>

<details>
<summary><b>How are different production enviornments used and why?</b></summary><br>

In software development, different production environments are used to facilitate the deployment, testing, and running of an application in a way that is specific to the stage of development and the purpose of that environment.

There are typically three different production environments: development, testing, and production.

Development environment: This is where the application is developed and tested by developers. It's usually a local environment, but it can also be a shared environment that is used by multiple developers.
Testing environment: This is where the application is tested by QA (quality assurance) team to ensure that it works as expected before it is released to production. The testing environment should mimic the production environment as much as possible.
Production environment: This is where the application is deployed for the end-users. It's a live environment that is publicly accessible. Any changes or updates that are made to the application should be thoroughly tested in the testing environment before being deployed to production to ensure that the application remains stable and secure.

</details>

<details>
<summary><b>Provide a general explanation of how SSL works.</b></summary><br>

SSL (Secure Sockets Layer) is a protocol used to establish a secure and encrypted communication between a client and a server over the internet. It was replaced by TLS (Transport Layer Security), but the term SSL is still often used.

When a client (such as a web browser) initiates an SSL connection to a server, the following process takes place:

1. The client sends a request to the server to initiate an SSL connection.
2. The server responds with its SSL certificate, which contains a public key and other information about the certificate holder.
3. The client verifies the certificate's validity by checking it against a list of trusted root certificates installed on the client's device.
4. The client generates a session key, encrypts it using the server's public key, and sends it to the server.
5. The server decrypts the session key using its private key.
6. The client and server use the session key to encrypt and decrypt data exchanged during the session.

</details>

<details>
<summary><b>Explain in a few points the boot process of the Linux system.</b></summary><br>

**BIOS**: Full form of BIOS is Basic Input or Output System that performs integrity checks, and it will search and load, and then it will execute the bootloader.

**Bootloader**: Since the earlier phases are not specific to the operating system, the BIOS-based boot process for x86 and x86-64 architectures is considered to start when the master boot record (MBR) code is executed in real mode and the first-stage bootloader is loaded. In UEFI systems, a payload, such as the Linux kernel, can be executed directly. Therefore, no bootloader is necessary. Some popular bootloaders: **GRUB**, **Syslinux/Isolinux** or **Lilo**.

**Kernel**: The kernel in Linux handles all operating system processes, such as memory management, task scheduling, I/O, interprocess communication, and overall system control. This is loaded in two stages - in the first stage, the kernel (as a compressed image file) is loaded into memory and decompressed, and a few fundamental functions such as basic memory management are set up.

**Init**: Is the parent of all processes on the system, it is executed by the kernel and is responsible for starting all other processes.

* `SysV init` - init's job is to get everything running the way it should be once the kernel is fully running. Essentially it establishes and operates the entire user space. This includes checking and mounting file systems, starting up necessary user services, and ultimately switching to a user-environment when system startup is completed.
* `systemd` - the developers of systemd aimed to replace the Linux init system inherited from Unix System V. Like init, systemd is a daemon that manages other daemons. All daemons, including systemd, are background processes. Systemd is the first daemon to start (during booting) and the last daemon to terminate (during shutdown).
* `runinit` - runinit is an init scheme for Unix-like operating systems that initializes, supervises, and ends processes throughout the operating system. It is a reimplementation of the daemontools process supervision toolkit that runs on the Linux, Mac OS X, \*BSD, and Solaris operating systems.

Useful resources:

* [Analyzing the Linux boot process](https://opensource.com/article/18/1/analyzing-linux-boot-process)
* [systemd Boot Process](https://insujang.github.io/2018-11-22/systemd-boot-process/)

</details>

<details>
<summary><b>What is SELinux and how does it work?</b></summary><br>

SELinux, or Security-Enhanced Linux, is a security module for the Linux kernel that provides access control mechanisms to enforce mandatory access control policies. It works by labeling resources such as files, directories, processes, and network sockets with security context labels.

SELinux uses a set of rules called policies that determine what actions are allowed or denied for each labeled resource based on the security context of the process trying to access it. The policies are defined in a policy language and can be modified or extended to suit specific security requirements.

SELinux provides a more fine-grained level of access control than traditional Linux file permissions, which are based on user and group ownership. It is designed to provide a more secure environment by preventing applications or processes from accessing resources they do not have permission to access, even if the underlying Linux file permissions allow it.

SELinux operates on a set of modes, which include enforcing mode, permissive mode, and disabled mode. In enforcing mode, SELinux denies access to any resource that violates the security policy. In permissive mode, it only logs violations without actually enforcing them, which is useful for debugging policy issues. In disabled mode, SELinux is turned off completely.

</details>

<details>
<summary><b>Is 1.00 CPU load on a four-core processor a bad thing?</b></summary><br>

It depends on the context and the workload running on the processor. In general, a CPU load of 1.00 on a four-core processor indicates that all four cores are being fully utilized. If this is expected and desired behavior for the workload, then a CPU load of 1.00 is not necessarily a bad thing.

However, if the workload is not designed to fully utilize all four cores or if there are other processes running on the system that are also competing for CPU resources, a sustained CPU load of 1.00 may indicate that the system is under heavy load and may be struggling to keep up. In this case, it could be a bad thing as the system's performance could be negatively impacted and may become unresponsive or unstable. It's important to monitor CPU load in conjunction with other performance metrics to get a better understanding of system behavior and identify potential issues.

Useful resources:

* [Proper way of interpreting system load on a 4 core 8 thread processor](https://serverfault.com/questions/618130/proper-way-of-interpreting-system-load-on-a-4-core-8-thread-processor)
* [Understanding Linux CPU Load - when should you be worried?](http://blog.scoutapp.com/articles/2009/07/31/understanding-load-averages)

</details>

<details>
<summary><b>What does it mean when the effective user is root, but the real user ID is still your username?</b></summary><br>

The **real user ID** is who you really are (the user who owns the process), and the **effective user ID** is what the operating system looks at to make a decision whether you are allowed to do something (most of the time, there are some exceptions).

When you log in, the login shell sets both the **real and effective user ID** to the same value (your **real user ID**) as supplied by the password file.

If, for instance, you execute setuid, and besides running as another user (e.g. **root**) the setuid program is also supposed to do something on your behalf.

After executing setuid, it will have your **real ID** (since you're the process owner) and the effective user id of the file owner (for example **root**) since it is setuid.

Let's use the case of `passwd`:

```bash
-rwsr-xr-x 1 root root 45396 may 25  2012 /usr/bin/passwd
```

When user2 wants to change their password, they execute `/usr/bin/passwd`.

The **RUID** will be user2 but the **EUID** of that process will be root.

user2 can use only passwd to change their own password, because internally passwd checks the **RUID** and, if it is not root, its actions will be limited to real user's password.

It's necessary that the **EUID** becomes root in the case of passwd because the process needs to write to `/etc/passwd` and/or `/etc/shadow`.

Useful resources:

* [Difference between Real User ID, Effective User ID and Saved User ID? (original)](https://stackoverflow.com/questions/30493424/what-is-the-difference-between-a-process-pid-ppid-uid-euid-gid-and-egid)
* [What is the difference between a pid, ppid, uid, euid, gid and egid?](https://stackoverflow.com/questions/30493424/what-is-the-difference-between-a-process-pid-ppid-uid-euid-gid-and-egid)

</details>

<details>
<summary><b>How do you prevent logs from getting too big?</b></summary><br>

Using `logrotate` is the usual way of dealing with logfiles. But instead of adding content to `/etc/logrotate.conf` you should add your own job to `/etc/logrotate.d/`, to avoid issues between release upgrades and to better organize different tasks rather than searching through a large logrotate.conf file.

Useful resources:

* [How to Use logrotate to Manage Log Files](https://www.linode.com/docs/uptime/logs/use-logrotate-to-manage-log-files/)
* [System logging](https://developer.ibm.com/tutorials/l-lpic1-108-2/)

</details>

<details>
<summary><b>How can you see what files are associated with a running process? What is one example of why you would use this command?</b></summary><br>

To see the files associated with a running process, you can use the lsof command, which stands for "list open files." Every file, including devices, network sockets, pipes, and more, is represented as a file in UNIX-like systems.

**Example:**
Let's say you have a process with the PID 1234, and you want to see the files it has opened:

**Why would you use this command?**

* **Troubleshooting Network Issues**: If a process is misbehaving or is suspected of unauthorized network activity, you can use lsof to check which network connections the process has established.
* **File Locks**: If a process has locked a file and other processes can't access it, you can use lsof to identify the locking process and the locked file.
* **Resource Leaks**: If you suspect that a process is not releasing file handles or consuming too many resources, lsof can provide insights by listing all open files by the process.
* **Disk Space Issues**: Sometimes, deleted files continue to consume disk space because they are still open in a process. With lsof, you can identify such "deleted" but open files.
* **Security Audits**: If you're conducting a security check, lsof can help you identify what resources and network connections each process is using, aiding in the identification of suspicious activities.

Useful resources:

* [Linux Processes](https://www.tldp.org/LDP/tlk/kernel/processes.html)

</details>

<details>
<summary><b>What kind of information can you see with the <code>top</code> command and how is it they useful?</b></summary><br>

The top command in UNIX-like operating systems provides a dynamic real-time overview of system performance.

**System Summary Information:**

* **Uptime**: How long the system has been running.
* **Number of Users**: How many users are currently logged in.
* **Load Averages**: The system load averages for the last 1, 5, and 15 minutes. A general rule of thumb is that if the 1-minute load average is higher than the number of CPU cores, it might indicate the system is overloaded.
* **Tasks**: Number of total tasks and their breakdown (running, stopped, sleeping, etc.).
* **CPU Usage**: A breakdown of CPU time in user processes, system processes, processes with priority upgrade nice, idle processes, and more.
* **Memory and Swap**: Total, used, and free physical memory (RAM) and swap space.

**How is the top command useful?**

* **Performance Monitoring**: Quickly identify which processes are consuming the most resources, allowing administrators to troubleshoot performance issues.
* **Resource Analysis**: Observe real-time data on system memory, CPU, and swap usage to make informed decisions about system health and when to upgrade resources.
* **Process Management**: Identify rogue or misbehaving processes. From within top, you can send signals to processes. For example, you can terminate unresponsive processes directly from the top interface.
* **System Health**: The load average, uptime, and the number of active tasks provide a quick view of the system's overall health and performance.
* **User Activity**: Monitor which users are consuming the most resources, especially in shared or multi-user environments.
* **Trends and Patterns**: Over time, consistently monitoring with top can help administrators recognize performance trends and patterns.

Useful resources:

* [top explained visually](https://svennd.be/top-explained-visually/)

</details>

<details>
<summary><b>You need to upgrade <code>ntpd</code> service at 200 servers. What is the best way to go about upgrading all of these to the latest?</b></summary><br>

By using **Infrastructure as a Code** approach, there are multiple good ways:

1. **Configuration Synchronization Change Management Model**:

There are Configuration Management Tools (Ansible, Chef, Puppet, Saltstack, ...), that can be used to automatically update `ntpd` service on all servers. To keep systems stable, system packages on servers are usually auto-updated with only security updates. Major or minor versions of packages are usually version locked in configuration definitions to prevent misconfiguration of the service. Change is then deployed by changing `ntpd` version in configuration definition.

With this approach, it is important to be careful when deploying changes into infrastructure massively. The pipeline of deployment should include Unit, Integration and System tests, and eventually be first deployed into Staging environment to prove configuration. If tests prove configuration correctness, deployment should be done by incremental rollout with ability to rollback in case of errors or failure.

2. **Immutable Servers Model**:

In Immutable Server model, whole unit (server, container) is replaced by new updated image rather than making changes to running server (this eliminates configuration drift). With this approach you usually build server image with tools like Packer or Docker with Dockerfile. This image is then tested and deployed similarly as in option above (1.), but now using techniques such as Canary Release, which also has ability to incremental rollout and rollback.

Useful resources:

* [Infrastructure as a Code - Chapter 8: Patterns for Updating and Changing Servers](https://www.oreilly.com/library/view/infrastructure-as-code/9781491924334/)

</details>

<details>
<summary><b>How do you permanently set <code>$PATH</code> on Linux/Unix? Why is this variable so important?</b></summary><br>

The `$PATH` variable is crucial because it tells the system where to look for executables when you run a command. By modifying the `$PATH`, you can ensure the system can locate your custom or additional scripts and binaries without needing to specify their full paths.

Here’s how to permanently set or modify the `$PATH` variable on Linux/Unix:

### 1. **Modify `$PATH` for a Specific User**

   To set the `$PATH` variable permanently for a specific user, modify their shell configuration file (usually `.bashrc`, `.bash_profile`, `.profile`, or `.zshrc` depending on the shell).

     - Edit the user’s **`.bashrc`** or **`.bash_profile`** file:
       ```bash
       vim ~/.bashrc   # or ~/.bash_profile
       ```
     - Add the following line to modify the `$PATH`:
       ```bash
       export PATH="$PATH:/path/to/directory"
       ```
     - Save the file and source it to apply the changes immediately:
       ```bash
       source ~/.bashrc  # or ~/.bash_profile
       ```
     - The `$PATH` modification will now persist across sessions for that user.

### 2. **Modify `$PATH` System-Wide**

   To set the `$PATH` variable for all users, edit one of the global shell configuration files.

* **For all users (system-wide)**:
  * Edit **`/etc/profile`** or add a new file to **`/etc/profile.d/`**:

       ```bash
       sudo vim /etc/profile
       ```

  * Add the following:

       ```bash
       export PATH="$PATH:/path/to/directory"
       ```

  * Alternatively, create a new file in `/etc/profile.d/` (e.g., `custom_path.sh`):

       ```bash
       sudo vim /etc/profile.d/custom_path.sh
       ```

  * Add the following:

       ```bash
       export PATH="$PATH:/path/to/directory"
       ```

  * Save the file and source `/etc/profile` or log out and log back in for changes to take effect.

* **For all users on a specific shell**:
  * For **Bash**, you can edit **`/etc/bash.bashrc`** to modify the `$PATH` for all users using Bash.

### 3. **Modify `$PATH` for a Single Session**

   You can also set the `$PATH` for the current session only by directly exporting it in the shell. This change will last until the session ends (e.g., when the terminal is closed):

   ```bash
   export PATH="$PATH:/path/to/directory"
   ```

The `$PATH` variable defines the directories that the system searches when you run a command without specifying its full path. If a directory containing an executable is not in the `$PATH`, you would need to provide the full path to that executable every time you run it.

1. **Simplifies Command Execution**:
   * With `$PATH` set correctly, you can execute programs, scripts, and binaries from any location without having to specify their full file paths.

2. **Prioritizes Executable Locations**:
   * The system searches directories in the order they are listed in `$PATH`. You can prioritize certain directories by placing them earlier in the `$PATH`, ensuring that specific versions of programs are executed.

3. **Customizability**:
   * You can extend the `$PATH` to include custom locations for user-installed programs, third-party software, or local scripts, giving you flexibility and control over your environment.

4. **Multiple Executable Versions**:
   * If multiple versions of the same command (e.g., different versions of Python) exist in different directories, the one found first in the `$PATH` will be executed. Adjusting `$PATH` allows you to control which version is run.

5. **Security**:
   * By controlling the `$PATH`, you can limit the risk of executing untrusted or malicious binaries by ensuring that system directories are prioritized, and user directories are well defined. It is generally recommended not to include `.` (the current directory) in the `$PATH`, as it can lead to unintended or malicious command execution.

</details>

<details>
<summary><b>When your server is booting up some errors appears on the console. How do you examine the system boot log and where are they stored?</b></summary><br>

Your console has two types of messages:

* **generated by the kernel** (via printk)
* **generated by userspace** (usually your init system)

Kernel messages are always stored in the **kmsg** buffer, visible via `dmesg` command. They're also often copied to your **syslog**. This also applies to userspace messages written to `/dev/kmsg`, but those are fairly rare.

Meanwhile, when userspace writes its fancy boot status text to `/dev/console` or `/dev/tty1`, it's not stored anywhere at all. It just goes to the screen and that's it.

`dmesg` is used to review boot messages contained in the kernel ring buffer. A ring buffer is a buffer of fixed size for which any new data added to it overwrites the oldest data in it.

It shows operations once the boot process has completed, such as command line options passed to the kernel; hardware components detected, events when a new USB device is added, or errors like NIC (Network Interface Card) failure and the drivers report no link activity detected on the network and so much more.

If system logging is done via the journal component you should use `journalctl`. It shows messages include kernel and boot messages; messages from syslog or various services.

Boot issues/errors calls for a system administrator to look into certain important files in conjunction with particular commands (handled differently by different versions of Linux):

* `/var/log/boot.log` - system boot log, it contains all that unfolded during the system boot
* `/var/log/messages` - stores global system messages, including the messages that are logged during system boot
* `/var/log/dmesg` - contains kernel ring buffer information

Useful resources:

* [How to view all boot messages in Linux after booting? (original)](https://superuser.com/questions/1188407/how-to-view-all-boot-messages-in-linux-after-booting)
* [Differences in /var/log/{syslog,dmesg,messages} log files](https://superuser.com/questions/565927/differences-in-var-log-syslog-dmesg-messages-log-files)
* [How can the messages that scroll by when booting a Debian system be reviewed later?](https://serverfault.com/questions/516411/all-debian-boot-messages)

</details>

<details>
<summary><b>Swap usage too high. What are the reasons for this and how do you resolve swapping problems?</b></summary><br>

**Swap** space is a restricted amount of physical memory that is allocated for use by the operating system when available memory has been fully utilized. It is memory management that involves swapping sections of memory to and from physical storage.

If the system needs more memory resources and the RAM is full, inactive pages in memory are moved to the swap space. While swap space can help machines with a small amount of RAM, it should not be considered a replacement for more RAM. **Swap** space is located on hard drives, which have a slower access time than physical memory.

Workload increases your RAM demand. You are running a workload that requires more memory. Usage of the entire swap indicates that. Also, changing `swappiness` to **1** might not be a wise decision. Setting `swappiness` to **1** does not indicate that swapping will not be done. It just indicates how aggressive kernel will be in respect of swapping, it does not eliminate swapping. Swapping will happen if it needs to be done.

* **Increasing the size of the swap space** - firstly, you'd have increased disk use. If your disks aren't fast enough to keep up, then your system might end up thrashing, and you'd experience slowdowns as data is swapped in and out of memory. This would result in a bottleneck.

* **Adding more RAM** - the real solution is to add more memory. There's no substitute for RAM, and if you have enough memory, you'll swap less.

For monitoring swap space usage:

* `cat /proc/swaps` - to see total and used swap size
* `grep SwapTotal /proc/meminfo` - to show total swap space
* `free` - to display the amount of free and used system memory (also swap)
* `vmstat` - to check swapping statistics
* `top`, `htop`- to check swap space usage
* `atop` - to show is that your system is overcommitting memory
* or use one-liner shell command to list all applications with how much swap space search is using in kilobytes:

```bash
for _fd in /proc/*/status ; do
  awk '/VmSwap|Name/{printf $2 " " $3}END{ print ""}' $_fd
done | sort -k 2 -n -r | less
```

Useful resources:

* [Linux ate my ram!](https://www.linuxatemyram.com/)
* [How to find out which processes are using swap space in Linux?](https://stackoverflow.com/questions/479953/how-to-find-out-which-processes-are-using-swap-space-in-linux)
* [8 Useful Commands to Monitor Swap Space Usage in Linux](https://www.tecmint.com/commands-to-monitor-swap-space-usage-in-linux/)
* [What is the danger in having a fully used SWAP in an Ubuntu server?](https://serverfault.com/questions/499301/what-is-the-danger-in-having-a-fully-used-swap-in-an-ubuntu-server)
* [How to empty swap if there is free RAM?](https://askubuntu.com/questions/1357/how-to-empty-swap-if-there-is-free-ram)

</details>

<details>
<summary><b>What is umask? Describe a scenario where you might need to change it for a user.</b></summary><br>

`umask` is a default permission setting that determines the permissions that are assigned to newly created files and directories.

The umask value is subtracted from the default permissions of a file or directory to determine its final permissions. For example, if the umask value is set to 022, the default permissions for a file would be 666 (rw-rw-rw-) and the final permissions would be 644 (rw-r--r--), since 022 is subtracted from 666.

A scenario where you might need to change the umask for a user is when you want to control the default permissions for new files or directories created by that user. For example, if you have a user who is creating sensitive files that should not be accessible to other users, you might want to set their umask value to 077, which would result in files with permissions 600 (rw-------) and directories with permissions 700 (rwx------). This would ensure that only the owner of the files or directories can access them, and no other users on the system can read or modify them.

Useful resources:

* [What is Umask and How To Setup Default umask Under Linux?](https://www.cyberciti.biz/tips/understanding-linux-unix-umask-value-usage.html)

</details>

<details>
<summary><b>In SQL, how can you combine rows from two or more tables, based on a related column between them?</b></summary><br>

In SQL, you can combine rows from two or more tables using the JOIN clause based on a related column between them. The JOIN clause combines the specified columns from two or more tables using a specified condition.

There are different types of JOIN operations in SQL, including:

* INNER JOIN: Returns only the rows that have matching values in both tables.
* LEFT JOIN: Returns all the rows from the left table and the matched rows from the right table. If there are no matches in the right table, NULL values are returned.
* RIGHT JOIN: Returns all the rows from the right table and the matched rows from the left table. If there are no matches in the left table, NULL values are returned.
* FULL OUTER JOIN: Returns all the rows from both tables. If there are no matches, NULL values are returned.

Here is an example of an INNER JOIN query that combines rows from two tables based on a related column:

<code>
SELECT customers.customer_id, customers.name, orders.order_id, orders.order_date
FROM customers
INNER JOIN orders
ON customers.customer_id = orders.customer_id;
</code>

This query combines the customers table with the orders table based on the customer_id column, and returns only the rows that have matching values in both tables. The resulting table contains the customer_id, name, order_id, and order_date columns.

</details>

<details>
<summary><b>What is the difference between a symbolic link and a hard link?</b></summary><br>

Underneath the file system files are represented by inodes (or is it multiple inodes not sure)

* a file in the file system is basically a link to an inode
* a hard link then just creates another file with a link to the same underlying inode

When you delete a file it removes one link to the underlying inode. The inode is only deleted (or deletable/over-writable) when all links to the inode have been deleted.

* a symbolic link is a link to another name in the file system

Once a hard link has been made the link is to the inode. deleting renaming or moving the original file will not affect the hard link as it links to the underlying inode. Any changes to the data on the inode is reflected in all files that refer to that inode.

Note: Hard links are only valid within the same file system. Symbolic links can span file systems as they are simply the name of another file.

Differences:

* **Hardlink** cannot be created for directories. Hard link can only be created for a file
* **Softlink** also termed a symbolic links or symlinks can link to a directory

Useful resources:

* [What is the difference between a hard link and a symbolic link?](https://medium.com/@wendymayorgasegura/what-is-the-difference-between-a-hard-link-and-a-symbolic-link-8c0493041b62)

</details>

<details>
<summary><b>How does the sticky bit work? Is <code>SUID/GUID</code> is the same?</b></summary><br>

The **SUID/GUID** bit and the **sticky-bit** are 2 completely different things.

**SUID/GUID**

The position that the x bit takes in the rwxrwxrwx for the user octal (1st group of rwx) and the group octal (2nd group of rwx) can take an additional state where the x becomes an s. When this occurs this file when executed (if it's a program and not just a shell script) will run with the permissions of the owner or the group of the file.

So if the file is owned by root and the **SUID** bit is turned on, the program will run as root. Even if you execute it as a regular user. The same thing applies to the **GUID** bit.

Examples:

**no suid/guid** - just the bits `rwxr-xr-x` are set.

```bash
ls -lt b.pl
-rwxr-xr-x 1 root root 179 Jan  9 01:01 b.pl
```

**suid & user's executable bit enabled (lowercase s)** - the bits `rwsr-x-r-x` are set.

```bash
chmod u+s b.pl
ls -lt b.pl
-rwsr-xr-x 1 root root 179 Jan  9 01:01 b.pl
```

**suid enabled & executable bit disabled (uppercase S)** - the bits `rwSr-xr-x` are set.

```bash
chmod u-x b.pl
ls -lt b.pl
-rwSr-xr-x 1 root root 179 Jan  9 01:01 b.pl
```

**guid & group's executable bit enabled (lowercase s)** - the bits `rwxr-sr-x` are set.

```bash
chmod g+s b.pl
ls -lt b.pl
-rwxr-sr-x 1 root root 179 Jan  9 01:01 b.pl
```

**guid enabled & executable bit disabled (uppercase S)** - the bits `rwxr-Sr-x` are set.

```bash
chmod g-x b.pl
ls -lt b.pl
-rwxr-Sr-x 1 root root 179 Jan  9 01:01 b.pl
```

**sticky bit**

The sticky bit on the other hand is denoted as `t`, such as with the `/tmp` directory:

```bash
ls -l /|grep tmp
drwxrwxrwt. 168 root root 28672 Jun 14 08:36 tmp
```

This bit should have always been called the _restricted deletion bit_ given that's what it really connotes. When this mode bit is enabled, it makes a directory such that users can only delete files & directories within it that they are the owners of.

Useful resources:

* [How does the sticky bit work? (original)](https://unix.stackexchange.com/questions/79395/how-does-the-sticky-bit-work)

</details>

<details>
<summary><b>In SQL, what is the difference between <code>REPLACE</code> and <code>INSERT</code>?</b></summary><br>

In SQL, both REPLACE and INSERT are used to add data into tables, but they behave differently when it comes to handling duplicate records.

If you try to `INSERT` a record that would result in a duplicate value in a unique indexed column or primary key, the database will typically raise an error and reject the operation.

The `REPLACE` statement either inserts or replaces the existing row if there's a duplicate unique or primary key.
If the new row doesn't conflict with any existing row based on the unique index or primary key, it's simply inserted.
If there's a conflict, the existing row is deleted, and the new row is inserted in its place.

**Error Handling:**
With INSERT, if you attempt to add a duplicate record that violates the primary key or unique index constraints, you get an error.
With REPLACE, if a duplicate is found, the old record is deleted, and the new one is inserted without any errors.

**Use Cases:**
You'd use INSERT when you want to add new data and ensure that you're not overwriting any existing data.
You'd use REPLACE when you want to add new data but overwrite any existing data if there's a primary key or unique index conflict.

**Underlying Operations:**
With REPLACE, the operation involves both a DELETE (if there's a conflict) and an INSERT.

</details>

<details>
<summary><b>How do you make a server or application high availability?</b></summary><br>

To make a server or application **highly available**, the goal is to minimize downtime and ensure the system remains operational, even in the event of failures. High availability (HA) is achieved through redundancy, failover mechanisms, load balancing, and eliminating single points of failure. Here are the key steps:

### 1. **Redundancy**

* **Multiple Servers/Instances**: Deploy multiple instances of your application or service across different servers or environments. If one server fails, another can continue serving requests.
* **Active-Active vs Active-Passive**:
  * **Active-Active**: All instances are actively serving traffic simultaneously.
  * **Active-Passive**: One instance is active, while another is on standby and takes over in case of failure.

### 2. **Load Balancing**

* **Distribute Traffic**: Use a load balancer (e.g., **Nginx**, **HAProxy**, **AWS ELB**) to distribute incoming requests across multiple servers. This ensures no single server is overwhelmed, and traffic is seamlessly redirected if a server fails.
* **Health Checks**: Configure load balancers to perform health checks on backend servers. If a server becomes unhealthy, it is automatically removed from the pool until it recovers.

### 3. **Failover Mechanisms**

* **Automatic Failover**: Implement failover mechanisms that detect when an instance or service goes down and automatically shift traffic to the remaining healthy servers.
* **DNS Failover**: Use DNS with short TTLs and failover services (like **Route 53** or **Cloudflare**) to redirect traffic to backup instances in case of failure.
* **Virtual IP (VIP)**: In some HA setups, use a shared virtual IP address that moves between servers in an active-passive configuration, so clients always connect to a single IP, regardless of which server is active.

### 4. **Clustering**

* **Database Clustering**: Use database clusters (e.g., **MySQL Galera Cluster**, **PostgreSQL Streaming Replication**) to replicate data across multiple database nodes, ensuring continuous availability even if one node fails.
* **Application Clustering**: Applications like web servers and middleware can be clustered for HA (e.g., **Apache HTTPD with mod_cluster**, **Tomcat clustering**).

### 5. **Data Replication**

* **File/Data Replication**: Ensure that critical data is replicated across servers or storage systems, so no single point of failure can result in data loss.
* **Distributed File Systems**: Use distributed or replicated file systems (e.g., **GlusterFS**, **Ceph**, **NFS**) to ensure file availability across multiple nodes.

### 6. **Eliminate Single Points of Failure**

* Ensure that every part of your architecture, including networking (switches, routers), storage (disks, SANs), and servers, has redundancy.
* Avoid reliance on single components like a single server, database, or load balancer.

### 7. **Geographic Redundancy**

* **Multi-Region Deployment**: Deploy services across multiple geographic regions or data centers. In case of a complete failure in one region (e.g., natural disaster, power outage), the other regions can continue serving traffic.
* **Global Load Balancing**: Use global load balancing services that route traffic to the nearest available region.

### 8. **Monitoring and Alerts**

* **Real-time Monitoring**: Implement continuous monitoring of servers, applications, and services to detect failures or performance degradation (e.g., using **Prometheus**, **Nagios**, or cloud-native monitoring tools).
* **Alerting**: Set up alerts for critical incidents to enable quick intervention by operations teams.

### 9. **Backup and Recovery**

* Regularly back up critical data and configurations.
* Ensure **automated recovery procedures** for systems or databases to restore service quickly after a failure.

### 10. **Automated Scaling**

* **Horizontal Scaling**: Set up automatic scaling to add or remove instances based on demand (e.g., using **AWS Auto Scaling**, **Kubernetes Horizontal Pod Autoscaler**).
* **Auto-restart and Self-healing**: Use container orchestrators like **Kubernetes** to automatically restart failed application instances or self-heal unhealthy pods.

</details>

<details>
<summary><b>You are configuring a new server. One of the steps is setting the permissions to the app directories. What steps will you take and what mistakes to avoid?</b></summary><br>

**1) Main requirements - remember about this**

* which users have access to the app filesystem
* permissions for web servers, e.g. Apache and app servers e.g. uwsgi
* permissions for specific directories such as **uploads**, **cache** and main app directory like a `/var/www/app01/html`
* correct `umask` value for users and **suid**/**sgid** (only for specific situations)
* permissions for all future files and directories
* permissions for cron jobs and scripts

**2) Application directories**

`/var/www` contains a directory for each website (isolation of the apps), e.g. `/var/www/app01`, `/var/www/app02`

```bash
mkdir /var/www/{app01,app02}
```

**3) Application owner and group**

Each application has a designated **owner** (e.g. **u01-prod**, **u02-prod**) and **group** (e.g. **g01-prod**, **g02-prod**) which are set as the owner of all files and directories in the website's directory:

```bash
chown -R u01-prod:g01-prod /var/www/app01
chown -R u02-prod:g02-prod /var/www/app02
```

**4) Developers owner and group**

All users that maintain the website have own groups, and they're attached to application group:

```bash
id alice
uid=2000(alice) gid=4000(alice) groups=8000(g01-prod)
id bob
uid=2001(bob) gid=4001(bob) groups=8000(g01-prod),8001(g02-prod)
```

So **alice** user has standard privileges for `/var/www/app01` and **bob** user has standard privileges for `/var/www/app01` and `/var/www/app02`.

**5) Web server owner and group**

Any files or directories that need to be written by the webserver have their owner. If the web servers is Apache, default owner/group are **apache:apache** or **www-data:www-data** and for Nginx it will be **nginx:nginx**. Don't change these settings.

If applications work with app servers, such as **uwsgi** or **php-fpm**, then you should set the appropriate user and group (e.g. for **app01** it will be **u01-prod:g01-prod**) in specific config files.

**6) Permissions**

Set properly permissions with **Access Control Lists**:

```bash
# For web server
setfacl -Rdm "g:apache:rwx" /var/www/app01
setfacl -Rm "g:apache:rwx" /var/www/app01

# For developers
setfacl -Rdm "g:g01-prod:rwx" /var/www/app01
setfacl -Rm "g:g01-prod:rwx" /var/www/app01
```

If you use **SELinux** remember about security context:

```bash
chcon -R system_u:object_r:httpd_sys_content_t /var/www/app01
```

**7) Security mistakes**

* **root** owner for files and directories
* **root** never executes any files in website directory, and shouldn't be creating files in there
* to wide permissions like a **777** so some critical files may be world-writable and world-readable
* avoid creating maintenance scripts or other critical files with suid root

If you allow your site to modify the files which form the code running your site, you make it much easier for someone to take over your server.

A file upload tool allows users to upload a file with any name and any contents. This allows a user to upload a mail relay PHP script to your site, which they can place wherever they want to turn your server into a machine to forward unsolicited commercial email. This script could also be used to read every email address out of your database, or other personal information.

If the malicious user can upload a file with any name but not control the contents, then they could easily upload a file which overwrites your `index.php` (or another critical file) and breaks your site.

Useful resources:

* [How to setup linux permissions for the WWW folder?](https://serverfault.com/questions/124800/how-to-setup-linux-permissions-for-the-www-folder)
* [What permissions should my website files/folders have on a Linux webserver?](https://serverfault.com/questions/357108/what-permissions-should-my-website-files-folders-have-on-a-linux-webserver)
* [Security Pitfalls of setgid Programs](https://www.agwa.name/blog/post/security_pitfalls_of_setgid_programs)

</details>

<details>
<summary><b>How do you change system runlevels? What are some reasons you would need to?</b></summary><br>

runlevels are different operating modes in which the system can run. There are typically seven runlevels, from 0 to 6, with each one defining a specific state or mode of operation. Each runlevel is designed to start a specific set of processes and services, and by changing the runlevel, you can control which processes and services are running on your system.

To change system runlevels, you can use the `systemctl isolate` command with the appropriate runlevel target. For example:

<code>systemctl isolate multi-user.target</code>

A few reasons you might need to switch runlevels:

* Troubleshooting: You might need to switch to a lower runlevel (such as runlevel 1 or 3) to troubleshoot a system issue or perform maintenance tasks.
* Upgrades: You might need to switch to a higher runlevel (such as runlevel 6) to perform a system upgrade or reboot the system.
* Security: You might need to disable certain services or processes that are not needed for security reasons.
* Performance: You might need to adjust the system runlevel to optimize system performance based on the workload or resources available.

</details>

<details>
<summary><b>The root password has been forgotten, and you are locked out of the system. How can you reset the root password?</b></summary><br>

If you've forgotten the root password and are locked out of a Linux system, you can reset it by booting into a single-user mode or using a rescue mode provided by some installation media.

**Using Single-User Mode:**

1. Reboot the system.
2. Access Boot Loader: As the system boots, you typically need to press a key (like Shift or Esc for GRUB) to access the boot loader menu.
3. Edit Boot Entry:
In the GRUB bootloader menu, highlight the default kernel entry (usually the top one), and press e to edit.
4. Modify Kernel Boot Parameters:

* Find the line starting with linux (or linux16 or linuxefi depending on your setup).
* At the end of this line, append the parameter init=/bin/bash or rw init=/bin/sh.
* This will instruct the system to boot directly to a shell without prompting for a password.

5. Boot the System: Press Ctrl + X or F10 to boot the system with the modified parameters.
6. Reset the Password: Once you get a root shell, you can reset the root password using the passwd command: `passwd root`
7. Reboot: Once you've reset the password, reboot the system: `exec /sbin/init`

**Using Rescue Mode:**

1. Boot from Installation Media: Insert the installation media (like a DVD or USB stick) for your Linux distribution and boot from it.
2. Enter Rescue Mode: Follow the prompts to enter rescue mode. This process can differ among distributions.
3. Mount the System: Once in rescue mode, you may need to mount your system's root filesystem. Some rescue modes will assist you in identifying and mounting the system.
4. Chroot into System: Use chroot to change the root directory to your system's root: `chroot /mnt/sysimage`
5. Reset the Password: Use the passwd command to reset the root password.
6. Exit and Reboot: Exit from the chroot environment and reboot the system.

</details>

<details>
<summary><b>How could you modify a text file without invoking a text editor?</b></summary><br>

You can modify a text file without invoking a text editor by using command-line utilities that allow you to directly manipulate the contents of the file. Here are several common ways to do this:

### 1. **Using `echo` and Redirection**

You can append or overwrite content in a file using `echo` and redirection (`>` for overwrite, `>>` for append).

* **Overwrite the file**:

   ```bash
   echo "New content" > file.txt
   ```

* **Append to the file**:

   ```bash
   echo "Additional content" >> file.txt
   ```

### 2. **Using `sed` (Stream Editor)**

`sed` allows you to perform in-place text replacements or modifications.

* **Replace a word or pattern**:

   ```bash
   sed -i 's/oldword/newword/g' file.txt
   ```

* **Delete specific lines** (e.g., delete line 3):

   ```bash
   sed -i '3d' file.txt
   ```

* **Insert text at a specific line** (e.g., insert "Hello" at line 2):

   ```bash
   sed -i '2iHello' file.txt
   ```

### 3. **Using `awk`**

`awk` is another powerful tool for text processing and can be used to modify files based on patterns or specific fields.

* **Replace a specific field in a line**:

   ```bash
   awk '{if(NR==2) $2="newvalue"}1' file.txt > temp && mv temp file.txt
   ```

### 4. **Using `tr` (Translate)**

`tr` is useful for character replacements.

* **Replace all occurrences of a character**:

   ```bash
   tr 'a' 'b' < file.txt > temp && mv temp file.txt
   ```

### 5. **Using `head` and `tail` to Modify Specific Parts**

You can extract parts of a file and replace specific lines using `head` and `tail`.

* **Replace line 3 with new content**:

   ```bash
   head -n 2 file.txt > temp && echo "New content" >> temp && tail -n +4 file.txt >> temp && mv temp file.txt
   ```

### 6. **Using `printf`**

`printf` allows formatted output and can be used similarly to `echo`.

* **Overwrite a file with formatted content**:

   ```bash
   printf "Formatted content\nNext line\n" > file.txt
   ```

</details>

<details>
<summary><b>How do you change kernel parameters? What kernel options might you need to tune?</b></summary><br>

You can change kernel parameters at boot time or during runtime using the `sysctl` command.

To change kernel parameters at boot time, you can modify the `GRUB_CMDLINE_LINUX` variable in the /etc/default/grub file, then run `update-grub` to update the GRUB configuration.

To change kernel parameters during runtime, you can use the `sysctl` command followed by the name of the parameter you want to change and its new value. For example, to increase the maximum number of open files, you can use the following command:

<code>sudo sysctl -w fs.file-max=100000</code>

Some kernel options that you might need to tune include:

* Network-related options, such as the maximum number of connections, the size of network buffers, and the default congestion control algorithm.
* File system-related options, such as the maximum number of open files, the size of disk caches, and the behavior of the journaling file system.
* Security-related options, such as the maximum number of processes and threads, the permissions for executing programs, and the behavior of system calls.

Useful resources:

* [How to Change Kernel Runtime Parameters in a Persistent and Non-Persistent Way](https://www.tecmint.com/change-modify-linux-kernel-runtime-parameters/)

</details>

<details>
<summary><b>What is the best way to remove a directory named <code>-rf</code>? Explain the issue.</b></summary><br>

The issue with trying to remove a directory named `-rf` is that the `rm` command interprets `-rf` as options (`-r` for recursive and `-f` for force), rather than as the name of the directory. This can be problematic because `rm -rf` is a common and powerful command used to forcefully and recursively remove directories and their contents, which could accidentally lead to removing unintended files if misused.

### The Best Ways to Remove a Directory Named `-rf`

#### 1. **Use `./` to Specify the Path**

   Prepend the directory name with `./` to indicate it is a directory in the current directory, not an option.

   ```bash
   rm -r ./-rf
   ```

   This works because the shell interprets `./-rf` as a file or directory path, avoiding confusion with the `rm` options.

#### 2. **Use `--` to Stop Option Parsing**

   The `--` argument tells the `rm` command to stop interpreting anything following it as an option, treating it as a literal argument (the directory name).

   ```bash
   rm -r -- -rf
   ```

   The `--` prevents `-rf` from being processed as an option.

#### 3. **Use an Absolute or Relative Path**

   If the directory is located in a specific path, using the full or relative path to the directory can also avoid confusion.

   ```bash
   rm -r /path/to/-rf
   ```

</details>

<details>
<summary><b>Explain the <code>/proc</code> filesystem.</b></summary><br>

`/proc` is a virtual file system that provides detailed information about kernel, hardware and running processes.

Since `/proc` contains virtual files, it is called virtual file system. These virtual files have unique qualities. Most of them are listed as zero bytes in size.

Virtual files such as `/proc/interrupts`, `/proc/meminfo`, `/proc/mounts` and `/proc/partitions` provide an up-to-the-moment glimpse of the system’s hardware. Others: `/proc/filesystems` file and the `/proc/sys/` directory provide system configuration information and interfaces.

Useful resources:

* [Linux Filesystem Hierarchy - /proc](https://www.tldp.org/LDP/Linux-Filesystem-Hierarchy/html/proc.html)

</details>

<details>
<summary><b>Describe your data backup process. How often should you test your backups?</b></summary><br>

* Determine what data needs to be backed up: Identify the critical data that needs to be backed up, such as files, databases, and configurations.
* Decide on a backup frequency: Determine how often you need to back up your data. The frequency will depend on how often the data changes and how critical it is to your business.
* Choose a backup method: There are several backup methods you can use, such as full backup, incremental backup, and differential backup. Each method has its advantages and disadvantages, so choose the one that best suits your needs.
* Select a backup location: Choose a secure location to store your backups, such as an external hard drive, a cloud storage service, or a dedicated backup server.
* Automate the backup process: Automate the backup process to ensure that backups are performed regularly and reliably.
* Test your backups: Regularly test your backups to ensure that they are complete and accurate. Testing backups is critical, as it helps ensure that you can recover your data in the event of a disaster.

It is recommended to test backups at least once every three months to ensure that they are working correctly. Additionally, you should test your backups after any significant changes to your system or data to ensure that your backup process is still effective.

</details>

<details>
<summary><b>Explain three types of journaling in ext4 and xfs.</b></summary><br>

There are three types of journaling available in **ext4 and xfs** file systems:

* **Data journaling**: In data journaling, only file data is logged in the journal. Metadata is written to disk directly, and file contents are written to the journal before being written to disk. In case of a system crash, only the data in the journal is lost. The metadata on disk remains consistent. This type of journaling is faster than other types because only the data is logged to the journal.
* **Ordered journaling**: In ordered journaling, metadata is written to the journal before file data. This ensures that metadata is always consistent, and files can be recovered correctly in case of a system crash. This type of journaling is slower than data journaling because metadata is logged before data.
* **Writeback journaling**: In writeback journaling, file data is written to disk before being logged in the journal. This can result in data inconsistencies in case of a system crash or power failure, as metadata can be updated before the corresponding data is written to the journal. However, writeback journaling is the fastest and most efficient journaling mode, as file data is written directly to disk without being logged in the journal first.

</details>

<details>
<summary><b>What is an inode? How do you find a file's inode number and how can you use it?</b></summary><br>

An **inode** is a data structure on a filesystem on Linux and other Unix-like operating systems that stores all the information about a file except its name and its actual data. A data structure is a way of storing data so that it can be used efficiently.

A Unix file is stored in two different parts of the disk - the data blocks and the inodes. I won't get into superblocks and other esoteric information. The data blocks contain the "contents" of the file. The information about the file is stored elsewhere - in the inode.

A file's inode number can easily be found by using the `ls` command, which by default lists the objects (i.e. files, links and directories) in the current directory (i.e. the directory in which the user is currently working), with its `-i` option. Thus, for example, the following will show the name of each object in the current directory together with its inode number:

```bash
ls -i
```

`df's` `-i` option instructs it to supply information about inodes on each filesystem rather than about available space. Specifically, it tells df to return for each mounted filesystem the total number of inodes, the number of free inodes, the number of used inodes and the percentage of inodes used. This option can be used together with the `-h` option as follows to make the output easier to read:

```bash
df -hi
```

**Finding files by inodes**

If you know the inode, you can find it using the find command:

```bash
find . -inum 435304 -print
```

**Deleting files with strange names**

Sometimes files are created with strange characters in the filename. The Unix file system will allow any character as part of a filename except for a null (ASCII 000) or a "/". Every other character is allowed.

Users can create files with characters that make it difficult to see the directory or file. They can create the directory ".. " with a space at the end, or create a file that has a backspace in the name, using:

```bash
touch `printf "aa\bb"`
```

Now what happens when you use the `ls` command:

```bash
ls
aa?b
ls | grep 'a'
ab
```

Note that when `ls` sends the result to a terminal, it places a "**?**" in the filename to show an unprintable character.

You can get rid of this file by using `rm -i *` and it will prompt you before it deletes each file. But you can also use `find` to remove the file, once you know the inode number.

```bash
ls -i
435304 aa?b
find . -inum 435304 -delete
```

Useful resources:

* [Understand UNIX/Linux Inodes Basics with Examples](https://www.thegeekstuff.com/2012/01/linux-inodes/)
* [What is an inode as defined by POSIX?](https://unix.stackexchange.com/questions/387087/what-is-an-inode-as-defined-by-posix/387093)

</details>

<details>
<summary><b><code>ls -l</code> shows file attributes as question marks. What this means and what steps will you take to remove unused "zombie" files?</b></summary><br>

This problem may be more difficult to solve because several steps may be required - sometimes you have get `test/file: Permission denied`, `test/file: No such file or directory` or `test/file: Input/output error`.

That happens when the user can't do a `stat()` on the files (which requires execute permissions), but can read the directory entries (which requires read access on the directory). So you get a list of files in the directory, but can't get any information on the files because they can't be read. If you have a directory which has read permission but not execute, you'll see this.

Some processes like a `rsync` generates temporary files that get created and dropped fast which will cause errors if you try to call other simple file management commands like `rm`, `mv` etc.

Example of output:

```bash
?????????? ? ?        ?               ?            ? sess_kee6fu9ag7tiph2jae
```

1) change permissions: `chmod 0777 sess_kee6fu9ag7tiph2jae` and try remove
2) change owner: `chown root:root sess_kee6fu9ag7tiph2jae` and try remove
3) change permissions and owner for directory: `chmod -R 0777 dir/ && chown -R root:root dir/` and try remove
4) recreate file: `touch sess_kee6fu9ag7tiph2jae` and try remove
5) watch out for other running processes on the server for example `rsync`, sometimes you can see this as a transient error when an NFS server is heavily overloaded
6) find file inode: `ls -i`, and try remove: `find . -inum <inode_num> -delete`
7) remount (if possible) your filesystem
8) boot system into single-user mode and repair your filesystem with `fsck`

Useful resources:

* [Question marks showing in ls of directory. IO errors too.](https://serverfault.com/questions/65616/question-marks-showing-in-ls-of-directory-io-errors-too)

</details>

<details>
<summary><b>What benefits does LVM provide?</b></summary><br>

* LVM makes it quite easy to move file systems around
* you can extend a volume group onto a new physical volume
* move any number of logical volumes of an old physical one
* remove that volume from the volume group without needing to unmount any partitions
* you can also make snapshots of logical volumes for making backups
* LVM has built in mirroring support, so you can have a logical volume mirrored across multiple physical volumes
* LVM even supports TRIM

Useful resources:

* [What is LVM and what is it used for?](https://askubuntu.com/questions/3596/what-is-lvm-and-what-is-it-used-for)

</details>

<details>
<summary><b>How do you increase the size of LVM partition?</b></summary><br>

Use the `lvextend` command for resize LVM partition.

* extending the size by 500MB:

```bash
lvextend -L +500M /dev/vgroup/lvolume
```

* extending all available free space:

```bash
lvextend -l +100%FREE /dev/vgroup/lvolume
```

and `resize2fs` or `xfs_growfs` to resize filesystem:

* for ext filesystems:

```bash
resize2fs /dev/vgroup/lvolume
```

* for xfs filesystem:

```bash
xfs_growfs mountpoint_for_/dev/vgroup/lvolume
```

Useful resources:

* [Extending a logical volume](https://www.tldp.org/HOWTO/LVM-HOWTO/extendlv.html)

</details>

<details>
<summary><b>What is a zombie/defunct process?</b></summary><br>

Is a process that has completed execution (via the `exit` system call) but still has an entry in the process table: it is a process in the "**Terminated state**".

Processes marked **defunct** are dead processes (so-called "zombies") that remain because their parent has not destroyed them properly. These processes will be destroyed by init if the parent process exits.

Useful resources:

* [What is a <defunct> process, and why doesn't it get killed?](https://askubuntu.com/questions/201303/what-is-a-defunct-process-and-why-doesnt-it-get-killed)

</details>

<details>
<summary><b>What is the proper way to upgrade/update a system in production? Do you automate these processes? Do you set downtime for them? Write recommendations.</b></summary><br>

Upgrading or updating a system in production requires careful planning to avoid service disruption, data loss, or downtime. Here are best practices and recommendations for handling system updates in a production environment:

### 1. **Plan Updates Carefully**

* **Determine the Type of Update**:
  * **Security patches**: Prioritize critical security updates to minimize vulnerabilities.
  * **Minor updates**: Bug fixes and minor enhancements are generally safer to apply without significant risk.
  * **Major upgrades**: Kernel, OS, or application upgrades that introduce significant changes should be carefully planned and tested.

* **Check Compatibility**: Ensure that the updates do not break existing dependencies, software, or services running on the system. Review release notes and update documentation for known issues or changes.

### 2. **Create a Backup/Recovery Plan**

* **Full system backup**: Before performing updates, create a full backup of the system, including important files, databases, and configurations.
* **Automated snapshots**: If you're using a system that supports snapshots (e.g., LVM snapshots or VM snapshots), take a snapshot before the update, allowing quick rollback if something goes wrong.
* **Test the recovery process**: Ensure that you have tested restoring backups or snapshots before you rely on them in production.

### 3. **Automate the Update Process (With Caution)**

   Automation helps ensure consistency and reduce human error, but you should balance automation with manual oversight in production environments.

* **Use configuration management tools**: Use automation tools like **Ansible**, **Puppet**, or **Chef** to handle updates across multiple servers.
  * Example Ansible playbook:

     ```yaml
     ---
     - name: Update packages on production servers
       hosts: production
       tasks:
         - name: Update all packages
           ansible.builtin.dnf:
             name: "*"
             state: latest
     ```

* **Staggered updates**: Automate the update process to be applied in small batches (canary deployments) to avoid updating all production systems simultaneously and exposing the entire environment to risks.
* **Automated testing**: Integrate automated post-update testing to ensure that the system is functional after updates are applied.

### 4. **Use Staging Environments for Testing**

* **Test updates in a staging environment**: Always apply updates first to a **staging environment** that mirrors the production system. This helps you detect any issues before they impact production.
* **Run automated and manual tests**: Perform tests that reflect production workloads, including automated tests for critical services, manual functional tests, and monitoring service performance.

### 5. **Schedule Downtime (if Necessary)**

* **Non-critical updates**: For minor updates that do not disrupt services, you can often apply them during regular operation without scheduling downtime.
* **Critical updates**: For major or disruptive updates (e.g., kernel updates, database migrations, or application upgrades), schedule a maintenance window or downtime when user impact is minimal. Inform stakeholders well in advance.
* **Hot patching**: For critical security updates on production systems where downtime is not an option, consider using **live patching** tools like **KernelCare** or **kpatch** to apply kernel patches without requiring a reboot.

### 6. **Monitoring and Rollback Strategy**

* **Monitor the system after updates**: Closely monitor the system after applying updates. Use tools like **Prometheus**, **Nagios**, or **Zabbix** to track key metrics such as CPU, memory usage, network traffic, and application performance.
* **Rollback plan**: Ensure that you have a rollback plan if something goes wrong. This could involve restoring a backup, rolling back a package to a previous version, or reverting a snapshot. Automate rollback procedures when possible.

### 7. **Communicate with Stakeholders**

* **Notify users**: Inform stakeholders (customers, users, and team members) about planned updates, potential downtime, and the expected impact. Provide timely updates if any issues arise.
* **Document changes**: Keep detailed documentation of the updates, including what was changed, who approved it, the time of implementation, and any issues encountered during the process.

### Recommended Process for Updating Production Systems

1. **Pre-Update Preparation**:
   * Review available updates and their impact.
   * Create a backup or snapshot.
   * Test the updates in a staging environment.
   * Schedule downtime or maintenance windows if needed.
   * Communicate with stakeholders.

2. **During the Update**:
   * Apply updates using automation or manually if necessary.
   * Apply the updates in batches or staggered across systems to minimize risk.
   * Monitor logs and services for any anomalies during the update process.

3. **Post-Update Monitoring**:
   * Verify system and application functionality after the updates.
   * Monitor performance metrics and logs to detect any post-update issues.
   * Be prepared to roll back if critical issues are detected.

4. **Follow-Up**:
   * Notify stakeholders of successful updates or any issues.
   * Document the update process, outcome, and lessons learned for future reference.

****

By automating where possible, rigorously testing updates, and planning for contingencies, you can reduce the risk of disruption in a production environment while keeping systems secure and up-to-date.

</details>

<details>
<summary><b>Present and explain the good ways of using the <code>kill</code> command.</b></summary><br>

Speaking of killing processes never use `kill -9/SIGKILL` unless absolutely mandatory. This kill can cause problems because of its brute force.

Always try to use the following simple procedure:

* first, send **SIGTERM** (`kill -15`) signal first which tells the process to shutdown and is generally accepted as the signal to use when shutting down cleanly (but remember that this signal can be ignored).
* next try to send **SIGHUP** (`kill -1`) signal which is commonly used to tell a process to shutdown and restart, this signal can also be caught and ignored by a process.

The far majority of the time, this is all you need - and is much cleaner.

Useful resources:

* [When should I not kill -9 a process?](https://unix.stackexchange.com/questions/8916/when-should-i-not-kill-9-a-process)
* [SIGTERM vs. SIGKILL](https://major.io/2010/03/18/sigterm-vs-sigkill/)

</details>

<details>
<summary><b>What is <code>strace</code> command and how should be used? Explain example of connect to an already running process.</b></summary><br>

`strace` is a powerful command line tool for debugging and troubleshooting programs in Unix-like operating systems such as Linux. It captures and records all system calls made by a process and the signals received by the process.

**Strace Overview**

`strace` can be seen as a lightweight debugger. It allows a programmer/user to quickly find out how a program is interacting with the OS. It does this by monitoring system calls and signals.

**Uses**

Good for when you don't have source code or don't want to be bothered to really go through it. Also, useful for your own code if you don't feel like opening up **GDB**, but are just interested in understanding external interaction.

**Example of attach to the process**

`strace -p <PID>` - to attach a process to strace.

`strace -e trace=read,write -p <PID>` - by this you can also trace a process/program for an event, like read and write (in this example). So here it will print all such events that include read and write system calls by the process.

Other such examples

* `-e trace=network` - trace all the network related system calls.
* `-e trace=signal` - trace all signal related system calls.
* `-e trace=ipc` - trace all IPC related system calls.
* `-e trace=desc` - trace all file descriptor related system calls.
* `-e trace=memory` - trace all memory mapping related system calls.

Useful resources:

* [How should strace be used? (original)](https://stackoverflow.com/questions/174942/how-should-strace-be-used)
* [How does strace connect to an already running process? (original)](https://stackoverflow.com/questions/7482076/how-does-strace-connect-to-an-already-running-process)
* [Tracing processes for fun and profit](https://techblog.rosedu.org/tracing-processes-for-fun-and-profit.html)

</details>

<details>
<summary><b>When would you use Access Control Lists (ACLs) instead of or in conjunction with the <code>chmod</code> command?</b></summary><br>

Use chmod when simple owner/group/other permissions suffice.
Use ACLs when you need fine-grained control for specific users or groups beyond that model.
ACLs let you grant or restrict access for individual users or multiple groups without changing file ownership or broad permissions.

</details>

<details>
<summary><b>Which algorithms are supported in <code>/etc/shadow</code> file?</b></summary><br>

Typical current algorithms are:

* MD5
* SHA-1 (also called SHA)

both should not be used for cryptographic/security purposes anymore!

* SHA-256
* SHA-512
* SHA-3 (KECCAK was announced the winner in the competition for a new federal approved hash algorithm in October 2012)

Useful resources:

* [What is the algorithm used to encrypt Linux passwords?](https://crypto.stackexchange.com/questions/40841/what-is-the-algorithm-used-to-encrypt-linux-passwords)
* [How to find the hashing algorithm used to obfuscate passwords?](https://unix.stackexchange.com/questions/430141/how-to-find-the-hashing-algorithm-used-to-obfuscate-passwords)

</details>

<details>
<summary><b>What is the use of ulimit in Unix-like systems?</b></summary><br>

Most Unix-like operating systems, including Linux and BSD, provide ways to limit and control the usage of system resources such as threads, files, and network connections on a per-process and per-user basis. These "**ulimits**" prevent single users from using too many system resources.

</details>

<details>
<summary><b>What are soft limits and hard limits?</b></summary><br>

**Hard limit** is the maximum allowed to a user, set by the superuser or root. This value is set in the file `/etc/security/limits.conf`. The user can increase the **soft limit** on their own in times of needing more resources, but cannot set the **soft limit** higher than the **hard limit**.

</details>

<details>
<summary><b>You have configured an RSA key login but your server show <code>Server refused our key</code> as expected. Where will you look for the cause of the problem?</b></summary><br>

**Server side**

Setting `LogLevel VERBOSE` in file `/etc/ssh/sshd_config` is probably what you need, although there are higher levels:

SSH auth failures are logged in `/var/log/auth.log`, `/var/log/secure` or `/var/log/audit/audit.log`.

The following should give you only ssh related log lines (for example):

```bash
grep 'sshd' /var/log/auth.log
```

Next, the most simple command to list all failed SSH logins is the one shown below:

```bash
grep "Failed password" /var/log/auth.log
```

also useful is:

```bash
grep "Failed\|Failure" /var/log/auth.log
```

On newer Linux distributions you can query the runtime log file maintained by Systemd daemon via `journalctl` command (`ssh.service` or `sshd.service`). For example:

```bash
journalctl _SYSTEMD_UNIT=ssh.service | egrep "Failed|Failure"
```

**Client side**

Also, you should run SSH client with `-v|--verbose` - it is in first level of verbosity. Next, you can enable additional (level 2 and 3) verbosity for even more debugging messages as shown with e.g. `-vv`.

Useful resources:

* [Enable Debugging Mode in SSH to Troubleshoot Connectivity Issues](https://www.tecmint.com/enable-debugging-mode-in-ssh/)

</details>

<details>
<summary><b>A Project Manager needs a new SQL Server. What questions would you ask to ensure the proper system is setup?</b></summary><br>

1. What is the expected workload and number of concurrent users?
2. What is the size of the database?
3. What is the growth rate of the database?
4. What are the performance requirements for the database?
5. What are the backup and recovery requirements for the database?
6. What is the budget for the project?
7. What is the expected availability requirement?
8. What are the security requirements for the database?

The answers to these questions will help determine the hardware and software requirements for the SQL Server. Based on the expected workload, database size, and performance requirements, the appropriate hardware can be chosen. The backup and recovery requirements will help determine the type and frequency of backups that will be required. The budget will also play a significant role in determining the hardware and software choices. The expected availability and security requirements will help determine the high availability and security features that will be required for the SQL Server.

</details>

<details>
<summary><b>Create a file with 100 lines with random values.</b></summary><br>

For example:

```bash
cat /dev/urandom | tr -dc 'a-zA-Z0-9' | fold -w 32 | head -n 100 > /path/to/file
```

</details>

<details>
<summary><b>How do you run a script as another user without password?</b></summary><br>

For example (with `visudo` command):

```bash
user1 ALL=(user2) NOPASSWD: /opt/scripts/bin/generate.sh
```

The command paths must be absolute! Then call `sudo -u user2 /opt/scripts/bin/generate.sh` from the user1 shell.

</details>

<details>
<summary><b>Can you give a particular example when is indicated to use <code>nobody</code> account? Tell me the differences running httpd service as a <code>nobody</code> and <code>www-data</code> accounts.</b></summary><br>

In many Unix variants, `nobody` is the conventional name of a user account which owns no files, is in no privileged groups, and has no abilities except those which every other user has.

It is common to run daemons as `nobody`, especially servers, in order to limit the damage that could be done by a malicious user who gained control of them.

However, the usefulness of this technique is reduced if more than one daemon is run like this, because then gaining control of one daemon would provide control of them all. The reason is that `nobody`-owned processes have the ability to send signals to each other and even debug each other, allowing them to read or even modify each other's memory.

**When should I use `nobody` account?**

When permissions aren't required for a program's operations. This is most notable when there isn't ever going to be any disk activity.

A real world example of this is **memcached** (a key-value in-memory cache/database/thing), sitting on my computer and my server running under the `nobody` account. Why? Because it just doesn't need any permissions and to give it an account that did have write access to files would just be a needless risk.

A good example are also web servers. Imagine if Apache ran as root and someone found a way to send custom commands to the console through Apache would have access to your entire system.

`nobody` account also is used as a restricted shell for giving users filesystem access without an actual shell like bash. This should prevent them from being able to execute things.

**`nobody` or `www-data` for httpd (Apache)**

Upon starting Apache needs root access, but it quickly drops this and assumes the identity of a non-privileged user. This user can either be `nobody` or `apache`, or `www-data`.

Several applications use the user `nobody` as a default. For example, you probably never really want say the Apache service to be overwriting files that belong to bind. Having a per-service account tends to be a very good idea.

Getting Apache to run as `nobody:nobody` is pretty easy, just update the user and group settings. But as I mentioned above I don't really recommend that particular user/group. It is entirely possible that you may be tempted to add a service to the system at some time in the future that also runs as `nobody`, and you will forget that have given write access on the filesystem to the user `nobody`.

 If somehow, `nobody` were to become compromised they could potentially have more impact than if an application isolate user, such as `www-data`. Of course a lot of this will depend on the file and group permissions. `nobody` uses the permissions of others, while an application specific user could be configured to allow file read access, but other could still be denied.

Useful resources:

* [What is nobody user and group?](https://unix.stackexchange.com/questions/186568/what-is-nobody-user-and-group)
* [What is the purpose of the 'nobody' user?](https://askubuntu.com/questions/329714/what-is-the-purpose-of-the-nobody-user)

</details>

<details>
<summary><b>Is there a way to redirect output to a file and have it display on stdout?</b></summary><br>

The command you want is named tee:

`foo | tee output.file`

For example, if you only care about stdout:

`ls -a | tee output.file`

If you want to include stderr, do:

`program [arguments...] 2>&1 | tee outfile`

`2>&1` redirects channel 2 (stderr/standard error) into channel 1 (stdout/standard output), such that both is written as stdout. It is also directed to the given output file as of the tee command.

Furthermore, if you want to append to the log file, use `tee -a` as:

`program [arguments...] 2>&1 | tee -a outfile`

</details>

<details>
<summary><b>What is the preferred bash shebang and why? What is the difference between executing a file using <code>./script</code> or <code>bash script</code>?</b></summary><br>

You should use `#!/usr/bin/env bash` for portability: different \*nixes put bash in different places, and using `/usr/bin/env` is a workaround to run the first bash found on the `PATH`.

Running `./script` does exactly that, and requires execute permission on the file, but is agnostic to what type of program it is. It might be a **bash script**, a **sh script**, or a **Perl**, **Python**, **awk**, or **expect script**, or an actual **binary executable**. Running `bash script` would force it to be run under `sh`, instead of anything else.

Useful resources:

* [What is the preferred Bash shebang? (original)](https://stackoverflow.com/questions/10376206/what-is-the-preferred-bash-shebang)

</details>

<details>
<summary><b>You must run command that will be performed for a very long time. How do you prevent killing this process after the ssh session drops?</b></summary><br>

Use `nohup` to make your process ignore the hangup signal:

```bash
nohup long-running-process &
exit
```

or to prevent a command from being killed after the SSH session drops, you can use **`tmux`**, a terminal multiplexer that allows you to run multiple terminal sessions and keep them running even after disconnecting from the SSH session.

Here’s how to use `tmux` to run a long-running process:

### 1. **Start a New tmux Session**

First, connect to your server via SSH and start a new `tmux` session:

```bash
tmux new -s mysession
```

Here, `mysession` is the name of the session. You can choose any name you prefer.

### 2. **Run Your Command**

Inside the tmux session, run the command that is expected to take a long time.

```bash
long_running_command
```

This command will now run inside the tmux session, independent of your SSH connection.

### 3. **Detach from the tmux Session**

To safely disconnect from the tmux session while keeping the command running in the background, **detach** from the session by pressing:

```plaintext
Ctrl + b, then d
```

This will bring you back to your original shell while leaving the long-running process active within the tmux session.

### 4. **Reconnect to the tmux Session Later**

If you lose connection or want to reconnect to your tmux session later, SSH back into the server and reattach to the session:

```bash
tmux attach -t mysession
```

This will resume the tmux session exactly where you left off, showing the progress of your long-running command.

### 5. **List Active tmux Sessions**

If you forget the session name or want to see all active tmux sessions, use:

```bash
tmux ls
```

This will display a list of active tmux sessions that you can reattach to.

</details>

<details>
<summary><b>What is the main purpose of the intermediate certification authorities?</b></summary><br>

To find out the main purpose of an intermediate CA, you should first learn about **Root CAs**, **Intermediate CAs**, and the **SSL Certificate Chain Trust**.

**Root CAs** are primary CAs which typically don’t directly sign end entity/server certificates. They issue Root certificates which are usually pre-installed within all browsers, mobiles, and applications. The private key of these certificates is used to sign other subsequent certificates called intermediate certificates. Root CAs are usually kept "offline" and in a highly secure environment with stringently limited access.

**Intermediates CAs** are CAs that subordinate to the Root CA by one or more levels, being trusted by these to sign certificates on their behalf. The purpose of creating and using Intermediate CAs is primarily for security because if the intermediate private key is compromised, then the Root CA can revoke the intermediate certificate and create a new one with a new cryptographic key pair.

**SSL Certificate Chain Trust** is the list of SSL certificates, from the root certificate to the end entity/server certificate. For an SSL Certificate to be trusted, it must be issued by a trusted CAs which is included in the trusted CA list of the connecting device (browser, mobile, and application). Therefore, the connecting device will test the trustworthiness of each SSL Certificate in the Chain Trust until it matches the one issued by a trusted CA.

The **Root-Intermediate CA** structure is created by each major CA to protect against the disastrous effects of a root key compromise. If a root key is compromised, it would render the root and all subordinated certificates untrustworthy. For this reason, creating an Intermediate CA is a best practice to ensure a rigorous protection of the primary root key.

Useful resources:

* [How certificate chains work](https://knowledge.digicert.com/solution/how-certificate-chains-work)

</details>

<details>
<summary><b>You have added several aliases to <code>.bash_profile</code>. How can you reload shell without exiting?</b></summary><br>

The best way is `exec $SHELL -l` because `exec` replaces the current process with a new one. Another solution is to simply source the file `. ~/.profile`.

Useful resources:

* [How to reload .bash_profile from the command line?](https://stackoverflow.com/questions/4608187/how-to-reload-bash-profile-from-the-command-line)

</details>

<details>
<summary><b>What are the advantages of using a reverse proxy server?</b></summary><br>

**Hide the topology and characteristics of your back-end servers**

The **reverse proxy server** can hide the presence and characteristics of the origin server. It acts as an intermediate between internet cloud and web server. It is good for security reason especially when you are using web hosting services.

**Allows transparent maintenance of backend servers**

Changes you make to servers running behind a reverse proxy are going to be completely transparent to your end users.

**Load Balancing**

The reverse proxy will then enforce a load balancing algorithm such as round-robin, weighted-round robin, least connections, weighted least connections, or random, to distribute the load among the servers in the cluster.

When a server goes down, the system will automatically failover to the next server up and users can continue with their secure file transfer activities.

**SSL offloading/termination**

Handles incoming HTTPS connections, decrypting the requests and passing unencrypted requests on to the web servers.

**IP masking**

Using a single ip but different URLs to route to different back end servers.

Useful resources:

* [The Benefits of a Reverse Proxy](https://dzone.com/articles/benefits-reverse-proxy)

</details>

<details>
<summary><b>Is there an easy way to search inside 1000s of files in a complex directory structure to find files which contain a specific string?</b></summary><br>

For example use `fgrep`:

```bash
fgrep * -R "string"
```

or:

```bash
grep -insr "pattern" *
```

* `-i` ignore case distinctions in both the **PATTERN** and the input files
* `-n`  prefix each line of output with the 1-based line number within its input file
* `-s` suppress error messages about nonexistent or unreadable files.
* `-r` read all files under each directory, recursively.

Useful resources:

* [How to grep a string in a directory and all its subdirectories files in LINUX?](https://stackoverflow.com/questions/15622328/how-to-grep-a-string-in-a-directory-and-all-its-subdirectories-files-in-linux)

</details>

<details>
<summary><b>How do you find out what dynamic libraries executables load when run?</b></summary><br>

You can do this with `ldd` command:

```bash
ldd /bin/ls
```

</details>

<details>
<summary><b>What is the difference between a container and a VM? Mention some benefits of each.</b></summary><br>

A container is a lightweight, portable software package that includes everything an application needs to run, such as code, libraries, and dependencies, but shares the host OS kernel. A virtual machine (VM), on the other hand, is a complete operating system with its own kernel that runs on top of a hypervisor or virtualization layer.

Some benefits of containers include:

* Efficiency: Containers are lightweight and share the host OS kernel, so they require fewer resources and have faster startup times than VMs.
* Portability: Containers can run on any system that supports containerization, making them easy to move between development, testing, and production environments.
* Consistency: Containers ensure that an application runs the same way in any environment, eliminating the "works on my machine" problem.
* Scalability: Containers are designed to be scalable and can be easily orchestrated with tools like Kubernetes.

Some benefits of VMs include:

* Isolation: VMs provide complete isolation between applications and the host OS, making them more secure.
* Flexibility: VMs can run different operating systems and versions, making them useful for testing and compatibility purposes.
* Robustness: VMs have a proven track record of stability and reliability.

Useful resources:

* [RedHat: Containers vs VMs](https://www.redhat.com/en/topics/containers/containers-vs-vms)

</details>

<details>
<summary><b>Why wouldn't hostnames resolve on your server and how would you troubleshoot the issue?</b></summary><br>

Some possible reasons and troubleshooting steps to resolve the issue are:

* DNS server misconfiguration: Check if the server is configured to use the correct DNS server and if the DNS server is working correctly. You can check this by using the "nslookup" command to look up a hostname and see if it resolves to the correct IP address. If the DNS server is misconfigured, correct the configuration or use a different DNS server.

* Incorrect hostname resolution order: Check the hostname resolution order on the server. This can be checked by examining the /etc/nsswitch.conf file. Make sure that the desired method for hostname resolution is listed first.

* Firewall blocking DNS traffic: Check if the firewall on the server is blocking DNS traffic. You can check this by temporarily disabling the firewall and testing if hostname resolution works. If it does, then the firewall is the issue, and you need to allow DNS traffic through it.

* DNS cache issues: Check if the DNS cache on the server is causing issues. You can clear the cache using the "systemd-resolve --flush-caches" command.

* Incorrect DNS record: Check if the DNS record for the hostname is correct. This can be done by using the "dig" or "nslookup" command and checking if the DNS record for the hostname matches the expected IP address.

* Network connectivity issues: Check if there are any network connectivity issues that are preventing the server from accessing the DNS server. This can be done by using the "ping" command to check if the server can communicate with the DNS server.

</details>

#### Network Questions

<details>
<summary><b>What is Boot to LAN?</b></summary><br>

Boot to LAN is most often used when you are doing a fresh install on a system. What you would do is setup a network-based installer capable of network-booting via PXE. Boot to LAN enables this by allowing a pre-boot environment to look for a DHCP server and connect to the broadcasting network installation server. Environments that have very large numbers of systems more often than not have the capability of pushing out images via the network. This reduces the amount of hands-on time that is required on each system, and keeps the installs more consistent.

</details>

<details>
<summary><b>What is the difference between the Internet, Intranet, and Extranet?</b></summary><br>

The terminologies Internet, Intranet, and Extranet are used to define how the applications in the network can be accessed. They use similar TCP/IP technology but differ in terms of access levels for each user inside the network and outside the network.

* Internet: Applications are accessed by anyone from any location using the web.
* Intranet: It allows limited access to users in the same organization.
* Extranet: External users are allowed or provided with access to use the network application of the organization.

</details>

<details>
<summary><b>What is a packet filter and how does it work?</b></summary><br>

**Packet filtering** is a firewall technique used to control network access by monitoring outgoing and incoming packets and allowing them to pass or halt based on the source and destination Internet Protocol (IP) addresses, protocols and ports.

Packet filtering is appropriate where there are modest security requirements. The internal (private) networks of many organizations are not highly segmented. Highly sophisticated firewalls are not necessary for isolating one part of the organization from another.

However, it is prudent to provide some sort of protection of the production network from a lab or experimental network. A packet filtering device is a very appropriate measure for providing isolation of one subnet from another.

Operating at the network layer and transport layer of the TCP/IP protocol stack, every packet is examined as it enters the protocol stack. The network and transport headers are examined closely for the following information:

* **protocol (IP header, network layer)** - in the IP header, byte 9 (remember the byte count begins with zero) identifies the protocol of the packet. Most filter devices have the capability to differentiate between TCP, UPD, and ICMP.
* **source address (IP header, network layer)** - the source address is the 32-bit IP address of the host which created the packet.
* **destination address (IP header, network layer)** - the destination address is the 32-bit IP address of the host the packet is destined for.
* **source port (TCP or UDP header, transport layer)** - each end of a TCP or UDP network connection is bound to a port. TCP ports are separate and distinct from UDP ports. Ports numbered below 1024 are reserved – they have a specifically defined use. Ports numbered above 1024 (inclusive) are known as ephemeral ports. They can be used however a vendor chooses. For a list of "well known" ports, refer to RFP1700. The source port is a pseudo-randomly assigned ephemeral port number. Thus, it is often not very useful to filter on the source port.
* **destination port (TCP or UDP header, transport layer)** - the destination port number indicates a port that the packet is sent to. Each service on the destination host listens to a port. Some well-known ports that might be filtered are 20/TCP and 21/TCP - ftp connection/data, 23/TCP - telnet, 80/TCP - http, and 53/TCP - DNS zone transfers.
* **connection status (TCP header, transport layer)** - the connection status tells whether the packet is the first packet of the network session. The ACK bit in the TCP header is set to “false” or 0 if this is the first packet in the session. It is simple to disallow a host from establishing a connection by rejecting or discarding any packets which have the ACK bit set to "false" or 0.

Useful resources:

* [How does a packet filters work?](https://www.tutorialspoint.com/how-does-a-packet-filters-work)

</details>

<details>
<summary><b>What is a VPN? Describe briefly how it works.</b></summary><br>

A VPN, or virtual private network, is a network technology that allows users to establish a secure and encrypted connection over a public network, such as the internet.

When a user connects to a VPN, their device creates a secure tunnel between the user's device and the VPN server. All traffic that passes through this tunnel is encrypted and protected from unauthorized access or interception.

This encrypted tunnel allows users to access resources on the private network, such as files or applications, as if they were directly connected to the network. It also allows users to access the internet securely, without revealing their true location or IP address.

VPNs can be used to provide remote access for employees who need to access company resources while working from home or traveling, as well as to protect personal information and online activities from surveillance or monitoring.

</details>

<details>
<summary><b>According to an HTTP monitor, a website is down. You're able to telnet to the port, so how do you resolve it?</b></summary><br>

If you can telnet to the port, this means that the service listening on the port is running, and you can connect to it (it's not a networking problem). It is good to check this way for the IP address to which the domain is resolved and using the same domain to test connection.

First of all check if your site is online from another location. It then lets you know if the site is down everywhere, or if only your network is unable to view it. It is also a good idea to check what the web browser returns.

**If only IP connection working**

* you can use whois to see what DNS servers serve up the hostname to the site: `whois www.example.com`
* you can use tools like `dig` or `host` to test DNS to see if the host name is resolving: `host www.example.org dns.example.org`
* you can also check global public dns servers: `host www.example.com 9.9.9.9`

If domain not resolved it's probably problem with DNS servers.

**If domain resolved properly**

* investigate the log files and resolve the issue regarding the logs, it's the best way to show what's wrong
* check the http status code, usually it will be the response with the 5xx, maybe server is overload because clients making lots of connection to the website or specific url? maybe your caching rules not working properly?
* check web/proxy server configuration (e.g. `nginx -t -c </path/to/nginx.conf>`), maybe another sysadmin has made some changes to the domain configuration?
* maybe something on the server has crashed? maybe run out of space or run out of memory?
* maybe it's a programming error on the website?

</details>

<details>
<summary><b>Load balancing can positively impact server performance. Discuss several load balancing mechanisms.</b></summary><br>

Load balancing is the process of distributing network or application traffic across multiple servers to ensure no single server becomes overwhelmed, which improves performance, reliability, and availability. There are several load balancing mechanisms, each suited to different types of workloads and traffic patterns. Here's a discussion of the key load balancing techniques:

### 1. **Round Robin**

* **Mechanism**: In this method, requests are distributed across servers in a sequential and circular order. The first request goes to the first server, the second request to the second server, and so on. Once all servers have received a request, the cycle starts again.
* **Use Case**: Round Robin is ideal for environments where the servers have similar hardware and can handle roughly the same load.
* **Advantages**:
  * Simple to implement.
  * Does not require knowledge of server load.
* **Disadvantages**:
  * Does not account for server performance or current load, which can lead to performance degradation if one server is slower than the others or has more tasks to handle.

### 2. **Weighted Round Robin**

* **Mechanism**: Similar to Round Robin, but each server is assigned a weight based on its capacity. Servers with higher capacity (e.g., more CPU or memory) receive more requests, while those with lower capacity receive fewer requests.
* **Use Case**: Ideal when servers have different hardware configurations and processing capabilities, ensuring that more powerful servers handle more traffic.
* **Advantages**:
  * Distributes traffic more evenly according to server capacity.
  * Helps balance load in heterogeneous server environments.
* **Disadvantages**:
  * Still doesn’t take real-time server performance or load into account.

### 3. **Least Connections**

* **Mechanism**: The load balancer directs traffic to the server with the fewest active connections at any given time. This method assumes that servers with fewer connections can handle more load and therefore receive more traffic.
* **Use Case**: Suitable for environments where each client connection generates a different amount of load, such as when clients use persistent or long-lived connections.
* **Advantages**:
  * Balances traffic based on real-time connection load.
* **Disadvantages**:
  * Requires more overhead to track the number of connections per server.

### 4. **Weighted Least Connections**

* **Mechanism**: Combines the Weighted Round Robin and Least Connections algorithms. Servers are weighted based on their capacity, but traffic is distributed according to the number of active connections and server weight. Servers with fewer connections relative to their capacity receive more traffic.
* **Use Case**: Ideal when servers have different capacities, and connection load varies significantly.
* **Advantages**:
  * More efficient in balancing load based on both server capacity and connection count.
* **Disadvantages**:
  * Requires more overhead to monitor connection counts and server capacities.

### 5. **IP Hash (Source IP Hashing)**

* **Mechanism**: The load balancer uses a hash function based on the client’s IP address to determine which server will handle the request. The same client will always be directed to the same server as long as the server is available.
* **Use Case**: Useful when session persistence or "sticky sessions" are required, where clients need to be consistently directed to the same server (e.g., for stateful applications).
* **Advantages**:
  * Ensures that clients are always routed to the same server, helping with session persistence.
* **Disadvantages**:
  * If a server fails, session data can be lost unless additional mechanisms (like session replication) are used.
  * Not ideal if load distribution is a priority, as traffic may become unevenly distributed depending on the source IP distribution.

### 6. **Least Response Time**

* **Mechanism**: The load balancer monitors the response time of each server and sends traffic to the server that has the quickest response time. This ensures that servers that are responding more efficiently receive more traffic.
* **Use Case**: Useful for environments where response time is critical, and the load balancer needs to ensure that requests are sent to the least busy or fastest server.
* **Advantages**:
  * Accounts for server load and performance in real-time.
* **Disadvantages**:
  * Requires more overhead to monitor response times and adjust routing decisions accordingly.

### 7. **Geolocation-Based Load Balancing**

* **Mechanism**: Traffic is routed based on the geographic location of the client. The load balancer directs traffic to the nearest or most appropriate data center or server to reduce latency.
* **Use Case**: Useful for global applications or services with geographically distributed servers or data centers, such as CDNs (Content Delivery Networks).
* **Advantages**:
  * Minimizes latency by routing traffic to the closest server.
  * Helps improve user experience, especially for latency-sensitive applications.
* **Disadvantages**:
  * Does not consider server load, only geographic proximity, which can lead to imbalanced traffic if one location experiences much higher demand.

### 8. **Randomized Load Balancing**

* **Mechanism**: Traffic is randomly distributed to any of the available servers. Each request has an equal chance of going to any server, regardless of load or capacity.
* **Use Case**: This method is simple and rarely used alone in production environments but may be useful for very small, homogenous environments where load distribution is not a major concern.
* **Advantages**:
  * Easy to implement.
* **Disadvantages**:
  * Does not account for server capacity or current load, which can result in uneven distribution and performance bottlenecks.

### 9. **Global Server Load Balancing (GSLB)**

* **Mechanism**: GSLB distributes traffic across multiple geographically distributed data centers or servers based on various factors, such as proximity, server load, or response time.
* **Use Case**: Ideal for multinational companies or services that have data centers or cloud resources across the world and need to optimize traffic routing to improve performance and redundancy.
* **Advantages**:
  * Increases availability and fault tolerance by distributing traffic globally.
  * Can optimize for performance by considering both proximity and load.
* **Disadvantages**:
  * Requires more complex infrastructure, including DNS routing and monitoring.

### 10. **Dynamic Load Balancing**

* **Mechanism**: Traffic distribution decisions are made based on real-time server health and performance metrics, such as CPU load, memory usage, or disk I/O. The load balancer dynamically adjusts based on the state of the servers.
* **Use Case**: Best for high-performance environments where server load can fluctuate significantly, such as in cloud services or microservice architectures.
* **Advantages**:
  * Provides efficient load balancing by adjusting dynamically based on server performance.
  * Helps prevent overloading any server.
* **Disadvantages**:
  * High overhead in monitoring server health in real-time.

</details>

<details>
<summary><b>Explain difference between HTTP 1.1 and HTTP 2.0.</b></summary><br>

One of the major differences between HTTP 1.1 and HTTP 2.0 is how they handle data transfer. HTTP 1.1 relies on a serial transfer of data, which means that it can only send one request at a time, waiting for the response before sending the next request. This can result in a delay in loading web pages, particularly for sites with a lot of small files.

HTTP 2.0, on the other hand, uses a binary protocol and allows for multiple requests to be sent at the same time, in parallel. It also compresses headers and reduces the number of round trips required to establish a connection, which further speeds up the process of loading web pages.

Another significant difference between the two protocols is that HTTP 2.0 supports server push, which allows the server to send resources to the client before they are requested. This feature can further improve the loading speed of web pages.

Useful resources:

* [What is HTTP/2 - The Ultimate Guide](https://kinsta.com/learn/what-is-http2/)

</details>

<details>
<summary><b>What is handshake mechanism and why do we need 3 way handshake?</b></summary><br>

**Handshaking** begins when one device sends a message to another device indicating that it wants to establish a communications channel. The two devices then send several messages back and forth that enable them to agree on a communications protocol.

A **three-way handshake** is a method used in a TCP/IP network to create a connection between a local host/client and server. It is a three-step method that requires both the client and server to exchange `SYN` and `ACK` (`SYN`, `SYN-ACK`, `ACK`) packets before actual data communication begins.

Useful resources:

* [Why do we need a 3-way handshake? Why not just 2-way?](https://networkengineering.stackexchange.com/questions/24068/why-do-we-need-a-3-way-handshake-why-not-just-2-way)

</details>

<details>
<summary><b>Why is UDP faster than TCP?</b></summary><br>

UDP is often faster than TCP because it has a much simpler and less error-checking mechanism than TCP. UDP does not establish a connection, does not guarantee data delivery, and does not provide error-checking or retransmission of lost packets. Instead, UDP simply sends packets of data to the recipient and expects the recipient to process them in the correct order.

This lack of error-checking and retransmission makes UDP faster than TCP in some cases, as there is less overhead associated with managing the connection and ensuring that all packets are delivered.

Useful resources:

* [UDP vs TCP, how much faster is it?](https://stackoverflow.com/questions/47903/udp-vs-tcp-how-much-faster-is-it)

</details>

<details>
<summary><b>Which, in your opinion, are the 5 most important OpenSSH parameters that improve the security?</b></summary><br>

Here are the **five most important OpenSSH parameters** to improve security, along with their explanations and why they are critical:

### 1. **`PermitRootLogin no`**

* **Description**: Disables root login over SSH.
* **Why it's important**: Allowing root to log in via SSH poses a significant security risk since the root account has full control over the system. Disabling it forces users to log in with their own accounts and use `sudo` or `su` for elevated privileges. This adds a layer of security and accountability.
* **How to configure**: Edit `/etc/ssh/sshd_config` and set:

     ```bash
     PermitRootLogin no
     ```

### 2. **`PasswordAuthentication no`**

* **Description**: Disables password-based login, enforcing the use of more secure methods such as public key authentication.
* **Why it's important**: Password-based logins are vulnerable to brute-force attacks. By disabling password authentication, you force users to authenticate using SSH keys, which are significantly more secure and harder to crack.
* **How to configure**: Edit `/etc/ssh/sshd_config` and set:

     ```bash
     PasswordAuthentication no
     ```

### 3. **`AllowUsers` or `AllowGroups`**

* **Description**: Restricts which users or groups can log in via SSH.
* **Why it's important**: Limiting which users can access the server via SSH reduces the attack surface by preventing unauthorized or unnecessary users from attempting to log in.
* **How to configure**: You can specify the users or groups allowed to access the server by adding these directives:

     ```bash
     AllowUsers user1 user2
     ```

     Or:

     ```bash
     AllowGroups sshusers admin
     ```

### 4. - **`LoginGraceTime 60`**

* **Description**: Reduces the time allowed for login attempts, minimizing the time an attacker has to brute force login credentials.

  ```bash
  LoginGraceTime 60
  ```

### 5. **`MaxAuthTries 3`**

* **Description**: Limits the number of authentication attempts per connection.
* **Why it's important**: By limiting the number of authentication attempts, you reduce the window for brute-force attacks. After the limit is reached, the SSH connection is closed, forcing the attacker to reconnect and start over.
* **How to configure**: Edit `/etc/ssh/sshd_config` and set:

     ```bash
     MaxAuthTries 3
     ```

Useful resources:

* [OpenSSH security and hardening](https://linux-audit.com/audit-and-harden-your-ssh-configuration/)

</details>

<details>
<summary><b>What is NAT? What is it used for?</b></summary><br>

It enables private IP networks that use unregistered IP addresses to connect to the Internet. **NAT** operates on a router, usually connecting two networks together, and translates the private (not globally unique) addresses in the internal network into legal addresses, before packets are forwarded to another network.

Workstations or other computers requiring special access outside the network can be assigned specific external IPs using **NAT**, allowing them to communicate with computers and applications that require a unique public IP address. **NAT** is also a very important aspect of firewall security.

Useful resources:

* [Network Address Translation (NAT) Concepts](http://www.firewall.cx/networking-topics/network-address-translation-nat/227-nat-concepts.html)

</details>

<details>
<summary><b>What is the purpose of Spanning Tree?</b></summary><br>

This protocol operates at layer 2 of the OSI model with the purpose of preventing loops on the network. Without **STP**, a redundant switch deployment would create broadcast storms that cripple even the most robust networks. There are several iterations based on the original IEEE 802.1D standard; each operates slightly different from the others while largely accomplishing the same loop-free goal.

</details>

<details>
<summary><b>How do you check which ports are listening?</b></summary><br>

Use the:

* `lsof -i`
* `ss -l`
* `netstat -atn` (for tcp)
* `netstat -aun` (for udp)
* `netstat -tulapn`

</details>

<details>
<summary><b>What mean <code>Host key verification failed</code> when you connect to the remote host? Do you accept it automatically?</b></summary><br>

`Host key verification failed` means that the host key of the remote host was changed. This can easily happen when connecting to a computer whose host keys in `/etc/ssh` have changed if that computer was upgraded without copying its old host keys. The host keys here are proof when you reconnect to a remote computer with ssh that you are talking to the same computer you connected to the first time you accessed it.

Whenever you connect to a server via SSH, that server's public key is stored in your home directory (or possibly in your local account settings if using a Mac or Windows desktop) file called **known_hosts**. When you reconnect to the same server, the SSH connection will verify the current public key matches the one you have saved in your **known_hosts** file. If the server's key has changed since the last time you connected to it, you will receive the above error.

Don't delete the entire **known_hosts** file as recommended by some people, this totally voids the point of the warning. It's a security feature to warn you that a man in the middle attack may have happened.

Before accepting the new host key, contact your/other system administrator for verification.

Useful resources:

* [Git error: "Host Key Verification Failed" when connecting to remote repository](https://stackoverflow.com/questions/13363553/git-error-host-key-verification-failed-when-connecting-to-remote-repository)

</details>

<details>
<summary><b>How do you connect to a mail server using <code>nc</code> (netcat)?</b></summary><br>

`nc mail.example.com 25`

SMTP Conversation:
After connecting, you should receive a 220 response code, indicating the server is ready. From there, you can manually type in SMTP commands to simulate an email transaction:

```HELO myhostname.com
MAIL FROM:<sender@example.com>
RCPT TO:<recipient@example.com>
DATA
Subject: Test mail from netcat
This is a test email sent from netcat.
.
QUIT
```

Each SMTP command should result in a response from the server, typically beginning with a 250 response code indicating success.

</details>

<details>
<summary><b>How do you kill program using e.g. 80 port in Linux?</b></summary><br>

To list any process listening to the port 80:

```bash
# with lsof
lsof -i:80

# with fuser
fuser 80/tcp
```

To kill any process listening to the port 80:

```bash
kill $(lsof -t -i:80)
```

or more violently:

```bash
kill -9 $(lsof -t -i:80)
```

or with `fuser` command:

```bash
fuser -k 80/tcp
```

Useful resources:

* [How to kill a process running on particular port in Linux?](https://stackoverflow.com/questions/11583562/how-to-kill-a-process-running-on-particular-port-in-linux/32592965)
* [Finding the PID of the process using a specific port?](https://unix.stackexchange.com/questions/106561/finding-the-pid-of-the-process-using-a-specific-port)

</details>

<details>
<summary><b>You get <code>curl: (56) TCP connection reset by peer</code>. What steps will you take to solve this problem?</b></summary><br>

* check if the URL is correct, maybe you should add `www` or set correctly `Host:` header? Check also scheme (http or https)
* check the domain is resolving into a correct IP address
* enable debug tracing with `--trace-ascii curl.dump`. `Recv failure` is a really generic error, so it's hard for more info
* use external proxy with `--proxy` for debug connection from external ip
* use network sniffer (e.g. `tcpdump`) for debug connection in the lower TCP/IP layers
* check firewall rules on the production environment and on the exit point of your network, also check your NAT rules
* check MTU size of packets traveling over your network
* check SSL version with ssl/tls `curl` params if you are connecting to the HTTPS protocol
* it may be a problem on the client side e.g. the netfilter drop or limit  connections from your IP address to the domain

Useful resources:

* [CURL ERROR: Recv failure: Connection reset by peer - PHP Curl](https://stackoverflow.com/questions/10285700/curl-error-recv-failure-connection-reset-by-peer-php-curl)

</details>

<details>
<summary><b>How do you allow traffic to/from specific IP with firewalld?</b></summary><br>

To allow traffic to or from a specific IP address using `firewalld`, you can configure rules that permit access based on the source or destination IP. Firewalld operates using **zones**, so you need to ensure the rule is applied to the correct zone where your interface resides.

Here’s how to allow traffic to/from a specific IP address in `firewalld`:

### 1. **Allow Traffic From a Specific IP (Source IP)**

This rule allows incoming traffic from a specific IP address. You can apply this rule globally or to a specific zone.

* To allow traffic from a specific IP (e.g., `192.168.1.100`), use:

```bash
sudo firewall-cmd --zone=public --add-source=192.168.1.100
```

* To make the rule persistent across reboots, add `--permanent`:

```bash
sudo firewall-cmd --zone=public --add-source=192.168.1.100 --permanent
```

* Reload the firewall to apply permanent changes:

```bash
sudo firewall-cmd --reload
```

This command adds the IP `192.168.1.100` as a trusted source in the specified zone (`public` in this example).

### 2. **Allow Traffic to a Specific IP (Destination IP)**

To allow outgoing traffic to a specific IP address, use a rich rule. This allows finer control over traffic permissions.

* To allow traffic to a specific destination IP (e.g., `203.0.113.100`), use:

```bash
sudo firewall-cmd --zone=public --add-rich-rule='rule family="ipv4" destination address="203.0.113.100" accept'
```

* To make it persistent:

```bash
sudo firewall-cmd --zone=public --add-rich-rule='rule family="ipv4" destination address="203.0.113.100" accept' --permanent
```

* Reload the firewall:

```bash
sudo firewall-cmd --reload
```

### 3. **Allow Traffic to/from a Specific IP on Specific Ports**

If you need to allow traffic to/from a specific IP only on certain ports, you can specify both the IP address and the port.

* For example, to allow traffic from `192.168.1.100` on port `22` (SSH):

```bash
sudo firewall-cmd --zone=public --add-rich-rule='rule family="ipv4" source address="192.168.1.100" port protocol="tcp" port="22" accept'
```

* To make it persistent:

```bash
sudo firewall-cmd --zone=public --add-rich-rule='rule family="ipv4" source address="192.168.1.100" port protocol="tcp" port="22" accept' --permanent
```

* Reload the firewall:

```bash
sudo firewall-cmd --reload
```

### 4. **Checking and Verifying the Rules**

* List all current rules for a specific zone to verify that the rules are applied:

```bash
sudo firewall-cmd --zone=public --list-all
```

This will display all the allowed sources, services, and rich rules applied to the `public` zone.

</details>

<details>
<summary><b>Explain four types of responses from firewall when scanning with <code>nmap</code>.</b></summary><br>

There might be four types of responses:

* **Open port** - few ports in the case of the firewall
* **Closed port** - most ports are closed because of the firewall
* **Filtered** - `nmap` is not sure whether the port is open or not
* **Unfiltered** - `nmap` can access the port but is still confused about the open status of the port

Useful resources:

* [NMAP - Closed vs Filtered](https://security.stackexchange.com/questions/182504/nmap-closed-vs-filtered)

</details>

<details>
<summary><b>What does <code>tcpdump</code> do and what are some examples for its use?</b></summary><br>

Tcpdump is a command-line packet analyzer tool that is used for network troubleshooting, analysis, and security auditing. It captures packets that are being transmitted or received over a network interface and displays detailed information about the packets, such as the source and destination addresses, protocols, ports, and payload.

`tcpdump` puts your network card into promiscuous mode, which basically tells it to accept every packet it receives. It allows the user to see all traffic being passed over the network.

Some examples of how tcpdump can be used include:

* Troubleshooting network connectivity issues: Tcpdump can be used to capture packets on a network interface to diagnose connectivity issues, such as dropped packets, slow response times, and incorrect routing.
* Monitoring network traffic: Tcpdump can be used to monitor network traffic for suspicious or unauthorized activity, such as malware infections, network attacks, and data breaches.
* Analyzing network protocols: Tcpdump can be used to analyze network protocols and their behavior, such as TCP/IP, DNS, DHCP, and HTTP.
* Debugging network applications: Tcpdump can be used to debug network applications, such as web servers, mail servers, and VoIP applications, by capturing and analyzing packets exchanged between the client and server.
* Auditing network security: Tcpdump can be used to audit network security by capturing packets and analyzing them for security vulnerabilities, such as weak passwords, unencrypted traffic, and unauthorized access.

</details>

#### Devops Questions

<details>
<summary><b>What some of the top DevOps tools? How do all these tools work together?</b></summary><br>

The most popular DevOps tools are mentioned below:

* **Git** : Version Control System tool
* **Jenkins** : Continuous Integration tool
* **Selenium** : Continuous Testing tool
* **Puppet**, **Chef**, **Ansible** : Configuration Management and Deployment tools
* **Nagios**, **Zabbix** : Continuous Monitoring tool
* **Docker** : Containerization tool

* Developers develop the code and this source code is managed by Version Control System tools like Git etc.
* Developers send this code to the Git repository and any changes made in the code is committed to this Repository
* Jenkins pulls this code from the repository using the Git plugin and build it using tools like Ant or Maven
* Configuration management tools like puppet deploys & provisions testing environment and then Jenkins releases this code on the test environment on which testing is done using tools like selenium
* Once the code is tested, Jenkins send it for deployment on the production server (even production server is provisioned & maintained by tools like puppet)
* After deployment It is continuously monitored by tools like Nagios
* Docker containers provides testing environment to test the build features

</details>

<details>
<summary><b>What is Agile and how is it beneficial?</b></summary><br>

### What is Agile?

**Agile** is a project management and software development methodology that promotes an iterative, flexible, and collaborative approach to delivering high-quality software or products. Agile focuses on incremental progress, continuous feedback, and the ability to adapt to changing requirements quickly. It emphasizes collaboration between cross-functional teams and stakeholders and encourages frequent reassessment of project goals and priorities.

Agile frameworks, such as **Scrum**, **Kanban**, and **Extreme Programming (XP)**, guide how Agile is implemented in practice, but the core principles are defined by the **Agile Manifesto**, which prioritizes:

* **Individuals and interactions** over processes and tools
* **Working software** over comprehensive documentation
* **Customer collaboration** over contract negotiation
* **Responding to change** over following a plan

### Key Agile Practices

1. **Iterations/Sprints**: Short cycles of development (typically 1-4 weeks) during which teams deliver a potentially shippable product increment.
2. **Continuous Feedback**: Regular feedback from stakeholders and customers to ensure the project remains aligned with evolving requirements.
3. **Collaboration**: Close cooperation between team members, including developers, testers, and product owners.
4. **Adaptability**: Ability to change project scope and direction based on real-time feedback and changing requirements.
5. **Daily Stand-ups**: Short, daily meetings where the team discusses progress, obstacles, and goals for the day.

****

### Benefits of Agile

1. **Flexibility and Adaptability**:
   * Agile's iterative approach allows teams to adapt to changes in requirements or market conditions more easily. This is particularly useful in dynamic environments where customer needs may evolve during the development process.

2. **Improved Product Quality**:
   * By breaking the project into smaller increments and regularly testing and reviewing each piece, Agile enables early detection and resolution of bugs and issues, leading to better overall product quality.

3. **Faster Time-to-Market**:
   * Agile’s incremental approach enables teams to deliver functional versions of the product more quickly, allowing stakeholders and users to see value earlier and get the product to market faster.

4. **Customer Satisfaction**:
   * Continuous collaboration with customers ensures their feedback is incorporated throughout the development process. This leads to a product that better meets customer expectations, improving overall satisfaction.

5. **Increased Transparency**:
   * Agile promotes transparency through regular communication, such as daily stand-ups, sprint reviews, and retrospectives. Stakeholders are kept informed about progress and challenges, creating a sense of shared ownership.

6. **Risk Management**:
   * By delivering small increments regularly and getting constant feedback, teams can identify risks and issues early, allowing them to address problems before they escalate.

7. **Team Empowerment and Collaboration**:
   * Agile encourages self-organizing teams, where team members have more autonomy and are empowered to make decisions. This fosters a collaborative environment where each member contributes to the project's success.

8. **Continuous Improvement**:
   * Agile promotes a culture of continuous improvement through regular retrospectives, where teams reflect on what went well and what could be improved, leading to better processes over time.

9. **Higher Productivity**:
   * Short development cycles and focused sprints help teams stay on track, avoid delays, and deliver value efficiently. Agile's iterative nature also means that the team focuses on high-priority tasks, improving productivity.

10. **Better Alignment with Business Goals**:
    * Agile encourages close collaboration with product owners and stakeholders, ensuring that the team’s efforts are aligned with business priorities and delivering real value.

</details>

<details>
<summary><b>What is Continuous Integration and Continous Deployment?</b></summary><br>

Continuous Integration (CI) and Continuous Deployment (CD) are modern software development practices that are part of the DevOps methodology. They focus on automating the software delivery process to improve speed, consistency, and reliability.

**Continuous Integration (CI)**:

Continuous Integration is the practice of frequently integrating code changes into a shared repository. With CI, each integration (i.e., code commit) is automatically tested to detect and rectify integration errors as quickly as possible. The key principles of CI are:

1. **Frequent Commits**: Developers integrate their changes multiple times a day.
2. **Automated Testing**: Upon each integration, automated tests run to ensure that new changes do not break existing functionality or introduce new bugs.
3. **Immediate Feedback**: Developers receive immediate feedback on the success or failure of their changes.
4. **Maintain a Single Source Repository**: All code changes are stored in a version control system, ensuring a single source of truth.
5. **Consistent Build Process**: Ensure the build process is consistent and reproducible.

**Continuous Deployment (CD)**:

Continuous Deployment is an extension of Continuous Delivery, a practice where every change in the software, after passing through the CI process, is automatically deployed to production without human intervention.

1. **Automated Deployments**: Every change that passes CI tests is automatically deployed to production.
2. **Quick Release Cycle**: With CD, software can be released in minutes, ensuring features, bug fixes, and other changes reach users rapidly.
3. **Reliable Releases**: Automated testing and deployment processes ensure that releases are consistent and reliable.
4. **Rollbacks**: In case of an issue, the process should support quick rollbacks to restore service.

It's worth noting the difference between Continuous Delivery and Continuous Deployment:

**Continuous Delivery**: Ensures that the software can be released at any time. It stops short of pushing changes to production automatically. Instead, the final deployment step requires manual approval.

**Continuous Deployment**: Doesn't require human intervention and pushes changes to production automatically once they've passed automated tests.

</details>

#### Cybersecurity Questions

<details>
<summary><b>What are salted hashes?</b></summary><br>

**Salt** at its most fundamental level is random data. When a properly protected password system receives a new password, it will create a hashed value for that password, create a new random salt value, and then store that combined value in its database. This helps defend against dictionary attacks and known hash attacks.

For example, if a user uses the same password on two different systems, if they used the same hashing algorithm, they could end up with the same hash value. However, if even one of the systems uses salt with its hashes, the values will be different.

The encrypted passwords in `/etc/shadow` file are stored in the following format:

```bash
$ID$SALT$ENCRYPTED
```

The `$ID` indicates the type of encryption, the `$SALT` is a random string (up to 16 characters) and `$ENCRYPTED` is a password’s hash.

</details>

<details>
<summary><b>Explain the four types of access control.</b></summary><br>

Access control is a security mechanism used to restrict or allow access to resources based on various criteria. There are four main types of access control:

* Mandatory Access Control (MAC): MAC is a strict form of access control that is typically used in high-security environments, such as government and military organizations. It enforces a centralized security policy that dictates who can access which resources based on their security clearance level.
* Discretionary Access Control (DAC): DAC is a more flexible form of access control that allows users to set permissions on their own resources. In DAC, each resource has an owner who determines who can access it and at what level of access.
* Role-Based Access Control (RBAC): RBAC is a popular access control model used in large organizations with many users and resources. It assigns users to roles based on their job function or responsibilities, and then grants access permissions to those roles. This simplifies access management and reduces the risk of human error or intentional abuse.
* Attribute-Based Access Control (ABAC): ABAC is a newer form of access control that is based on a set of attributes or properties, such as user identity, location, time of day, and device type. It uses a rules engine to evaluate these attributes and determine access permissions for each resource. ABAC is more fine-grained than RBAC, but also more complex to set up and manage.

</details>

<details>
<summary><b>What are some golden rules for reducing the impact of hacked system.</b></summary><br>

1) **The principle of least privilege**

You should configure services to run as a user with the least possible rights necessary to complete the service's tasks. This can contain a hacker even after they break in to a machine.

As an example, a hacker breaking into a system using a zero-day exploit of the Apache webserver service is highly likely to be limited to just the system memory and file resources that can be accessed by that process. The hacker would be able to download your html and php source files, and probably look into your mysql database, but they should not be able to get root or extend their intrusion beyond apache-accessible files.

Many default Apache webserver installations create the 'apache' user and group by default, and you can easily configure the main Apache configuration file (`httpd.conf`) to run apache using those groups.

2) **The principle of separation of privileges**

If your website only needs read-only access to the database, then create an account that only has read-only permissions, and only to that database.

**SElinux** is a good choice for creating context for security, `app-armor` is another tool. **Bastille** was a previous choice for hardening.

Reduce the consequence of any attack, by separating the power of the service that has been compromised into it own "Box".

3) **Whitelist, don't blacklist**

You're describing a blacklist approach. A whitelist approach would be much safer.

An exclusive club will never try to list everyone who can't come in; they will list everyone who can come in and exclude those not on the list.

Similarly, trying to list everything that shouldn't access a machine is doomed. Restricting access to a short list of programs/IP addresses/users would be more effective.

Of course, like anything else, this involves some trade-offs. Specifically, a whitelist is massively inconvenient and requires constant maintenance.

To go even further in the tradeoff, you can get great security by disconnecting the machine from the network.

**Also interesting are**:

Use the tools available. It's highly unlikely that you can do as well as the guys who are security experts, so use their talents to protect yourself.

* public key encryption provides excellent security
* enforce password complexity
* understand why you are making exceptions to the rules above - review your exceptions regularly
* hold someone to account for failure, it keeps you on your toes

Useful resources:

* [How to prevent zero day attacks (original)](https://serverfault.com/questions/391370/how-to-prevent-zero-day-attacks)

</details>

<details>
<summary><b>Developer uses private key on the server to deploy app through ssh. Why is this a security risk and what is the better, but not ideal, solution in such situations?</b></summary><br>

You have the private key for your personal account. The server needs your public key so that it can verify that your private key for the account you are trying to use is authorized.

The whole point with private keys is that they are private, meaning only you have your private key. If someone takes over your private key, it will be able to impersonate you any time he wants.

A better solutions is the use of ssh key forwarding. An essence, you need to create a `~/.ssh/config` file, if it doesn't exist. Then, add the hosts (either domain name or IP address in the file and set `ForwardAgent yes`). Example:

```bash
Host git.example.com
    User john
    PreferredAuthentications publickey
    IdentityFile ~/.ssh/id_rsa.git.example.com
    ForwardAgent yes
```

Your remote server must allow SSH agent forwarding on inbound connections and your local `ssh-agent` must be running.

Forwarding an ssh agent carries its own security risk. If someone on the remote machine can gain access to your forwarded ssh agent connection, they can still make use of your keys. However, this is better than storing keys on remote machines: the attacker can only use the ssh agent connection, not the key itself. Thus, only while you're logged into the remote machine can they do anything. If you store the key on the remote machine, they can make a copy of it and use it whenever they want.

If you use ssh keys remember about passphrases which is strongly recommended to reduce risk of keys accidentally leaking.

Useful resources:

* [How to forward local keypair in an SSH session?](https://stackoverflow.com/questions/12257968/how-to-forward-local-keypair-in-a-ssh-session)
* [Using SSH agent forwarding](https://developer.github.com/v3/guides/using-ssh-agent-forwarding/)
* [SSH Agent Forwarding considered harmful](https://heipei.github.io/2015/02/26/SSH-Agent-Forwarding-considered-harmful/)
* [Security Consideration while using ssh-agent](https://www.commandprompt.com/blog/security_considerations_while_using_ssh-agent/)

</details>

<details>
<summary><b>How would you secure a newly provisioned server?</b></summary><br>

* if machine is a new install, protect it from hostile network traffic, until the operating system is installed and hardened
* create a separate partition with the `nodev`, `nosuid`, and `noexec` options set for `/tmp`
* create separate partitions for `/var`, `/var/log`, `/var/log/audit`, and `/home`
* enable randomized virtual memory region placement
* remove legacy services (e.g. `telnet-server`, `rsh`, `rlogin`, `rcp`, `ypserv`, `ypbind`, `tftp`, `tftp-server`, `talk`, `talk-server`).
* limit connections to services running on the host to authorized users of the service via firewalls and other access control technologies
* disable source routed packet acceptance
* enable **TCP/SYN** cookies
* disable SSH root login
* install and configure **AIDE**
* install and configure **OSsec HIDS**
* configure **SELinux**
* all administrator or root access must be logged
* integrity checking of system accounts, group memberships, and their associated privileges should be enabled and tested
* set password creation requirements (e.g. with PAM)

Useful resources:

* [Security Harden RHEL 9](https://docs.redhat.com/en/documentation/red_hat_enterprise_linux/9/pdf/security_hardening/Red_Hat_Enterprise_Linux-9-Security_hardening-en-US.pdf)
* [CIS Red Hat Enterprise Linux 8](https://www.tenable.com/audits/CIS_Red_Hat_EL8_Server_v3.0.0_L1)

</details>

<details>
<summary><b>What is the difference between Host Intrusion Detection and Network Intrusion Detection? Is one better than the other?</b></summary><br>

Host Intrusion Detection system runs on individual hosts, such as an antivirus, while Network Intrusion Detection system oversees the network. One is not "better" than the other as they have similar but different functions. A **HIDS** is important to monitor and protect individual hosts generally from user actions, while a **NIDS** is important to monitor and protect hosts from each other as well as from outside networks.

</details>

<details>
<summary><b>What is Compliance?</b></summary><br>

Compliance refers to the set of rules and regulations that organizations must follow to protect sensitive data and prevent security breaches. Compliance frameworks, such as the Payment Card Industry Data Security Standard (PCI DSS), the Health Insurance Portability and Accountability Act (HIPAA), and the General Data Protection Regulation (GDPR), provide guidelines and best practices for protecting personal information and preventing unauthorized access.

Compliance is important because it helps ensure that organizations are taking the necessary steps to protect their data and the data of their customers or clients. Failure to comply with regulations can result in legal and financial penalties, as well as damage to the organization's reputation. Compliance also helps to establish trust with customers and stakeholders, as they can be confident that the organization is taking steps to protect their information.

</details>

<details>
<summary><b>What is the difference between hashing and encryption?</b></summary><br>

Hashing is a one-way process that converts plain text into a fixed-length string of characters, known as a hash value or message digest. The hash value is unique to the input, meaning that the same input will always produce the same hash value. However, it is practically impossible to reverse the hash function and obtain the original input from the hash value. Hashing is commonly used for password storage, digital signatures, and file integrity checking.

Encryption, on the other hand, is a two-way process that transforms plain text into ciphertext, which can only be read by someone who has the key to decrypt it. Encryption is commonly used for data protection during storage or transmission. There are two main types of encryption: symmetric encryption and asymmetric encryption. Symmetric encryption uses the same key for both encryption and decryption, while asymmetric encryption uses a public key to encrypt data and a private key to decrypt it.

</details>

<br>

### :diamond_shape_with_a_dot_inside: <a name="senior-sysadmin">Senior Sysadmin</a>

<details>
<summary><b>In the context of computing, what is Split-Brain and why is it a problem?</b></summary><br>

Split-Brain refers to a state in which a distributed system consisting of multiple nodes becomes divided into two or more separate, independent clusters due to a loss of communication between the nodes. Each cluster then operates independently of the others, potentially resulting in inconsistencies and conflicts between them.

Split-Brain is a problem because it can lead to a loss of data consistency and integrity. If each cluster is making decisions and changes independently, without knowledge of the other clusters, it can result in data inconsistencies that are difficult to reconcile. In addition, it can lead to a situation where multiple nodes are trying to perform the same task simultaneously, resulting in conflicts and errors.

To prevent Split-Brain, distributed systems often use a quorum-based approach, in which a majority of nodes must agree on a decision before it is made. This helps to ensure that there is always a single authoritative copy of data and that decisions are made consistently across the system. Additionally, various techniques such as fencing and STONITH (Shoot The Other Node In The Head) are used to prevent rogue nodes from causing problems in the system.

Useful resources:

* [What is Split brain and why do you need to worry about it?](https://www.45drives.com/community/articles/what-is-split-brain/)

</details>

<details>
<summary><b>What is Split-horizon DNS and how do you implement it?</b></summary><br>

Split-horizon DNS is a technique used to provide different DNS query responses based on the requester's network location. In other words, it enables the DNS server to provide different responses to different clients depending on whether they are inside or outside the local network.

The split-horizon DNS technique can be used to resolve issues when the internal network has the same domain name as an external network, and the internal DNS server needs to resolve addresses differently than the external DNS server. For example, suppose a company has a website with the domain name "example.com." The company's internal network may also use the same domain name for its internal servers, such as "mail.example.com," "intranet.example.com," etc. External clients that access the company's website should receive the external IP address of the web server, while internal clients should receive the internal IP address of the web server.

To implement split-horizon DNS, you need to create two sets of DNS zones: one for internal clients and another for external clients. You can achieve this by setting up two DNS servers, each with a different view of the zone files. The internal DNS server should contain a complete set of zone files for the internal network, while the external DNS server should only contain zone files for the public-facing domain names.

You can also implement split-horizon DNS using the same DNS server, by using the BIND software's "view" feature. This feature enables you to create multiple views of the zone files, with each view containing a different set of DNS records. With views, you can create a separate view for internal clients and another for external clients, each containing the appropriate DNS records.

Useful resources:

* [What is Split-Horizon DNS?](https://splitdns.net/)

</details>

#### System Questions

<details>
<summary><b>What are some keep elements to keep in mind when writing good documentation?</b></summary><br>

Technical documentation serves as a valuable resource for users, developers, system administrators, and other stakeholders, enabling them to understand and effectively work with a software or system.

1. **Audience Understanding**: Know your audience. Different readers (e.g., end-users, developers, system administrators) have different needs. Tailor your content to the specific needs and technical proficiency of your target audience.

2. **Clear Structure and Organization**: Organize the content logically, usually starting with fundamental concepts and progressing to advanced topics. Use headings, subheadings, tables of contents, and indexes to guide readers.

3. **Consistency**: Be consistent in terminology, writing style, formatting, and naming conventions. Consistency makes documentation predictable and easier to follow.

4. **Use of Visuals**: Incorporate diagrams, screenshots, flowcharts, and other visuals where appropriate. They can help clarify complex concepts and provide visual breaks in text-heavy content.

5. **Step-by-Step Tutorials**: For documentation that instructs users on how to perform tasks, provide detailed, step-by-step tutorials. Ensure they are tested and validated for accuracy.

6. **Concise and Precise Writing**: Avoid unnecessary jargon and verbosity. Use clear and concise language, ensuring that explanations are straightforward.

7. **Active Voice**: Use the active voice ("Click the button") rather than the passive voice ("The button should be clicked"). It's more direct and easier to understand.

8. **Code Samples and Examples**: When documenting software, provide code samples, examples, and usage scenarios. Ensure all code is tested and accurate.

9. **Cross-Referencing**: Link to related topics within the documentation. This allows readers to quickly jump to additional relevant information.

10. **Versioning**: Clearly indicate for which version of the software or system the documentation applies. Update the documentation with each new version or significant change.

11. **Continuous Updates**: Technical documentation should be treated as a living document. As products or systems evolve, documentation should be updated accordingly.

12. **Review and Testing**: Before publishing, have the documentation reviewed by peers, technical experts, or a dedicated editor. Consider user testing, where individuals unfamiliar with the topic try to complete tasks using only the documentation as a guide.

</details>

<details>
<summary><b>How would you remotely provision a blank server in a datacenter to be a LAMP stack web server with predefined users and configurations? Assume all datacenter hardware has been setup and networking side of things is also ready (e.g. VLAN tag).</b></summary><br>

1. **Access the Server**: Use the datacenter’s out-of-band management (e.g., IPMI, iLO) to access the server remotely and boot it using a network boot (PXE) or virtual media.

2. **Install the OS**: Perform an automated OS installation using a method like **Kickstart** (for RHEL/AlmaLinux) or **Preseed** (for Debian/Ubuntu) to ensure the OS is installed with predefined configurations.

3. **Automate Configuration**: After the OS installation, use a configuration management tool like **Ansible**, **Puppet**, or **Chef** to install the LAMP stack (Apache, MySQL, PHP), create predefined users, and configure necessary services like virtual hosts, databases, and firewall rules.

4. **Set Up Security**: Secure the server by enabling **SSH key authentication**, configuring the **firewall** (e.g., allowing only HTTP, HTTPS, and SSH), and optionally configuring **SELinux** and installing tools like **fail2ban**.

5. **Automate Backups and Monitoring**: Set up automated backups for the server (e.g., using `rsnapshot` or a similar tool) and install monitoring tools (e.g., **Nagios**, **Zabbix**, or **Prometheus**) to track system performance and availability.

6. **Document the Process**: Maintain documentation of the entire setup process for future maintenance and scalability, including backup policies, firewall rules, and configurations applied.

</details>

<details>
<summary><b>What is the difference between EXT4, XFS, and ZFS?</b></summary><br>

EXT4 is the default file system used in most Linux distributions. It is a mature and stable file system that supports large files and file systems, and offers good performance for most workloads. It has been in use for many years and is well understood by system administrators and developers.

XFS is known for its high performance, especially for large files and file systems. It also has features like snapshots and online defragmentation that make it useful for certain applications.

ZFS is a file system originally developed by Sun Microsystems for their Solaris operating system. It has since been ported to other operating systems like FreeBSD and Linux. ZFS is known for its advanced features like built-in data compression, deduplication, and snapshotting. It also has a unique approach to storage management, using a pool of disks instead of individual disks.

EXT4 is the most widely used file system in Linux and is a good choice for most workloads. XFS is a good choice for large files and file systems, while ZFS is a good choice for advanced features like snapshots and data management. Ultimately, the choice of file system depends on the specific requirements of the system and the workload it will be used for.

</details>

<details>
<summary><b>The Junior dev accidentally destroyed production database. How can you prevent such situations?</b></summary><br>

**Create disaster recovery plan**

Disaster recovery and business continuity planning are integral parts of the overall risk management for an organization. Is a documented process or set of procedures to recover and protect a business IT infrastructure.

If you don’t have a recovery solution, then your restoration efforts will become rebuilding efforts, starting from scratch to recreate whatever was lost.

You should use commonly occurring real life data disaster scenarios to simulate what your backups will and won’t do in a crisis.

**Create disaster recovery center**

As a result, in the event of unplanned interruptions in the functioning of the primary location, service and all operational activities are switched to the backup center and therefore the unavailability of services is limited to the absolute minimum.

Does the facility have sufficient bandwidth options and power to scale and deal with the increased load during a major disaster? Are resources available to periodically test failover?

**Create regular backups and tested it!**

Backups are a way to protect the investment in data. By having several copies of the data, it does not matter as much if one is destroyed (the cost is only that of the restoration of the lost data from the backup).

When you lose data, one thing is certain: downtime.

To assure the validity and integrity of any backup, it's essential to carry out regular restoration tests. Ideally, a test should be conducted after every backup completes to ensure data can be successfully secured and recovered. However, this often isn't practical due to a lack of available resources or time constraints.

Make backups of entire virtual machines and important components in the middle of them.

**Create snapshots: vm, disks or lvm**

Snapshots are perfect if you want to recover a server from a previous state, but it's only a "quick method", it cannot restore the system after too many items changed.

Create them always before making changes on production environments (and not only).

Disk snapshots are used to generate a snapshot of an entire disk. These snapshots don't make it easy to restore individual chunks of data (e.g. a lost user account), though it's possible. The primary purpose is to restore entire disks in case of disk failure.

The LVM snapshots can be primarily used to easily copy data from production environment to staging environment.

Remember: Snapshots are not backups!

**Development and testing environments**

A production environment is the real instance of the application and its database used by the company or the clients. The production database has all the real data.

Setting up development environments based directly on the production database, instead of using a backup for this (removing the need for the above). Dev and test environment that your engineers can get to and a prod environment that only a few people can push updates to following an approved change.

All environments such as prod, dev and test should have one major difference: authorization data for services. For example postgres database instance on testing environment should be consistent (if possible) with the production base, however, in order to eliminate errors of database names and logins and passwords for authorization should be different.

**Single point of failure**

The general method to avoid single points of failures is to provide redundant components for each necessary resource, so service can continue if a component fails.

**Synchronization and replication process for databases**

The replication procedure is super fragile and prone to error.

A good idea is also slightly longer delay of data replication (e.g. for DRC). As in replicas, the data changes will usually be replicated within minutes, so the lost data won’t be on the replica database either once that happens.

**Create database model with users, roles and rights, use different methods of protection**

Only very advanced devs have permissions for db admin access. The other really don't need Write access to clone a database. On the other hand just don't give a developer write access to prod.

The production database should refuse connections from any server and pc which isn't the one running the production application, even if it provides a valid username/password.

How the hell development machines can access a production database right like that? How about a simple firewall rule to just let the servers needing the DB data access the database?

**Create summary/postmortem documents after failures**

The post-mortem audience includes customers, direct reports, peers, the company's executive team and often investors.

Explain what caused the outage on a timeline. Every incident begins with a specific trigger at a specific time, which often causes some unexpected behavior. For example, our servers were rebooted, and we expected them to come back up intact, which didn't happen.

Furthermore, every incident has a root cause: the reboot itself was trigger, however a bug in the driver caused the actual outage. Finally, there are consequences to every incident, the most obvious one is that the site goes down.

The post-mortem answers the single most important question of what could have prevented the outage.

Despite how painful an outage may have been, the worst thing you can do is to bury it and never properly close the incident in a clear and transparent way.

**If you also made a big mistake...**

  > "_Humans are just apes with bigger computers._" - african_cheetah (Reddit)
  >
  > "_I've come to appreciate not having access to things I don't absolutely need._" - warm_vanilla_sugar (Reddit)
  >
  > Document whatever happened somewhere. Write setup guides. Failure is instructive.

Useful resources:

* [Accidentally destroyed production database on first day of a job...](https://www.reddit.com/r/cscareerquestions/comments/6ez8ag/accidentally_destroyed_production_database_on/)
* [Postmortem of database outage of January 31](https://about.gitlab.com/2017/02/10/postmortem-of-database-outage-of-january-31/)
* [What is an Incident Postmortem?](https://www.pagerduty.com/resources/learn/incident-postmortem/)

</details>

<details>
<summary><b>How do you add a new disk to a Linux server without rebooting? How do you rescan and add it in LVM?</b></summary><br>

### 1. **Identify the New Disk**

First, check the available disks before and after adding the new one. This helps confirm that the new disk is detected by the system.

* Before adding the disk:

  ```bash
  lsblk
  fdisk -l
  ```

* After adding the disk:

  ```bash
  echo "- - -" > /sys/class/scsi_host/host0/scan
  ```

  Then check again with `lsblk` or `fdisk -l` to verify the new disk is detected (e.g., `/dev/sdb`).

### 2. **Create a Partition on the New Disk (Optional)**

   You can directly use the entire disk for LVM or create a partition. If you want to create a partition, use `fdisk` or `parted`:

* Using `fdisk`:

     ```bash
     fdisk /dev/sdb
     ```

     Inside `fdisk`, create a new primary partition:
  * Press `n` to create a new partition.
  * Press `p` to make it a primary partition.
  * Press `w` to write changes.

* Using `parted` (for GPT partition table):

     ```bash
     parted /dev/sdb mklabel gpt
     parted /dev/sdb mkpart primary 0% 100%
     ```

### 3. **Mark the Partition for LVM**

Once the partition is created, mark it for LVM use with the correct partition type.

* Using `fdisk`:

  ```bash
  fdisk /dev/sdb
  ```

  * Type `t` to change the partition type.
  * Select partition (usually `1`).
  * Enter `8e` (LVM partition type).
  * Type `w` to save changes.

### 4. **Create a Physical Volume (PV)**

   Initialize the new disk or partition as a physical volume for LVM.

* For the entire disk:

  ```bash
  pvcreate /dev/sdb
  ```

* If you created a partition (e.g., `/dev/sdb1`):

  ```bash
  pvcreate /dev/sdb1
  ```

### 5. **Extend the Volume Group (VG)**

   Add the newly created physical volume to your existing volume group.

* Check existing volume groups:

  ```bash
  vgdisplay
  ```

* Add the new physical volume to the volume group:

  ```bash
  vgextend <VolumeGroupName> /dev/sdb1  # or /dev/sdb if using the whole disk
  ```

### 6. **Extend the Logical Volume (LV)**

   After adding the physical volume to the volume group, you can extend the logical volume.

* Check existing logical volumes:

  ```bash
  lvdisplay
  ```

* Extend the logical volume while also extending the underlying filesystem:

  ```bash
  lvextend -r -l +100%FREE /dev/<VolumeGroupName>/<LogicalVolumeName>
  ```

### 8. **Verify the Changes**

   Verify that the logical volume and filesystem have been resized correctly.

* Check the new size:

  ```bash
  df -h
  lvdisplay
  ```

</details>

<details>
<summary><b>What does it mean to mount the root file system?</b></summary><br>

Mounting the root file system means making the root directory of a file system accessible to the operating system. In other words, it allows the operating system to access and read/write files stored on the root file system.

When a computer boots up, the bootloader loads the kernel into memory and passes control to the kernel. The kernel then initializes the hardware and mounts the root file system so that it can access the system files and start up the rest of the operating system.

Useful resources:

* [What does "mounting a root file system" mean exactly?](https://superuser.com/questions/193918/what-does-mounting-a-root-file-system-mean-exactly)
* [How does a kernel mount the root partition?](https://unix.stackexchange.com/questions/9944/how-does-a-kernel-mount-the-root-partition)

</details>

<details>
<summary><b>A bare metal server's root partition is full and will not boot. How do you troubleshoot and fix the issue?</b></summary><br>

### 1. **Access the System in Rescue Mode or with a Live CD/USB**

* **Boot into Rescue Mode**:
  * If your system uses a Linux distribution that supports rescue mode (like AlmaLinux/RHEL), boot into rescue mode from the installation media.
  * During boot, select the appropriate recovery/rescue option from the GRUB menu.
* **Use a Live CD/USB**:
  * If rescue mode isn’t available, use a Linux live CD/USB to boot the system. This gives you access to the filesystem so you can troubleshoot.

### 2. **Mount the Root Filesystem**

* Once in rescue mode or a live environment, you’ll need to mount the root partition to gain access to the system’s files.
* **Identify the root partition**:
  * Use `lsblk`, `fdisk -l`, or `blkid` to identify the root partition (e.g., `/dev/sda1`, `/dev/nvme0n1p1`).
* **Mount the root partition**:

     ```bash
     mkdir /mnt/root
     mount /dev/sda1 /mnt/root
     ```

* If you have separate partitions for `/boot`, `/var`, or `/home`, you may need to mount those as well:

     ```bash
     mount /dev/sda2 /mnt/root/boot
     mount /dev/sda3 /mnt/root/var
     ```

### 3. **Identify Large Files to Delete**

* **Change to the mounted root filesystem**:

     ```bash
     chroot /mnt/root
     ```

* **Check disk usage**:
  * Use `du` or `df` to determine which directories or files are taking up the most space:

     ```bash
     df -h          # Check the overall usage of the root filesystem
     du -sh /*      # Identify large directories
     du -sh /var/*  # Drill down into the `/var` directory, which is often a culprit
     ```

* **Common directories to check**:
  * **/var/log/**: Large or old log files.
  * **/var/cache/**: Package manager caches (e.g., DNF, YUM, APT caches).
  * **/tmp/**: Temporary files that may not be necessary anymore.
  * **/root/** or **/home/**: Check for large personal files (backups, ISOs, etc.).

### 4. **Free Up Space**

* **Delete or compress log files**:
  * Identify and delete old or large log files in `/var/log/`. You can either remove them or compress them:

     ```bash
     rm -f /var/log/*.log  # Remove old logs
     gzip /var/log/*.log    # Compress logs to save space
     ```

* **Clear package cache**:
  * For RPM-based systems (AlmaLinux/RHEL/Fedora):

     ```bash
     dnf clean all    # or yum clean all for older systems
     ```

  * For APT-based systems (Debian/Ubuntu):

     ```bash
     apt-get clean
     ```

* **Remove orphaned packages** (optional):
  * Check for orphaned or unnecessary packages and remove them to free space.

     ```bash
     dnf autoremove  # For RPM-based systems
     apt-get autoremove  # For APT-based systems
     ```

### 5. **Check for and Remove Old Kernels**

* On systems with a separate `/boot` partition, it can fill up if old kernels aren’t cleaned up. You can list installed kernels and remove old ones:
  * List kernels:

     ```bash
     rpm -q kernel  # RHEL/AlmaLinux
     dpkg --list | grep linux-image  # Debian/Ubuntu
     ```

  * Remove old kernels, keeping the current and one or two previous versions:

     ```bash
     dnf remove kernel-old-version
     ```

### 6. **Check for Core Dumps or Large Swap Files**

* **Core dumps**:
  * Check for large core dump files in `/var/lib/systemd/coredump/` or `/var/crash/`. These can take up a lot of space and are safe to remove unless needed for debugging.

     ```bash
     rm -f /var/lib/systemd/coredump/*
     ```

* **Large swap files**:
  * If the root partition contains a large swap file, consider moving it to another partition temporarily or reducing its size.

### 7. **Resize the Partition (if necessary)**

* If space is consistently an issue, you may need to resize the root partition. This step is complex and risky, especially if the disk is already partitioned. Use tools like `gparted` or `parted` from a live CD to resize partitions if possible. Alternatively, consider adding another disk or creating a new partition for data.

### 8. **Reboot the Server**

* After freeing up enough space, unmount the root partition and reboot the server:

     ```bash
     exit   # Exit chroot
     umount /mnt/root
     reboot
     ```

* The system should now boot normally.

### 9. **Set Up Monitoring (Post-Fix)**

* Once the issue is resolved, it’s good practice to implement monitoring to avoid future disk space issues:
  * **Disk usage monitoring**: Use tools like `df` or monitoring solutions (e.g., Nagios, Zabbix, Prometheus) to alert you when disk usage exceeds a certain threshold.
  * **Log rotation**: Ensure that log files are rotated properly using tools like `logrotate` to prevent logs from consuming excessive disk space.
  * **Package cache cleaning**: Automate cleaning of package caches periodically to prevent them from accumulating.

</details>

<details>
<summary><b>What considerations come into play when designing a highly available application, both at the architecture level and the application level?</b></summary><br>

**Architecture considerations**

* **Redundancy and isolation**: Remove single points of failure. Use multiple instances, AZs, and where justified, multi‑region. Prefer independent failure domains.
* **Traffic management**: Load balancers for distribution and health‑checks; DNS or global load balancing for regional failover. Automate failover and recovery.
* **Capacity and scaling**: Right‑size, then auto‑scale horizontally. Plan for N+1 (or more) capacity during failures.
* **State and data**: Keep stateless frontends. Use replicated data stores with quorum where needed. Define RPO/RTO and a tested DR plan (e.g., backup/restore, warm standby, active‑active).
* **Observability**: Centralized logs, metrics, traces, SLOs with error budgets. Alert on user‑visible symptoms.
* **Change safety**: Progressive delivery (canary/blue‑green), safe rollbacks, config as code, regular game‑days/chaos tests.

**Application considerations**

* **Failure handling**: Timeouts everywhere, retries with jitter, **circuit breakers**, and backoff. Make operations idempotent.
* **Graceful degradation**: Shed load and degrade non‑critical features first; implement bulkheads and rate limits.
* **State management**: Externalize sessions; design for at‑least‑once processing and exactly‑once effects where required.
* **Compatibility**: Backward‑compatible APIs and data migrations; feature flags to decouple deploy from release.
* **Startup/shutdown**: Health endpoints, readiness/liveness checks, fast cold‑start, safe termination hooks.
* **Performance under failure**: Use caches carefully, apply backpressure, and keep critical paths simple to avoid cascading failures.

</details>

<details>
<summary><b>Explain the risks and caveats of LVM (Logical Volume Manager).</b></summary><br>

**Risks of using LVM**

* Single point of failure: LVM metadata, which contains information about logical volumes, physical volumes, and volume groups, is stored on the disk. If this metadata is lost or corrupted, it can result in data loss or system downtime.
* Performance overhead: LVM adds another layer of abstraction between the physical storage and file system, which can result in performance overhead. While the performance impact is generally negligible for most use cases, it can be significant for I/O-intensive workloads.
* Complexity: LVM introduces additional complexity to the system and requires a good understanding of how the underlying storage works. This can make troubleshooting and maintenance more challenging.
* Fragmentation: LVM can lead to data fragmentation because it can allocate space in small chunks. This can result in reduced performance and increased disk usage.
* Data loss: LVM provides the ability to move and resize volumes, which can lead to data loss if not done correctly. It is essential to have a backup strategy in place before making any changes to LVM configurations.

Useful resources:

* [LVM dangers and caveats (original)](https://serverfault.com/questions/279571/lvm-dangers-and-caveats)

</details>

<details>
<summary><b>What if <code>kill -9</code> does not work? Describe exceptions for which the use of SIGKILL is insufficient.</b></summary><br>

`kill -9` (`SIGKILL`) always works, provided you have the permission to kill the process. Basically either the process must be started by you and not be setuid or setgid, or you must be root. There is one exception: even root cannot send a fatal signal to PID 1 (the init process).

However `kill -9` is not guaranteed to work immediately. All signals, including `SIGKILL`, are delivered asynchronously: the kernel may take its time to deliver them. Usually, delivering a signal takes at most a few microseconds, just the time it takes for the target to get a time slice. However, if the target has blocked the signal, the signal will be queued until the target unblocks it.

Normally, processes cannot block `SIGKILL`. But kernel code can, and processes execute kernel code when they call system calls.

A process blocked in a system call is in uninterruptible sleep. The `ps` or `top` command will (on most unices) show it in state **D**.

To remove a **D** State Process, since it is uninterruptible, only a machine reboot can solve the problem in case it's not automatically handled by the system.

Usually there is a very few chance that a process stays in **D** State for long. And if it does then there is something not properly being handled in the system. This can be a potential bug as well.

A classical case of long uninterruptible sleep is processes accessing files over NFS when the server is not responding; modern implementations tend not to impose uninterruptible sleep (e.g. under Linux, the intr mount option allows a signal to interrupt NFS file accesses).

You may sometimes see entries marked **Z** (or **H** under Linux) in the `ps` or `top` output. These are technically not processes, they are zombie processes, which are nothing more than an entry in the process table, kept around so that the parent process can be notified of the death of its child. They will go away when the parent process pays attention (or dies).

Summary exceptions:

* Zombie processes cannot be killed since they are already dead and waiting for their parent processes to reap them
* Processes that are in the blocked state will not die until they wake up again
* The init process is special: It does not get signals that it does not want to handle, and thus it can ignore **SIGKILL**. An exception from this exception is while init is ptraced on Linux
* An uninterruptibly sleeping process may not terminate (and free its resources) even when sent **SIGKILL**. This is one of the few cases in which a Unix system may have to be rebooted to solve a temporary software problem

Useful resources:

* [What if kill -9 does not work? (original)](https://unix.stackexchange.com/questions/5642/what-if-kill-9-does-not-work)
* [How to kill a process in Linux if kill -9 has no effect](https://serverfault.com/questions/458261/how-to-kill-a-process-in-linux-if-kill-9-has-no-effect)
* [When should I not kill -9 a process?](https://unix.stackexchange.com/questions/8916/when-should-i-not-kill-9-a-process)
* [SIGTERM vs. SIGKILL](https://major.io/p/sigterm-vs-sigkill/)

</details>

<details>
<summary><b>What is the main advantage of using <code>chroot</code>? When and why do we use it? What is the purpose of the mount dev, proc, sys in a chroot environment?</b></summary><br>

An advantage of having a chroot environment is the file-system is totally isolated from the physical host. `chroot` has a separate file-system inside the file-system, the difference is its uses a newly created root(/) as its root directory.

A chroot jail is a way to isolate a process and its children from the rest of the system. It should only be used for processes that don't run as root, as root users can break out of the jail very easily.

The idea is that you create a directory tree where you copy or link in all the system files needed for a process to run. You then use the `chroot()` system call to change the root directory to be at the base of this new tree and start the process running in that chroot'd environment. Since it can't actually reference paths outside the modified root, it can't perform operations (read/write etc.) maliciously on those locations.

On Linux, using a bind mounts is a great way to populate the chroot tree. Using that, you can pull in folders like `/lib` and `/usr/lib` while not pulling in `/usr`, for example. Just bind the directory trees you want to directories you create in the jail directory.

A chroot environment is useful for:

* reinstall bootloader
* reset a forgotten password
* perform a kernel upgrade (or downgrade)
* rebuild your initramdisk
* fix your **/etc/fstab**
* reinstall packages using your package manager
* whatever

When working in a chrooted environment, there is a few special file systems that needs to be mounted so all programs behave properly.

Limitation is that `/dev`, `/sys` and `/proc` are not mounted by default but needed for many tasks.

Useful resources:

* [It's all about Chroot](https://medium.com/@itseranga/chroot-316dc3c89584)
* [Best Practices for UNIX chroot() Operations](http://www.unixwiz.net/techtips/chroot-practices.html)
* [Is there an easier way to chroot than bind-mounting?](https://askubuntu.com/questions/32418/is-there-an-easier-way-to-chroot-than-bind-mounting)
* [What's the proper way to prepare chroot to recover a broken Linux installation?](https://superuser.com/questions/111152/whats-the-proper-way-to-prepare-chroot-to-recover-a-broken-linux-installation)

</details>

<details>
<summary><b>What are segmentation faults (segfaults), and how can identify what's causing them?</b></summary><br>

A **segmentation fault** (aka _segfault_) is a common condition that causes programs to crash. Segfaults are caused by a program trying to read or write an illegal memory location.

Program memory is divided into different segments:

* a text segment for program instructions
* a data segment for variables and arrays defined at compile time
* a stack segment for temporary (or automatic) variables defined in subroutines and functions
* a heap segment for variables allocated during runtime by functions, such as `malloc` (in C)

In practice, segfaults are almost always due to trying to read or write a non-existent array element, not properly defining a pointer before using it, or (in C programs) accidentally using a variable's value as an address. Thus, when Process A reads memory location 0x877, it reads information residing at a different physical location in RAM than when Process B reads its own 0x877.

All modern operating systems support and use segmentation, and so all can produce a segmentation fault.

Segmentation fault can also occur under following circumstances:

* a buggy program/command, which can be only fixed by applying patch
* it can also appear when you try to access an array beyond the end of an array under C programming
* inside a chrooted jail this can occur when critical shared libs, config file or `/dev/` entry missing
* sometime hardware or faulty memory or driver can also create problem
* maintain suggested environment for all computer equipment (overheating can also generate this problem)

To debug this kind of error try one or all of the following techniques:

* enable core files: `$ ulimit -c unlimited`
* reproduce the crash: `$ ./<program>`
* debug crash with gdb: `$ gdb <program> [core file]`
* or run `LD_PRELOAD=...path-to.../libSegFault.so <program>` to get a report with backtrace, loaded libs, etc

Also:

* make sure correct hardware installed and configured
* always apply all patches and use updated system
* make sure all dependencies installed inside jail
* turn on core dumping for supported services such as Apache
* use `strace` which is a useful diagnostic, instructional, and debugging tool

Sometimes segmentation faults are not caused by bugs in the program but are caused instead by system memory limits being set too low. Usually it is the limit on stack size that causes this kind of problem (stack overflows). To check memory limits, use the `ulimit` command in bash.

Useful resources:

* [What are segmentation faults (segfaults), and how can I identify what's causing them? (original)](https://kb.iu.edu/d/aqsj)
* [What is a segmentation fault on Linux?](https://stackoverflow.com/questions/3200526/what-is-a-segmentation-fault-on-linux)
* [Segmentation fault when calling a recursive bash function](https://unix.stackexchange.com/questions/296641/segmentation-fault-when-calling-a-recursive-bash-function)
* [Troubleshooting Segmentation Violations/Faults](https://web.mit.edu/10.001/Web/Tips/tips_on_segmentation.html)
* [Can one use libSegFault.so to get backtraces for SIGABRT?](https://stackoverflow.com/questions/18706496/can-one-use-libsegfault-so-to-get-backtraces-for-sigabrt)

</details>

<details>
<summary><b>In terms of *nix systems, what does it mean when we say everything is a file?</b></summary><br>

### 1. **Traditional Files**

* Regular files containing data (e.g., text files, binaries) are the most obvious representation of this concept. Operations like reading and writing are done via standard file operations (`open`, `read`, `write`, `close`).

### 2. **Directories**

* Directories are treated as special types of files that store information about other files and subdirectories. They can be read to list their contents but cannot be written directly like regular files.

### 3. **Devices**

* **Character devices and block devices**: Hardware devices (e.g., hard drives, keyboards, mice, terminals) are represented as files in the `/dev` directory. For example:
  * **Character devices** (e.g., `/dev/tty`, `/dev/null`) are accessed character-by-character.
  * **Block devices** (e.g., `/dev/sda`, `/dev/loop0`) allow random access to blocks of data, typical for disk drives.
* Accessing or interacting with devices is done using the same read/write operations as with regular files.

### 4. **Pipes and Sockets**

* **Named pipes** (`FIFO files`) and **UNIX domain sockets** are special files that allow inter-process communication. They enable data to be passed between processes, similar to how data is read from and written to a regular file.
  * **Pipes**: Used for unidirectional communication (e.g., `|` in shell commands).
  * **Sockets**: Enable bidirectional communication between processes, often used for network services.

### 5. **Processes**

* Processes are represented as files under the `/proc` directory. Each running process has a directory (`/proc/<PID>`) containing information about the process, such as memory usage, file descriptors, and environment variables. This directory provides a file-based interface to the kernel’s process-related information.

### 6. **Symbolic Links**

* Symbolic links (symlinks) are special files that point to other files or directories. These links allow flexible file and directory manipulation, abstracting access to target files.

### 7. **Input/Output Streams**

* Standard input, output, and error streams (`stdin`, `stdout`, `stderr`) are treated as files with descriptors (`0`, `1`, and `2`, respectively). This file-based abstraction allows redirecting input/output between files, devices, and other processes seamlessly.

### 8. **Network Interfaces**

* Network interfaces can be accessed via special files (e.g., `/dev/tun` for tunneling interfaces). Network communication, especially through UNIX domain sockets, can be treated similarly to reading and writing to files.

### 9. **System Information**

* **System resources and kernel settings**: The `/proc` and `/sys` directories provide access to system information and kernel parameters. Files in these directories allow the inspection and modification of kernel behavior, such as managing hardware, checking memory usage, or tuning kernel parameters.

</details>

<details>
<summary><b>What is the difference between /dev/random and /dev/urandom ?</b></summary><br>

You should use `/dev/urandom`, not `/dev/random`. The differences between `/dev/random` and `/dev/urandom` are:

* `/dev/random` might be theoretically better _in the context of an information-theoretically secure algorithm_. This is the kind of algorithm which is secure against today's technology, and also tomorrow's technology, and technology used by aliens.

* `/dev/urandom` will not block, while `/dev/random` may do so. `/dev/random` maintains a counter of "how much entropy it still has" under the assumption that any bits it has produced is a lost entropy bit. Blocking induces very real issues, e.g. a server which fails to boot after an automated install because it is stalling on its SSH server key creation.

So you want to use `/dev/urandom` and stop to worry about this entropy business.

The trick is that `/dev/urandom` never blocks, ever, even when it should: `/dev/urandom` is secure as long as it has received enough bytes of "initial entropy" since the last boot (32 random bytes are enough). A normal Linux installation will create a random seed (from `/dev/random`) upon installation, and save it on the disk. Upon each reboot, the seed will be read, fed into `/dev/urandom`, and a new seed immediately generated (from `/dev/urandom`) to replace it. Thus, this guarantees that `/dev/urandom` will always have enough initial entropy to produce cryptographically strong alea, perfectly sufficient for any mundane cryptographic job, including password generation.

Should any of these daemons require randomness when all available entropy has been exhausted, they may pause to wait for more, which can cause excessive delays in your application. Even worse, since most modern applications will either resort to using its own random seed created at program initialization, or to using `/dev/urandom` to avoid blocking, your applications will suffer from lower quality random data. This can affect the integrity of your secure communications, and can increase the chance of cryptoanalysis on your private data.

Useful resources:

* [When to use /dev/random vs /dev/urandom](https://unix.stackexchange.com/questions/324209/when-to-use-dev-random-vs-dev-urandom)

</details>

<details>
<summary><b>What is the difference between <code>/sbin/nologin</code>, <code>/bin/false</code>, and <code>/bin/true</code>?</b></summary><br>

When `/sbin/nologin` is set as the shell, if user with that shell logs in, they'll get a polite message saying 'This account is currently not available'.

`/bin/false` is just a binary that immediately exits, returning false, when it's called, so when someone who has false as shell logs in, they're immediately logged out when false exits. Setting the shell to `/bin/true` has the same effect of not allowing someone to log in but false is probably used as a convention over true since it's much better at conveying the concept that person doesn't have a shell.

`/bin/nologin` is the more user-friendly option, with a customizable message given to the user trying to log in, so you would theoretically want to use that; but both nologin and false will have the same end result of someone not having a shell and not being able to ssh in.

Useful resources:

* [What's the difference between /sbin/nologin and /bin/false](https://unix.stackexchange.com/questions/10852/whats-the-difference-between-sbin-nologin-and-bin-false)
* [Why do some system users have /usr/bin/false as their shell?](https://superuser.com/questions/1183311/why-do-some-system-users-have-usr-bin-false-as-their-shell)

</details>

<details>
<summary><b>Which symptoms might be suffering from a disk bottleneck?</b></summary><br>

### 1. **Slow Read/Write Operations**

* **Long disk access times**: Operations involving disk I/O (file reads/writes, database queries) take much longer than usual.
* **Sluggish application performance**: Applications that rely on disk access (e.g., databases, web servers) may become slow, especially during peak usage times.

### 2. **High Disk Utilization**

* **High disk I/O wait**: High `iowait` values (visible in `top`, `iostat`, or `vmstat`) indicate that processes are waiting for disk operations to complete.
* **High disk utilization percentage**: Disk utilization nearing 100% in monitoring tools (e.g., `iostat`, `iostat -x`, `dstat`, or graphical monitoring like Grafana) indicates the disk is being fully utilized, leaving little room for additional requests.

### 3. **System Freezes or Stalls**

* **Temporary system hangs**: The system may freeze temporarily, especially when performing disk-heavy operations like backups or loading large files.
* **Slow boot times**: The system may take much longer to boot if it is trying to read or write a lot of data during startup.

### 4. **Excessive Page Faulting/Swapping**

* **Increased swapping**: When the system runs low on memory, it swaps data to disk. If the disk is already bottlenecked, this increases the load, leading to slower performance as the system struggles to swap efficiently.
* **High number of page faults**: Page faults happen when the system tries to access data that is not in memory and has to retrieve it from disk, which is slow during a disk bottleneck.

### 5. **Slow Database Performance**

* **Delayed database queries**: Queries take a long time to return results due to slow disk I/O, especially on databases using spinning disks or slow SSDs for storage.
* **Increased latency in transaction processing**: Applications relying on databases may experience high transaction latency, indicating the database is waiting on disk access.

### 6. **High I/O Load on Monitoring Tools**

* **High `await` and `svctm` times**: Tools like `iostat` and `sar` can show high average wait times (`await`) and service times (`svctm`), indicating that disk operations are taking longer to complete.
* **Queue size buildup**: An increasing queue size (`avgqu-sz` in `iostat`) suggests that disk requests are stacking up because the disk can’t keep up with the demand.

### 7. **Increased CPU I/O Wait Time**

* **High CPU I/O wait time**: The CPU spends significant time in an "I/O wait" state, visible in tools like `top` or `vmstat`. This indicates the CPU is idle, waiting for the disk to complete operations.
* **Low CPU usage despite slow performance**: You may notice low CPU usage, even though the system is slow, because the CPU is frequently waiting for disk operations to finish.

### 8. **High Latency on Disk Operations**

* **Slow response times**: High latency in disk read and write operations, which can be monitored using tools like `ioping` or `fio`, signals that the disk is struggling to meet the demand.
* **Excessive time for I/O-bound tasks**: Tasks like copying large files or running backup jobs take much longer than expected.

### 9. **Unresponsiveness During Disk-Intensive Tasks**

* **Application timeouts**: Applications might time out when trying to access the disk for large reads/writes.
* **System becomes unresponsive**: The entire system may become unresponsive or exhibit noticeable slowdowns when performing disk-heavy tasks like backups, indexing, or compiling large projects.

### 10. **Error Messages and Logs**

* **Disk-related error logs**: Disk bottlenecks might cause errors or warnings in system logs, such as timeouts or delays in disk operations (visible in `/var/log/messages`, `dmesg`, or journal logs).
* **Frequent I/O errors**: Frequent I/O errors or retries in log files may indicate that the disk is under strain or approaching failure.

### 11. **Poor Virtual Machine or Container Performance**

* **Virtual machines (VMs) slow down**: VMs may experience degraded performance if they share the same storage, especially if one or more VMs are I/O heavy.
* **Containers experience delays**: Similarly, containers relying on disk operations might exhibit slow performance, particularly when using shared volumes or slow disk storage.

### 12. **Slow Backup and Restore Operations**

* **Backup jobs take longer**: If backups or restores take significantly longer than usual, it might indicate the disk is overwhelmed by the number of I/O requests.

</details>

<details>
<summary><b>Load averages are above 30.00 on a server with 24 cores but CPU shows around 70 percent idle. One of the common causes of this condition is? How can this be debugged and fixed?</b></summary><br>

Requests which involve disk I/O can be slowed greatly if cpu(s) needs to wait on the disk to read or write data. I/O Wait, is the percentage of time the CPU has to wait on disk.

First, attempt to confirm if disk I/O is slowing down application performance by using a few terminal command line tools (`top`, `atop` and `iotop`).

Example of debugging:

* answering whether I/O is causing system slowness
* finding which disk is being written to
* finding the processes that are causing high I/O
* process list **state**
* finding what files are being written too heavily
* do you see your copy process put in **D** state waiting for I/O work to be done by pdflush?
* do you see heavy synchronous write activity on your disks?

also:

* using `top` command - load averages and wa (wait time)
* using `atop` command to monitor DSK (disk) I/O stats
* using `iotop` command for real-time insight on disk read/writes

For improvement performance:

* check drive array configuration
* check disk queuing algorithms and tuning them
* tuning general block I/O parameters
* tuning virtual memory management to improve I/O performance
* check and tuning mount options and filesystem params (also responsible for cache)

Useful resources:

* [Linux server performance: Is disk I/O slowing your application? (original)](https://haydenjames.io/linux-server-performance-disk-io-slowing-application/)
* [Debugging Linux I/O latency](https://superuser.com/questions/396696/debugging-linux-i-o-latency)
* [How do pdflush, kjournald, swapd, etc. interoperate?](https://unix.stackexchange.com/questions/76970/how-do-pdflush-kjournald-swapd-etc-interoperate)
* [5 ways to improve HDD speed on Linux](https://thecodeartist.blogspot.com/2012/06/improving-hdd-performance-linux.html)

</details>

<details>
<summary><b>You have just discovered a server you manage for the company you work at has been hacked. Go through the steps of what you do and recover from this.</b></summary><br>

**Immediate actions**

* Disconnect the host from the network (isolate at switch, security group, or hypervisor).
* Preserve evidence: avoid rebooting or changing files; capture a memory dump and copy disks or snapshots if possible.
* Notify stakeholders and open an incident ticket with an initial timeline.

**Triage and analysis**

* Capture volatile data: running processes, open connections, logged-in users, listening ports, scheduled tasks/cron, startup items, kernel modules.
* Collect artifacts: logs (/var/log, application logs), /etc, web roots, user homes, SSH keys, recent binaries; record hashes and timestamps.
* Determine initial access, privilege escalation, lateral movement, and persistence; extract indicators of compromise (IoCs).

**Eradication and recovery**

* Revoke exposed credentials, rotate passwords/keys, invalidate sessions and tokens.
* Patch exploited services and misconfigurations; tighten access controls and firewall rules.
* Rebuild the system from known-good media or a gold image; do **not** attempt in-place cleaning of a compromised OS.
* Restore required data from clean backups; validate integrity with checksums and application-level tests.
* Return to production gradually behind stricter controls; enable enhanced monitoring and alerting.

**Post-incident**

* Write a postmortem with timeline, root cause, and corrective actions.
* Add detections: alerts for the collected IoCs and anomalous auth/file/activity patterns.
* Improve baseline: MFA, least privilege, hardened configs, regular backups and restore tests, immutable/centralized logs, configuration management.

</details>

<details>
<summary><b>You have a LAMP stack with Nginx as a reverse proxy. Going to the site served by this web server results in a 500 Internal Server Error. List the possible causes for this issue.</b></summary><br>

### 1. **Nginx Configuration Issues**

* **Improper reverse proxy configuration**:
  * The proxy settings in the Nginx configuration might be incorrect. For example, issues with the `proxy_pass` directive or missing upstream server definitions.
* **Incorrect permissions**:
  * Nginx may not have proper permissions to access certain files, such as the Unix socket used by PHP-FPM.
* **Proxy buffer size issues**:
  * If the responses from Apache or PHP are too large, and the Nginx proxy buffers are too small, you could encounter a 500 error. Adjusting `proxy_buffer_size`, `proxy_buffers`, and `proxy_busy_buffers_size` may help.

### 2. **Apache or PHP Configuration Issues**

* **Apache misconfiguration**:
  * Issues with the virtual host configuration or `.htaccess` files can cause Apache to respond with a 500 error. Check for syntax errors in the configuration.
* **PHP-FPM not working**:
  * If PHP-FPM is used to handle PHP requests and isn’t running or misconfigured, Nginx will return a 500 error when it can’t forward requests properly.
* **Incorrect permissions for PHP files**:
  * If PHP files are not readable or executable by Apache or PHP-FPM, it can result in a 500 error. This can happen due to incorrect ownership or file permissions.
* **Memory or execution time limits**:
  * The `php.ini` file may have restrictive memory (`memory_limit`) or execution time (`max_execution_time`) settings, causing scripts to fail.

### 3. **PHP Application Errors**

* **Syntax or fatal errors in the PHP code**:
  * A 500 error can result from unhandled exceptions, syntax errors, or PHP fatal errors that crash the application.
* **Missing PHP modules**:
  * If the application requires specific PHP modules that are not installed or enabled (e.g., `mysqli`, `pdo_mysql`), it can cause a 500 error.
* **Incorrect database credentials**:
  * If the PHP application is unable to connect to the database due to incorrect MySQL credentials or a missing database, it might return a 500 error.

### 4. **Database Issues**

* **MySQL/MariaDB service not running**:
  * If the MySQL/MariaDB service is down, the application will fail to retrieve data, potentially causing a 500 error.
* **Database connection issues**:
  * Network issues or improper configuration of MySQL (e.g., bind-address issues) might prevent PHP from connecting to the database, resulting in a 500 error.

### 5. **Permission Issues**

* **File and directory permissions**:
  * The files and directories being served must have the correct permissions. For example, files should typically have `644` permissions, and directories should have `755`. Incorrect permissions can prevent execution or access.
* **SELinux issues** (if applicable):
  * If SELinux is enabled, it may block access to certain resources unless the appropriate contexts are set. A 500 error could occur if SELinux is blocking access to necessary files.

### 6. **Log Files and Error Reporting**

* **Check Nginx logs**:
  * Nginx logs (usually in `/var/log/nginx/error.log`) can provide insights into proxy errors, bad gateway issues, or permission problems.
* **Check Apache logs**:
  * Look for errors in the Apache logs (`/var/log/httpd/error_log` or `/var/log/apache2/error.log` depending on the system) that might indicate script failures or configuration issues.
* **PHP error logging**:
  * PHP errors may not be visible unless logging is enabled. Ensure `display_errors` is off and `log_errors` is on in `php.ini`, and check the PHP error log (typically `/var/log/php-fpm/error.log` or similar).
* **MySQL logs**:
  * If database issues are suspected, check the MySQL error logs for any service crashes or connection issues.

### 7. **Resource Limitations**

* **Memory exhaustion**:
  * If your server is running out of memory (RAM), processes might be killed (especially PHP or MySQL), resulting in a 500 error. Check system logs (`dmesg` or `/var/log/messages`) for any memory-related issues.
* **Process limits**:
  * Exceeding process limits (e.g., `max_children` in PHP-FPM) can result in the server being unable to process requests, causing a 500 error.
* **Disk space exhaustion**:
  * If the disk is full, PHP may not be able to write sessions, logs, or other temporary data, leading to a 500 error.

### 8. **Misbehaving Plugins or Extensions**

* **Web application plugins**:
  * For CMS platforms like WordPress, Joomla, or Drupal, a misbehaving plugin or extension can crash the application and result in a 500 error.
* **Application configuration changes**:
  * Recent changes to the application’s configuration (such as changes to a `.htaccess` file or PHP settings) may lead to a misconfiguration that causes a 500 error.

### 9. **SSL/TLS Misconfigurations**

* **SSL certificate issues**:
  * If the site uses HTTPS, issues with the SSL certificate, including expired or invalid certificates, can cause Nginx to fail in its role as a reverse proxy and return a 500 error.
* **Misconfigured SSL settings in Nginx**:
  * Incorrect SSL settings, such as outdated ciphers or protocols, can cause Nginx to fail to establish a secure connection, resulting in a 500 error.

### 10. **Miscommunication Between Nginx and Apache**

* **Incorrect FastCGI settings**:
  * If Nginx is using FastCGI to communicate with Apache or PHP-FPM, misconfigurations in the FastCGI parameters (e.g., incorrect `fastcgi_param` settings) could cause data transmission issues.
* **Timeouts**:
  * Nginx and Apache might be timing out while processing requests. Check both Nginx and Apache timeout settings (e.g., `proxy_read_timeout` in Nginx or `Timeout` in Apache).

</details>

<details>
<summary><b>Is it safe to attach the <code>strace</code> to a running process on the production? What are the consequences?</b></summary><br>

`strace` is the system call tracer for Linux. It currently uses the arcane `ptrace()` (process trace) debugging interface, which operates in a violent manner: **pausing the target process** for each syscall so that the debugger can read state. And doing this twice: when the syscall begins, and when it ends.

This means `strace` pauses your application twice for each syscall, and context-switches each time between the application and `strace`. It's like putting traffic metering lights on your application.

Cons:

* can cause significant and sometimes massive performance overhead, in the worst case, slowing the target application by over 100x. This may not only make it unsuitable for production use, but any timing information may also be so distorted as to be misleading
* can't trace multiple processes simultaneously (with the exception of followed children)
* visibility is limited to the system call interface

Useful resources:

* [strace Wow Much Syscall (original)](http://www.brendangregg.com/blog/2014-05-11/strace-wow-much-syscall.html)

</details>

<details>
<summary><b>MySQL replication for one Slave is failing. How do you troubleshoot the issue?</b></summary><br>

* Check the MySQL error log on both the master and the slave servers. Look for any error messages that might indicate the source of the problem.
* Verify that the slave server is connected to the master server and that the replication process is running. You can do this by running the following command on the slave server:
`SHOW SLAVE STATUS\G`
* This command will show you the current replication status of the slave, including the replication thread state, the last SQL statement executed, and the current position in the replication stream.
* Check the network connectivity between the master and slave servers. Make sure that there are no firewalls or other network devices blocking the replication traffic.
* Verify that the data on the slave server matches the data on the master server. You can do this by comparing the output of the following commands on both the master and the slave servers:
`SELECT COUNT(*) FROM table_name;`
* If the number of rows returned by the two commands does not match, then there is a problem with the replication process.
* Check the MySQL configuration files on both the master and slave servers. Verify that the replication settings are correct and that the servers are configured to use the same character set and collation.
* If none of the above steps resolve the issue, you may need to rebuild the replication process from scratch. This involves stopping the replication process, resetting the slave server to the master's current position in the replication stream, and then restarting the replication process.
* Monitor the replication process for a period of time to ensure that it is working correctly.

Useful resources:

* [MySQL: Troubleshooting Replication](https://dev.mysql.com/doc/mysql-replication-excerpt/8.0/en/replication-problems.html)

</details>

#### Network Questions

<details>
<summary><b>Is it better to set <code>-j REJECT</code> or <code>-j DROP</code> in iptables?</b></summary><br>

Using -j REJECT will send an error message back to the client, letting them know that their request was denied. This can be useful for troubleshooting and for providing feedback to legitimate users. It also makes it easier to identify and investigate potential attacks or suspicious activity.

Using -j DROP, on the other hand, simply discards the traffic without providing any feedback to the client. This can be useful for denying traffic from known malicious sources or for denying traffic to services that should not be accessible from the public internet.

Useful resources:

* [Is it better to set -j REJECT or -j DROP in iptables?](https://unix.stackexchange.com/questions/109459/is-it-better-to-set-j-reject-or-j-drop-in-iptables)
* [Drop versus Reject](https://www.chiark.greenend.org.uk/~peterb/network/drop-vs-reject)

</details>

<details>
<summary><b>What is ARP?</b></summary><br>

ARP, or Address Resolution Protocol can be likened to DNS for MAC Addresses. Standard DNS allows for the mapping of human-friendly URLs to IP addresses, while ARP allows for the mapping of IP addresses to MAC addresses. In this way it lets systems go from a regular domain name down to the actual piece of hardware it resides upon.

</details>

<details>
<summary><b>If you try resolve hostname you get <code>NXDOMAIN</code> from <code>host</code> command. Your <code>resolv.conf</code> stores two nameservers but only second of this store this domain name. Why did not the local resolver check the second nameserver?</b></summary><br>

**NXDOMAIN** is nothing but non-existent Internet or Intranet domain name. If domain name is unable to resolved using the DNS, a condition called the **NXDOMAIN** occurred.

The default behavior for `resolv.conf` and the `resolver` is to try the servers in the order listed. The resolver will only try the next nameserver if the first nameserver times out.

The algorithm used is to try a name server, and if the query times out, try the next, until out of name servers, then repeat trying all the name servers until a maximum number of retries are made.

If a nameserver responds with **SERVFAIL** or a referral (**nofail**) or terminate query (**fail**) also only the first dns server will be used.

Example:

```plaintext
nameserver 192.168.250.20   # it's not a dns
nameserver 8.8.8.8          # not store gate.test.int
nameserver 127.0.0.1        # store gate.test.int
```

so if you check:

```bash
host -v -t a gate.test.int
Trying "gate.test.int"                        # trying first dns (192.168.250.20) but response is time out, so try the next nameserver
Host gate.test.int not found: 3(NXDOMAIN)     # ok but response is NXDOMAIN (not found this domain name)
Received 88 bytes from 8.8.8.8#53 in 43 ms
Received 88 bytes from 8.8.8.8#53 in 43 ms
                                              # so the last server in the list was not asked
```

To avoid this you can use e.g. `nslookup` command which will use the second nameserver if it receives a **SERVFAIL** from the first nameserver.

Useful resources:

* [Second nameserver in /etc/resolv.conf not picked up by wget](https://serverfault.com/questions/398837/second-nameserver-in-etc-resolv-conf-not-picked-up-by-wget)

</details>

<details>
<summary><b>A client of the company you work at reports their server has stopped receiving data from your server. Go through the steps of troubleshooting the issue both on your end and your communications with them.</b></summary><br>

### 1. **Gather Information from the Client**

* **Initial Communication**:
  * **Ask the client** for details: When did the issue start? What kind of data is not being received (specific service, API, etc.)? Are there any error messages or logs that indicate the failure?
  * **Determine any changes**: Ask if they have recently changed firewall rules, network configuration, or updated software (on either the server or network layer).
  * **Get context**: Determine if this is an intermittent issue or a complete failure, and whether the failure is only with your server or across multiple services.

### 2. **Verify Connectivity and Status on Your End**

* **Check server health**:
  * Ensure your server is running normally and that the service responsible for sending the data is active (e.g., database, API server, or file transfer service).
  * Check for any recent service or network configuration changes that could affect outbound data transmission.
* **Network/Firewall checks**:
  * Review firewall rules and security groups to ensure that the necessary ports for communication with the client's server are open (e.g., port 80 for HTTP, 443 for HTTPS, or any other relevant protocol).
  * If your infrastructure uses a load balancer, ensure it's forwarding traffic to the correct backend servers and that no misconfigurations exist.
* **Logs inspection**:
  * Look at your server logs for any failed data transfers or connection attempts. This could provide insight into whether your server is attempting to send data and encountering failures.
  * Check the logs of the relevant service (e.g., web server, API service, or data processing system) to see if there are errors during the data transmission.
* **Data queues and buffers**:
  * If you're using a message queue or batch system, check whether data has accumulated in queues or is stuck in transit.
  * Investigate if there are network timeouts or message drop issues.

### 3. **Perform Connectivity Tests**

* **Ping test**: Try pinging the client's server from your server to verify basic connectivity (if ICMP is allowed).
* **Traceroute**: Run a traceroute from your server to their server to diagnose network issues, like routing problems or latency spikes.
* **Port tests**: Use `nc` (netcat) to verify that you can reach the relevant service port on the client’s server.
* **Test data transmission**:
  * Send a test request (e.g., using `curl` or `wget`) to their endpoint and inspect the response. This will show whether the server is reachable and how it responds.
  * If data is transferred via an API, manually call the API with the expected payload and verify the result.

### 4. **Communicate with the Client Throughout**

* **Initial response**:
  * Let the client know you are investigating the issue and outline the steps you are taking.
  * Ask for specific logs or monitoring data from their side that could give more details (e.g., HTTP logs, connection errors, or security event logs).
* **Share findings**:
  * If you identify issues on your end, communicate them and provide an estimated resolution time.
  * If no issues are found on your side, let them know what tests you’ve conducted and share the results (e.g., ping success, traceroute path).
* **Request client-side checks**:
  * Ask the client to verify the health of their server, including whether their services are running correctly and whether they can reach your server.
  * Suggest they perform similar tests: ping, traceroute, and port checks from their server to your server. This will help identify if the issue lies within their network or your connection.
  * If they use firewalls or security appliances, ask them to confirm that traffic from your IP address is not being blocked.
* **Suggest a temporary bypass**:
  * If possible, ask the client to disable any recent firewall rules or security features temporarily to rule out misconfigurations.

### 5. **Investigate External Factors**

* **DNS Issues**: Check whether the DNS name used to connect to the client’s server is resolving correctly. Ask the client if they’ve made any DNS changes recently.
* **ISP/Network provider issues**: If connectivity seems fine but data still isn’t flowing, investigate whether an issue exists with either your ISP or the client’s ISP, especially if routing paths or latency are problematic.

### 6. **Escalation and Collaboration**

* **Involve Network and Security Teams**: If the issue appears network-related, escalate it to your network team or security team to check for deeper routing or firewall issues (both on your side and theirs).
* **Set up a conference call**: If needed, set up a real-time troubleshooting session with the client’s technical team. This allows both sides to run tests in parallel and exchange findings quickly.

### 7. **Monitor and Confirm Resolution**

* **Test again**: After making any changes, send test data from your server to the client’s server and confirm successful transmission.
* **Ask for confirmation**: Request the client to confirm that they are now receiving the data and that everything is working as expected.
* **Monitor for stability**: Keep an eye on logs and monitoring systems to ensure the issue is fully resolved and doesn’t reoccur.

</details>

<details>
<summary><b>What is SNI SSL and in which cases it is useful?</b></summary><br>

SNI (Server Name Indication) is an extension to the SSL/TLS protocol that allows a client to specify the hostname it is trying to connect to during the SSL handshake. This enables the server to present the correct SSL certificate based on the requested hostname, even when multiple domain names are hosted on the same IP address.

### When SNI SSL is useful

1. **Multiple SSL certificates on the same IP address**: SNI allows hosting multiple SSL-enabled websites on a single IP address. Without SNI, each site would need a unique IP address to present the correct SSL certificate.

2. **Shared hosting environments**: For providers hosting numerous websites on the same server, SNI allows serving multiple HTTPS sites from the same server, making it cost-effective and scalable without needing separate IP addresses.

3. **Cloud and CDN services**: SNI enables cloud and content delivery services to handle multiple secure domains without requiring multiple IP addresses or additional configuration, especially when traffic routing to different backend services.

4. **Virtual hosting**: In virtual hosting environments (where one server hosts multiple domains), SNI is essential for serving different SSL certificates for different domains over HTTPS on the same IP address.

</details>

<details>
<summary><b>What types of DNS cache are being checked when you type example.com in your browser and press return?</b></summary><br>

Browser checks if the domain is in its cache. When this cache fails, it simply asks the OS to resolve the domain.

The OS resolver has its own cache which it will check. If it fails this, it resorts to asking the OS configured DNS servers.

The OS configured DNS servers will typically be configured by DHCP from the router where the DNS servers are likely to be the ISP's DNS servers configured by DHCP from the internet gateway to the router.

In the event the router has its own DNS servers, it may have its own cache otherwise you should be directed straight to your ISP's DNS servers most typically as soon as the OS cache was found to be empty.

Useful resources:

* [What happens when...](https://github.com/alex/what-happens-when)
* [DNS Explained - How Your Browser Finds Websites](https://scotch.io/tutorials/dns-explained-how-your-browser-finds-websites)
* [Firefox invalidate dns cache](https://stackoverflow.com/questions/13063496/firefox-invalidate-dns-cache)

</details>

<details>
<summary><b>What are the layers in OSI Reference Models? Describe each layer briefly.</b></summary><br>

a) <b>Physical Layer (Layer 1)</b>: It converts data bits into electrical impulses or radio signals. Example: Ethernet.

b) <b>Data Link Layer (Layer 2)</b>: At the Data Link layer, data packets are encoded and decoded into bits, and it provides a node to node data transfer. This layer also detects the errors that occurred at Layer 1.

c) <b>Network Layer (Layer 3)</b>: This layer transfers variable length data sequence from one node to another node in the same network. This variable-length data sequence is also known as “Datagrams”.

d) <b>Transport Layer (Layer 4)</b>: It transfers data between nodes and also provides acknowledgment of successful data transmission. It keeps track of transmission and sends the segments again if the transmission fails.

e) <b>Session Layer (Layer 5)</b>: This layer manages and controls the connections between computers. It establishes, coordinates, exchange and terminates the connections between local and remote applications.

f) <b>Presentation Layer (Layer 6)</b>: It is also called as “Syntax Layer”. Layer 6 transforms the data into the form in which the application layer accepts.

g) <b>Application Layer (Layer 7)</b>: This is the last layer of the OSI Reference Model and is the one that is close to the end-user. Both end-user and application layer interacts with the software application. This layer provides services for email, file transfer, etc.

</details>

#### Cybersecurity Questions

<details>
<summary><b>Explain briefly how the Spectre vulnerability works.</b></summary><br>

The Spectre vulnerability is a class of speculative execution attacks that can allow an attacker to read sensitive data from the memory of a victim process. The vulnerability arises due to the speculative execution feature of modern processors, where they attempt to predict future program behavior and execute instructions in advance to improve performance. Spectre exploits the branch prediction mechanism of the processor to leak information from one process to another or even from the kernel to user-space applications.

The Spectre attack works by tricking the processor's branch predictor into speculatively executing a set of instructions that should not be executed based on the actual program control flow. The attacker then carefully times their own code to observe the effects of these speculatively executed instructions, such as changes to the processor cache or other side effects. By analyzing these effects, the attacker can deduce the contents of sensitive data stored in memory, including passwords, cryptographic keys, and other confidential information.

Useful resources:

* [Spectre (security vulnerability)](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability))

</details>

<details>
<summary><b>What is the difference between policies, processes and guidelines?</b></summary><br>

* Policies: Policies are high-level statements that define an organization's rules and principles. They provide a framework for decision-making and guide employees in their actions. Policies are typically developed by senior management and are designed to align with the organization's mission, values, and strategic goals. Examples of policies include information security policy, acceptable use policy, and employee code of conduct.

* Processes: Processes are a set of interrelated activities that transform inputs into outputs. They describe how work is done in an organization and provide a structured approach to achieving specific objectives. Processes are often defined at a lower level than policies and are designed to be repeatable and scalable. Examples of processes include incident management process, change management process, and procurement process.

* Guidelines: Guidelines are recommendations or best practices that provide direction on how to achieve a specific objective. Unlike policies and processes, guidelines are not mandatory and are often subject to interpretation. They are designed to assist employees in making decisions and performing tasks. Guidelines can be developed internally or externally, and they may be specific to a particular function or industry. Examples of guidelines include security configuration guidelines, data retention guidelines, and accessibility guidelines.

</details>

<br>

## <a name="extra-knowledge">Extra Knowledge</a>

<details>
<summary><b>Explain what is Event-Driven architecture and how it improves performance?</b></summary><br>

An event-driven architecture uses events to trigger and communicate between decoupled services; an event being a change in state. Event-driven architecture allows for proper and easier decoupling of services, less resource usage by being push-based, and easier to add consumers to scale.

</details>

<details>
<summary><b>Explain <code>:(){ :|:& };:</code> and how stop this code if you are already logged into a system?</b></summary><br>

It's a **fork bomb**.

* `:()` - this defines the function. `:` is the function name and the empty parenthesis shows that it will not accept any arguments
* `{ }` - these characters shows the beginning and end of function definition
* `:|:` - it loads a copy of the function `:` into memory and pipe its output to another copy of the `:` function, which has to be loaded into memory
* `&` - this will make the process as a background process, so that the child processes will not get killed even though the parent gets auto-killed
* `:` - final `:` will execute the function again and hence the chain reaction begins

The best way to protect a multi-user system is to use **PAM** to limit the number of processes a user can use. We know the biggest problem with a fork bomb is the fact it takes up so many processes.

So we have two ways of attempting to fix this, if you are already logged into the system:

* execute a **SIGSTOP** command to stop the process: `killall -STOP -u user1`
* if you can't run at the command line you will have to use `exec` to force it to run (due to processes all being used): `exec killall -STOP -u user1`

With fork bombs, the best thing to do is preventing it from being an issue in the first place.

</details>

<details>
<summary><b>How do you recover a deleted file still held open, e.g. by Apache?</b></summary><br>

If a file has been deleted but is still open, that means the file still exists in the filesystem (it has an inode) but has a hard link count of 0. Since there is no link to the file, you cannot open it by name. There is no facility to open a file by inode either.

Linux exposes open files through special symbolic links under `/proc`. These links are called `/proc/12345/fd/42` where 12345 is the **PID** of a process and 42 is the number of a file descriptor in that process. A program running as the same user as that process can access the file (the read/write/execute permissions are the same you had as when the file was deleted).

The name under which the file was opened is still visible in the target of the symbolic link: if the file was `/var/log/apache/foo.log`, then the target of the link is `/var/log/apache/foo.log (deleted)`.

Thus, you can recover the content of an open deleted file given the **PID** of a process that has it open and the descriptor that it's opened on like this:

```bash
recover_open_deleted_file () {
  old_name=$(readlink "$1")
  case "$old_name" in
    *' (deleted)')
      old_name=${old_name%' (deleted)'}
      if [ -e "$old_name" ]; then
        new_name=$(TMPDIR=${old_name%/*} mktemp)
        echo "$oldname has been replaced, recovering content to $new_name"
      else
        new_name="$old_name"
      fi
      cat <"$1" >"$new_name";;
    *) echo "File is not deleted, doing nothing";;
  esac
}
recover_open_deleted_file "/proc/$pid/fd/$fd"
```

If you only know the process **ID** but not the descriptor, you can recover all files with:

```bash
for x in /proc/$pid/fd/* ; do
  recover_open_deleted_file "$x"
done
```

If you don't know the process **ID** either, you can search among all processes:

```bash
for x in /proc/[1-9]*/fd/* ; do
  case $(readlink "$x") in
    /var/log/apache/*) recover_open_deleted_file "$x";;
  esac
done
```

You can also obtain this list by parsing the output of `lsof`, but it isn't simpler nor more reliable nor more portable (this is Linux-specific anyhow).

</details>

<details>
<summary><b>Rsync triggered the Linux OOM killer on a single 50 GB file. How does the OOM killer decide which process to kill first? How to control this?</b></summary><br>

Major distribution kernels set the default value of `/proc/sys/vm/overcommit_memory` to zero, which means that processes can request more memory than is currently free in the system.

If memory is exhaustively used up by processes, to the extent which can possibly threaten the stability of the system, then the **OOM killer** comes into the picture.

NOTE: It is the task of the **OOM Killer** to continue killing processes until enough memory is freed for the smooth functioning of the rest of the process that the Kernel is attempting to run.

The **OOM Killer** has to select the best process(es) to kill. Best here refers to that process which will free up the maximum memory upon killing and is also the least important to the system.

The primary goal is to kill the least number of processes that minimizes the damage done and at the same time maximizing the amount of memory freed.

To facilitate this, the kernel maintains an `oom_score` for each of the processes. You can see the oom_score of each of the processes in the `/proc` filesystem under the pid directory.

  > When analyzing OOM killer logs, it is important to look at what triggered it.

```bash
cat /proc/10292/oom_score
```

The higher the value of `oom_score` of any process, the higher is its likelihood of getting killed by the **OOM Killer** in an out-of-memory situation.

If you want to create a special control group containing the list of processes which should be the first to receive the **OOM killer's** attention, create a directory under `/mnt/oom-killer` to represent it:

```bash
mkdir lambs
```

Set `oom.priority` to a value high enough:

```bash
echo 256 > /mnt/oom-killer/lambs/oom.priority
```

`oom.priority` is a 64-bit unsigned integer, and can have a maximum value an unsigned 64-bit number can hold. While scanning for the process to be killed, the **OOM-killer** selects a process from the list of tasks with the highest `oom.priority` value.

Add the PID of the process to be added to the list of tasks:

```bash
echo <pid> > /mnt/oom-killer/lambs/tasks
```

To create a list of processes, which will not be killed by the **OOM-killer**, make a directory to contain the processes:

```bash
mkdir invincibles
```

Setting `oom.priority` to zero makes all the process in this cgroup to be excluded from the list of target processes to be killed.

```bash
echo 0 > /mnt/oom-killer/invincibles/oom.priority
```

To add more processes to this group, add the pid of the task to the list of tasks in the invincible group:

```bash
echo <pid> > /mnt/oom-killer/invincibles/tasks
```

Useful resources:

* [Rsync triggered Linux OOM killer on a single 50 GB file](https://serverfault.com/questions/724469/rsync-triggered-linux-oom-killer-on-a-single-50-gb-file)
* [Taming the OOM killer](https://lwn.net/Articles/317814/)

</details>

<details>
<summary><b>You have a lot of sockets hanging in <code>TIME_WAIT</code>. Your http service is behind a proxy and serves a lot of small http requests. How to check and reduce <code>TIME_WAIT</code> sockets?</b></summary><br>

To check and reduce the number of `TIME_WAIT` sockets on a server handling many small HTTP requests behind a proxy:

### Check `TIME_WAIT` Sockets

* Use tools like `ss` or `netstat` to view the number of sockets in `TIME_WAIT`.
* Get detailed information to diagnose the connections causing `TIME_WAIT`.

### Reduce `TIME_WAIT` Sockets

1. **Enable TCP socket reuse**: Allow the system to reuse `TIME_WAIT` sockets for new connections when safe.
2. **Lower `TIME_WAIT` duration**: Adjust the timeout value for `TIME_WAIT` to shorten the time sockets remain in this state.
3. **Increase available ports**: Expand the range of ephemeral ports to reduce port exhaustion.
4. **Use Keep-Alive connections**: Enable keep-alive in your web server or proxy to reuse connections and reduce the creation of new ones.
5. **Tune proxy settings**: Adjust connection handling settings in the proxy to minimize socket overhead.

After applying these settings, monitor the system to ensure the changes effectively reduce `TIME_WAIT` sockets without impacting service. Make these settings persistent by adding them to your system configuration.

Useful resources:

* [How to reduce number of sockets in TIME_WAIT?](https://serverfault.com/questions/212093/how-to-reduce-number-of-sockets-in-time-wait)

</details>

<details>
<summary><b>In context of an Operating System, what are Protection Rings?</b></summary><br>

**Protection Rings** are a mechanism used by an operating system to control access to hardware and system resources, providing a hierarchical level of privilege for executing code. The concept is often associated with **CPU architecture**, particularly in modern processors (like x86). Protection rings enforce different levels of permissions, thereby improving system security and stability by isolating different types of code execution.

### Key Concepts

* **Rings**: Protection rings are typically visualized as concentric layers, with **Ring 0** at the center, representing the most privileged level, and outer rings (like **Ring 3**) representing less privileged levels.

* **Ring 0 (Kernel Mode or Supervisor Mode)**:
  * The **most privileged** level, where the operating system kernel and core system components run.
  * Code running in this ring has **direct access** to hardware resources (e.g., memory, CPU, and I/O devices) and can execute privileged instructions.
  * Only trusted, critical system processes run in Ring 0, as a failure or security breach at this level can compromise the entire system.

* **Ring 1 and Ring 2** (Often Unused in Modern Systems):
  * Historically, **Ring 1** and **Ring 2** were designed for device drivers or lower-level system services that needed more privileges than user applications but less than the kernel.
  * In practice, modern operating systems typically combine Rings 1 and 2 into **Ring 0**, so these rings are often unused.

* **Ring 3 (User Mode)**:
  * The **least privileged** ring, where **user applications** and **processes** run.
  * Code in Ring 3 has **no direct access to hardware** or system resources. Instead, user-mode applications must make system calls (via the kernel) to interact with hardware or perform privileged operations.
  * Isolating user processes in this ring ensures that even if an application crashes or is compromised, it cannot directly affect the kernel or other system resources.

### Why Protection Rings Matter

1. **Security**: By restricting privileged access, protection rings limit the potential impact of malicious or buggy code. Code running in lower-privilege rings (e.g., user applications) cannot directly interfere with the system or other applications.

2. **Stability**: If an application or driver running in a less privileged ring fails, it cannot crash the entire system because it doesn't have access to critical kernel-level resources.

3. **Controlled Access to Resources**: System resources (like memory, I/O, and CPU instructions) are protected by limiting direct access to Ring 0. All requests from Ring 3 (user mode) must go through the kernel (via system calls), allowing the OS to manage and enforce security policies.

### Common OS Implementation

* **Most modern operating systems** like Linux, Windows, and macOS, typically implement **two rings**:
  * **Ring 0**: Kernel mode, where the OS kernel and low-level drivers run.
  * **Ring 3**: User mode, where applications and services run.
  
### Virtualization and Hypervisors

* In virtualized environments, a **Ring -1** is sometimes used for the **hypervisor**, which controls virtual machines. This allows the hypervisor to manage multiple operating systems, each operating in its own Ring 0, without them having direct access to the actual hardware.

* [What are Rings in Operating Systems?](https://www.baeldung.com/cs/os-rings)
* [Protecting Ring](https://en.wikipedia.org/wiki/Protection_ring)

</details>

<details>
<summary><b>Is it possible to have SSL certificate for IP address, not domain name?</b></summary><br>

It is possible (but rarely used) as long as it is a public IP address.

An SSL certificate is typically issued to a Fully Qualified Domain Name (FQDN) such as `https://www.domain.com`. However, some organizations need an SSL certificate issued to a public IP address. This option allows you to specify a public IP address as the Common Name in your Certificate Signing Request (CSR). The issued certificate can then be used to secure connections directly with the public IP address (e.g. `https://1.1.1.1`.).

According to the CA Browser forum, there may be compatibility issues with certificates for IP addresses unless the IP address is in both the commonName and subjectAltName fields. This is due to legacy SSL implementations which are not aligned with RFC 5280, notably, Windows OS prior to Windows 10.

Useful resources:

* [Are SSL certificates bound to the servers ip address?](https://stackoverflow.com/questions/1095780/are-ssl-certificates-bound-to-the-servers-ip-address)
* [SSL certificate for a public IP address?](https://serverfault.com/questions/193775/ssl-certificate-for-a-public-ip-address)

</details>
