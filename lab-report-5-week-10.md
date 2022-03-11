* How did you found the tests with different results? 
Answer : I used the program diff on the command line that shows the difference between the two result files. 

# Test 1:
* Actual Output for the shared markdown-parse: 

  ![image](https://user-images.githubusercontent.com/97641897/157789743-35571fd0-76bd-4108-b7bf-48cc20ab1297.png)

* Actual output for my markdown-parse : 

  ![image](https://user-images.githubusercontent.com/97641897/157789824-82654668-b21c-44b6-9b0f-9605e514d4ec.png)

* Expected Output : `[]`
* Correct Implementation : my markdown-parse

* Bug : The input uses `\` before a `[` to escape it, so it shouldn’t be treated as an open bracket for a link but rather as just an open bracket character. The code in the shared markdown-parse however fails to check for escape characters before `[` or anywhere at all in the mardown file.

* Code to be fixed :

  ![image](https://user-images.githubusercontent.com/97641897/157791122-08b8182d-badc-4ba1-92d4-0be685be8e75.png)

# Test 2:
* Actual Output for the shared markdown-parse: 
  
  ![image](https://user-images.githubusercontent.com/97641897/157792779-23a64dc2-90aa-430c-b554-ffbf2f3b291d.png)

* Actual output for my markdown-parse : 

  ![image](https://user-images.githubusercontent.com/97641897/157792834-aa0b37a2-fbdc-48b8-adbf-591e6f510374.png)

* Expected Output : `[]`
* Correct Implementation : my markdown-parse

* Bug : The input has some characters and words after the `]` and before the `(`, so it shouldn’t be treated as a link. The shared markdown-parse fails to check for characters between the `]` and `(` and rather just directly searches for the index of the next `(` after finding `]`.

* Code to be fixed :

 ![image](https://user-images.githubusercontent.com/97641897/157792981-87c442a1-fc1b-4be7-87eb-abfad53f8a07.png)

