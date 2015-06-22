# Rails tutorial

## Request/Response Cycle

<img src='http://s3.amazonaws.com/codecademy-content/projects/3/request-response-cycle-dynamic.svg'>
<i>www.codecademy.com</i>

1. USER sends request to BROWSER.

2. BROWSER forwards to RAILS ROUTER.

3. RAILS ROUTER processes the request and forwards it to the CONTROLLER.

4. CONTROLLER requests data from MODEL.

5. MODEL requests the data from the DATABASE and sends back to the CONTROLLER.

6. CONTROLLER sends the data to the VIEW.

7. VIEW renders the requested HTML page and sends back to the CONTROLLER.

8. CONTROLLER compiles all the data and send back to the BROWSER.

## Steps (without MODEL and DATABASE)

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

