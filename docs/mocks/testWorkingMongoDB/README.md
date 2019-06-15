﻿## Getting Started

In the root directory of the project...

1. Install flask `pip install Flask`
2. Install dotenv `pip install python-dotenv`
3. Install azure-cosmos module `pip install pymongo`
4. Install bson modules `pip install bson`
5. Install node modules `yarn install` or `npm install`.
6. Start development server `yarn start` or `npm start`.

## Next Steps

### Sample Data

Replace the sample data stored in /server/sampleData.js.
Replace the default images stored in /src/images.

### Adding a New Page

1. Create a folder in `/src/components` with your react components.
2. Add a route for your page to `/src/App.js`.
3. Add a button to the navigation bar in `/src/components/NavBar/index.js`.

### Cosmos Database

**Do Not share the keys stored in the .env file publicly.**
The Cosmos database will take approximately 5 minutes to deploy. Upon completion of deployment,
a notification will appear in VS Code and your connection string will be automatically added
the .env file. The schema and operations for the Cosmos database are defined in `/server` folder.
Additional documentation can be found here: [Cosmos Docs](https://github.com/Microsoft/WebTemplateStudio/blob/dev/docs/services/azure-cosmos.md).

### Deployment

The generated templates can be deployed to Azure App Service using the following steps:

1. In the root directory of the project `yarn build` or `npm build` to create a build folder.
2. Move the build folder inside the server folder.
3. Deploy the server folder to Azure App Service using the [Azure App Service Extension](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azureappservice).
4. If a database is used, add the environment variables defined in .env to your Application Settings.
5. Consider adding authentication and securing back-end API's by following [Azure App Service Security](https://docs.microsoft.com/en-us/azure/app-service/overview-security).
   Full documentation for deployment to Azure App Service can be found here: [Deployment Docs](https://github.com/Microsoft/WebTemplateStudio/blob/dev/docs/deployment.md).

## File Structure

The front-end is based on [create-react-app](https://github.com/facebook/create-react-app).

The back-end is based on [Flask](https://github.com/pallets/flask).

The front-end is served on http://localhost:3000/ and the back-end on http://localhost:3001/.

```
.
├── server/ - Flask server that provides API routes and serves front-end
│ ├── createdDB.py - Handles connection with the cosmos database
│ ├── server.py - Handles API calls for routes
│ ├── sampleData.py - Contains all sample text data for generate pages
│ ├── constants.py - Defines the constants for the endpoints and port
│ └── settings.py - Enable access to environment variables
├── src - React front-end
│ ├── components - React components for each page
│ ├── App.jsx - React routing
│ └── index.jsx - React root component
├── .env - API Keys
└── README.md
```

## Additional Documentation

- React - https://reactjs.org/
- React Router - https://reacttraining.com/react-router/

- Bootstrap CSS - https://getbootstrap.com/
- Flask - http://flask.pocoo.org/

* Cosmos DB - https://docs.microsoft.com/en-us/azure/cosmos-db/create-mongodb-flask

  This project was created using [Microsoft Web Template Studio](https://github.com/Microsoft/WebTemplateStudio).
