# VG SNP-Aware

The official VG repo is https://github.com/vgteam/vg 

VG SNP-Aware is a custom reimplementation of the map command of VG. 
To use it replace the mapping.cpp and map_main.cpp on the official project. 

VG SNP-Aware aims to reduce the mapping time used by VG by approximating the alignment, considering only exact matches and using a depth-limited like
search on the graph. VG SNP-Aware is able to significantly reduce the time of the alignment phase. 

To use VG SNP-Aware add the sequentialSearch parameter to the VG map command:  
* vg map -f input_reads.fq -x graph.xg -g graph.gcsa --printMin --sequentialSearch -j
* vg map -f input_reads.fq -x graph.xg -g graph.gcsa --sequentialSearch -j

The printMin parameter allows to reduce the size of output to only reads with one or more reference or alternative base of SNPs.



