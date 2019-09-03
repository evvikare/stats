# stats

stats is a bash script that computes the arithmetic mean and median of a set of numbers.
This was an assignment completed for CS344 Operating Systems at OSU.

## Usage

Stats can be run on its own:

    stats {-rows|-cols} [input_file]

But it is intended to be run against a grading script:

    ./p1gradingscript > p1results 2>&1

And the results are meant to be compared with "perfect" output:

    diff -y p1results p1perfectoutput | egrep -z --color=always '\s[\|<>]\s|$' | less -R

## Notes

The numbers can come from a file or via standard input on a Linux terminal.

There should be cosmetic (but not calculation) differences when diff is run on results and "perfect" output.

Stats is not intended to calculate rows greater than 1,000 bytes in length.

All rows are assumed to be the same length.
