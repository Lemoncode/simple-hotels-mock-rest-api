# Simple hotels mock rest api

A very simple local test rest-api, ideal to make quick front end examples, or to share with students.

It contains detailed information about ten hotels located in seattle (if you want to add
more entries to this local api please check the _Contributors welcome_ section).

# Why this dev local api?

Hitting real world api's is great, but when a training is on going, it can happen that 
the internet connectivity has some firewall restrictions (or even worse no internet connection available), you need an auth api key per
student, or even worse that the api has been deprecated and  your examples don't work because of that.

The goal of this project is to provide a dumb mock-data api to let trainers / students focus
on the content of their training (e.g. Front End development), and reduce the external noise going around.

If you are looking for other dumb rest-api's available online, check out:

- JSON Place holder: https://jsonplaceholder.typicode.com/
- Star wars api: https://swapi.co/

# How it works

## Getting started

If you don't have already installed nodejs you will need to install it, you can download it from this
url: https://nodejs.org/en/

Download or clone the repo.

Open the console log and install the needed packages.

```
npm install
```

Now you can run the server by running:

```
npm run mock-server
```

## Querying the API

Just open your web browser, postman or favourite tool, and type the following url's

- Get the list of hotels available:

```
http://localhost:3000/api/hotels
```

- To get the details of a given hotel (last url chunk is the id of the hotel):

```
http://localhost:3000/api/hotels/0248058a-27e4-11e6-ace6-a9876eff01b3
```

This api support sort, filtering paging... more info: [json-server](https://github.com/typicode/json-server)

- Get hotels having a rating equal to 3

```
http://localhost:3000/api/hotels/?hotelRating=3
```

- Sort list of hotels by name alphabetical order:

```
http://localhost:3000/api/hotels/?_sort=name&_order=asc
```

Load a given image from a given hotel (you can find the hotel picture path in the
_./mock-data/hotes-data.json_ file in each hotel entry under the entry _thumbNailUrl_).

```
http://localhost:3000/thumbnails/16950_158_t.jpg
```

# Contributors welcome

It would be great to get more hotels mock-data into this api, if you are keen on adding more entries
please fork this project and start adding them, you can find: 

- Hotels data in the following path:
_./mock-data/hotels-data.json_.

- Thumbnail images are stored under the following folder:
_./public/thumbnails_.

# Acknowledge

Original JSON feed extracted from this [apigee/DevJam](https://github.com/apigee/DevJam/blob/master/Resources/hotels-data.json) Github project.

Mock rest-api based on [json-server](https://github.com/typicode/json-server)

# About Basefactor + Lemoncode

We are an innovating team of Javascript experts, passionate about turning your ideas into robust products.

[Basefactor, consultancy by Lemoncode](http://www.basefactor.com) provides consultancy and coaching services.

[Lemoncode](http://lemoncode.net/services/en/#en-home) provides training services.

For the LATAM/Spanish audience we are running an Online Front End Master degree, more info: http://lemoncode.net/master-frontend
