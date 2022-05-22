# Week 8 Lab Report 4 
* link to my repository: https://github.com/magikarp620/markdown-parser 
* link to my repository: https://github.com/Mnohem/markdown-parser  
Expected parsed output from: https://spec.commonmark.org/dingus/
* Snippet 1
  ![Screen Shot 2022-05-22 at 1 47 58 PM](https://user-images.githubusercontent.com/98373624/169715236-dcfae4dd-02a2-4eef-84e8-08ac17f3cd50.png)
  ## Test: 
  ![Screen Shot 2022-05-22 at 2 21 34 PM](https://user-images.githubusercontent.com/98373624/169716387-be5a0b5b-e0a9-418d-9397-b7006adfc163.png)    
  ## Their output:![Screen Shot 2022-05-22 at 2 23 01 PM](https://user-images.githubusercontent.com/98373624/169716437-91f11016-770f-44bd-b416-a2a4b0370061.png)
  ## Our output:![Screen Shot 2022-05-22 at 2 20 17 PM](https://user-images.githubusercontent.com/98373624/169716376-2619e54e-e27b-4571-a54a-43e0a8a0aca3.png)
  ## Round 1 both failed
* Snippet 2
  ![Screen Shot 2022-05-22 at 1 48 24 PM](https://user-images.githubusercontent.com/98373624/169715258-436a9e2a-5e69-47a3-ac66-877a4c9d5c49.png)
  ## Test:
  ![Screen Shot 2022-05-22 at 2 26 59 PM](https://user-images.githubusercontent.com/98373624/169716588-aeb9cad9-8368-495e-bb26-ab2c124ce260.png)  

  ## Their Output:
  ![Screen Shot 2022-05-22 at 2 27 17 PM](https://user-images.githubusercontent.com/98373624/169716593-49a0cf4f-8f99-4487-b199-806d14e29734.png). 

  ## Ouroutput:
  ![Screen Shot 2022-05-22 at 2 27 09 PM](https://user-images.githubusercontent.com/98373624/169716590-5da299c6-6880-490d-9d30-b41a9d8fc9d0.png). 
  ## Round 2 both failed
* Snippet 3
  ![Screen Shot 2022-05-22 at 1 48 55 PM](https://user-images.githubusercontent.com/98373624/169715268-11e9f31d-257a-4130-b090-4cbff14fef95.png)
  ## Test:
  ![Screen Shot 2022-05-22 at 2 30 01 PM](https://user-images.githubusercontent.com/98373624/169716715-747d3ac8-05cf-473f-86c4-da3282e2ef73.png). 

  ## Their Output:
  ![Screen Shot 2022-05-22 at 2 30 43 PM](https://user-images.githubusercontent.com/98373624/169716725-9f519986-42b9-4333-925b-438dbb52b264.png). 

  ## Our Output:
  ![Screen Shot 2022-05-22 at 2 30 32 PM](https://user-images.githubusercontent.com/98373624/169716716-f9cbb346-b30b-4f1a-b8f7-56f16eb40af3.png). 

* Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.  
    >> Yes, in the first snippet, out code read the earlier ] close bracket causing the the last line not read into the code. We can check for extra parenthesis or bracket to avoid reading them as a mark but as a String.  
* Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.  
    >> In the second snipped test, a similar situation arised, with the extra closing parenthesis, the code is going to read the first of the closing parenthesis and ignore whatever comes after. If we take the last parenthesis instead we could have gotten the data in between.  
* Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.  
    >> In the thrid snippe, our code successfully read the link but did not parse the space in front of the link, also a link without closing parenthesis are also read and outputted. We need to check if every element bracket/parenthesis is in the link in order to output.  
