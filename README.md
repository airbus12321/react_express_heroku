# React-Node-Heroku

React-Node-Heroku is for deploying react, express project to heroku

### Create Client

- create-react-app client
- npm run build

### Create Server

- npx express-generator server

### Deployment

- Cut and paste buidl directory from client to server
- Update app.js like this:

>....
>app.use(express.static(path.join(__dirname, 'build')));
>app.get('/*', (req, res) => {
>   res.sendFile(path.join(__dirname, 'build', 'index.html'));
>});
>....


- Create new app in heroku dashboard with react-node name
- Run the the following commands one by one.
$ git init
$ git add .
$ git commit -m "first commmit"
$ heroku git:remote -a react-node
$ git push heroku master
$ heroku open
$ heroku ps:restart; heroku logs --tail

