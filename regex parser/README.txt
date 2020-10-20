Author: Mukesh Viswanathan
Data of Submission: 04/17/2020

Regex parser that does the following: 
 Regular expression to NFA to DFA to MFA(min dfa)

How it works:

1. Use Thompson algorithm to convert the regular expression to NFA  
2. Use the subset construct to convert NFA to DFA  
3. Minimize DFA to MFA (Min DFA) 
4. Use MFA to match strings

How to run:

1. download the zip file and add to your workspace. 
2. open on a java compiler
3. run "test.java" from the main folder. 
4. Enter Regualr expression
5. Enter string to check correct/incorrect.
The dependancies are clearly given while importing for each routine. 
for example: 
 /test.java -
            import dfa.DFA;
            import mfa.MFA;
            import nfa.NFA;
        
    So every construction has it's own dependancy
The tables were created with the help of the java libraries to be more clear.
Inputs to give can be found in test_suite.data
Regular expression   Valid           Invalid
(ab|a)(bc|c)    	    abc 	   acb
(ab)c|abc       	   abc 		   ab
(a*)(b?)(b+)     	   aaabbbb	   aaaa
((a|a)|a)        		   a   		   aa
(a*)(a|aa)      		   aaaa    	   b
a(b)|c(d)|a(e)f  	   aef 		   adf
(a|b)c|a(b|c)    	   ac  		   acc
(a|b)c|a(b|c)    	   ab  		   acc
(a|b)*c|(a|ab)*c   	   abc 		   bbbcabbbc




refernces:
https://stackoverflow.com/questions/2745206/output-in-a-table-format-in-javas-system-out/32515408
https://github.com/xysun/regex
https://math.stackexchange.com/questions/219948/creating-a-minimal-dfa-from-a-regular-expression
https://cyberzhg.github.io/toolbox/nfa2dfa



