Exatrack NTFS crash p0c

MFT $Extend (11) -> IndexRoot.DirectoryIndex.EntriesOffset set to 0xD0 on an old Windows 7 NTFS partition. A Windows 10 system will try to add entries (0x146 bytes over 0x1D0 are consumed, this will cause a relocation, which will cause the overflow).

Just mount the VHD on a win10 system. You can also copy it to a removable drive.

**You definitely don't want to run this on your host machine : no BSOD might cause corrupted system in some cases, maybe related to other NTFS kernel objects corruption.**

Original advisory :
- https://twitter.com/ExaTrack/status/1186554050629779456 
- https://exatrack.com/public/vuln_NTFS_EN.pdf

Helpful NTFS links : 
- https://github.com/Heurs/parseNTFS
- https://ultradefrag.net/doc/man/ntfs/NTFS_On_Disk_Structure.pdf
- https://www.ivanlef0u.tuxfamily.org/?p=76
