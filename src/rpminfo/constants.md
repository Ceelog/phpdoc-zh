预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`RPMVERSION`** (<span class="type">string</span>)  
<span class="simpara"> System librpm version. </span>

**`RPMSENSE_ANY`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_LESS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_GREATER`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_EQUAL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_POSTTRANS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_PREREQ`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_PRETRANS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_INTERP`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_SCRIPT_PRE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_SCRIPT_POST`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_SCRIPT_PREUN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_SCRIPT_POSTUN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_SCRIPT_VERIFY`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_FIND_REQUIRES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_FIND_PROVIDES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_TRIGGERIN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_TRIGGERUN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_TRIGGERPOSTUN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_MISSINGOK`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_RPMLIB`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_TRIGGERPREIN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_KEYRING`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMSENSE_CONFIG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMMIRE_DEFAULT`** (<span class="type">integer</span>)  
<span class="simpara"> Search pattern is a regular expression with \\.,
.\* and ^...$ added. </span>

**`RPMMIRE_STRCMP`** (<span class="type">integer</span>)  
<span class="simpara"> Search pattern is a <span
class="type">string</span>, using strcmp(3). </span>

**`RPMMIRE_REGEX`** (<span class="type">integer</span>)  
<span class="simpara"> Search pattern is a regular expression, using
regcomp(3). </span>

**`RPMMIRE_GLOB`** (<span class="type">integer</span>)  
<span class="simpara"> Search pattern is a glob expression, using
fnmatch(3). </span>

**`RPMTAG_ARCH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_ARCHIVESIZE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_BASENAMES`** (<span class="type">integer</span>)  
<span class="simpara"> Name (not path) of files, with database index.
</span>

**`RPMTAG_BUGURL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_BUILDARCHS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_BUILDHOST`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_BUILDTIME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_C`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_CHANGELOGNAME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_CHANGELOGTEXT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_CHANGELOGTIME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_CLASSDICT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_CONFLICTFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_CONFLICTNAME`** (<span class="type">integer</span>)  
<span class="simpara"> Conflicting dependencies, with database index.
</span>

**`RPMTAG_CONFLICTNEVRS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_CONFLICTS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_CONFLICTVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_COOKIE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_DBINSTANCE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_DEPENDSDICT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_DESCRIPTION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_DIRINDEXES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_DIRNAMES`** (<span class="type">integer</span>)  
<span class="simpara"> Directory of files, with database index. </span>

**`RPMTAG_DISTRIBUTION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_DISTTAG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_DISTURL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_DSAHEADER`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_E`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_ENCODING`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_ENHANCEFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_ENHANCENAME`** (<span class="type">integer</span>)  
<span class="simpara"> Weak dependencies, with database index, requires
librpm \>= 4.13. </span>

**`RPMTAG_ENHANCENEVRS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_ENHANCES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_ENHANCEVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_EPOCH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_EPOCHNUM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_EVR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_EXCLUDEARCH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_EXCLUDEOS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_EXCLUSIVEARCH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_EXCLUSIVEOS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILECAPS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILECLASS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILECOLORS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILECONTEXTS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILEDEPENDSN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILEDEPENDSX`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILEDEVICES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILEDIGESTALGO`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILEDIGESTS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILEFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILEGROUPNAME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILEINODES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILELANGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILELINKTOS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILEMD5S`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILEMODES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILEMTIMES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILENAMES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILENLINKS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILEPROVIDE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILERDEVS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILEREQUIRE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILESIGNATURELENGTH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILESIGNATURES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILESIZES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILESTATES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILETRIGGERCONDS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILETRIGGERFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILETRIGGERINDEX`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILETRIGGERNAME`** (<span class="type">integer</span>)  
<span class="simpara"> File trigger name, with database index, requires
librpm \>= 4.13. </span>

**`RPMTAG_FILETRIGGERPRIORITIES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILETRIGGERSCRIPTFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILETRIGGERSCRIPTPROG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILETRIGGERSCRIPTS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILETRIGGERTYPE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILETRIGGERVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILEUSERNAME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FILEVERIFYFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_FSCONTEXTS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_GIF`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_GROUP`** (<span class="type">integer</span>)  
<span class="simpara"> Group of the package, with database index.
</span>

**`RPMTAG_HDRID`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_HEADERCOLOR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_HEADERI18NTABLE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_HEADERIMAGE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_HEADERIMMUTABLE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_HEADERREGIONS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_HEADERSIGNATURES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_ICON`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_INSTALLCOLOR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_INSTALLTID`** (<span class="type">integer</span>)  
<span class="simpara"> Installation transaction ID, with database index.
</span>

**`RPMTAG_INSTALLTIME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_INSTFILENAMES`** (<span class="type">integer</span>)  
<span class="simpara"> Path of files, with database index. </span>

**`RPMTAG_INSTPREFIXES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_LICENSE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_LONGARCHIVESIZE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_LONGFILESIZES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_LONGSIGSIZE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_LONGSIZE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_MODULARITYLABEL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_N`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_NAME`** (<span class="type">integer</span>)  
<span class="simpara"> Package name, with database index. </span>

