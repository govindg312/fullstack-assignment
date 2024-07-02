# GraphQL React Fullstack Assignment

## Application Requirements

The application has be to built entirely in TypeScript for the UI and backend. Use of types and interfaces will be evaluated. 

### UI
1. UI has to be built with React. 
2. Component library of your choice. We prefer 
3. Provide a list of all 3rd party libraries used with its justification for them.

### Backend
1. Backend has to be implemented with GraphQL
2. There is no preference on the libraries used here. Please provide a justification for them being used. 

Justifications for the libraries can be included as a section within the `readme`.

## Functional Requirements
As a user, I should be able to filter through a list of characters from Star Wars. Once I select a character, I should see below attributes:
1. name
2. birth year
3. height

I should be able to view the character's following homeworld attributes:
1. Planet Name
2. Climate 
3. Terrain

I should be able to view the character's associated film attributes:
1. Film title
2. episode ID 

I should be able to view the character's associated vehicle and starship attributes:
1. name
2. model
3. class
4. credits

The choice of components and design is up to you. We use tailwindcss in our projects, so bonus points if you can demonstrate that in the implementation.

## Technical Requirements

To meet the functional requirements, please use the following public API for star wars which is available at:

```
https://swapi.info
```

To retrieve user details, use the `/people` route.

**It is a requirement to create GraphQL queries on top of the provided API from `swapi.info`. The assignment will not be considered if you making requests directly to the public API from the UI.**

When a user selects a character (in the below example, the user has selected Luke Skywalker), this is the expected response on from the graphql query, given that all fields have been selected: 

```
{
  "name": "Luke Skywalker",
  "birthYear": "19BBY",
  "height": "172",
  "homeworld": {
    "name": "Tatooine",
    "climate": "arid",
    "terrain": "desert"
  }
  "films": [
    {
      "title": "The Phantom Menace",
      "episode": 1
    },
    {
      "title": "Attack of the Clones",
      "episode": 2
    },
    {
      "title": "Revenge of the Sith",
      "episode": 3
    },
    {
      "title": "Return of the Jedi",
      "episode": 6
    }
  ],
  "vehicles": [
    {
      "name": "Snowspeeder",
      "model": "t-47 airspeeder",
      "class": "airspeeder",
      "cost": null // since the value on the API is 'unknown' and this expects a number
    },
    {
      "name": "Imperial Speeder Bike",
      "model": "74-Z speeder bike",
      "class": "speeder",
      "cost": 8000 
    }
  ],
  "starships": [
    {
      "name": "X-wing",
      "model": "T-65 X-wing",
      "class": "Starfighter",
      "cost": 149999
    },
    {
      "name": "Imperial shuttle",
      "model": "Lambda-class T-4a shuttle",
      "class": "Armed government transport",
      "cost": 240000 
    }
  ]
}
```
When the user selects a character, the above response schema has to be retrieved within a single network call on the UI.


## Submission requirements
1. Please provide a github/gitlab url to the repository. A verbose git history would be nice to see.
2. Provide a `readme` file with setup instructions to run the application within the local environment.

### Bonus points for 
1. Unit tests
2. Linting rules applied and its compliance
3. Optimization patterns used and explained
3. Deployment on to any cloud provider of your choice


