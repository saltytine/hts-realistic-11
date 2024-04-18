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
It has a post with a link to a page with all the user agents of visitors  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/4cab5c82-ccca-4ad8-a8c7-fc44b7d38557)  
And it's posted by rsmith. I used an incredible amount of deductive reasoning to figure out that he's Rich Smith, who made the site.  
You can click on his profile, and it takes you to a very simple profile page  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/f3c44a61-4d78-45ec-8279-fcb19f896787)  
Most notable is the ID  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/a723188d-c353-4cdd-8ab3-7ac268d06053)  
I looked through a few user pages before I found id=0  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/ca95bc36-9686-4c65-943c-32577c3c0f4a)  
This is a reference to a previous challenge, but it is interesting how we can change the pass  
Might be an accident idk  
So I'm gonna change the pass  
Then you put in the username and pass at the top and get in  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/c185d8f7-e22d-4034-a4f9-cd70fbd61a3c)  
There's a little mod button there, and it leads to a mod page  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/6269f770-b0b2-4f15-89d8-2fcb0620c4a4)  
I forgot what I was doing for a bit cause we're not really on the right page  
But I figured you can probably access files of the site hoster, with the right sql query  
Tried a few, but it just kept crashing  
Took a look at the page source and found this  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/944f14fc-ef9b-40a3-adc7-ea6218c166f7)  
We just have to change that so it will show the cool database we found: bs.dbase  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/2235e12b-0aa3-4bfa-9bda-48a880fd9f76)  
Now we stick in the silly little query:  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/1b65a3b6-bcbf-45f0-b933-dc13be4d1322)  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/3b148913-92ba-4795-9168-dd84309176c1)  
Yayyyy  
Now you chuck SELECT * FROM web_hosting in there and get  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/e52215e8-cecd-45cf-8c2f-192fa50be4f5)  
Now this is very nice  
Trying to sign in as space46 will tell you he was banned, but:  
I said before, when smth (usually id) is 1, its the first. And wonderdiet has that (he also has admin in his email). Now we probably have what we need for the admin pannel.  
wonderdiet; suckereveryminute  
And it works :D  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/53328ece-8955-4a07-8853-e78e97f360da)
Download looks nice but we're in the wonderdiet document area, not the space46 area  
You can see how the url is being hidden, and is only shown as the admin portal  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/bf70a298-b482-4e83-89aa-5aae6e18ddd1)  
But they did a silly thing, because clicking download shows the whole link  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/9b037b38-2ce5-4ad7-84ee-ddcd2345e814)  
So if you change that rq  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/a3fb62e5-3b6d-4115-a4e3-7e6c6e59ebd7)  
We did it :D  
![image](https://github.com/saltytine/hts-realistic-11/assets/156854448/b4eeb7be-d5ec-43aa-a093-a820d5ca07ed)
