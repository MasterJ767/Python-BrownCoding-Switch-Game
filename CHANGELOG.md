# CHANGELOG

* v1.1.0 [2019-11-08]: Added a SmartAI computer opponent.
  Added strategy players.SmartAI
  None of the bugs have been fixed.

* v1.1.0 [2019-10-25]: First major release.
  This version is known to contain some bugs.

* v1.1.1 [2019-11-19]: Bug fixes.
    - Syntax Error: Added a missing parenthesis from line 50 of players.py file.

* v1.1.1 [2019-11-20]: Bug fixes.
    - Spelling Mistakes: Corrected misspelt words in comments on lines 24 and 48 of switch.py.
    - Logic Error: Removed second A from the possible card values as this was causing the generation of a deck of size 
    56 rather than the intended size of 52.
    - Assertion Error: Corrected a K to an A in line 97 of test_switch.py as that function is supposed to be checking if 
    it is okay to discard an A onto a given card not a K.
    - Logic Error: Added a test for the fourth suit of A and Q to make discardable check test exhaustive.
    - Logic Error: Added an `if __name__ == '__main__'` clause to the switch.py file so that the game plays when the 
    program is run.

* v1.2.0 [2019-11-20]: Fixed discardable check.
  Changed can_discard function in switch.py file to correctly return True or False under the right conditions. 
  Then changed the input parameters of can_discard and draw_and_discard so that they require the input of the card, 
  currently at the top of the discard pile.
  
