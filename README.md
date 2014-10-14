# This is NOT the official repo for osslsigncode  
This project was copied from osslsigncode 1.7.1 to apply some patches for compiling with cygwin and being able to add unauthenticated blobs.  The official source for the project is at: http://sourceforge.net/projects/osslsigncode/


You will see a message "WARNING This is NOT the official osslsigncode project." when you run it.

## Compiling under cygwin

- Ensure you install the development libraries for openssl, libgfs, and curl.
- Install pkg-config


## Features added
Adds the argument "-addBlob" to add a 1024 byte unauthenticated blob of data to the signature in the same area as the timestamp.  You can take a code signed file and run "osslsigncode.exe add -addBlob -in myfile.exe -out myoutfile.exe"

This technique is used by Dropbox as discussed here:

- https://tech.dropbox.com/2014/08/tech-behind-dropboxs-new-user-experience-for-mobile/
- http://blogs.msdn.com/b/ieinternals/archive/2014/09/04/personalizing-installers-using-unauthenticated-data-inside-authenticode-signed-binaries.aspx
