# README

This is a Pinterest-clone following the tutorial by [Mackenzie Child](https://mackenziechild.me/) in his
[12-apps-in-12-weeks](https://mackenziechild.me/12-in-12/) series.  
* The video for the tutorial is located here: [Week 11: How To Build A Notebook App With Rails 4](https://mackenziechild.me/12-in-12/11/)
* Mackenzie's GitHub repo for this project is here: [notenote](https://github.com/mackenziechild/notenote)


####Things to look up later


#### CM Comments


#### ~39:14
* If I want different roots for signed in and non-signed in users, I can do the following:
```ruby
	# routes.rb
authenticated :user do
	root 'notes#index', as: "authenticated_root"  	
end

root 'welcome#index'
```

* I can't get the welcome image to come through
  * "SOLVED": So I try to add the images one at a time but that didn't work for some reason.  Once I added the second image,
	which was the callouts background, they both came through.
* Note submission styling.  I need to look into the simple_format method because it actually recognizes new lines and other pieces that it normally wouldn't pick up
```haml
%p= simple_format(@note.content)
```
