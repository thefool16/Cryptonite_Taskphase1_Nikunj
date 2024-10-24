```
Connected!
hacker@man~searching-for-manuals:~$ man man
MAN(1)                                                             Manual pager utils                                                             MAN(1)

NAME
       man - an interface to the system reference manuals

SYNOPSIS
       man [man options] [[section] page ...] ...
       man -k [apropos options] regexp ...
       man -K [man options] [section] term ...
       man -f [whatis options] page ...
       man -l [man options] file ...
       man -w|-W [man options] page ...

DESCRIPTION
       man is the system's manual pager.  Each page argument given to man is normally the name of a program, utility or function.  The manual page asso‐
       ciated with each of these arguments is then found and displayed.  A section, if provided, will direct man to look only in  that  section  of  the
       manual.   The  default  action  is  to search in all of the available sections following a pre-defined order (see DEFAULTS), and to show only the
       first page found, even if page exists in several sections.

       The table below shows the section numbers of the manual followed by the types of pages they contain.

       1   Executable programs or shell commands
       2   System calls (functions provided by the kernel)
       3   Library calls (functions within program libraries)
       4   Special files (usually found in /dev)
       5   File formats and conventions, e.g. /etc/passwd
       6   Games
       7   Miscellaneous (including macro packages and conventions), e.g. man(7), groff(7)
       8   System administration commands (usually only for root)
       9   Kernel routines [Non standard]

       A manual page consists of several sections.

       Conventional section names include NAME, SYNOPSIS, CONFIGURATION, DESCRIPTION, OPTIONS, EXIT STATUS, RETURN VALUE,  ERRORS,  ENVIRONMENT,  FILES,
       VERSIONS, CONFORMING TO, NOTES, BUGS, EXAMPLE, AUTHORS, and SEE ALSO.

       The following conventions apply to the SYNOPSIS section and can be used as a guide in other sections.

       bold text          type exactly as shown.
       italic text        replace with appropriate argument.
       [-abc]             any or all arguments within [ ] are optional.
       -a|-b              options delimited by | cannot be used together.
       argument ...       argument is repeatable.
       [expression] ...   entire expression within [ ] is repeatable.

       Exact  rendering  may vary depending on the output device.  For instance, man will usually not be able to render italics when running in a termi‐
       nal, and will typically use underlined or coloured text instead.

       The command or function illustration is a pattern that should match all possible invocations.  In some cases it is advisable to  illustrate  sev‐
       eral exclusive invocations as is shown in the SYNOPSIS section of this manual page.

EXAMPLES
       man ls
           Display the manual page for the item (program) ls.

       man man.7
           Display the manual page for macro package man from section 7.  (This is an alternative spelling of "man 7 man".)

       man 'man(7)'
           Display  the  manual page for macro package man from section 7.  (This is another alternative spelling of "man 7 man".  It may be more conve‐
           nient when copying and pasting cross-references to manual pages.  Note that the parentheses must normally be quoted to protect them from  the
           shell.)

       man -a intro
           Display,  in succession, all of the available intro manual pages contained within the manual.  It is possible to quit between successive dis‐
           plays or skip any of them.

       man -t bash | lpr -Pps
           Format the manual page for bash into the default troff or groff format and pipe it to the printer named ps.  The default output for groff  is
           usually PostScript.  man --help should advise as to which processor is bound to the -t option.

       man -l -Tdvi ./foo.1x.gz > ./foo.1x.dvi
           This  command  will  decompress and format the nroff source manual page ./foo.1x.gz into a device independent (dvi) file.  The redirection is
           necessary as the -T flag causes output to be directed to stdout with no pager.  The output could be viewed with a program  such  as  xdvi  or
           further processed into PostScript using a program such as dvips.

       man -k printf
           Search  the  short  descriptions  and  manual page names for the keyword printf as regular expression.  Print out any matches.  Equivalent to
           apropos printf.

       man -f smail
           Lookup the manual pages referenced by smail and print out the short descriptions of any found.  Equivalent to whatis smail.

OVERVIEW
       Many options are available to man in order to give as much flexibility as possible to the user.  Changes can be made to the search path,  section
       order, output processor, and other behaviours and operations detailed below.

       If set, various environment variables are interrogated to determine the operation of man.  It is possible to set the "catch-all" variable $MANOPT
       to any string in command line format, with the exception that any spaces used as part of an option's argument must  be  escaped  (preceded  by  a
       backslash).   man  will  parse $MANOPT prior to parsing its own command line.  Those options requiring an argument will be overridden by the same
       options found on the command line.  To reset all of the options set in $MANOPT, -D can be specified as the initial  command  line  option.   This
       will allow man to "forget" about the options specified in $MANOPT, although they must still have been valid.

       Manual  pages  are normally stored in nroff(1) format under a directory such as /usr/share/man.  In some installations, there may also be prefor‐
       matted cat pages to improve performance.  See manpath(5) for details of where these files are stored.

       This package supports manual pages in multiple languages, controlled by your locale.  If your system did not set this up for  you  automatically,
       then  you may need to set $LC_MESSAGES, $LANG, or another system-dependent environment variable to indicate your preferred locale, usually speci‐
       fied in the POSIX format:

       <language>[_<territory>[.<character-set>[,<version>]]]

       If the desired page is available in your locale, it will be displayed in lieu of the standard (usually American English) page.

       If you find that the translations supplied with this package are not available in your native language and you would like to supply them,  please
       contact the maintainer who will be coordinating such activity.

       Individual  manual  pages are normally written and maintained by the maintainers of the program, function, or other topic that they document, and
       are not included with this package.  If you find that a manual page is missing or inadequate, please report that to the maintainers of the  pack‐
       age in question.

       For information regarding other features and extensions available with this manual pager, please read the documents supplied with the package.

DEFAULTS
       The  order  of  sections to search may be overridden by the environment variable $MANSECT or by the SECTION directive in /etc/manpath.config.  By
       default it is as follows:

              1 n l 8 3 2 3posix 3pm 3perl 3am 5 4 9 6 7

       The formatted manual page is displayed using a pager.  This can be specified in a number of ways, or else will fall back to a default (see option
       -P for details).

       The  filters  are  deciphered by a number of means.  Firstly, the command line option -p or the environment variable $MANROFFSEQ is interrogated.
       If -p was not used and the environment variable was not set, the initial line of the nroff file is parsed for a preprocessor string.  To  contain
       a valid preprocessor string, the first line must resemble

       '\" <string>

       where string can be any combination of letters described by option -p below.

       If none of the above methods provide any filter information, a default set is used.

       A  formatting  pipeline is formed from the filters and the primary formatter (nroff or [tg]roff with -t) and executed.  Alternatively, if an exe‐
       cutable program mandb_nfmt (or mandb_tfmt with -t) exists in the man tree root, it is executed instead.  It gets passed the manual  source  file,
       the preprocessor string, and optionally the device specified with -T or -E as arguments.

OPTIONS
       Non-argument options that are duplicated either on the command line, in $MANOPT, or both, are not harmful.  For options that require an argument,
       each duplication will override the previous argument value.

   General options
       -C file, --config-file=file
              Use this user configuration file rather than the default of ~/.manpath.

       -d, --debug
              Print debugging information.

       -D, --default
              This option is normally issued as the very first option and resets man's behaviour to its default.  Its use is to reset those options that
              may have been set in $MANOPT.  Any options that follow -D will have their usual effect.

       --warnings[=warnings]
              Enable  warnings from groff.  This may be used to perform sanity checks on the source text of manual pages.  warnings is a comma-separated
              list of warning names; if it is not supplied, the default is "mac".  See the “Warnings” node in info groff for a list of available warning
              names.

   Main modes of operation
       -f, --whatis
              Equivalent to whatis.  Display a short description from the manual page, if available.  See whatis(1) for details.

       -k, --apropos
              Equivalent to apropos.  Search the short manual page descriptions for keywords and display any matches.  See apropos(1) for details.

       -K, --global-apropos
              Search for text in all manual pages.  This is a brute-force search, and is likely to take some time; if you can, you should specify a sec‐
              tion to reduce the number of pages that need to be searched.  Search terms may be simple strings (the default), or regular expressions  if
              the --regex option is used.

              Note that this searches the sources of the manual pages, not the rendered text, and so may include false positives due to things like com‐
              ments in source files.  Searching the rendered text would be much slower.

       -l, --local-file
              Activate "local" mode.  Format and display local manual files instead of searching through the system's manual  collection.   Each  manual
              page argument will be interpreted as an nroff source file in the correct format.  No cat file is produced.  If '-' is listed as one of the
              arguments, input will be taken from stdin.  When this option is not used, and man fails to find the page required, before  displaying  the
              error message, it attempts to act as if this option was supplied, using the name as a filename and looking for an exact match.

       -w, --where, --path, --location
              Don't  actually  display the manual page, but do print the location of the source nroff file that would be formatted.  If the -a option is
              also used, then print the locations of all source files that match the search criteria.

       -W, --where-cat, --location-cat
              Don't actually display the manual page, but do print the location of the preformatted cat file that would be displayed.  If the -a  option
              is also used, then print the locations of all preformatted cat files that match the search criteria.

              If  -w  and  -W  are both used, then print both source file and cat file separated by a space.  If all of -w, -W, and -a are used, then do
              this for each possible match.

       -c, --catman
              This option is not for general use and should only be used by the catman program.

       -R encoding, --recode=encoding
              Instead of formatting the manual page in the usual way, output its source converted to the specified encoding.  If you  already  know  the
              encoding  of  the source file, you can also use manconv(1) directly.  However, this option allows you to convert several manual pages to a
              single encoding without having to explicitly state the encoding of each, provided that they were already installed in a structure  similar
              to a manual page hierarchy.

              Consider  using  man-recode(1) instead for converting multiple manual pages, since it has an interface designed for bulk conversion and so
              can be much faster.

   Finding manual pages
       -L locale, --locale=locale
              man will normally determine your current locale by a call to the C function setlocale(3) which interrogates various environment variables,
              possibly  including  $LC_MESSAGES  and $LANG.  To temporarily override the determined value, use this option to supply a locale string di‐
              rectly to man.  Note that it will not take effect until the search for pages actually begins.  Output such as the help message will always
              be displayed in the initially determined locale.

       -m system[,...], --systems=system[,...]
              If  this  system has access to other operating system's manual pages, they can be accessed using this option.  To search for a manual page
              from NewOS's manual page collection, use the option -m NewOS.

              The system specified can be a combination of comma delimited operating system names.  To include a search of the native operating system's
              manual pages, include the system name man in the argument string.  This option will override the $SYSTEM environment variable.

       -M path, --manpath=path
              Specify  an  alternate  manpath to use.  By default, man uses manpath derived code to determine the path to search.  This option overrides
              the $MANPATH environment variable and causes option -m to be ignored.

              A path specified as a manpath must be the root of a manual page hierarchy structured into sections as described in the man-db manual  (un‐
              der "The manual page system").  To view manual pages outside such hierarchies, see the -l option.

       -S list, -s list, --sections=list
              The given list is a colon- or comma-separated list of sections, used to determine which manual sections to search and in what order.  This
              option overrides the $MANSECT environment variable.  (The -s spelling is for compatibility with System V.)

       -e sub-extension, --extension=sub-extension
              Some systems incorporate large packages of manual pages, such as those that accompany the Tcl package, into the main manual  page  hierar‐
              chy.   To get around the problem of having two manual pages with the same name such as exit(3), the Tcl pages were usually all assigned to
              section l.  As this is unfortunate, it is now possible to put the pages in the correct section, and to assign a  specific  "extension"  to
              them,  in  this case, exit(3tcl).  Under normal operation, man will display exit(3) in preference to exit(3tcl).  To negotiate this situa‐
              tion and to avoid having to know which section the page you require resides in, it is now possible to give man a sub-extension string  in‐
              dicating  which  package the page must belong to.  Using the above example, supplying the option -e tcl to man will restrict the search to
              pages having an extension of *tcl.

       -i, --ignore-case
              Ignore case when searching for manual pages.  This is the default.

       -I, --match-case
              Search for manual pages case-sensitively.

       --regex
              Show all pages with any part of either their names or their descriptions matching each page argument as  a  regular  expression,  as  with
              apropos(1).   Since  there is usually no reasonable way to pick a "best" page when searching for a regular expression, this option implies
              -a.

       --wildcard
              Show all pages with any part of either their names or their descriptions matching each page argument using shell-style wildcards, as  with
              apropos(1)  --wildcard.   The  page  argument  must  match the entire name or description, or match on word boundaries in the description.
              Since there is usually no reasonable way to pick a "best" page when searching for a wildcard, this option implies -a.

       --names-only
              If the --regex or --wildcard option is used, match only page names, not page descriptions, as with whatis(1).  Otherwise, no effect.

       -a, --all
              By default, man will exit after displaying the most suitable manual page it finds.  Using this option forces man to display all the manual
              pages with names that match the search criteria.

       -u, --update
              This  option  causes  man to update its database caches of installed manual pages.  This is only needed in rare situations, and it is nor‐
              mally better to run mandb(8) instead.

       --no-subpages
              By default, man will try to interpret pairs of manual page names given on the command line as equivalent to a single manual page name con‐
              taining  a hyphen or an underscore.  This supports the common pattern of programs that implement a number of subcommands, allowing them to
              provide manual pages for each that can be accessed using similar syntax as would be used to invoke the subcommands themselves.  For  exam‐
              ple:

                $ man -aw git diff
                /usr/share/man/man1/git-diff.1.gz

              To disable this behaviour, use the --no-subpages option.

                $ man -aw --no-subpages git diff
                /usr/share/man/man1/git.1.gz
                /usr/share/man/man3/Git.3pm.gz
                /usr/share/man/man1/diff.1.gz

   Controlling formatted output
       -P pager, --pager=pager
              Specify  which output pager to use.  By default, man uses pager, falling back to cat if pager is not found or is not executable.  This op‐
              tion overrides the $MANPAGER environment variable, which in turn overrides the $PAGER environment variable.  It is not used in conjunction
              with -f or -k.

hacker@man~searching-for-manuals:~$ man -k flag
dpkg-buildflags (1)  - returns build flags to use during package build
Dpkg::BuildFlags (3perl) - query build flags
fegetexceptflag (3)  - floating-point rounding and exception handling
fesetexceptflag (3)  - floating-point rounding and exception handling
i386 (8)             - change reported architecture in new program environment and/or set personality flags
ioctl_iflags (2)     - ioctl() operations for inode flags
linux32 (1)          - change reported architecture in new program environment and/or set personality flags
linux64 (1)          - change reported architecture in new program environment and/or set personality flags
nuxpscdyjc (1)       - print the flag!
pcap-config (1)      - write libpcap compiler and linker flags to standard output
security_compute_av_flags (3) - query the SELinux policy database in the kernel
security_compute_av_flags_raw (3) - query the SELinux policy database in the kernel
set_matchpathcon_flags (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure the behaviour of validity checking a...
set_matchpathcon_invalidcon (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure the behaviour of validity check...
set_matchpathcon_printf (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure the behaviour of validity checking ...
setarch (1)          - change reported architecture in new program environment and/or set personality flags
setarch (8)          - change reported architecture in new program environment and/or set personality flags
x86_64 (8)           - change reported architecture in new program environment and/or set personality flags
hacker@man~searching-for-manuals:~$ man nuxpscdyjc

CHALLENGE(1)                                                       Challenge Commands                                                       CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --nuxpsc NUM
              print the flag if NUM is 563

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-luminarium/>

SEE ALSO
       man(1) bash-builtins(7)

pwn.college                                                             May 2024                                                            CHALLENGE(1)
hacker@man~searching-for-manuals:~$ /challenge/challenge --nuxpsc 563
Correct usage! Your flag: pwn.college{InuG56HCTL_C3PKx67IMpCOsUcS.dZTM4QDLyIjN0czW}




i searched whole database using man -k flag and found a file nuxpscdyjc in which file is written and then i man nuxpscdyjc got the argument to find the flag
got the flag
yeah!!
```