**`RPMTAG_NEVR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_NEVRA`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_NOPATCH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_NOSOURCE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_NVR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_NVRA`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_O`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_OBSOLETEFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_OBSOLETENAME`** (<span class="type">integer</span>)  
<span class="simpara"> Obsoleted packages, with database index. </span>

**`RPMTAG_OBSOLETENEVRS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_OBSOLETES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_OBSOLETEVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_OLDENHANCES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_OLDENHANCESFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_OLDENHANCESNAME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_OLDENHANCESVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_OLDFILENAMES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_OLDSUGGESTS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_OLDSUGGESTSFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_OLDSUGGESTSNAME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_OLDSUGGESTSVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_OPTFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_ORDERFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_ORDERNAME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_ORDERVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_ORIGBASENAMES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_ORIGDIRINDEXES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_ORIGDIRNAMES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_ORIGFILENAMES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_OS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_P`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PACKAGER`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PATCH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PATCHESFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PATCHESNAME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PATCHESVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PAYLOADCOMPRESSOR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PAYLOADDIGEST`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PAYLOADDIGESTALGO`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PAYLOADFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PAYLOADFORMAT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PKGID`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PLATFORM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_POLICIES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_POLICYFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_POLICYNAMES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_POLICYTYPES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_POLICYTYPESINDEXES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_POSTIN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_POSTINFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_POSTINPROG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_POSTTRANS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_POSTTRANSFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_POSTTRANSPROG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_POSTUN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_POSTUNFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_POSTUNPROG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PREFIXES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PREIN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PREINFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PREINPROG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PRETRANS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PRETRANSFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PRETRANSPROG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PREUN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PREUNFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PREUNPROG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PROVIDEFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PROVIDENAME`** (<span class="type">integer</span>)  
<span class="simpara"> Provided dependencies, with database index.
</span>

**`RPMTAG_PROVIDENEVRS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PROVIDES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PROVIDEVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_PUBKEYS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_R`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_RECOMMENDFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_RECOMMENDNAME`** (<span class="type">integer</span>)  
<span class="simpara"> Recommended weak dependencies, with database
index, requires librpm \>= 4.13. </span>

**`RPMTAG_RECOMMENDNEVRS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_RECOMMENDS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_RECOMMENDVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_RECONTEXTS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_RELEASE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_REMOVETID`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_REQUIREFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_REQUIRENAME`** (<span class="type">integer</span>)  
<span class="simpara"> Required dependencies, with database index.
</span>

**`RPMTAG_REQUIRENEVRS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_REQUIRES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_REQUIREVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_RPMVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_RSAHEADER`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_SHA1HEADER`** (<span class="type">integer</span>)  
<span class="simpara"> SHA1 signature, with database index. </span>

**`RPMTAG_SHA256HEADER`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_SIGGPG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_SIGMD5`** (<span class="type">integer</span>)  
<span class="simpara"> MD5 signature, with database index. </span>

**`RPMTAG_SIGPGP`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_SIGSIZE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_SIZE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_SOURCE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_SOURCEPACKAGE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_SOURCEPKGID`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_SOURCERPM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_SUGGESTFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_SUGGESTNAME`** (<span class="type">integer</span>)  
<span class="simpara"> Suggested weak dependencies, with database index,
requires librpm \>= 4.13. </span>

**`RPMTAG_SUGGESTNEVRS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_SUGGESTS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_SUGGESTVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_SUMMARY`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_SUPPLEMENTFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_SUPPLEMENTNAME`** (<span class="type">integer</span>)  
<span class="simpara"> Weak dependencies, with database index, requires
librpm \>= 4.13. </span>

**`RPMTAG_SUPPLEMENTNEVRS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_SUPPLEMENTS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_SUPPLEMENTVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_TRANSFILETRIGGERCONDS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_TRANSFILETRIGGERFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_TRANSFILETRIGGERINDEX`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_TRANSFILETRIGGERNAME`** (<span class="type">integer</span>)  
<span class="simpara"> Transaction file trigger name, with database
index, requires librpm \>= 4.13. </span>

**`RPMTAG_TRANSFILETRIGGERPRIORITIES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_TRANSFILETRIGGERSCRIPTFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_TRANSFILETRIGGERSCRIPTPROG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_TRANSFILETRIGGERSCRIPTS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_TRANSFILETRIGGERTYPE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_TRANSFILETRIGGERVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_TRIGGERCONDS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_TRIGGERFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_TRIGGERINDEX`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_TRIGGERNAME`** (<span class="type">integer</span>)  
<span class="simpara"> Trigger name, with database index. </span>

**`RPMTAG_TRIGGERSCRIPTFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_TRIGGERSCRIPTPROG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_TRIGGERSCRIPTS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_TRIGGERTYPE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_TRIGGERVERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_URL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_V`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_VCS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_VENDOR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_VERBOSE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_VERIFYSCRIPT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_VERIFYSCRIPTFLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_VERIFYSCRIPTPROG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_VERSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`RPMTAG_XPM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>
