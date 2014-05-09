PETRARCH-Development
====================

Code for the stand-alone development version of PETARCH (PETR.coder.py and associated modules)

See the header of PETR_coder.py for details on the current state of the program. In a 
nutshell, this works -- it coded 60,000 AFP sentences from the GigaWord corpus without 
crashing, using the included dictionaries -- but the pattern matching is only partially 
implemented (and there are about six known potentially lethal errors that are currently 
trapped in order to avoid crashes). However, it now has almost all of the features of
the TABARI coder

Documentation could also use a little work (really??) but is fairly complete, though 
scattered in """...""" blocks throughout the program.

Due to constraints on time, this has not been retrofitted into the structure found in 
the "PETRARCH" repo: we will eventually do this.

	============= Unit tests ============

Commits should always successfully complete 

	python PETR.coder.py -v PETR.UnitTest.records.txt

The final record should read

	Sentence: FINAL-RECORD [ DEMO ]
	ALL OF THE UNIT TESTS WERE CODED CORRECTLY. 
	No events should be coded
	No events were coded
	Events correctly coded in FINAL-RECORD
	Exiting: <Stop> record 

	====== Compatibilities with TABARI dictionaries =====

PETRARCH has a much richer dictionary syntax than TABARI, which will eventually accommodate 
the WordNet-enhanced dictionaries developed at Penn State as well as reducing the level 
of redundancy in the existing dictionaries. While the initial version of the program 
could use existing TABARI dictionaries, this compatibility will decline with further 
developments and only the PETRARCH-specific dictionaries can be used

15-Nov-2013: Requires TABARI 0.8 indented date restrictions, not older in-line format
23-Apr-2014: PETRARCH-formatted agents dictionary required