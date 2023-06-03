# DevNotes
Notes for trivial things

# 30/5/2023
- How to deploy laravel project

https://calebporzio.com/easy-free-serverless-laravel-with-vercel

# 2/6/2023

### Laravel

- Using php artisan make:component {{name of component}} will need manual insertion on app/{{name of component}}

it'll return "Undefined variable" if you use artisan to make component (best to add component manually)

Insert value to component

- index
```php
<x-tag :sometag="$project[0]['tags']" />
```

- tag Component
```php
dd($sometag);
```

Expected output:

"(Show value of $sometag)"

The output:

"Undefined variable of $sometag"

Reason:

" $sometag are not included on on app/tag.php "

Workaround:

- Don't use php artisan make:component to make component, instead create component manually (Chaotic Neutral)
- Add $sometag variable to app/tag.php (Lawful Neutral)

# 3/6/2023
### Flutter/Dart
The only difference between the final and const keyword is that final is a runtime-constant, which in turn means that its value can be assigned at runtime instead of the compile-time that we had for the const keyword.

### Git
##### Problem

Need to merge specific file

##### Answer

"Although not a merge per se, sometimes the entire contents of another file on another branch are needed. Jason Rudolph's blog post provides a simple way to copy files from one branch to another. Apply the technique as follows:
```git
$ git checkout branch1 # ensure in branch1 is checked out and active
$ git checkout branch2 file.py
```
Now file.py is now in branch1."
