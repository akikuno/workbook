# Beginner

## Target level

- Those who can open terminal
- (Optional) Those who know [BED format](https://m.ensembl.org/info/website/upload/bed.html).

## Preparation

Execute the following code.


```sh
TAB="$(printf '\t')"

cat << EOF > test.bed
1${TAB}100${TAB}1000${TAB}geneA${TAB}20
1${TAB}100${TAB}1000${TAB}geneA${TAB}200
1${TAB}900${TAB}2000${TAB}geneB${TAB}100
1${TAB}1000${TAB}2200${TAB}geneB${TAB}10
2${TAB}100${TAB}1500${TAB}geneC${TAB}1000
10${TAB}100${TAB}1000${TAB}geneD${TAB}2000
1${TAB}100${TAB}1000${TAB}geneA${TAB}200
EOF
```

## Questions

### Environments

- Execute `pwd`
- Execute `ls`

### Directory

- Execute `mkdir test_insilico`, then `ls`
- Execute `cd test_insilico`, then `pwd`, then `ls`
- Execute `cd ../`, then `pwd`, then `ls`
- Execute `rm -rf test_insilico`, then `ls`

### I/O

- Display `test.bed` (`cat`)
- Display the first 3 lines (`head`)
- Display the 2 lines from the end (`tail`)
- Display 3 lines from the beginning and 2 lines from the end（`head`, `tail`, `|`: pipe)
- Display the first 3 lines and save to `test2.bed` (`head`, `>`:redirect)

### sort, uniq

- Sort `test.bed` by lexicographic order (`sort`)
- Sort `test.bed` by numerical order (`sort -n`)
- Sort `test.bed` by numerical order based on column 5 (`sort -k`)
- Remove the duplicate lines in `test.bed` (`sort -u`)
- Count the number of dupilicate lines in `test.bed` (`sort`, `uniq -c`)

### grep

- Display the lines containing `geneB` (`grep`)
- Display the lines tat do not containing `geneB` (`grep -v`)
- Display the lines containing `geneA` or `geneB` (`grep -e`)
- Display the lines containing `geneA` or `geneB`, and score `20` (`grep -e`, `|`)

### sed

- Replace `gene` to `Gene` (`sed`)
- Add a `chr` at the beginning of the first row (`sed`, regular expression)
- Replace tab delimited to comma delimited (`sed`, escape sequence)
