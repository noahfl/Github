# ABOUT #

The premise of this project is to examine the C functions used by web browsers and see what information can be extrapolated from them. Variations on this concept include running based on limited information (small windows of functions).

This repo contains the standard program that reads an entire strace file as well as the program that reads small chunks of strace files and determines which site they're generated from.

Note: This repo is similar to motif-site_grouping, but has more output files available. Mostly for record keeping purposes.

#Requirements#
- SciPy
- NumPy
- Scikit-learn


#Program Notes#

curl/wget:

www.google.com
www.reddit.com
www.yahoo.com
www.microsoft.com
www.wfu.edu
www.nyu.edu
www.netflix.com
www.amazon.com
www.soundcloud.com
www.youtube.com

//TODO
websites that don't exist
set some flags
downloading files
big websites (lots of traffic)

ls:

~/
~/Documents
~/Desktop
~/Downloads
~/grive
~/Music
~/Pictures
~/Public
~/Videos
~/Templates

//TODO
add flags (for all dirs done before)
- done, used flags -a, -h, -l, -F
nonexistent directory

strace:

ls
wget www.google.com
curl www.google.com
cal
dir
df
ping www.google.com
vi
date
dc

more/less:
output_parser_0.3.py
window_classifier.py
curl_1.txt
curl_10.txt
ls_1.txt
ls_10.txt
strace_1.txt
strace_10.txt
wget_1.txt
wget_10.txt


new ones:

ssh
telnet
sftp
scp
ftp


can you predict an application will end?
vector for end lines
vector for elsewhere
id's for each, run and see

checking number of connections:

ps -ef
more proc/[proc_num]/net/sockstat

wget www.google.com & 


Goal:

create sliding window (n, n+1, etc.)
that serves as testing set
use current output chunks as testing set
see if utility can make a prediction
