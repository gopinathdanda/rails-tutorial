# Steps (without MODEL and DATABASE)

1. Make project: <br/>
<pre>
	rails new Project	//make new project folder
	cd Project			//go into folder
	bundle install		//install gem files
</pre>

2. Generate CONTROLLER:<br/>
<pre>
	rails generate controller Pages		//generate controller named Pages
</pre>
Add method (e.g. home) inside PagesController class of <b>app/controllers/pages_controller.rb</b>

3. ROUTE request to CONTROLLER Methods:<br/>
Add routing line in <b>config/routes.rb</b>
<pre>
	get 'welcome' => 'pages#home'	//route request for welcome to method home in controller
</pre>

4. Create VIEW page:<br/>
Add HTML file in <b>app/views/pages/home.html.erb</b><br/>
Add CSS file in <b>app/assets/stylesheets/pages.css.scss</b>

5. Run project:<br/>
<pre>
	rails server		//start server
	rails s -p 8080		//start server on port 8080
</pre>