# React Hook REST API - GET and POST :star::star::star::star::star:

### How to Load Data from a REST API with React Hooks

With React Hooks there is another way to get data into your app. Finally we can have stateful logic in functional components – which allows us to have functional components as “containers”. If we now want a component to load data at mount, we don’t need a class component anymore. At least not just because we need state or lifecycle. Two Hooks make that possible: useState allows us to add state functionality to our component. and useEffect gives us the possibility to perform so called side effects like fetching data asynchronously.

### Install and Run
In the root:
```
sudo yarn install
yarn start
```
### With GET
```javascript
useEffect(() => {
     axios
     .get("https://jsonplaceholder.typicode.com/users")
     .then(result => setData(result.data));
}, []);
```
### With POST
```javascript
useEffect(() => {
     const params = {"general_params": {"service":["instagram"]}, "influencer_only_params":{"minimum_followers": 100000, "maximum_followers": 100000000}};
     axios.post(`https://es-staging.bm3.elife.com.br/influencers.json?key=zAtAmexezeqaTRaGapHEc4TaDaZESEsT`,  
     {params} )
     .then(result => {setData(result.data); console.log(result.data)});
}, []);
```

### Please leave a star :) 
:star::star::star::star::star:

Create by [RonnyldoSilva](https://github.com/RonnyldoSilva)
