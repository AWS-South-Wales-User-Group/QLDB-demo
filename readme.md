# QLDB-demo

This is a demo application that will be built up to showcase a React UI front end communicating with a backend comprising of various AWS services including QLDB.

This initial release includes a React UI that uses Amplify to integrate with AWS Cognito for sign up and sign out.

### Frontend

The frontend was created initially with the following command:

`npx create-react-app frontend`

It integrates a CSS preprocessor which is installed as follows:

`npm install node-sass`

It also uses `react-bootstrap` as a complete re-implementation of the Bootstrap components using React. To allow customising the Bootstrap Sass files vanilla bootstrap is installed as well.

`npm install react-bootstrap bootstrap`
 

### Backend

The backend uses the serverless framework and was created with the following command:

`sls create --template aws-nodejs --path backend`

It creates a Cognito user pool configured to verify a new user's email address, and a Cognito user pool client.

It uses the `aws-amplify-exports-serverless-plugin` to generate the appropriate configuration files for using AWS Amplify with the Serverless Framework.


### Running the Demo

To run the demo, you need to first deploy the backend, by navigating to the backend directory and running the following:

`sls deploy`

This will generate the required `aws-export.js` file in the frontend directory. Next navigate to the frontend directory and start up the development server using:

`npm start`

