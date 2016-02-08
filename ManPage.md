NAME
> ogg2mp3 - Convert Ogg Vorbis to MP3

SYNOPSIS
> ogg2mp3 [options](options.md) inputfiles ...

DESCRIPTION
> The  ogg2mp3  command  line  utility converts Ogg Vorbis files into MP3
> files using the lame MP3 encoder.

> Possible input files are single files or directoris  where  directories
> are  processed  recursively. Only valid Ogg Vorbis files are converted,
> other files are ignored. For each input file a new MP3 output  file  is
> written with the extension changed to ".mp3".

OPTIONS
> -h, --help
> > Print help information and exit.


> ogg2mp3  supports  ABR as well as VBR encoding through lame. If neither
> method is specified (see below) ogg2mp3 will use ABR using the  average
> bit  rate  of  the input file as target bitrate of the output MP3 file.
> Because each input file is evaluated separately this is especially use
> ful if  the input files do vary in quality. Caveat: As Ogg Vorbis
> provides better overall quality than MP3 at the  same  bitrate  this  will
> result in lower quality output files.

> -a, --abr=BITRATE
> > Use  ABR  encoding  method  with specified average rate. See the
> > lame man page for details.


> -v, --vbr=QUALITY
> > Use VBR encoding method with specified quality.  Default  is  4,
> > use  0  for high or 9 for low quality. See the lame man page for
> > details.


> -m, --mode=MODE
> > Define stereo mode where MODE may be (j)oint, (s)imple, (f)orce,
> > (d)dual-mono, (m)ono. See the lame man page for details.


> -q, --quality=QUALITY
> > Define lame algorithm quality. Default is 5, use 2 for high or 7
> > for reasonable low quality. See the lame man page for details.


> -d, --delete
> > Delete input files after transcoding.


> --quiet
> > Suppress all status information.


> --verbose
> > Print verbose information.

AUTHORS

> Christoph Souris (christoph.souris at googlemail.com)

SEE ALSO
> mp32ogg(1), oggdec(1), lame(1)