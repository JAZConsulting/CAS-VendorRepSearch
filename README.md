# CAS Vendor Rep Search
This is a pretty basic application that searches select columns within a select number of sharepoint lists. The results are returned to the user, sorted into each sharepoint list. This allows us to search for a vendor and find all information related to that vendor/manufacturer. 

## How to Install
This application is pretty easy to install:

1) Go through the installation instructions to host @gitbrent's sprLib Javascript Library Demo. 

TIP: I have included a forked version in the spRestLib folder as I still use the Demo as a sandbox for my other code. I have 2 script editors in my page with one that is minimized with a webpart containing the sprLib Demo on my deployed sharepoint app to speed up deployment and changes. It stays hidden from users unless you leave it maximized.

2) Host a legacy or Sharepoint 2013 web page on your sharepoint server; we use Sharepoint 365 which allows for using an 'old' style Sharepoint site. You can look up directions to hosting a 'legacy' Sharepoint site on Office 365.
3) Add a web part to the page; I chose a full-width Style page for best viewing
	3a) You will want to add a Script Editor into the web part; see [Image](https://github.com/JAZConsulting/CAS-VendorRepSearch/blob/master/vendor%20rep%20search/assets/images/setup-1.png).
	3b) Paste the contents of 'index.html' into the script editor and press apply/ok.
4) You should be able to see the HTML Code in your sharepoint site; see [Image](https://github.com/JAZConsulting/CAS-VendorRepSearch/blob/master/vendor%20rep%20search/assets/images/setup-2.png).

## Modifying this project
This is a pretty nice base to start from if you are looking for a similar functionality. The index file can easily be altered to support your own Sharepoint lists.Start with modifying:
* ListMaster && ReferenceMaster JSON Objects
 * * these hold quick references to your sharepoint list meta data like links to lists and list items
 * * be sure to alter/remove the callback functions and reference your own sharepoint list field names
* Commented HTML Code Tables and List Names
 * * there are 6 lists that we use; you should alter each accordion item appropriately with your own sharepoint list data. DON'T FORGET TO EDIT THE LINKS!
* Your sharepoint lists. 
 * * Because of the fact that we run this on the sharepoint server as a script, the application user's own credential will be used to access the sharepoint lists, therefore, take care to provide permissions to each user that needs access to the appropriate lists. You can even check permissions using the sprLib javascript library and decide what to display from there.

 One more big thank you to @gibrent for providing a super-sweet way to talk to sharepoint. 