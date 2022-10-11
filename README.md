# netrw
Make file sizes in a longlist (w/file sizes&amp;dates) right-aligned (easyier to read)

I took netrw.vim today (in /usr/share/vim/vim90/autoload), copied it to ~/.vim/autoload and added a line (#11090)

11087a11089,11091
> " +++ make sz right-aligned
>     let sz   = printf("%15S", sz)
> " +++
    
to make the file list (when the 'long' listing format shows file sizes) having right-aligned file-sizes. Before, it looked like:

    " ============================================================================
    " Netrw Directory Listing                                        (netrw v171)
    "   /usr/share/doc/vim-common
    "   Sorted by exten
    "   Hiding:        \(^\|\s\s\)\zs\.\S\+
    "   Quick Help: <F1>:help  -:go up dir  D:delete  R:rename  s:sort-by  x:special
    " ==============================================================================
    docs@                                            0 Mo 10 Okt 2022 17:58:47 CEST
    README.md                                        6985 Fr 16 Sep 2022 10:04:27 CEST
    README_VIM9.md                                   10888 Fr 16 Sep 2022 10:04:27 CEST
    README.txt                                       4900 Fr 16 Sep 2022 10:04:27 CEST
    README_ami.txt                                   1252 Fr 16 Sep 2022 10:04:28 CEST
    README_vms.txt                                   1858 Fr 16 Sep 2022 10:04:28 CEST
    README_os2.txt                                   234 Fr 16 Sep 2022 10:04:28 CEST

Now, it looks like:

    " ============================================================================
    " Netrw Directory Listing                                        (netrw v171a)
    "   /usr/share/doc/vim-common
    "   Sorted by exten
    "   Hiding:        \(^\|\s\s\)\zs\.\S\+
    "   Quick Help: <F1>:help  -:go up dir  D:delete  R:rename  s:sort-by  x:special
    " ==============================================================================
    docs@                                          0 Mo 10 Okt 2022 17:58:47 CEST
    README.md                                   6985 Fr 16 Sep 2022 10:04:27 CEST
    README_VIM9.md                             10888 Fr 16 Sep 2022 10:04:27 CEST
    README.txt                                  4900 Fr 16 Sep 2022 10:04:27 CEST
    README_os2.txt                               234 Fr 16 Sep 2022 10:04:28 CEST
