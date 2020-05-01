id3\_get\_frame\_long\_name
===========================

Get the long name of an ID3v2 frame

### 说明

<span class="type">string</span> <span
class="methodname">id3\_get\_frame\_long\_name</span> ( <span
class="methodparam"><span class="type">string</span> `$frameId`</span> )

<span class="function">id3\_get\_frame\_long\_name</span> returns the
long name for an ID3v2 frame.

### 参数

`frameId`  
An ID3v2 frame

### 返回值

Returns the frame long name or **`FALSE`** on errors.

### 范例

**示例 \#1 <span class="function">id3\_get\_frame\_long\_name</span>
example**

``` php
<?php
$longName = id3_get_frame_long_name("TOLY");
echo $longName;
?>
```

以上例程会输出：

    Original lyricist(s)/text writer(s)

### 参见

-   <span class="function">id3\_get\_frame\_short\_name</span>

id3\_get\_frame\_short\_name
============================

Get the short name of an ID3v2 frame

### 说明

<span class="type">string</span> <span
class="methodname">id3\_get\_frame\_short\_name</span> ( <span
class="methodparam"><span class="type">string</span> `$frameId`</span> )

<span class="function">id3\_get\_frame\_short\_name</span> returns the
short name for an ID3v2 frame.

### 参数

`frameId`  
An ID3v2 frame

### 返回值

Returns the frame short name or **`FALSE`** on errors.

The values returned by <span
class="function">id3\_get\_frame\_short\_name</span> are used in the
array returned by <span class="function">id3\_get\_tag</span>.

### 范例

**示例 \#1 <span class="function">id3\_get\_frame\_short\_name</span>
example**

``` php
<?php
$shortName = id3_get_frame_short_name("TOLY");
echo $shortName;
?>
```

以上例程会输出：

    originalLyricist

### 参见

-   <span class="function">id3\_get\_frame\_long\_name</span>

id3\_get\_genre\_id
===================

Get the id for a genre

### 说明

<span class="type">int</span> <span
class="methodname">id3\_get\_genre\_id</span> ( <span
class="methodparam"><span class="type">string</span> `$genre`</span> )

<span class="function">id3\_get\_genre\_id</span> returns the id for a
genre.

### 参数

`genre`  
Genre name as string.

### 返回值

The genre id or **`FALSE`** on errors.

### 范例

**示例 \#1 <span class="function">id3\_get\_genre\_id</span> example**

``` php
<?php
$id = id3_get_genre_id("Alternative");
echo $id;
?>
```

以上例程会输出：

    20

### 参见

-   <span class="function">id3\_get\_genre\_name</span>
-   <span class="function">id3\_get\_genre\_list</span>

id3\_get\_genre\_list
=====================

Get all possible genre values

### 说明

<span class="type">array</span> <span
class="methodname">id3\_get\_genre\_list</span> ( <span
class="methodparam">void</span> )

<span class="function">id3\_get\_genre\_list</span> returns an array
containing all possible genres that may be stored in an ID3 tag. This
list has been created by Eric Kemp and later extended by WinAmp.

This function is useful to provide you users a list of genres from which
they may choose one. When updating the ID3 tag you will always have to
specify the genre as an integer ranging from 0 to 147.

### 返回值

Returns an array containing all possible genres that may be stored in an
ID3 tag.

### 范例

**示例 \#1 <span class="function">id3\_get\_genre\_list</span> example**

``` php
<?php
$genres = id3_get_genre_list();
print_r($genres);
?>
```

