#Module 3

## Exercise 1 

I opened terminal on my computer 

Then curl http://archive.org/stream/diplomaticcorre33statgoog/diplomaticcorre33statgoog_djvu.txt > texas.txt

Then nano texas.txt. 

Followed the instructions and deleted up until the index started 

sed -e -i.bak 's/(.+\bto\b.+)/~\1/g' texas.txt

and then ls

and then nano texas.txt

nothing happended, I did not have any ~

So then I tried again

I did $ mv texas.txt.bak texas.txt

Then sed -e -i.bak 's/(.+\bto\b.+)/~\1/g' texas.txt

Then Ls

Then nano texas.txt 

Still no ~ 

I then asked for help in the Slack group

In the mean time, I looked back at my data and noticed that I had way more than 2000 lines, I had over 5000, so I had forgotten to remove the rest of the data like was previously mentioned a couple steps above

So I went and removed that data

Thought maybe that would change things 

So I re did the steps

sed -e -i.bak 's/(.+\bto\b.+)/~\1/g' texas.txt

got error code – so I copy pasted it directly off the slack page

command worked 

sed -e -i.bak 's/(.+\bto\b.+)/~\1/g' texas.txt

and then ls

and then nano texas.txt

still nothing happended 

re read the instructions to see if I can find another stop I went wrong

Couldn’t find anything

Received helped from @dr.graham on Slack, the rest of the info comes from the workbook & the video he created.

Ran sed -E -i.bak 's(.+ to .+)/-\1/g' texas.txt

then sed -E -i.bak's(.+ to .+)/-\1/g' texas.txt

then sed -E -i.bak 's/(.+ to .+)/~\1/g' texas.txt

and it worked – I got ~ on all of them 

then did $ grep '~' texas.txt

then grep '~' texas.txt > index

did not work – realized I forgot the .txt

then did grep '~' texas.txt > index.txt

nano index.txt

then sed -E -i.bak 's/(,)( [0-9]{4})(.+)/\2/g' index.txt
 
then nano index.txt to confirm 

then sed -E -i.bak 's/~/ /g' index.txt

then nano index.txt to confirm they are ~ gone

then grep -E ".+,.+,.+," index.txt
 
and then cp index.txt cleaned-correspondence.csv to save the file on my hardrive 

uploaded file to github 

## Exercise 2

Downloaded openrefine

Created a project 

Downloaded my file from exercise 1

Named the project m3-exercise2

Selected the Text Facet for both Sender & Recipient 

Clicked on 'cluster'

Did the various cluster methods for both Sender & Recipient 

Then selected 'Trim leading and trailing whitespace' for both of them

Saved the a .csv file of the work on my computer 

After, went back in and changed sender to source and recipient to target

Saved it again to my hardrive

Uploaded the files to Github
