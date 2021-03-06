# Cache middleware application for Edgeryders Discourse API

Mini application writen in NodeJS/Express that retrieves and caches data from Edgeryders Discourse API

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development purposes

### Installing

A step by step series of examples that tell you how to get a development env running

```
# install dependencies - execute the command in project root:
$ npm install

# run app in development mode:
$ npm run dev

# run app in production mode:
$ npm run prod
```
`

## Built With

* [Nodejs.js docs](https://nodejs.com/) - The NodeJS 

* [Express.js docs](https://expressjs.com/) - The NodeJS framework used to set up cache middleware app


## License

This project is licensed under the [MIT License](https://choosealicense.com/licenses/mit/) 

## NOTES

* This is minimal NodeJS/Express application writen for purposes of retrieving and caching data from Edgeryders Discourse API
* Runs on port 3001
* Exposes only one GET endpoint `/get-data` that accepts `endpoint` query parameter (pass desired Edgeryders Discourse API endpoint here)
* Example: `http://localhost:3001/get-data?endpoint=https://edgeryders.eu/t/edgeryders-culture-squad/9591`
* It accepts endpoint as query parameter, retrieves data from `https://edgeryders.eu/t/edgeryders-culture-squad/9591` in this case, caches it and retrieves data to caller

---
#### Example API call from frontend:

```
async getData() {
    const response = await $axios.get(`http://localhost:3001/get-data?endpoint=https://edgeryders.eu/tags/webcontent-culturessquad-burning`);
    
    return response.data;
}
```
