# sw-bdsmm
Implementation of Smith-Waterman alignment algorithm for CBB 752.

## Usage
python sw_align.py [-h] -i INPUT -s SCORE [-o OPENGAP] [-e EXTGAP]

Required arguments:
  -h, --help            show this help message and exit
  -i INPUT, --input INPUT
                        input file (text file of 2 sequences, one per line)
  -s SCORE, --score SCORE
                        score file (tab- or space-delimited substitution matrix)
                        
Optional arguments:
  -o OPENGAP, --opengap OPENGAP {Default: -2}
                        open gap
  -e EXTGAP, --extgap EXTGAP {Default: -1}
                        extension gap
                        
Notes:
* It's assumed that your input sequences and substitution matrix files are properly formatted (no illegal characters, nonsensical values, etc.).
* You can pick your own gap-opening and gap-extension penalties, but they're expected to be negative values.

## Example
python sw_align.py -i sample-input.txt -s blosum62.txt

If you run this example, the output should be equivalent to that found in sample-output.txt.