以上例程会输出：

    Array
    (
        [0] => Blues
        [1] => Classic Rock
        [2] => Country
        [3] => Dance
        [4] => Disco
        [5] => Funk
        [6] => Grunge
        [7] => Hip-Hop
        [8] => Jazz
        [9] => Metal
        [10] => New Age
        [11] => Oldies
        [12] => Other
        [13] => Pop
        [14] => R&B
        [15] => Rap
        [16] => Reggae
        [17] => Rock
        [18] => Techno
        [19] => Industrial
        [20] => Alternative
        [21] => Ska
        [22] => Death Metal
        [23] => Pranks
        [24] => Soundtrack
        [25] => Euro-Techno
        [26] => Ambient
        [27] => Trip-Hop
        [28] => Vocal
        [29] => Jazz+Funk
        [30] => Fusion
        [31] => Trance
        [32] => Classical
        [33] => Instrumental
        [34] => Acid
        [35] => House
        [36] => Game
        [37] => Sound Clip
        [38] => Gospel
        [39] => Noise
        [40] => Alternative Rock
        [41] => Bass
        [42] => Soul
        [43] => Punk
        [44] => Space
        [45] => Meditative
        [46] => Instrumental Pop
        [47] => Instrumental Rock
        [48] => Ethnic
        [49] => Gothic
        [50] => Darkwave
        [51] => Techno-Industrial
        [52] => Electronic
        [53] => Pop-Folk
        [54] => Eurodance
        [55] => Dream
        [56] => Southern Rock
        [57] => Comedy
        [58] => Cult
        [59] => Gangsta
        [60] => Top 40
        [61] => Christian Rap
        [62] => Pop/Funk
        [63] => Jungle
        [64] => Native US
        [65] => Cabaret
        [66] => New Wave
        [67] => Psychadelic
        [68] => Rave
        [69] => Showtunes
        [70] => Trailer
        [71] => Lo-Fi
        [72] => Tribal
        [73] => Acid Punk
        [74] => Acid Jazz
        [75] => Polka
        [76] => Retro
        [77] => Musical
        [78] => Rock & Roll
        [79] => Hard Rock
        [80] => Folk
        [81] => Folk-Rock
        [82] => National Folk
        [83] => Swing
        [84] => Fast Fusion
        [85] => Bebob
        [86] => Latin
        [87] => Revival
        [88] => Celtic
        [89] => Bluegrass
        [90] => Avantgarde
        [91] => Gothic Rock
        [92] => Progressive Rock
        [93] => Psychedelic Rock
        [94] => Symphonic Rock
        [95] => Slow Rock
        [96] => Big Band
        [97] => Chorus
        [98] => Easy Listening
        [99] => Acoustic
        [100] => Humour
        [101] => Speech
        [102] => Chanson
        [103] => Opera
        [104] => Chamber Music
        [105] => Sonata
        [106] => Symphony
        [107] => Booty Bass
        [108] => Primus
        [109] => Porn Groove
        [110] => Satire
        [111] => Slow Jam
        [112] => Club
        [113] => Tango
        [114] => Samba
        [115] => Folklore
        [116] => Ballad
        [117] => Power Ballad
        [118] => Rhytmic Soul
        [119] => Freestyle
        [120] => Duet
        [121] => Punk Rock
        [122] => Drum Solo
        [123] => Acapella
        [124] => Euro-House
        [125] => Dance Hall
        [126] => Goa
        [127] => Drum & Bass
        [128] => Club-House
        [129] => Hardcore
        [130] => Terror
        [131] => Indie
        [132] => BritPop
        [133] => Negerpunk
        [134] => Polsk Punk
        [135] => Beat
        [136] => Christian Gangsta
        [137] => Heavy Metal
        [138] => Black Metal
        [139] => Crossover
        [140] => Contemporary C
        [141] => Christian Rock
        [142] => Merengue
        [143] => Salsa
        [144] => Thrash Metal
        [145] => Anime
        [146] => JPop
        [147] => SynthPop
    )

### 参见

-   <span class="function">id3\_get\_genre\_name</span>
-   <span class="function">id3\_get\_genre\_id</span>

id3\_get\_genre\_name
=====================

Get the name for a genre id

### 说明

<span class="type">string</span> <span
class="methodname">id3\_get\_genre\_name</span> ( <span
class="methodparam"><span class="type">int</span> `$genre_id`</span> )

<span class="function">id3\_get\_genre\_name</span> returns the name for
a genre id.

### 参数

`genre_id`  
An integer ranging from 0 to 147

### 返回值

Returns the name as a string.

### 范例

**示例 \#1 <span class="function">id3\_get\_genre\_name</span> example**

``` php
<?php
$genre = id3_get_genre_name(20);
echo $genre;
?>
```

以上例程会输出：

    Alternative

### 参见

-   <span class="function">id3\_get\_genre\_list</span>
-   <span class="function">id3\_get\_genre\_id</span>

