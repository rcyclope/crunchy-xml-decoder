crunchy-xml-decoder
===================

Requires PyCrypto (http://www.voidspace.org.uk/python/modules.shtml#pycrypto) and lxml (https://pypi.python.org/pypi/lxml/3.2.5)
if crunchy-xml-decoder could automatically install PyCrypto and lxml use the above link to download manually 


This is a composite of various scripts required to download video files from CrunchyRoll 
that have been automated with a batch file.


INSTRUCTIONS:

    Pre-Setup (Only need to do these once.):
    1.  Install Python 2.7.5. (sudo apt-get install  python2.7 libxml2-dev libxslt1-dev python-dev )
    2.  Install lxml (sudo apt-get install python-lxml or sudo easy_install lxml )
    3.  Install PyCrypto ( sudo easy_install pycrypto-2.6.1 )
    4.  Install RTMPDUMP ( sudo apt-get install rtmpdump )
    5.  Install Mkvtoolnix ( sudo apt-get install mkvtollnix )
    6.  Run crunchy-xml-decoder.bat or crunchy-xml-decoder.py to generate necessary files (settings.ini and cookies)
    7.  choices	from the option 

    Per-Video Process:
    1.  Copy the URL of the CrunchyRoll video you want to download from your web browser
    2.  Run crunchy-xml-decoder.bat or crunchy-xml-decoder.py choice 1 and paste link
    8.  Download will start automatically. Everything is automated.
    11. Browse to the 'export' folder to view the completed file.


WHAT IS THE POINT OF THIS SCRIPT? WHAT IS IT ACTUALLY DOING?:

    The process of getting a working download from CrunchyRoll is effectively doing the following:
        - Downloading and decrypting subtitles
        - Downloading the video as FLV
        - Splitting the FLV file into 264 video and aac audio
        - Merging video, audio, and subtitles into a mkv file
        - Naming the new video something other than 'video.mkv'


NOTES FROM THE AUTHORS:
    From the DX author:
        Yeah, I wrote the basis for this "new 'n' improved version". Basically, I monitored the traffic
        to and from Crunchyroll while a video was loading, found a few (read: a lot of) similarities, and
        basically wrote the script to do the same thing, but parse the file and call upon RTMPdump to
        dump the video (RTMPexplorer was doing the same thing basically).

    From the anonymous original author:
        I did not write these programs, and I didn't even come up with this method. All I have done is 
        created a few little bat files to bring them together. Original instructions on how this is 
        done can be found here: 
        http://www.darkztar.com/forum/showthread.php?219034-Ripping-videos-amp-subtitles-from-Crunchyroll-%28noob-friendly%29
