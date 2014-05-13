AxisGetCurrentImageUsingQt
==========================


version 1
I debug one of the bug in my code in function GetCurrentImage:
priviously it reports can not access to QVariant private, it is because 

I want to use QVariant* MediaBuffer;
but QList<QVariant> varList; 
    varList <<0<<MediaBuffer<<MediaBufferSize;

    QVariant can not accpet address type,

so this can be achieved by:
	
	QVariant MediaBuffer;
	long MediaBufferSize
	QList<QVariant> varList;
    varList << 0 << MediaBuffer << MediaBufferSize;

    axWidget->dynamicCall("GetCurrentImage(int, QVariant&, long&)",varList);




/***************/

AxisGetCurrentImageUsingQt
Axis getCurrentImage 

it is a very small program 
that implement 

1. play network video

2. stop network video

3. snapshot the video

4. getCurrentImage 

the 4th function can be used for image processing in the program in the future 

but the getCurrentImage function has bug in it
if you can debug this problem out, please let me know by post message on 
http://qt-project.org/forums/viewthread/42370/


you can play with this code after installing the AXIS Media Control sdk, which only need few second to install them
below is the address of AXIS Media Control sdk,

http://www.axis.com/techsup/cam_servers/dev/activex.htm

the function document is under the doc in the installing directory (..\AXIS Media Control SDK\doc)

running environment
qt 4.8.5
qtcreator 3.1.0
visual studio 2010 compiler



best regards,

szysagittarius
