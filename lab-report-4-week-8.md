  - Link to my Markdown repository : [Link](https://github.com/ajakhanwal/markdown-parse)
  - Link to the repository reviewed : [Link](https://github.com/floatboat/markdown-parse)
  
  1) Test Snippet 1 :
  - Excpected output using Vs Code Preview :
  ![image](https://user-images.githubusercontent.com/97641897/155628519-2acbb228-43de-47c1-8bcf-cbbea4cbb780.png)

   - Showing the test code in MarkdownParseTest.java : 
   ![image](https://user-images.githubusercontent.com/97641897/155629007-27e06a7e-65a9-4506-8731-2e9cd5f54fc4.png)

   - For my implementation, the corresponding output
   It fails the test :
   ![image](https://user-images.githubusercontent.com/97641897/155630042-6aab69c4-ac5b-4a74-bc29-344ab9709878.png)

   - For the reviewed implementation, the corresponding output :
   ![image](https://user-images.githubusercontent.com/97641897/155631968-5894d61f-fbdd-4ddc-8b92-bdcaeab02a7b.png)

    
   2) Test Snippet 2 :
   - Excpected output using Vs Code Preview :
   ![image](https://user-images.githubusercontent.com/97641897/155630165-3922b652-1dd1-4591-8b0e-4951fc8d44d6.png)

   - Showing the test code in MarkdownParseTest.java : 
   ![image](https://user-images.githubusercontent.com/97641897/155630325-9e85b60b-d813-4dd3-b927-4ace5665ce24.png)

   - For my implementation, the corresponding output
   It fails the test : 
   ![image](https://user-images.githubusercontent.com/97641897/155630560-6a6f6a50-fbea-48be-88e4-8c113cf3e9ab.png)

   - For the reviewed implementation, the corresponding output :
   ![image](https://user-images.githubusercontent.com/97641897/155632012-a0e00af8-e35b-457a-8e13-ec58171151b5.png)


   3) Test Snippet 3 : 
   - Excpected output using Vs Code Preview :
   ![image](https://user-images.githubusercontent.com/97641897/155630708-96b7fdbd-8aaf-4a9e-908e-231013c073d4.png)

   - Showing the test code in MarkdownParseTest.java : 
   ![image](https://user-images.githubusercontent.com/97641897/155630969-076ab50b-5adf-4449-97d1-26868ce7ab27.png)

   - For my implementation, the corresponding output
   It fails the test : 
   ![image](https://user-images.githubusercontent.com/97641897/155631165-637524ad-77bb-4537-8dd8-8d5c9401785b.png)

   - For the reviewed implementation, the corresponding output :
  ![image](https://user-images.githubusercontent.com/97641897/155632062-91dda4a8-b219-483c-9b60-e8e02a821aed.png)
  
  
  4) Answering Questions about possible code change
  - Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change : *Yes, I believe adding a if check statement after line 24 would solve the bug. By checking at if curr is equal to a backstick we can just escape move our currentIndex to the next character by incrementing it by one and then adding a cotinue statment.* 
  
  
  - Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change : *Yes, I believe if we add another equals statement on Line 36 we could fix the bug. We can check if the character after the curr is not another closed bracket. We add a `&&` in the if statement such that if the next character is a closed bracket it will continue until the last closed bracket is found.*


  - Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change : *No, I believe the code would require more involved changes greater than 10 lines to fix the bug. The issue at hand is that we do not trim the spaces in the links and another issue is that if a link does not have a closing paranthesis, the code still considers it as a link. I believe this a more complex issue and would require some more logic to fix.*



  
  

