We will need the google drive shareable link. Example of what a google drive shareable link:
https://drive.google.com/file/d/13oki4nUEp3z_6Sl4NovhldB90HZ1w1c-/view?usp=sharing

Identify the FILEID in the link above. FILEID = 13oki4nUEp3z_6Sl4NovhldB90HZ1w1c-
Identify the FILENAME in the link above. FILENAME = Linemod_and_Occlusion.zip

Replace FILEID and FILENAME in the command below:

wget --load-cookies /tmp/cookies.txt "https://docs.google.com/uc?export=download&confirm=$(wget --quiet --save-cookies /tmp/cookies.txt --keep-session-cookies --no-check-certificate 'https://docs.google.com/uc?export=download&id=FILEID' -O- | sed -rn 's/.*confirm=([0-9A-Za-z_]+).*/\1\n/p')&id=FILEID" -O FILENAME && rm -rf /tmp/cookies.txt

After replacing the FILEID and FILENAME, the command will look like:

wget --load-cookies /tmp/cookies.txt "https://docs.google.com/uc?export=download&confirm=$(wget --quiet --save-cookies /tmp/cookies.txt --keep-session-cookies --no-check-certificate 'https://docs.google.com/uc?export=download&id=13oki4nUEp3z_6Sl4NovhldB90HZ1w1c-' -O- | sed -rn 's/.*confirm=([0-9A-Za-z_]+).*/\1\n/p')&id=13oki4nUEp3z_6Sl4NovhldB90HZ1w1c-" -O Linemod_and_Occlusion.zip && rm -rf /tmp/cookies.txt

Finally, this will download the Google Drive file on your machine using only your terminal screen of your Linux machine.
