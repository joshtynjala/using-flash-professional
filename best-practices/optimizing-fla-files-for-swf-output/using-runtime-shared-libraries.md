# Using runtime shared libraries

You can sometimes improve download time by using runtime shared libraries. These
libraries are usually necessary for larger applications or when numerous
applications on a site use the same components or symbols. By externalizing the
common assets of your SWF files, you do not download classes repeatedly. The
first SWF file that uses a shared library has a longer download time, because
both the SWF file and the library load. The library caches on the user's
computer, and then all the subsequent SWF files use the library. This process
can greatly improve download time for some larger applications.
