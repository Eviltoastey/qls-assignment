**Project setup QLS**


1. go to root and run npm install
2. install all composer dependencies
3. run make up


**S3 bucket**
For this product im using an AWS S3 bucket. The credentials for this I will send in an email!
Or you can couple it with your own AWS bucket if you have one.


**NOTES**

Make sure that you have imagick on your system.

brew install imagemagick
pecl install imagick



Imagick doesnt have permission in docker to make the image into a PDF. I tried to adjust the dockerfile so it would work but it didnt..
Debugging took a bit long so if youre running the code in docker and have the same problem do the following:


run: ./vendor/bin/sail exec laravel.test bash

Now youre in the container

find / -name policy.xml 2>/dev/null

When this return the policy path copy it and run:

nano YOURPATHHERE
