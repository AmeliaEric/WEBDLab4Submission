# Ruby-On-Rails CRUD

Here's a step-by-step guide on how to create a simple CRUD app using Ruby on Rails along with some CSS styling.

**Prerequisites:**
- Ruby on Rails installed on your system.
- Basic knowledge of Ruby and Rails.

**Step 1: Create a New Rails Application**

Open your terminal and run the following command to create a new Rails application:

```bash
rails new crud_app
```

Navigate to the project directory:

```bash
cd crud_app
```

**Step 2: Generate a Scaffold**

In Rails, you can use scaffolding to quickly generate the code for a CRUD application. For this example, let's create a simple CRUD app for managing tasks. Run the following command to generate a scaffold:

```bash
rails generate scaffold Task name:string description:text
```

This command generates a model, controller, views, and a database migration for the "Task" resource, which has a name and description.

**Step 3: Run Migrations**

Run the database migration to create the "tasks" table:

```bash
rails db:migrate
```

**Step 4: Set a Root Route**

Open the `config/routes.rb` file and set the root route to the tasks index:

```ruby
root 'tasks#index'
```

**Step 5: Generate Some Sample Data**

You can generate some sample data for your application by running the Rails console:

```bash
rails console
```

Then, create a few tasks to populate the database:

```ruby
Task.create(name: "Task 1", description: "Description for Task 1")
Task.create(name: "Task 2", description: "Description for Task 2")
```

**Step 6: Add Some Styling with CSS**

You can add CSS to your Rails application by creating a CSS file and linking it to your views.

1. Create a new CSS file in the `app/assets/stylesheets` directory. You can name it something like `application.css`:

   ```css
   /* app/assets/stylesheets/application.css */

   /* Add your CSS styles here */
   body {
     font-family: Arial, sans-serif;
     background-color: #f0f0f0;
     margin: 0;
     padding: 0;
   }

   header {
     background-color: #333;
     color: #fff;
     text-align: center;
     padding: 10px;
   }

   .container {
     margin: 20px;
     padding: 20px;
     background-color: #fff;
     border-radius: 5px;
     box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
   }

   /* Add more styles as needed */
   ```

**Step 7: Start the Server**

Now, start the Rails server:

```bash
rails server
```

Visit `http://localhost:3000` in your browser to see your CRUD application with basic CSS styling.
