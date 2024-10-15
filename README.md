# Creating-Hash-Values

## Scenario
In Linux, create Hash in values of two separate files that appear to contain similar data to determine if they are identical.

### Generate Hashes for Files
First I will list the contents of the directory with the **ls** command. This outputs "file1.txt" and "file2.txt", these are the files I will be comparing.
Next I will display the contents of each file individually using the **cat** command. Comparing the outputs of both files, they appear to be identical.
The commands and outputs are detailed below:
![image](https://github.com/user-attachments/assets/84426c51-6a94-489d-b496-7a9ac3d37782)

To create Hashes for each file, I will use the command **sha256sum** with each file individually. Comparing the hash outputs of both files, visually we can see the values differ.
![image](https://github.com/user-attachments/assets/e7eaa7fe-3f82-448b-8cc4-0a6008c47cd2)

Another method of comparing Hashes will require writing each Hash to separate files. I will do this with the code "sha256sum file1.txt >> file1hash" and "sha256sum file2.txt >> file2hash" respectively. Then using the **cat** command to verify that the Hashes were written to the new files correctly.
Now that we have the Hashes written to new files, I can use the **cmp** command to compare the contents of these files byte by byte and will output the first byte and line number it detects a difference.
The commands and outputs are detailed below:
![image](https://github.com/user-attachments/assets/0e2585ae-e878-44e6-83f1-fe94ce90d202)
