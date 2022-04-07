<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains over 2000 video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Read One-to-Many basics & try with this code as you want

Go throw **laravel documentation** to read about it & many more blog

First you need to clone this and save **.env.example as .env** and setup your environment or just change the database configure

```sh
- DB_CONNECTION=mysql
- DB_HOST=127.0.0.1
- DB_PORT=3306
- DB_DATABASE=your-database-name
- DB_USERNAME=your-database-user-name
- DB_PASSWORD=your-database-password(if have)
```

Now just run some command on terminal one by one

```sh
composer install
php artisan migrate
php artisan serve
```

As I have said this is One to One relationship. // Imagine part
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

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the Laravel [Patreon page](https://patreon.com/taylorotwell).

### Premium Partners

- **[Vehikl](https://vehikl.com/)**
- **[Tighten Co.](https://tighten.co)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Cubet Techno Labs](https://cubettech.com)**
- **[Cyber-Duck](https://cyber-duck.co.uk)**
- **[Many](https://www.many.co.uk)**
- **[Webdock, Fast VPS Hosting](https://www.webdock.io/en)**
- **[DevSquad](https://devsquad.com)**
- **[Curotec](https://www.curotec.com/services/technologies/laravel/)**
- **[OP.GG](https://op.gg)**
- **[WebReinvent](https://webreinvent.com/?utm_source=laravel&utm_medium=github&utm_campaign=patreon-sponsors)**
- **[Lendio](https://lendio.com)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
<<<<<<< HEAD
=======

## Read One-to-Many basics & try with this code as you want

Go throw **laravel documentation** to read about it & many more blog

First you need to clone this and save **.env.example as .env** and setup your environment or just change the database configure

```sh
- DB_CONNECTION=mysql
- DB_HOST=127.0.0.1
- DB_PORT=3306
- DB_DATABASE=your-database-name
- DB_USERNAME=your-database-user-name
- DB_PASSWORD=your-database-password(if have)
```

Now just run some command on terminal one by one

```sh
composer install
php artisan migrate
php artisan serve
```

As I have said this is One to Many relationship. // Imagine part
- Example1: A User can many posts
- Example2: Student can have many Books
- Example3: Office can have many employees
- Example3: Owner can have many cars

So I have just created Two model
- **User**
- **Post**

User Model are relation with hasMany

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

And controller code are depend's on condition what I need. So you can got throw the controller method.

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
>>>>>>> c723723bcd7918c7330091f679ee5612de9e6b04