id3\_get\_tag
=============

Get all information stored in an ID3 tag

### 说明

<span class="type">array</span> <span
class="methodname">id3\_get\_tag</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$version`<span class="initializer"> = ID3\_BEST</span></span> \] )

<span class="function">id3\_get\_tag</span> is used to get all
information stored in the id3 tag of the specified file.

### 参数

`filename`  
The path to the MP3 file

Instead of a filename you may also pass a valid stream resource

`version`  
Allows you to specify the version of the tag as MP3 files may contain
both, version 1.x and version 2.x tags

Since version 0.2 <span class="function">id3\_get\_tag</span> also
supports ID3 tags of version 2.2, 2.3 and 2.4. To extract information
from these tags, pass one of the constants ID3\_V2\_2, ID3\_V2\_3 or
ID3\_V2\_4 as the second parameter. ID3 v2.x tags can contain a lot more
information about the MP3 file than ID3 v1.x tags.

### 返回值

Returns an associative array with various keys like: *title*, *artist*,
..

The key *genre* will contain an integer between 0 and 147. You may use
<span class="function">id3\_get\_genre\_name</span> to convert it to a
human readable string.

### 范例

**示例 \#1 <span class="function">id3\_get\_tag</span> example**

``` php
<?php
$tag = id3_get_tag( "path/to/example.mp3" );
print_r($tag);
?>
```

以上例程的输出类似于：

    Array
    (
        [title] => DN-38416
        [artist] => Re:\Legion
        [album] => Reflections
        [year] => 2004
        [genre] => 19
    )

**示例 \#2 <span class="function">id3\_get\_tag</span> example**

``` php
<?php
$tag = id3_get_tag( "path/to/example2.mp3", ID3_V2_3 );
print_r($tag);
?>
```

以上例程的输出类似于：

    Array
    (
        [copyright] => Dirty Mac
        [originalArtist] => Dirty Mac
        [composer] => Marcus Götze
        [artist] => Dirty Mac
        [title] => Little Big Man
        [album] => Demo-Tape
        [track] => 5/12
        [genre] => (17)Rock
        [year] => 2001
    )

### 参见

-   <span class="function">id3\_set\_tag</span>
-   <span class="function">id3\_remove\_tag</span>
-   <span class="function">id3\_get\_version</span>

id3\_get\_version
=================

Get version of an ID3 tag

### 说明

<span class="type">int</span> <span
class="methodname">id3\_get\_version</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

<span class="function">id3\_get\_version</span> retrieves the version(s)
of the ID3 tag(s) in the MP3 file.

If a file contains an ID3 v1.1 tag, it always contains a 1.0 tag, as
version 1.1 is just an extension of 1.0.

### 参数

`filename`  
The path to the MP3 file

Instead of a filename you may also pass a valid stream resource

### 返回值

Returns the version number of the ID3 tag of the file. As a tag can
contain ID3 v1.x and v2.x tags, the return value of this function should
be bitwise compared with the predefined constants **`ID3_V1_0`**,
**`ID3_V1_1`** and **`ID3_V2`**.

### 范例

**示例 \#1 <span class="function">id3\_get\_version</span> example**

``` php
<?php
$version = id3_get_version( "path/to/example.mp3" );
if ($version & ID3_V1_0) {
    echo "Contains a 1.x tag\n";
}
if ($version & ID3_V1_1) {
    echo "Contains a 1.1 tag\n";
}
if ($version & ID3_V2) {
    echo "Contains a 2.x tag\n";
}
?>
```

以上例程的输出类似于：

    Contains a 1.x tag
    Contains a 1.1 tag

### 参见

-   <span class="function">id3\_set\_tag</span>
-   <span class="function">id3\_get\_tag</span>
-   <span class="function">id3\_remove\_tag</span>

id3\_remove\_tag
================

Remove an existing ID3 tag

### 说明

<span class="type">bool</span> <span
class="methodname">id3\_remove\_tag</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$version`<span class="initializer"> = ID3\_V1\_0</span></span> \] )

<span class="function">id3\_remove\_tag</span> is used to remove the
information stored of an ID3 tag.

### 参数

`filename`  
The path to the MP3 file

Instead of a filename you may also pass a valid stream resource

