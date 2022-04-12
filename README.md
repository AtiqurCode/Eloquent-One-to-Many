## Read One-to-Many basics & try with this code as you want

Go throw **laravel documentation** to read about it & many more blog

First you need to clone this and save **.env.example as .env** and setup your environment or just change the database configure

```sh
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your-database-name
DB_USERNAME=your-database-user-name
DB_PASSWORD=your-database-password(if have)
```

Now just run some command on terminal one by one

```sh
composer install
php artisan migrate
php artisan serve
```

As I have said this is One to Many relationship. // Imagine part
- Example1: A User can have many posts
- Example2: Student can have many Books
- Example3: Office can have many employees
- Example3: Owner can have many cars

So I have just created Two model
- **User**
- **Post**

User Model are relation with hasOne

```sh
    public function posts()
    {
        return $this->hasMany(Post::class);
    }
```

Posts Model are relation with belongsTo

```sh
    public function user()
    {
        return $this->belongsTo(User::class);
    }

    // You can save return $this->belongsTo(User::class, 'user_id'); relation column name if you didn't follow the naming convention 
```

And controller code are depend's on condition what I need. So you can got throw the controllers method.

if you have **Postman**/any software like that please import One-to-Many.postman_collection.json file either call
```sh
- {url-of-your-app}/api/users                 --method : get      // get all user list
- {url-of-your-app}/api/users/{user}          --method : get      // get one user by id with her/his posts
- {url-of-your-app}/api/users                 --method : post     // insert user details
- {url-of-your-app}/api/users/{user}          --method : put      // update user details
- {url-of-your-app}/api/users/{user}          --method : delete   // delete user and her/his posts 
- {url-of-your-app}/api/posts                 --method : get      // get all posts 
- {url-of-your-app}/api/posts/{post}          --method : get      // get one posts with user details by post_id/id
- {url-of-your-app}/api/posts/                --method : post     // create post
- {url-of-your-app}/api/posts/{post}          --method : put      // update post by post_id/id
- {url-of-your-app}/api/posts/{post}          --method : delete   // delete post by post_id/id
```
