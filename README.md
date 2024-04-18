# a silly lil writeup of hts realistic 11
pretty fun one  

The lil blurb that tells us what to do
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/d2ac04c7-be8b-4310-a530-e2bb19bdf958)

This is the main page  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/40eba16b-766a-4d0a-9e05-7121ff56a6b1)  
Where there are 5 other pages:  
Features
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/bcc5af4f-09d7-4772-a59a-69cb5b791257)  
FAQ  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/bcf29616-38b2-409d-b160-485bc0e54d63)  
Terms of Service  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/d8fddb83-cade-4c8a-b0b9-41d5fb71aec0)  
Pricing (had to zoom out for this one)  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/416375cd-0dc1-4ef0-877c-fc8272a67e41)  
And WebMail  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/b91c5259-a952-485a-98a6-facc09456cad)  
In the search bar though, it says pl  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/11b26732-e0af-4bf9-b1aa-1f8c9e1447f7)  
Which is pearl, meaning its running on a linux box.
Just have to get the list of shit in it's directory. It wasn't working but with the magic of google I learned you gotta add these: |  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/ae80f9a7-3df9-4052-9c8a-9297d9ed8a9b)  
Which shows us  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/c8a85952-4eab-4f9c-95f1-f915fae2074e)  
There are a bunch of silly things here  
There's admin, which is always nice and there's client_http_docs which is probably the websites that are being hosted  
I also see a database file, bs.dbase which might be helpful  
I looked at client_http_docs first, bc my goal is to recover space's files  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/03c3fd20-c0ad-4c7a-a035-a31360757c89)  
Unfortunately, clicking on space's account leads to a page that says  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/8123e52f-9246-4330-88c5-5486886e2a3e)  
Trying to get the file from the page doesn't work either :(  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/b0f51e40-f727-4f2e-b3b3-34b3434a43ae)  
Next thing I did was try to login to the admin pannel  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/d0f0d10b-5869-432c-bdcb-8c74d43fdd83)  
Tried a few things here, no sql injections work or anything  
Got stumped and even went through the other things listed with the ls command  
Then I looked back at client_http_docs and looked through the other pages  
I played around with wonderdiet's ordering page but didn't really find anything  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/d659328b-901f-40ef-bf7d-a9a9ba1b1350)  
Then I looked at the right way radio website  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/123369ac-1d19-4d4b-a014-3be79b295260)  
