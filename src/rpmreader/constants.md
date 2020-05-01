预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

The following list of constants are used to obtain information using the
<span class="function">rpm\_get\_tag</span> function. These constants
represent the tag number to be retrieved from the RPM file's header
section. Descriptions are given below as to what data the tag number
constants reference.

**`RPMREADER_MINIMUM`** (<span class="type">integer</span>)  
<span class="simpara"> The minimum valid value of any RPM tag number.
</span>

**`RPMREADER_NAME`** (<span class="type">integer</span>)  
<span class="simpara"> The name of the RPM package. </span>

**`RPMREADER_VERSION`** (<span class="type">integer</span>)  
<span class="simpara"> The version of the RPM package. </span>

**`RPMREADER_RELEASE`** (<span class="type">integer</span>)  
<span class="simpara"> The release of the RPM package. </span>

**`RPMREADER_EPOCH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_SERIAL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_SUMMARY`** (<span class="type">integer</span>)  
<span class="simpara"> The summary text of the RPM package. </span>

**`RPMREADER_DESCRIPTION`** (<span class="type">integer</span>)  
<span class="simpara"> The full description text of the RPM package.
</span>

**`RPMREADER_BUILDTIME`** (<span class="type">integer</span>)  
<span class="simpara"> The date and time when the RPM package was built.
</span>

**`RPMREADER_BUILDHOST`** (<span class="type">integer</span>)  
<span class="simpara"> The name of the host on which the RPM package was
built. </span>

**`RPMREADER_INSTALLTIME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_SIZE`** (<span class="type">integer</span>)  
<span class="simpara"> The size of the RPM package. </span>

**`RPMREADER_DISTRIBUTION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_VENDOR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_GIF`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_XPM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_LICENSE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_COPYRIGHT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_PACKAGER`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_GROUP`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_SOURCE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_PATCH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_URL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_OS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_ARCH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_PREIN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_POSTIN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_PREUN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_POSTUN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_OLDFILENAMES`** (<span class="type">integer</span>)  
<span class="simpara"> The list of files in an RPM package (deprecated
format). The correct way is now to use a combination of 3 tags
(RPMREADER\_BASENAMES, RPMREADER\_DIRINDEXES, RPMREADER\_DIRNAMES) in
what RPM now calls "CompressedFileNames". This tag is still used in
older RPM files that did not use the "CompressedFileNames" method and is
maintained for backward compatibility. </span>

**`RPMREADER_FILESIZES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_FILESTATES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_FILEMODES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_FILERDEVS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_FILEMTIMES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_FILEMD5S`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_FILELINKTOS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_FILEFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_FILEUSERNAME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_FILEGROUPNAME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_ICON`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_SOURCERPM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_FILEVERIFYFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_ARCHIVESIZE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_PROVIDENAME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_PROVIDES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_REQUIREFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_REQUIRENAME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_REQUIREVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_CONFLICTFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_CONFLICTNAME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_CONFLICTVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_EXCLUDEARCH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_EXCLUDEOS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_EXCLUSIVEARCH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_EXCLUSIVEOS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_RPMVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_TRIGGERSCRIPTS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_TRIGGERNAME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_TRIGGERVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_TRIGGERFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_TRIGGERINDEX`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_VERIFYSCRIPT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_CHANGELOGTIME`** (<span class="type">integer</span>)  
<span class="simpara"> The list of dates from changelog entries. </span>

**`RPMREADER_CHANGELOGNAME`** (<span class="type">integer</span>)  
<span class="simpara"> The list of changelog entry names. </span>

**`RPMREADER_CHANGELOGTEXT`** (<span class="type">integer</span>)  
<span class="simpara"> The list of the text from changelog entries.
</span>

**`RPMREADER_PREINPROG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_POSTINPROG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_PREUNPROG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_POSTUNPROG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_BUILDARCHS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_OBSOLETENAME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_OBSOLETES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_VERIFYSCRIPTPROG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_TRIGGERSCRIPTPROG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_COOKIE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_FILEDEVICES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_FILEINODES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_FILELANGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_PREFIXES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_INSTPREFIXES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_PROVIDEFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_PROVIDEVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_OBSOLETEFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_OBSOLETEVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_DIRINDEXES`** (<span class="type">integer</span>)  
<span class="simpara"> The list of indices that relate directory names
to files in the RPM package. This tag is used in conjunction with
RPMREADER\_BASENAMES and RPMREADER\_DIRNAMES to reconstruct filenames in
the RPM package stored with the new "CompressedFileNames" method in RPM.
</span>

**`RPMREADER_BASENAMES`** (<span class="type">integer</span>)  
<span class="simpara"> The list of the names of files in the RPM package
without path information. This tag is used in conjunction with
RPMREADER\_DIRINDEXES and RPMREADER\_DIRNAMES to reconstruct filenames
in the RPM package stored with the new "CompressedFileNames" method in
RPM. </span>

**`RPMREADER_DIRNAMES`** (<span class="type">integer</span>)  
<span class="simpara"> The list of directory names used by files in the
RPM package. This tag is used in conjunction with RPMREADER\_BASENAMES
and RPMREADER\_DIRINDEXES to reconstruct filenames in the RPM package
stored with the new "CompressedFileNames" method in RPM. </span>

**`RPMREADER_OPTFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_DISTURL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_PAYLOADFORMAT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_PAYLOADCOMPRESSOR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_PAYLOADFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_INSTALLCOLOR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_INSTALLTID`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_REMOVETID`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_RHNPLATFORM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_PLATFORM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_PATCHESNAME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_PATCHESFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_PATCHESVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_CACHECTIME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_CACHEPKGPATH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_CACHEPKGSIZE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_CACHEPKGMTIME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_FILECOLORS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_FILECLASS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_CLASSDICT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_FILEDEPENDSX`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_FILEDEPENDSN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_DEPENDSDICT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_SOURCEPKGID`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_FILECONTEXTS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_FSCONTEXTS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_RECONTEXTS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_POLICIES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMREADER_MAXIMUM`** (<span class="type">integer</span>)  
<span class="simpara"> The maximum valid value of any RPM tag number.
</span>
