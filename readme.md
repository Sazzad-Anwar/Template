<!-- PROJECT Title -->
<br />
<p align="center">
<img src="./public/images/MERN.jpg" height="150" />
  <h2 align="center"><a href="https://github.com/Sazzad-Anwar/Template">Template for any MERN stack PWA project</a></h2>
</p>

## Which npm packages and which stack has been followed in this template

### This template includes structure for `Nodejs` server as backend service and `React` as frontend/clientend service with `Redux`

#### For development purpose below npm packages have been included

1. Node Server (Backend)

    - `express`
    - `express-async-handler`
    - `axios`
    - `bcryptjs`
    - `cors`
    - `dotenv`
    - `concurrently`
    - `multer`
    - `nanoid`
    - `winston`
    - `jsonwebtoken`
    - `auth-middleware-jwt`
    - Database
        - `mysql`
        - Driver
            - `sequelize`
        - `mongoose`

2. React (Frontend /client)
    - `axios`
    - `bootstrap`
    - `nanoid`
    - `react-awesome-slider`
    - `react-bootstrap`
    - `react-dropzone`
    - `react-hook-form`
    - `react-redux`
    - `react-router-dom`
    - `react-toast-notifications`
    - `redux`
    - `redux-devtools-extension`
    - `redux-thunk`
    - `@tinymce/tinymce-react`
    - `@material-ui/pickers`
    - `@material-ui/lab`
    - `@material-ui/icons`
    - `@material-ui/core`
    - `@date-io/moment`
    - `@date-io/date-fns`
    - `workbox-background-sync`
    - `workbox-broadcast-update`
    - `workbox-cacheable-response`
    - `workbox-core`
    - `workbox-expiration`
    - `workbox-google-analytics`
    - `workbox-navigation-preload`
    - `workbox-precaching`
    - `workbox-range-requests`
    - `workbox-routing`
    - `workbox-strategies`
    - `workbox-streams`

<br />
<!-- HOW TO RUN -->

## How to install packages and run

Please follow the below instructions to run this project in your computer:

1. Clone this repository

    ```sh
    git clone https://github.com/Sazzad-Anwar/Template.git
    ```

2. Install NPM packages for node server and react with one line command

    ```sh
    yarn install-all
    ```

3. Install only node server npm packages

    ```sh
    yarn server-install
    ```

4. Install only react client npm packages

    ```sh
    yarn client-install
    ```

5. Before running the application you need to make a `.env` in `client` folder and set as below

    ```sh
    SKIP_PREFLIGHT_CHECK=true
    ```

6. Run node server and react client application with concurrently

    ```sh
    yarn dev
    ```

7. Run node server only

    ```sh
    yarn server
    ```

8. Run node react client only

    ```sh
    yarn client
    ```

9. Your node server should be available in <http://localhost:8080>
10. Your react client app should be available in <http://localhost:3000>

<br />
<br />

## Tips for JsonWebToken assigning in header

### Do not assign JWT token again and again to your request header rather follow bellow two lines of code

1. Open Postman open the request for login and select the `Tests` option

2. Write these code:

    ```sh
    var res = pm.response.json();
    pm.environment.set('token', res.token);
    ```

#### Now while requesting the authenticated API just click on `Authorization` select `Type` to `Bearer Token` then write `{{token}}` in the `Token` field on right-side
