
## Rails file structure

The Ruby on Rails file structure is designed to follow the MVC (Model-View-Controller) architecture, making it easy to navigate and organize code. Here's a brief description of key directories:

- `app/:` Contains the core components of the application:
    - `models/:` Business logic and data management (database).
    - `views/:` HTML templates to display data.
    - `controllers/:` Control the flow of data between models and views.
    - `helpers/:` Utility functions for views.
    - `assets/:` JavaScript, CSS, and images.
- `config/:` Configuration settings for routes, database, and environment-specific setups.
- `db/:` Database-related files, including migrations and seeds.
- `lib/:` Custom libraries and modules.
- `public/:` Static files like HTML, images, and other public assets.
- `test/:` Test files for models, controllers, and features.
- `Gemfile:` Defines the gems (libraries) your application uses.


## Create Model
Create a Model named `BlogPost`
```code 
rails generate BlogPost title:string body:text
```

Migrate the database
```code 
rails db:migrate
```

Create a blog item 
```code
 BlogPost.create(title:"First Blog", body:"This is the very first blog of this project")
```
Find items with its `id`
```code
 BlogPost.find(1)
```
To update record. We have to first find the record with it's id and store as an object variable. Then call update() function with this object.
```code
blog = BlogPost.find(1)
blog.update(title:"New Title")
```
To delete the object 
```code
blog = BlogPost.find(1)
blog.destroy()
```



