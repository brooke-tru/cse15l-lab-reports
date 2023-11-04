# `StringServer` code
![string-server-code](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/13d8814a-a28a-41c9-a9b4-9c328c743138)

# Part 1
# `/add-message` Example 1
![add-message1](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/30b31aad-fb5d-4206-9861-b42f6c4bfd8e)
* Which methods in your code are called? `public String handleRequest(URI url)`
* What are the relevant arguments to those methods, and the values of any relevant fields of the class? The argument in the method is URI url. The values I have are String s and URI url.
* How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why. Changing url can do a few different things depending on what request was made. Starting with the path, `/add-message?s=My name is Brooke` the string "My name is Brooke" gets added and assigned to the variable s in my code. Depending on what comes after the '=' is what gets added and assigned to `s`, and adding "My name is Brooke" shows how `s` was changed. If I attempt to call `/add-message?s=` I get a 404 Not Found message because I didn't give a string to be added, hence the name of the path `/add`. I can completely take away the path and it will just continue to show the contents of String s on the page. 

# `/add-message` Example 2
![add-message2](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/bed9c5f3-40bf-4669-8288-84014c0e9e2a)
* Which methods in your code are called? `public String handleRequest(URI url)`
* What are the relevant arguments to those methods, and the values of any relevant fields of the class? The argument in the method is URI url. The values I have are String s and URI url.
* How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why. Changing url can do a few different things depending on what request was made. Starting with the path, `/add-message?s=Stream and stan ATEEZ` the string "Stream and stan ATEEZ" gets added and assigned to the variable s in my code. Then it is displayed to the page. Depending on what comes after the '=' is what gets added and assigned to `s`, and the example with "Stream and stan ATEEZ" shows how s was changed. If I attempt to call `/add-message?s=` I get a 404 Not Found message because I didn't give a string to be added, hence the name of the path /add. I can completely take away the path and it will just continue to show the contents of String s on the page.

---
# Part 2
* The path to the private key for your SSH key for logging into ieng6 (on your computer or on the home directory of the lab computer)
![ls private key](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/45825a07-248b-4f1c-a639-65f47ff8372f)

* The path to the public key for your SSH key for logging into ieng6 (within your account on ieng6)
* The path to the public key for my SSH key is `/.ssh/authorized_keys`.
![ls public key](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/bd90ff8a-82d0-40b6-924b-1b9532a19364)

* A terminal interaction where you log into ieng6 with your course-specific account without being asked for a password.
![ssh without pass](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/e1d353d0-5a43-4bb8-8214-74aa828ca551)

--- 
# Part 3
* In a couple of sentences, describe something you learned from lab in week 2 or 3 that you didn’t know before. I learned many things from weeks 2 and 3 of lab, but I think the most interesting is URL's because of the paths, queries, and fragments. For example, if I want to search Lana Del Rey on Google, I simply use the Google domain, search path, and Lana Del Rey as the query. When put all of those elements together into `https://google.com/search?q=Lana Del Rey` and hit enter, I get images, articles, and lists of websites about Lana Del Rey! I could simply change my search from Lana Del Rey to Ariana Grande by changing the query which is pretty cool. By implementing this change, I get the google search results for Ariana Grande instead of Lana Del Rey. 
