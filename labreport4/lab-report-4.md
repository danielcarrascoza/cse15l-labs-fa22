# Lab Report 4

## Using the Find Command

### Using ```find . -type c```

- We can first use the command to find all the files in the given directory by using ```find . -type d```.

```
danielcarrascoza@Daniels-MacBook-Air docsearch % cd technical  
danielcarrascoza@Daniels-MacBook-Air technical % find . -type d
.
./government
./government/About_LSC
./government/Env_Prot_Agen
./government/Alcohol_Problems
./government/Gen_Account_Office
./government/Post_Rate_Comm
./government/Media
./plos
./biomed
./911report
danielcarrascoza@Daniels-MacBook-Air technical % 
```

- Now, lets use find to find a specific file name by using ```find filename.type -type f```

```danielcarrascoza@Daniels-MacBook-Air technical % find ./plos/journal.pbio.002000
1.txt -type f
./plos/journal.pbio.0020001.txt
danielcarrascoza@Daniels-MacBook-Air technical % 
```
- Let's find all type f using ```find . -type f```

```
./technical/plos/journal.pbio.0020068.txt
./technical/plos/journal.pbio.0020054.txt
./technical/plos/journal.pbio.0020040.txt
./technical/plos/pmed.0010066.txt
./technical/plos/journal.pbio.0030131.txt
./technical/plos/journal.pbio.0020337.txt
./technical/plos/pmed.0020198.txt
./technical/plos/pmed.0010067.txt
./technical/plos/journal.pbio.0020121.txt
./technical/plos/pmed.0020007.txt
./technical/plos/journal.pbio.0030050.txt
./technical/plos/pmed.0020239.txt
./technical/plos/journal.pbio.0020241.txt
./technical/plos/pmed.0020005.txt
./technical/plos/journal.pbio.0020043.txt
./technical/plos/pmed.0020039.txt
./technical/plos/pmed.0010071.txt
./technical/plos/journal.pbio.0030127.txt
./technical/plos/pmed.0010058.txt
./technical/plos/pmed.0010070.txt
./technical/plos/pmed.0010064.txt
./technical/plos/pmed.0020158.txt
./technical/plos/journal.pbio.0020042.txt
./technical/plos/journal.pbio.0020297.txt
./technical/plos/pmed.0020206.txt
```

### using find . -size 

- using find . -size -1024
```
danielcarrascoza@Daniels-MacBook-Air docsearch %  find . -type f -size -1024c 
./URLHandler.class
./count-txts.sh
./DocSearchServer.class
./README.md
./Handler.class
./count-txtss.sh
./.git/config
./.git/objects/6f/b93f4938a2568b6da4f3c6be5e9e31d99a4bbb
./.git/objects/02/fda6e0b9cec03be2a5c6f6128b6c720326682a
./.git/objects/a4/0d47c88f17fdf0668c47300c04f5a1bfe94106
./.git/objects/bb/e0a0a4c8af52f9b875d1f6791e15ad434a7aec
./.git/objects/ab/ed38d69409aea3d47337002d3a8353907869e1
./.git/objects/c7/f970621f7bb61d2473b0cffb0ec1b6d3a30f4a
./.git/objects/c7/d26e3b75df3a81dab811269256a9d77b618d33
./.git/objects/c0/07e12331f15fd096d9c9731679913224fd7b27
./.git/objects/ec/35bdf2605157098accf33760252b77cdd41a40
./.git/objects/ec/1fcff542cdc23aab6176143ec8bcfa280788d0
./.git/objects/10/1c819387dfa5de5aaa29680439fef42c418606
./.git/objects/08/0c229f05b84666f7fdbdf6569f4e70eabcb4d8
./.git/objects/d5/079985d0f4e3be2d929a9cd22ca64a6027b3f0
./.git/objects/f9/38f8f6016b8902c60a43794f3a4c2ced817d07
./.git/objects/46/ca393e5d2473083540d82d1c91d2a8edc1e0de
./.git/objects/12/84a844c61e61f3c416fa7bfedf8ee66809b8b8
./.git/HEAD
./.git/info/exclude
./.git/logs/HEAD
./.git/logs/refs/heads/main
./.git/logs/refs/remotes/upstream/main
./.git/description
./.git/hooks/commit-msg.sample
./.git/hooks/applypatch-msg.sample
./.git/hooks/pre-receive.sample
./.git/hooks/post-update.sample
./.git/hooks/pre-merge-commit.sample
./.git/hooks/pre-applypatch.sample
./.git/refs/heads/main
./.git/refs/remotes/origin/HEAD
./.git/refs/remotes/upstream/HEAD
./.git/refs/remotes/upstream/main
./.git/packed-refs
./.git/FETCH_HEAD
./technical/plos/pmed.0020191.txt
./technical/plos/pmed.0020226.txt
```

