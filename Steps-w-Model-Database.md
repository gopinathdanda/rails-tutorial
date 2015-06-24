# Steps (with MODEL and DATABASE)

1. In addition to the above steps, generate a new MODEL:
<pre>
	rails generate model Message
</pre>
This creates
a. Model file: app/models/message.rb
b. Migration file: db/migrate (to update DB)

2. Change database structure in <b>db/migrate</b>:
<pre>
	def change			//what to change in DB
		create_table :messages do |t|
			t.text :content		//text column called content
	      	t.timestamps		//timestamp columns called created_at and updated_at
		end
	end
</pre>

3. Update DB:
<pre>
	rake db:migrate
</pre>

4. Seed DB with default values:
<pre>
	rake db:seed
</pre>