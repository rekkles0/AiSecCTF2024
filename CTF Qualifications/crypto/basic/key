# Text
Imagine a key that shifts, like changing gears in a car, but this one dances to a classic tune named after a French cipher.

# Solution
For this challenge a file with a encrypted value is given. The file is named `key`, but the value is probably not a key but the flag... Well, going over to CyberChef and trying some base encodings (the title is *basic*, might be a hint).



```
key that shifts? 
french cipher? Omg i knew it, its vigenere ciphere.
```

A google search for `french cipher` led to a huge amount of results containing `Vignère cipher`, for instance [`here`](https://cryptii.com/pipes/vigenere-cipher), giving the information that:

> Method of encrypting alphabetic text by using a series of interwoven Caesar ciphers based on the letters of a keyword

So heading over to CyberChef again and applying `Vignère cipher`, but with what key? Guessing the name of the file could also be an hint I entered `Key` as key. The result still was encrypted. Then I used the `Magic` operator and let CyberChef take the lead. After a couple of tries the following sequence gave the hint:

```
Vigenère_Decode('Key')
From_Base32('A-Z2-7=',false)
From_Base32('A-Z2-7=',false)
From_Base64('A-Za-z0-9+/=',true,false)
From_Base32('A-Z2-7=',false)
From_Base64('A-Za-z0-9+\\-=',true,false)
From_Base32('A-Z2-7=',false)
From_Base64('A-Za-z0-9+/=',true,false)
From_Base32('A-Z2-7=',false)
From_Base32('A-Z2-7=',false)
From_Base64('A-Za-z0-9_.',true,false)

```

AisecCTF{C1ph3r_c1an_s0m3tim3s_tr1cky_t0F1nd}

