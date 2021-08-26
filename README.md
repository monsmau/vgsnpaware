# VG SNP-Aware
 

VG SNP-Aware is a custom reimplementation of the map command of VG. 
To run it, replace the mapping.cpp and map_main.cpp source files on the official project (https://github.com/vgteam/vg). 

VG SNP-Aware aims to reduce the mapping time used by VG by approximating the alignment, considering only exact matches and using a depth-limited like
search on the graph. VG SNP-Aware is able to significantly reduce the time of the alignment phase. 

To use VG SNP-Aware add the sequentialSearch parameter to the VG map command:  
* vg map -f input_reads.fq -x graph.xg -g graph.gcsa --printMin --sequentialSearch -j
* vg map -f input_reads.fq -x graph.xg -g graph.gcsa --sequentialSearch -j

The printMin parameter allows to reduce the output size to only reads with one or more reference or alternative base of SNPs.

The  VG  version is v1.29.0-44-ga74417fcb "Sospiro".



