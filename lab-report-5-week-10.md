# Week 10 Lab Report 5 
I manually look through the output, and try to fix exceptions and then fix different outputs.
## Code Difference #1
Mine:  
![Screen Shot 2022-06-02 at 12 29 33 PM](https://user-images.githubusercontent.com/98373624/171723091-a4a502a9-409b-4eba-ac96-c85cf3b74f3f.png)  
Provided:  
![Screen Shot 2022-06-02 at 12 28 07 PM](https://user-images.githubusercontent.com/98373624/171723100-e655cd9b-8699-41fc-9bef-53f6cc19ce5c.png)  
Test file 17.md:  
![Screen Shot 2022-06-02 at 12 29 55 PM](https://user-images.githubusercontent.com/98373624/171723109-d380b519-3c2b-45cc-9526-14c72cda965d.png)   
Correct Output:  
![Screen Shot 2022-06-02 at 12 31 27 PM](https://user-images.githubusercontent.com/98373624/171723278-6d9444a8-6d93-44f4-9e26-b1572bc2cc73.png)  
There are no link when we hover on the string so the correct outpur should be []
The provided code has the correct output  
This test file contains no close Bracket which returns -1 to closeBracket varible. 
When we tried to read the substring it returns OutofBound error  
![Screen Shot 2022-06-02 at 12 38 22 PM](https://user-images.githubusercontent.com/98373624/171724875-ad5318fe-f3aa-41a6-9a0b-29dd35367190.png)
## Results after Code Change. 
![Screen Shot 2022-06-02 at 12 41 02 PM](https://user-images.githubusercontent.com/98373624/171724884-a4450ac2-2cd9-42e9-9dbe-91d4930328c4.png)
--------
## Code Difference #2
Mine:   
Screen Shot 2022-06-02 at 1.04.38 PM
Provided:   
![Screen Shot 2022-06-02 at 1 04 47 PM](https://user-images.githubusercontent.com/98373624/171728738-124ac584-33bc-4509-8d3a-caab81f3b148.png)  
Test file 578.md:  
![Screen Shot 2022-06-02 at 1 04 38 PM](https://user-images.githubusercontent.com/98373624/171729063-f6802d74-e956-4ddf-9f52-3dbe2afd93cf.png)  
Correct Output:  
![Screen Shot 2022-06-02 at 1 07 45 PM](https://user-images.githubusercontent.com/98373624/171729116-b64bc3f8-b2ae-4698-ab83-9ff0a5d548b0.png)  
There are no link when we hover on the string so the correct outpur should be []
The provided code has the correct output  
## Code Change 
We used to catch image files by checking if the string ends with .png or .jpg. 
I changed the code to if it contains .png or .jpg  
![Screen Shot 2022-06-02 at 1 12 46 PM](https://user-images.githubusercontent.com/98373624/171730110-ea219036-433e-4eb8-a281-728f399f2c1e.png)
## Results  
![Screen Shot 2022-06-02 at 1 13 33 PM](https://user-images.githubusercontent.com/98373624/171730154-aca1be05-979e-4986-8583-0c018b07de84.png)
