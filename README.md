# lattice-info
Prints out information about a table of Kaldi lattices (just like fstinfo does for OpenFST's finite state transducers).

The tool is able to print out information of each individual lattices (with --summary=false), or show the average statistics for the 
whole set of lattices in the Kaldi tables (with --summary=true).

Lattices can also be filtered by utterance-id to display only information about the lattices in the --include list, or to exclude 
the ones in the --exclude list.

```
Usage: lattice-info [options] lattice-rspecifier1 [lattice-rspecifier2 ...]
 e.g.: lattice-info --summary=false ark:1.lats ark:2.lats

Options:
  --compact                   : If true, work with lattices in compact form. (bool, default = true)
  --exclude                   : Text file, the first field of each line being interpreted as an utterance-id whose lattices will be excluded (string, default = "")
  --include                   : Text file, the first field of each line being interpreted as the utterance-id whose lattices will be included (string, default = "")
  --summary                   : If true, summarizes the information of all lattices. (bool, default = true)
```
