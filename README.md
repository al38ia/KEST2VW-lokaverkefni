# KEST2VW-lokaverkefni

# JOURNAL

These past few days I’ve been working through steps 2, 3, and 4 of the KEST2VW final project, and honestly, it’s been a mix of confusion, trial-and-error, and small victories. I started by getting my Windows 11 virtual machine ready. I installed Python, Git, and VS Code since those were required, and made sure everything was working before moving on. Once the basics were set up, I began working on the user management part, which ended up taking way longer than I expected.

The assignment required setting up nine users for a fictional company, each with their own department group, plus an “Allir” group that everyone belongs to. Instead of creating users one by one, I made a CSV file with all their info: full name, first name, last name, username, and department. Then I wrote a PowerShell script that imported that CSV and automatically created each account. I set the password for all users to “1234kest” at first, then made sure that the password had to be changed on the first login. I learned how to do this using a YouTube tutorial about PowerShell user creation, since the built-in documentation was a little confusing. After running the script, I used commands like Get-LocalUser and Get-LocalGroupMember to double-check everything. It actually felt pretty satisfying seeing all the users show up correctly.

Next came the folders and permissions. I created a folder called “Gögn” on the C: drive, and inside it I made folders for each group: Sala, Innkaup, Yfirstjórn, plus a shared folder called Sameign. For each folder, I set NTFS permissions so only members of the matching group had access. Sameign was open to everyone. I also added a text file inside each folder named after the group. This part wasn’t too hard, but I had to redo it once because I accidentally applied permissions to the wrong user.

After that, I moved on to the security settings. I opened the Local Security Policy tool and changed the password rules so the minimum length was 8 characters and password complexity was required. I tested this by trying to change a user's password to something weak just to see if Windows blocked it, and it did. Then I configured the firewall. I set it so all incoming network traffic was blocked except ICMP (ping), because the assignment said ping should still work. Once I applied the rule, I tested it with ping to make sure the machine still responded.

By the end of all this, I had steps 2 through 4 fully done. It took time, and I ran into a bunch of small issues, but everything works now and I feel a lot more confident with PowerShell, user management, and Windows permissions than when I started.

## *Here are the pictures that show my windows project* 

#### This image shows that the groups have been created.
![img](pics/KEST/groups.png)
#### This image is to show that (GÖGN) have been created and its content.
![img](pics/KEST/files_in_gögn.png)
#### This image shows that (GÖGN) has the right content in it.
![img](pics/KEST/folders_in_gogn.png)
#### The next 4 images shows the (txt.file) that is with in the files in (GÖGN).
![img](pics/KEST/innkauptxt.png)
![img](pics/KEST/salatxt.png)
![img](pics/KEST/sameigntxt.png)
![img](pics/KEST/yfirstjorntxt.png)
### This here shows the groups and the users that belongs to that group.
#### Users in (Innkaup) group.
![img](pics/KEST/innkaup_users.png)
#### Users in (Sala) group.
![img](pics/KEST/sala_users.png)
#### Users in (Yfirstjorn) group.
![img](pics/KEST/yfirstjorn_users.png)
#### This picture here shows that all the users are in the (Allir) group.
![img](pics/KEST/allir_users.png)
#### This picture proofs that the users are active currntly.
![img](pics/KEST/proof_that_users_are-active.png)
#### This is a seconed proof are users are active.
![img](pics/KEST/proof2_that_users_are_enabled.png)
### Now in the next 9 pictures you will see information that includes everything you need to know about the users one by one.
#### This is for the user (GudEir).
![img](pics/KEST/proof_out_og_GudEir.png)
#### This is for the user (AsdMag).
![img](pics/KEST/proof_out_of_AsdMag.png)
#### This is for the user (BalBal).
![img](pics/KEST/proof_out_of_BalBal.png)
#### This is for the user (EvaMar).
![img](pics/KEST/proof_out_of_EvaMar.png)
#### This is for the user (GudBja).
![img](pics/KEST/proof_out_of_GudBja.png)
#### This is for the user (KriSno).
![img](pics/KEST/proof_out_of_KriSno.png)
#### This is for the user (OlaLei).
![img](pics/KEST/proof_out_of_OlaLei.png)
#### This is for the user (PerSte).
![img](pics/KEST/proof_out_of_PerSte.png)
#### This is for the user (VilTra).
![img](pics/KEST/proof_out_of_VilTra.png)
#### This picture shows the password has been set to min-length (8) columns.
![img](pics/KEST/password_min_length_is8.png)
#### This is from the firewall part and shwos that pings are allowed.
![img](pics/KEST/ping_is_allowed.png)
#### This image shows that the inpund connections are blocked by default.
![img](pics/KEST/shows_that_inpound_connections_are_blocked_by_default.png)
### The next 2 images are for the apps that we were required to download on the VM.
#### This shows that ive downloaded (VScode)-(Python).
![img](pics/KEST/proof_of_vscode_and_pythonT.png)
#### And this one shows (Git).
![img](pics/KEST/proof_of_Git.png)



