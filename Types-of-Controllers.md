# Types of Controllers

<img src="http://s3.amazonaws.com/codecademy-content/projects/3/seven-actions.svg">

For this to work, we need to define the functions in the controller. For example, for a CONTROLLER called Messages, inside <b>app/controllers/messages_controller.rb</b>:

<pre>
	def index
		@messages = Message.all
	end
</pre>

and inside ROUTE <b>config/routes.rb</b>:

<pre>
	get '/messages' => 'messages#index'
</pre>

and inside VIEW <b>app/views/messages/index.html.erb</b>

<pre>
	<% @messages.each do |message| %>
		&lt;div class="message"&gt;
	    	&lt;p class="content"&gt;<%= message.content %>&lt;/p&gt;
	    	&lt;p class="time"&gt;<%= message.created_at %>&lt;/p&gt;
	    &lt;/div&gt;
	<% end %>
</pre>

where the DB MIGRATION <b>db/migrate/create_messages.rb</b> is:

<pre>
	class CreateMessages < ActiveRecord::Migration
	  def change
	    create_table :messages do |t|
	      t.text :content
	      t.timestamps			//creates 2 columns: created_at and updated_at
	    end
	  end
	end
</pre>

and the DB TABLE is called <b>messages</b>.