- find direcoties with size +3k -size -5k

```
danielcarrascoza@Daniels-MacBook-Air docsearch % find . -type d -size +3k -size -5k
./technical/government/Media
```

- changing up the size in technical
```
danielcarrascoza@Daniels-MacBook-Air docsearch % find ./technical  -type f -size -2048c
./technical/government/Media/Helping_Hands.txt
./technical/government/Media/Campaign_Pays.txt
./technical/government/Media/Fire_Victims_Sue.txt
./technical/government/Media/Court_Keeps_Judge_From.txt
./technical/government/Media/It_Pays_to_Know.txt
./technical/government/Media/Self-Help_Website.txt
./technical/government/Media/Justice_requests.txt
./technical/government/Media/Wilmington_lawyer.txt
./technical/government/Media/Lawyer_Web_Survey.txt
./technical/plos/pmed.0020048.txt
./technical/plos/pmed.0020028.txt
./technical/plos/pmed.0020191.txt
./technical/plos/pmed.0020226.txt
./technical/plos/pmed.0020192.txt
./technical/plos/pmed.0020157.txt
./technical/plos/pmed.0020082.txt
./technical/plos/pmed.0020120.txt
```

### using find ./technical -iname [file name]

- case insensitive to find paths for files.

```
danielcarrascoza@Daniels-MacBook-Air docsearch % find ./technical -iname "sept*.txt"
./technical/government/Gen_Account_Office/Sept27-2002_d02966.txt
./technical/government/Gen_Account_Office/Sept14-2002_d011070.txt
danielcarrascoza@Daniels-MacBook-Air docsearch %
```

- Here, lets check using iname to find a capital file with lowercase in the command

```
danielcarrascoza@Daniels-MacBook-Air technical % find ./government -iname "config*.txt" 
./government/About_LSC/CONFIG_STANDARDS.txt
```

- Lets try it again and also combine this with a size command

```
anielcarrascoza@Daniels-MacBook-Air technical % find ./government -iname "legal*.txt"          
./government/About_LSC/LegalServCorp_v_VelazquezSyllabus.txt
./government/About_LSC/LegalServCorp_v_VelazquezDissent.txt
./government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt
./government/Media/Legal-aid_chief.txt
./government/Media/Legal_system_fails_poor.txt
./government/Media/Legal_Aid_in_Clay_County.txt
./government/Media/Legal_hotline.txt
./government/Media/Legal_Aid_looks_to_legislators.txt
./government/Media/Legal_Aid_Society.txt
./government/Media/Legal_Aid_attorney.txt
./government/Media/Legal_services_for_poor.txt
./government/Media/Legal_Aid_campaign.txt
danielcarrascoza@Daniels-MacBook-Air technical % find ./government -iname "legal*.txt" -size +3k
./government/About_LSC/LegalServCorp_v_VelazquezSyllabus.txt
./government/About_LSC/LegalServCorp_v_VelazquezDissent.txt
./government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt
./government/Media/Legal-aid_chief.txt
./government/Media/Legal_system_fails_poor.txt
./government/Media/Legal_Aid_in_Clay_County.txt
./government/Media/Legal_Aid_attorney.txt
./government/Media/Legal_services_for_poor.txt
```
- Here, we can see the use of both parts of the command line. The size filters out some of the files in the directory and the other makes sure that the legal does not have to be capitalized or in lowercase.