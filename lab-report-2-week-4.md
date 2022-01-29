# Code Change 1 : 
* Screenshot of the code change diff from Github : 

![image](https://user-images.githubusercontent.com/97641897/151634328-e92f85ea-f6ca-42cb-8652-a3d830cfd510.png)
![image](https://user-images.githubusercontent.com/97641897/151634376-4ef5b6e4-52fe-45c3-8f94-468206b434cd.png)

* Link to the test file for a failure inducing input that prompted a change in the code : [Link](https://github.com/ajakhanwal/markdown-parse/blob/57805bd132758189fdee8220876e148c895e7d35/Group-test-file2.md)

* Symptom of the failure-inducing input in the command line: 

Exception in thread "main" java.lang.OutOfMemoryError: Java heap space
        at java.base/java.util.Arrays.copyOf(Arrays.java:3512)
        at java.base/java.util.Arrays.copyOf(Arrays.java:3481)
        at java.base/java.util.ArrayList.grow(ArrayList.java:237)
        at java.base/java.util.ArrayList.grow(ArrayList.java:244)
        at java.base/java.util.ArrayList.add(ArrayList.java:454)
        at java.base/java.util.ArrayList.add(ArrayList.java:467)
        at MarkdownParse.getLinks(MarkdownParse.java:17)
        at MarkdownParse.main(MarkdownParse.java:25)
        
 * The test file has a link in the markdown format followed by a sentence that does not contain a link. This causes a symptom as the code has a bug such that it only searches for the brackets and paranthesis and keeps checking until you reach the end of the file.

# Code Change 2 : 
* Screenshot of the code change diff from Github : 

![image](https://user-images.githubusercontent.com/97641897/151635975-9e655d7b-5b85-4f35-a41d-68fb98069b0e.png)

* Link to the test file for a failure inducing input that prompted a change in the code : [link](https://github.com/ajakhanwal/markdown-parse/blob/a79bf2696baf65e357170e38c513c5af509c2646/Group-test-file3.md)

* Symptom of the failure-inducing input in the command line: [\]

*The test file has escape characters and paranthesis inside the the brackets which causes a symptom that prints the wrong output. The bug in the code is such that it fails to check if the current character is escape and that it fails to take into consideration possible paranthesis inside the brackets. 

# Code Change 3 :

* Screenshot of the code change diff from Github : 
![image](https://user-images.githubusercontent.com/97641897/151634328-e92f85ea-f6ca-42cb-8652-a3d830cfd510.png)
![image](https://user-images.githubusercontent.com/97641897/151634376-4ef5b6e4-52fe-45c3-8f94-468206b434cd.png)
![image](https://user-images.githubusercontent.com/97641897/151635975-9e655d7b-5b85-4f35-a41d-68fb98069b0e.png)
![image](https://user-images.githubusercontent.com/97641897/151637415-4d9b7e48-e715-41d8-8baf-4a3ad13df131.png)

* Link to the test file for a failure inducing input that prompted a change in the code : [link](https://github.com/ajakhanwal/markdown-parse/blob/60ad5f2b2ce0150af235f735b21f8d0a3ebe84fc/Group-test-file4.md)

* Symptom of the failure-inducing input in the command line:
        Exception in thread "main" java.lang.OutOfMemoryError: Java heap space
                at java.base/java.util.Arrays.copyOfRange(Arrays.java:3822)
                at java.base/java.lang.StringLatin1.newString(StringLatin1.java:769)
                at java.base/java.lang.String.substring(String.java:2709)
                at MarkdownParseOrg.getLinks(MarkdownParseOrg.java:17)
                at MarkdownParseOrg.main(MarkdownParseOrg.java:25)

* The input has one link plus another set of brackets followed by a closing paranthesis and few escape characters and so on. This causes a symptom in the original Markdown-parse file as it has bugs which do not check for what happens if the there is something else after brackets and that does not check for escape characters.
