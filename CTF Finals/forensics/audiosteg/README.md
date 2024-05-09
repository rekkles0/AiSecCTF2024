# AisecCTF2024

`Title`
> AudioSteg

`Description`
> Dont trust everything you see.

`Tag`
> Forensics.

# Solution

to solve this challenge we nedd to follow the steps bellow: 

	1.unzip the image robot_2.jpg
		when this is done we will get a directory that contain 2 file (another jpg file (ai1.jpg) that contain the flag and a wav file (pro.wav) that contain the protocole used to hash the passe phrase)
	2.now we will try to extract the hidden information in the ai1.jpg image using steghide tool, but first we should find the passe phrase for steghide
	3.the hashed pass phrase can be found in the image's metadata (ai1.jpg) (we can use exiftool)
	4.we can use the pro.wav file file to identify the protocole used to hash the pass phrase by using sonic-visualiser withw the spectogram feature
	4.decrypt the hash to get the pass phrase
	5.extract the hidden information in the image ( we should get a .txt file (flag.txt)
	