`version`  
Allows you to specify the version of the tag as MP3 files may contain
both, version 1.x and version 2.x tags.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">id3\_remove\_tag</span> example**

``` php
<?php
$result = id3_remove_tag( "path/to/example.mp3", ID3_V1_0 );
if ($result === true) {
    echo "Tag successfully removed\n";
}
?>
```

If the file is writable and contained a 1.0 tag, this will output:

    Tag successfully removed

### 注释

> **Note**: <span class="simpara"> Currently <span
> class="function">id3\_remove\_tag</span> only supports version 1.0 and
> 1.1. If you choose to remove a 1.0 tag and the file contains a 1.1
> tag, this tag will be removed, as v1.1 is only an extension of 1.0.
> </span>

### 参见

-   <span class="function">id3\_set\_tag</span>
-   <span class="function">id3\_get\_tag</span>
-   <span class="function">id3\_get\_version</span>

id3\_set\_tag
=============

Update information stored in an ID3 tag

### 说明

<span class="type">bool</span> <span
class="methodname">id3\_set\_tag</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
, <span class="methodparam"><span class="type">array</span>
`$tag`</span> \[, <span class="methodparam"><span
class="type">int</span> `$version`<span class="initializer"> =
ID3\_V1\_0</span></span> \] )

<span class="function">id3\_set\_tag</span> is used to change the
information stored of an ID3 tag. If no tag has been present, it will be
added to the file.

### 参数

`filename`  
The path to the MP3 file

Instead of a filename you may also pass a valid stream resource

`tag`  
An associative array of tag keys and values

The following keys may be used in the associative array:

| key     | possible value                                    | available in version |
|---------|---------------------------------------------------|----------------------|
| title   | string with maximum of 30 characters              | v1.0, v1.1           |
| artist  | string with maximum of 30 characters              | v1.0, v1.1           |
| album   | string with maximum of 30 characters              | v1.0, v1.1           |
| year    | 4 digits                                          | v1.0, v1.1           |
| genre   | integer value between 0 and 147                   | v1.0, v1.1           |
| comment | string with maximum of 30 characters (28 in v1.1) | v1.0, v1.1           |
| track   | integer between 0 and 255                         | v1.1                 |

`version`  
Allows you to specify the version of the tag as MP3 files may contain
both, version 1.x and version 2.x tags

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">id3\_set\_tag</span> example**

``` php
<?php
$data = array(
              "title" => "Re:Start",
              "artist" => "Re:\Legion",
              "comment" => "A nice track"
             );
$result = id3_set_tag( "path/to/example.mp3", $data, ID3_V1_0 );
if ($result === true) {
    echo "Tag successfully updated\n";
}
?>
```

If the file is writable, this will output:

    Tag successfully updated

### 注释

> **Note**: <span class="simpara"> Currently <span
> class="function">id3\_set\_tag</span> only supports version 1.0 and
> 1.1. </span>

### 参见

-   <span class="function">id3\_remove\_tag</span>
-   <span class="function">id3\_get\_tag</span>
-   <span class="function">id3\_get\_version</span>

**目录**

-   [id3\_get\_frame\_long\_name](/ref/id3.html#id3_get_frame_long_name)
    — Get the long name of an ID3v2 frame
-   [id3\_get\_frame\_short\_name](/ref/id3.html#id3_get_frame_short_name)
    — Get the short name of an ID3v2 frame
-   [id3\_get\_genre\_id](/ref/id3.html#id3_get_genre_id) — Get the id
    for a genre
-   [id3\_get\_genre\_list](/ref/id3.html#id3_get_genre_list) — Get all
    possible genre values
-   [id3\_get\_genre\_name](/ref/id3.html#id3_get_genre_name) — Get the
    name for a genre id
-   [id3\_get\_tag](/ref/id3.html#id3_get_tag) — Get all information
    stored in an ID3 tag
-   [id3\_get\_version](/ref/id3.html#id3_get_version) — Get version of
    an ID3 tag
-   [id3\_remove\_tag](/ref/id3.html#id3_remove_tag) — Remove an
    existing ID3 tag
-   [id3\_set\_tag](/ref/id3.html#id3_set_tag) — Update information
    stored in an ID3 tag
