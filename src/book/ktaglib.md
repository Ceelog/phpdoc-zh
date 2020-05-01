KTaglib
=======

**目录**

-   [简介](/intro/ktaglib.html)
-   [安装／配置](/ktaglib/setup.html)
    -   [需求](/ktaglib/setup.html#需求)
    -   [安装](/ktaglib/setup.html#安装)
-   [预定义常量](/ktaglib/constants.html)
-   [KTaglib\_MPEG\_File](/class/ktaglib-mpeg-file.html) — The
    KTaglib\_MPEG\_File class
    -   [KTaglib\_MPEG\_File::\_\_construct](/class/ktaglib-mpeg-file.html#KTaglib_MPEG_File::__construct)
        — Opens a new file
    -   [KTaglib\_MPEG\_File::getAudioProperties](/class/ktaglib-mpeg-file.html#KTaglib_MPEG_File::getAudioProperties)
        — Returns an object that provides access to the audio properties
    -   [KTaglib\_MPEG\_File::getID3v1Tag](/class/ktaglib-mpeg-file.html#KTaglib_MPEG_File::getID3v1Tag)
        — Returns an object representing an ID3v1 tag
    -   [KTaglib\_MPEG\_File::getID3v2Tag](/class/ktaglib-mpeg-file.html#KTaglib_MPEG_File::getID3v2Tag)
        — Returns a ID3v2 object
-   [KTaglib\_MPEG\_AudioProperties](/class/ktaglib-mpeg-audioproperties.html)
    — The KTaglib\_MPEG\_AudioProperties class
    -   [KTaglib\_MPEG\_AudioProperties::getBitrate](/class/ktaglib-mpeg-audioproperties.html#KTaglib_MPEG_AudioProperties::getBitrate)
        — Returns the bitrate of the MPEG file
    -   [KTaglib\_MPEG\_AudioProperties::getChannels](/class/ktaglib-mpeg-audioproperties.html#KTaglib_MPEG_AudioProperties::getChannels)
        — Returns the amount of channels of a MPEG file
    -   [KTaglib\_MPEG\_AudioProperties::getLayer](/class/ktaglib-mpeg-audioproperties.html#KTaglib_MPEG_AudioProperties::getLayer)
        — Returns the layer of a MPEG file
    -   [KTaglib\_MPEG\_AudioProperties::getLength](/class/ktaglib-mpeg-audioproperties.html#KTaglib_MPEG_AudioProperties::getLength)
        — Returns the length of a MPEG file
    -   [KTaglib\_MPEG\_AudioProperties::getSampleBitrate](/class/ktaglib-mpeg-audioproperties.html#KTaglib_MPEG_AudioProperties::getSampleBitrate)
        — Returns the sample bitrate of a MPEG file
    -   [KTaglib\_MPEG\_AudioProperties::getVersion](/class/ktaglib-mpeg-audioproperties.html#KTaglib_MPEG_AudioProperties::getVersion)
        — Returns the version of a MPEG file
    -   [KTaglib\_MPEG\_AudioProperties::isCopyrighted](/class/ktaglib-mpeg-audioproperties.html#KTaglib_MPEG_AudioProperties::isCopyrighted)
        — Returns the copyright status of an MPEG file
    -   [KTaglib\_MPEG\_AudioProperties::isOriginal](/class/ktaglib-mpeg-audioproperties.html#KTaglib_MPEG_AudioProperties::isOriginal)
        — Returns if the file is marked as the original file
    -   [KTaglib\_MPEG\_AudioProperties::isProtectionEnabled](/class/ktaglib-mpeg-audioproperties.html#KTaglib_MPEG_AudioProperties::isProtectionEnabled)
        — Returns if protection mechanisms of an MPEG file are enabled
-   [KTaglib\_Tag](/class/ktaglib-tag.html) — The KTaglib\_Tag class
    -   [KTaglib\_Tag::getAlbum](/class/ktaglib-tag.html#KTaglib_Tag::getAlbum)
        — Returns the album string from a ID3 tag
    -   [KTaglib\_Tag::getArtist](/class/ktaglib-tag.html#KTaglib_Tag::getArtist)
        — Returns the artist string from a ID3 tag
    -   [KTaglib\_Tag::getComment](/class/ktaglib-tag.html#KTaglib_Tag::getComment)
        — Returns the comment from a ID3 tag
    -   [KTaglib\_Tag::getGenre](/class/ktaglib-tag.html#KTaglib_Tag::getGenre)
        — Returns the genre from a ID3 tag
    -   [KTaglib\_Tag::getTitle](/class/ktaglib-tag.html#KTaglib_Tag::getTitle)
        — Returns the title string from a ID3 tag
    -   [KTaglib\_Tag::getTrack](/class/ktaglib-tag.html#KTaglib_Tag::getTrack)
        — Returns the track number from a ID3 tag
    -   [KTaglib\_Tag::getYear](/class/ktaglib-tag.html#KTaglib_Tag::getYear)
        — Returns the year from a ID3 tag
    -   [KTaglib\_Tag::isEmpty](/class/ktaglib-tag.html#KTaglib_Tag::isEmpty)
        — Returns true if the tag is empty
-   [KTaglib\_ID3v2\_Tag](/class/ktaglib-id3v2-tag.html) — The
    KTaglib\_ID3v2\_Tag class
    -   [KTaglib\_ID3v2\_Tag::addFrame](/class/ktaglib-id3v2-tag.html#KTaglib_ID3v2_Tag::addFrame)
        — Add a frame to the ID3v2 tag
    -   [KTaglib\_ID3v2\_Tag::getFrameList](/class/ktaglib-id3v2-tag.html#KTaglib_ID3v2_Tag::getFrameList)
        — Returns an array of ID3v2 frames, associated with the ID3v2
        tag
-   [KTaglib\_ID3v2\_Frame](/class/ktaglib-id3v2-frame.html) — The
    KTaglib\_ID3v2\_Frame class
    -   [KTaglib\_ID3v2\_Frame::getSize](/class/ktaglib-id3v2-frame.html#KTaglib_ID3v2_Frame::getSize)
        — Returns the size of the frame in bytes
    -   [KTaglib\_ID3v2\_Frame::\_\_toString](/class/ktaglib-id3v2-frame.html#KTaglib_ID3v2_Frame::__toString)
        — Returns a string representation of the frame
-   [KTaglib\_ID3v2\_AttachedPictureFrame](/class/ktaglib-id3v2-attachedpictureframe.html)
    — The KTaglib\_ID3v2\_AttachedPictureFrame class
    -   [KTaglib\_ID3v2\_AttachedPictureFrame::getDescription](/class/ktaglib-id3v2-attachedpictureframe.html#KTaglib_ID3v2_AttachedPictureFrame::getDescription)
        — Returns a description for the picture in a picture frame
    -   [KTaglib\_ID3v2\_AttachedPictureFrame::getMimeType](/class/ktaglib-id3v2-attachedpictureframe.html#KTaglib_ID3v2_AttachedPictureFrame::getMimeType)
        — Returns the mime type of the picture
    -   [KTaglib\_ID3v2\_AttachedPictureFrame::getType](/class/ktaglib-id3v2-attachedpictureframe.html#KTaglib_ID3v2_AttachedPictureFrame::getType)
        — Returns the type of the image
    -   [KTaglib\_ID3v2\_AttachedPictureFrame::savePicture](/class/ktaglib-id3v2-attachedpictureframe.html#KTaglib_ID3v2_AttachedPictureFrame::savePicture)
        — Saves the picture to a file
    -   [KTaglib\_ID3v2\_AttachedPictureFrame::setMimeType](/class/ktaglib-id3v2-attachedpictureframe.html#KTaglib_ID3v2_AttachedPictureFrame::setMimeType)
        — Set's the mime type of the picture
    -   [KTaglib\_ID3v2\_AttachedPictureFrame::setPicture](/class/ktaglib-id3v2-attachedpictureframe.html#KTaglib_ID3v2_AttachedPictureFrame::setPicture)
        — Sets the frame picture to the given image
    -   [KTaglib\_ID3v2\_AttachedPictureFrame::setType](/class/ktaglib-id3v2-attachedpictureframe.html#KTaglib_ID3v2_AttachedPictureFrame::setType)
        — Set the type of the image

简介
----

Represents an MPEG file. MPEG files can have ID3v1, ID3v2 tags and audio
properties.

Class synopsis
--------------

**KTaglib\_MPEG\_File**

<span class="ooclass"> class **KTaglib\_MPEG\_File** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="type">KTaglib\_MPEG\_File</span> <span
class="methodname">getAudioProperties</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">KTaglib\_ID3v1\_Tag</span> <span
class="methodname">getID3v1Tag</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$create`<span
class="initializer"> = **`FALSE`**</span></span> \] )

<span class="modifier">public</span> <span
class="type">KTaglib\_ID3v2\_Tag</span> <span
class="methodname">getID3v2Tag</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$create`<span
class="initializer"> = **`FALSE`**</span></span> \] )

}

KTaglib\_MPEG\_File::\_\_construct
==================================

Opens a new file

### 说明

<span class="modifier">public</span> <span
class="methodname">KTaglib\_MPEG\_File::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

Opens a new MPEG file.

### 参数

`filename`  
The file to read

### 范例

**示例 \#1 Opens a new MP3 file and read the title**

``` php
<?php
$mpeg = new KTaglib_MPEG_File('example.mp3');
echo $mpeg->getID3v1Tag()->getTitle();
?>
```

KTaglib\_MPEG\_File::getAudioProperties
=======================================

Returns an object that provides access to the audio properties

### 说明

<span class="modifier">public</span> <span
class="type">KTaglib\_MPEG\_File</span> <span
class="methodname">KTaglib\_MPEG\_File::getAudioProperties</span> (
<span class="methodparam">void</span> )

Returns an object that provides access to the audio properties of the
mpeg file.

### 返回值

Returns an KTaglib\_MPEG\_AudioProperties object or false.

KTaglib\_MPEG\_File::getID3v1Tag
================================

Returns an object representing an ID3v1 tag

### 说明

<span class="modifier">public</span> <span
class="type">KTaglib\_ID3v1\_Tag</span> <span
class="methodname">KTaglib\_MPEG\_File::getID3v1Tag</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$create`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Returns an object that represents an ID3v1 tag, which can be used to get
information about the ID3v1 tag.

### 返回值

Returns an KTaglib\_MPEG\_ID3v1Tag object or false if there is no ID3v1
tag.

KTaglib\_MPEG\_File::getID3v2Tag
================================

Returns a ID3v2 object

### 说明

<span class="modifier">public</span> <span
class="type">KTaglib\_ID3v2\_Tag</span> <span
class="methodname">KTaglib\_MPEG\_File::getID3v2Tag</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$create`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Returns a ID3v2 object for the mpeg file. If no ID3v2 Tag is present, an
KTaglib\_TagNotFoundException is thrown.

### 返回值

Returns the KTaglib\_ID3v2\_Tag object of the MPEG file or false if
there is no ID3v2 tag

简介
----

Represents the audio properties of a MPEG file, like length, bitrate or
samplerate.

Class synopsis
--------------

**KTaglib\_MPEG\_Audioproperties**

<span class="ooclass"> class **KTaglib\_MPEG\_AudioProperties** </span>
{

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_MPEG\_AudioProperties::getBitrate</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_MPEG\_AudioProperties::getChannels</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_MPEG\_AudioProperties::getLayer</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_MPEG\_AudioProperties::getLength</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_MPEG\_AudioProperties::getSampleBitrate</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_MPEG\_AudioProperties::getVersion</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">KTaglib\_MPEG\_AudioProperties::isCopyrighted</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">KTaglib\_MPEG\_AudioProperties::isOriginal</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">KTaglib\_MPEG\_AudioProperties::isProtectionEnabled</span>
( <span class="methodparam">void</span> )

}

KTaglib\_MPEG\_AudioProperties::getBitrate
==========================================

Returns the bitrate of the MPEG file

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_MPEG\_AudioProperties::getBitrate</span> (
<span class="methodparam">void</span> )

Returns the bitrate of the MPEG file

### 返回值

Returns the bitrate as an integer

KTaglib\_MPEG\_AudioProperties::getChannels
===========================================

Returns the amount of channels of a MPEG file

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_MPEG\_AudioProperties::getChannels</span> (
<span class="methodparam">void</span> )

Returns the amount of channels of the MPEG file

### 返回值

Returns the channel count as an integer

KTaglib\_MPEG\_AudioProperties::getLayer
========================================

Returns the layer of a MPEG file

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_MPEG\_AudioProperties::getLayer</span> (
<span class="methodparam">void</span> )

Returns the layer of the MPEG file (usually 3 for MP3).

### 返回值

Returns the layer as an integer

KTaglib\_MPEG\_AudioProperties::getLength
=========================================

Returns the length of a MPEG file

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_MPEG\_AudioProperties::getLength</span> (
<span class="methodparam">void</span> )

Returns the length of the MPEG file

### 返回值

Returns the length as an integer

KTaglib\_MPEG\_AudioProperties::getSampleBitrate
================================================

Returns the sample bitrate of a MPEG file

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_MPEG\_AudioProperties::getSampleBitrate</span>
( <span class="methodparam">void</span> )

Returns the sample bitrate of the MPEG file

### 返回值

Returns the sample bitrate as an integer

KTaglib\_MPEG\_AudioProperties::getVersion
==========================================

Returns the version of a MPEG file

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_MPEG\_AudioProperties::getVersion</span> (
<span class="methodparam">void</span> )

Returns the version of the MPEG file header. The possible versions are
defined in Tag\_MPEG\_Header (Version1, Version2, Version2.5).

### 返回值

Returns the version

KTaglib\_MPEG\_AudioProperties::isCopyrighted
=============================================

Returns the copyright status of an MPEG file

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">KTaglib\_MPEG\_AudioProperties::isCopyrighted</span>
( <span class="methodparam">void</span> )

Returns true if the MPEG file is copyrighted

### 返回值

Returns true if the MPEG file is copyrighted

KTaglib\_MPEG\_AudioProperties::isOriginal
==========================================

Returns if the file is marked as the original file

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">KTaglib\_MPEG\_AudioProperties::isOriginal</span> (
<span class="methodparam">void</span> )

Returns true if the file is marked as the original file

### 返回值

Returns true if the file is marked as the original file

KTaglib\_MPEG\_AudioProperties::isProtectionEnabled
===================================================

Returns if protection mechanisms of an MPEG file are enabled

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">KTaglib\_MPEG\_AudioProperties::isProtectionEnabled</span>
( <span class="methodparam">void</span> )

Returns true if protection mechanisms (like DRM) are enabled for this
file

### 返回值

Returns true if protection mechanisms (like DRM) are enabled for this
file

简介
----

Base class for ID3v1 or ID3v2 tags

Class synopsis
--------------

**KTaglib\_Tag**

<span class="ooclass"> class **KTaglib\_Tag** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getAlbum</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getArtist</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getComment</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getGenre</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getTitle</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getTrack</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getYear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isEmpty</span> ( <span
class="methodparam">void</span> )

}

KTaglib\_Tag::getAlbum
======================

Returns the album string from a ID3 tag

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getAlbum</span> ( <span
class="methodparam">void</span> )

Returns the album string of an ID3 tag. This method is implemented in
ID3v1 and ID3v2 tags.

### 返回值

Returns the album string

KTaglib\_Tag::getArtist
=======================

Returns the artist string from a ID3 tag

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getArtist</span> ( <span
class="methodparam">void</span> )

Returns the artist string of an ID3 tag. This method is implemented in
ID3v1 and ID3v2 tags.

### 返回值

Returns the artist string

KTaglib\_Tag::getComment
========================

Returns the comment from a ID3 tag

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getComment</span> ( <span
class="methodparam">void</span> )

Returns the comment of an ID3 tag. This method is implemented in ID3v1
and ID3v2 tags.

### 返回值

Returns the comment string

KTaglib\_Tag::getGenre
======================

Returns the genre from a ID3 tag

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getGenre</span> ( <span
class="methodparam">void</span> )

Returns the genre of an ID3 tag. This method is implemented in ID3v1 and
ID3v2 tags.

### 返回值

Returns the genre string

KTaglib\_Tag::getTitle
======================

Returns the title string from a ID3 tag

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getTitle</span> ( <span
class="methodparam">void</span> )

Returns the title string of an ID3 tag. This method is implemented in
ID3v1 and ID3v2 tags.

### 返回值

Returns the title string

KTaglib\_Tag::getTrack
======================

Returns the track number from a ID3 tag

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_Tag::getTrack</span> ( <span
class="methodparam">void</span> )

Returns the track number of an ID3 tag. This method is implemented in
ID3v1 and ID3v2 tags.

### 返回值

Returns the track number as an integer

KTaglib\_Tag::getYear
=====================

Returns the year from a ID3 tag

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_Tag::getYear</span> ( <span
class="methodparam">void</span> )

Returns the year of an ID3 tag. This method is implemented in ID3v1 and
ID3v2 tags.

### 返回值

Returns the year as an integer

KTaglib\_Tag::isEmpty
=====================

Returns true if the tag is empty

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">KTaglib\_Tag::isEmpty</span> ( <span
class="methodparam">void</span> )

Returns true if the tag exists, but is empty. This method is implemented
in ID3v1 and ID3v2 tags.

### 返回值

Returns true if the tag is empty, otherwise false.

简介
----

Represents and ID3v2 tag. It provides a list of ID3v2 frames and can be
used to add and remove additional frames.

Class synopsis
--------------

**KTaglib\_ID3v2\_Tag**

<span class="ooclass"> <span class="modifier">extends</span> class
**KTaglib\_Tag** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">addFrame</span> ( <span
class="methodparam"><span class="type">KTaglib\_ID3v2\_Frame</span>
`$frame`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getFrameList</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getAlbum</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getArtist</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getComment</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getGenre</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getTitle</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_Tag::getTrack</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_Tag::getYear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">KTaglib\_Tag::isEmpty</span> ( <span
class="methodparam">void</span> )

}

KTaglib\_ID3v2\_Tag::addFrame
=============================

Add a frame to the ID3v2 tag

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">KTaglib\_ID3v2\_Tag::addFrame</span> ( <span
class="methodparam"><span class="type">KTaglib\_ID3v2\_Frame</span>
`$frame`</span> )

Adds a frame to the ID3v2 tag. The frame must be a valid
KTaglib\_ID3v2\_Frame object. To save the tag, the save function needs
to be invoked.

### 返回值

Returns true on success, otherwise false.

KTaglib\_ID3v2\_Tag::getFrameList
=================================

Returns an array of ID3v2 frames, associated with the ID3v2 tag

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">KTaglib\_ID3v2\_Tag::getFrameList</span> (
<span class="methodparam">void</span> )

Returns an array of ID3v2 frames, associated with the ID3v2 tag.

### 返回值

Return an array of KTaglib\_ID3v2\_Frame objects

简介
----

The base class for ID3v2 frames. ID3v2 tags are separated in various
specialized frames. Some frames can exists multiple times.

Class synopsis
--------------

**KTaglib\_ID3v2\_Frame**

<span class="ooclass"> <span class="modifier">extends</span> class
**KTaglib\_Tag** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getSize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getAlbum</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getArtist</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getComment</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getGenre</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getTitle</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_Tag::getTrack</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_Tag::getYear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">KTaglib\_Tag::isEmpty</span> ( <span
class="methodparam">void</span> )

}

KTaglib\_ID3v2\_Frame::getSize
==============================

Returns the size of the frame in bytes

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_ID3v2\_Frame::getSize</span> ( <span
class="methodparam">void</span> )

Returns the size of the frame in bytes. Please refer to id3.org to see
what ID3v2 frames are and how they are defined.

### 返回值

Returns the size of the frame in bytes

KTaglib\_ID3v2\_Frame::\_\_toString
===================================

Returns a string representation of the frame

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_ID3v2\_Frame::\_\_toString</span> (
<span class="methodparam">void</span> )

Returns a string representation of the frame. This might be just the
frame id, but might contain more information. Please see the ktaglib
documentation for more information

### 返回值

Returns a string representation of the frame.

简介
----

Represents an ID3v2 frame that can hold a picture.

Class synopsis
--------------

**KTaglib\_ID3v2\_AttachedPictureFrame**

<span class="ooclass"> <span class="modifier">extends</span> class
**KTaglib\_ID3v2\_Frame** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getDescription</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getMimeType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">savePicture</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getMimeType</span> ( <span
class="methodparam"><span class="type">string</span> `$type`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setPicture</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setType</span> ( <span
class="methodparam"><span class="type">int</span> `$type`</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_ID3v2\_Frame::getSize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_ID3v2\_Frame::\_\_toString</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getAlbum</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getArtist</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getComment</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getGenre</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">KTaglib\_Tag::getTitle</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_Tag::getTrack</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_Tag::getYear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">KTaglib\_Tag::isEmpty</span> ( <span
class="methodparam">void</span> )

}

KTaglib\_ID3v2\_AttachedPictureFrame::getDescription
====================================================

Returns a description for the picture in a picture frame

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span
class="methodname">KTaglib\_ID3v2\_AttachedPictureFrame::getDescription</span>
( <span class="methodparam">void</span> )

Returns the attached description for a picture frame in an ID3v2.x
frame.

### 返回值

Returns a description for the picture in a picture frame

KTaglib\_ID3v2\_AttachedPictureFrame::getMimeType
=================================================

Returns the mime type of the picture

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span
class="methodname">KTaglib\_ID3v2\_AttachedPictureFrame::getMimeType</span>
( <span class="methodparam">void</span> )

Returns the mime type of the image represented by the attached picture
frame.

Please notice that this method might return different types. While
ID3v2.2 have a mime type that doesn't start with "image/", ID3v2.3 and
v2.4 usually start with "image/". Therefore the method might return
"image/png" for IDv2.3 frames and just "PNG" for ID3v2.2 frames.

Notice that even the frame is an attached picture, the mime type might
not be set and therefore an empty string might be returned.

### 返回值

Returns the mime type of the image represented by the attached picture
frame.

KTaglib\_ID3v2\_AttachedPictureFrame::getType
=============================================

Returns the type of the image

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">KTaglib\_ID3v2\_AttachedPictureFrame::getType</span>
( <span class="methodparam">void</span> )

Returns the type of the image.

The ID3v2 specification allows an AttachedPictureFrame to set the type
of an image. This can be e.g. FrontCover or FileIcon. Please refer to
the KTaglib\_ID3v2\_AttachedPictureFrame class description for a list of
available types.

### 返回值

Returns the integer representation of the type.

KTaglib\_ID3v2\_AttachedPictureFrame::savePicture
=================================================

Saves the picture to a file

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">KTaglib\_ID3v2\_AttachedPictureFrame::savePicture</span>
( <span class="methodparam"><span class="type">string</span>
`$filename`</span> )

Saves the attached picture to the given filename.

### 返回值

Returns true on success, otherwise false

KTaglib\_ID3v2\_AttachedPictureFrame::setMimeType
=================================================

Set's the mime type of the picture

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span
class="methodname">KTaglib\_ID3v2\_AttachedPictureFrame::getMimeType</span>
( <span class="methodparam"><span class="type">string</span>
`$type`</span> )

Sets the mime type of the image. This should in most cases be
"image/png" or "image/jpeg".

KTaglib\_ID3v2\_AttachedPictureFrame::setPicture
================================================

Sets the frame picture to the given image

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span
class="methodname">KTaglib\_ID3v2\_AttachedPictureFrame::setPicture</span>
( <span class="methodparam"><span class="type">string</span>
`$filename`</span> )

Sets the picture to the give image. The image is loaded from the given
filename. Please note that the picture is not saved unless you call the
save method of the corresponding file object.

### 返回值

Returns true on success, otherwise false

KTaglib\_ID3v2\_AttachedPictureFrame::setType
=============================================

Set the type of the image

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span
class="methodname">KTaglib\_ID3v2\_AttachedPictureFrame::setType</span>
( <span class="methodparam"><span class="type">int</span> `$type`</span>
)

Sets the type of the image. This can be e.g. FrontCover or FileIcon.
Please refer to the KTaglib\_ID3v2\_AttachedPictureFrame class
description for a list of available types and their constant mappings.
