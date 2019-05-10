# Project Format(To be done primarily)

**Decide between MongoDB or MySQL**

### Todo
* Create a project directory and cd into it
* run "npm init"
* run "npm install express --save"


## ===========BACKEND RESPONSIBILITY===============

## Root directory
### app.js
* import: (express, passport_config, mongoose, keys, path, bodyparser, cookieparser, express session)
* install ejs
* app.set(‘views’)
* app.use(passport.initialize())
* app.use(passport.session())
* app.set(‘port’, (process.env.PORT || 3000)

## models directory
### User.js
* import: (mongoose, bcrypt)
* createUser	=> use bcrypt for hashing the password
* getUserByUsername
* getUserById
* comparePassword
* export UserSchema as mongoose.model(‘user’, userSchema)

## config directory
### keys.js
* keys for db
* key for cookie session
* export keys
### passport.js
* import: (passport, passport-local, (google or facebook), keys, userModel)
* passport.use(both LocalStrategy and either Google or Facebook 	strategy)
* passport.serializeUser
* passport.deserializeUser

## routes directory
### auth.js
* import: (express, passport)
* app.get(‘/login’)
* app.post(‘/login’)
* app.get(‘/register’)
* app.post(‘/register’)
* export the router

## ============FRONTEND RESPONSIBILITY============

## views directory
* **Either in html or ejs**
* **Consider using Bootstrap as it makes things much easier to design**
### home.html
* contains template for homepage
* could be redirected to login or register page
*    => a href="/login" /a
*    => a href="/register" /a
* possibly add profile page?
### login.html
* form for login information
*   => form action="/login" /form
* **might contain Google or Facebook login buttons**
### register.html
* form for register information
*   => form action="/register /form
