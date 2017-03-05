---
layout: post
title: "Adapter Pattern"
date:   2017-02-28 12:15:56 -0500
categories: Notes
---

Set this on action/index.js

{% highlight javascript %}
	axios.defaults.baseURL = 'http://localhost:3000/api/v1'
	axios.defaults.headers.common['AUTHORIZATION'] = sessionStorage.getItem('jwt')
{% endhighlight %}

- Use sessionStorage to check response stores!

Set this in controller!
{% highlight ruby %}
	token = request.headers["HTTP_AUTHORIZATION"]
	If  token
		user_info = Auth.decode(token)
		@current_user ||= User.find(user_info['user_id'])
{% endhighlight %}

* new folder /adapters
	* userAdapter.js
	* export default notesAdapter = {
		fetchNotes: , loginUser: , createNote: , updateNote: , }	 
