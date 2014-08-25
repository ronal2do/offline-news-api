# offline-news-api [![Build Status](https://travis-ci.org/matthew-andrews/offline-news-api.svg?branch=master)](https://travis-ci.org/matthew-andrews/offline-news-api)

Simple RESTful API that allows you to get news either item by item or as an array of items.

## Install and run

```
git clone git@github.com:matthew-andrews/offline-news-api.git
cd offline-news-api
npm install
node index.js
```

## Documentation

### GET /stories

Returns an array of story objects - [see **GET /stories/:guid** for documentation on story objects](#get-storiesguid).

```
curl https://offline-news-api.herokuapp.com/stories
```

### GET /stories/:guid

Returns a story object with given guid.

```
curl https://offline-news-api.herokuapp.com/stories/http://blogs.ft.com/tech-blog/?p=248891
```

Property | Type      | Description
-------- | --------- | -----------------------------
guid     | string    | Unique identifier, also a URL
author   | string    | Author of the story
title    | string    | Title, usually the headline
body     | string    | Story body
date     | timestamp | Publish date 
