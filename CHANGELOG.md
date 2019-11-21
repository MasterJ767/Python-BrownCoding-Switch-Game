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
  
* v1.2.1 [2019-11-20]: Bug fixes.
    - Logic Error: Corrected discard_card function on line 236 of switch.py so that if a K is discarded, the direction 
    is multiplied by -1 instead of 1 so the direction is actually reversed.
    - Unbound Local Error: Changed the function pick_up_card to return n-1, which is equivalent to i at the 
    end of the for loop, instead of returning i. This is because the return statement is outside of the for loop so 
    it cannot call upon the iterator of the for loop.
    - Syntax Error: Corrected the run_player function in switch.py so that when setting variables to False it uses the 
    setting operator ('=') instead of the equivalence operator ('==').

* v1.3.0 [2019-11-21]: Fixed the win check.
 Changed the run_player function in switch.py file to correctly return True or False under the right conditions.
 Then changed a line in the run_round function from `i = i + self.direction % len(self.players)` to 
 `i = (i + self.direction) % len(self.players)` so that it has the correct functionality as the modulo operator is 
 carried out before the addition operator, however the correct functionality of the program requires the addition to 
 be completed first. 
 
* v1.3.1 [2019-11-21]: Bug Fixes.
    - Syntax Error: Corrected the format of the input of the all() function in the test_setup_round__deals_cards 
    function in the test_switch.py file.
    - Logic Error: Changed the range of the for loop for the pick_up_card function in switch.py so that the range goes
    from 1 to 1 greater than the number of cards which the player is picking up so that the player picks up the correct 
    number of cards. The same function now returns n instead of n + 1 as it needs to return the number of cards the 
    player picked up, which is 1 less than the limit of the range of the for loop.
    - Logic Error: Changed the elif statement in the discard_card function so that it correctly sets draw2 to true if 
    the player discards a card of value 2.
    
    
    
