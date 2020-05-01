范例
====

**目录**

-   [Examples on using the ogg://
    wrapper.](/oggvorbis/examples.html#Examples%20on%20using%20the%20ogg://%20wrapper.)

Examples on using the ogg:// wrapper.
-------------------------------------

**示例 \#1 Reading an OGG/Vorbis file**

``` php
<?php
dl("oggvorbis.so");

/* By default, ogg:// will decode to Signed 16-bit Little Endian */
$fp = fopen('ogg://myaudio.ogg', 'r');

/* Collect some information about the file. */
$metadata = stream_get_meta_data($fp);

/* Inspect the first song (usually the only song, 
   but OGG/Vorbis files may be chained) */
$songdata = $metadata['wrapper_data'][0];

echo "OGG/Vorbis file encoded by: {$songdata['vendor']}\n.";
echo "  {$songdata['channels']} channels of {$songdata['rate']}Hz sampling encoded at {$songdata['bitrate_nominal']}bps.\n";
foreach($songdata['comments'] as $comment) {
    echo "  $comment\n";
}

while ($audio_data = fread($fp, 8192)) {
  /* Do something with the PCM audio we're extracting from the OGG.
     Copying to /dev/dsp is a good target on linux systems, 
     just remember to setup the device for your sampling mode first. */
}

fclose($fp);

?>
```

**示例 \#2 Encode an audio file to OGG/Vorbis**

``` php
<?php
dl('oggvorbis.so');

$context = stream_context_create(array('ogg'=>array(
             'pcm_mode' => OGGVORBIS_PCM_S8,  /* Signed 8bit audio */
             'rate' => 44100,                 /* 44kHz CD quality */
             'bitrate' => 0.5,                /* Midquality VBR */
             'channels' => 1,                 /* Mono */
             'serialno' => 12345)));          /* Unique within our stream */

/* Open file for appending.  This will "chain" a second OGG stream at the end of the first. */
$ogg = fopen('ogg://mysong.ogg', 'a', false, $context);

$pcm = fopen('mysample.pcm', 'r');

/* Compress the raw PCM audio from mysample.pcm into mysong.ogg */
stream_copy_to_stream($pcm, $ogg);

fclose($pcm);
fclose($ogg);
?>
```
