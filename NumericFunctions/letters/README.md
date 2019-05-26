# Letters.sas
|  |  |
|--|--|
|**Author:**  |Mark J. Lamias  |
|E**mail Contact:**  |mlamias (-at-) stochasticgroup (-dot-) com  |
|**Copyright:**  |2019, The Stochastic Group, Inc.  |

### License:  
Users are free to use this software at no cost so long as it is not altered in any way and these comments remain intact with the source code.

### About:  
This function returns a letter in the English alphabet corresponding to the position of the letter given by the first argument.
|                |                          |                         |
|----------------|-------------------------------|-----------------------------|
|**Inputs:**|**x** - an integer between 1 and 26.<br>**lettercase** - if "U" or "u" is specified an uppercase letter is returned.  if "L" or "l" is specified, lowercase letters are returned.            |
|**Outputs:**|An uppercase letter corresponding to the position specifieed by x when "U" is specified for the second argument.  A lowercase version is returned if "L" is specified in the second position.  The table below shows typical inputs and outputs. 
|**Errors:**|If either argument is invalid an error message is printed to the SAS log and a value of -1 is returned.          




### Typical Inputs & Output:  
<table>
<tr>
<td><b>Input:</b></td>
<td><b>Output:</b></td>
</tr>
<tr>
<td>letters(1, "U") </td>
<td>A</td>
</tr>
<tr>
<td>letters(2, "U") </td>
<td>B</td>
</tr>
<tr>
<td>letters(26, "U")</td>
<td>Z</td>
</tr>
<tr>
<td>letters(1, "L")</td>
<td>a</td>
</tr>
<tr>
<td>letters(24, "d")</td>
<td>-1 is the returned value<br/>ERROR: The second argument to the letters function must be one of:<br> U, u, L, or l.</td>
</tr>
<tr>
<td>letters(30, "U")</td>
<td>-1<br/>ERROR: The second argument to the letters function must be one of:<br/> U, u, L, or l. </td>
</tr>
</table>

### Example Usage:
This shows example usage ***after*** running letters.sas

    options cmplib=sasuser.userfuncs;
    data _null_;
    do i = 1 to 30;
    	lowerletters=letters(i, "L");
    	upperletters=letters(i, "U");
    	put i lowerletters upperletters;
    end;
    run;

			  		
				
