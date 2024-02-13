# Button Exercise

This repository serves as the basis for a new project you are asked to develop. 
It features a book list which you will improve by adding data from a public JSON source. 
The files in the repository contain several to-dos that you are expected to complete. 
This description is an overview of these to-dos. 

Your task involves handling a user interaction: when a user clicks a specific button, 
the click event should be emitted to the application wrapper, 
activating the `fetchContentAndAppendToList` function. Each button click should 
retrieve two items from the JSON source, adding them to the existing list without 
replacing any current content. This updated list is then to be displayed in the 
OtList component. The attributes that should be displayed are `name`, `seed_count` and `last_update`

During data retrieval, the button should transition into a loading state, displaying 
only a spinning icon without any text.

The data source for this project is this public endpoint https://openlibrary.org/people/george08/lists.json. 
Utilize the limit and offset query parameters to fetch only two items at a time. 
For more details on how to accomplish this, refer to the 
[Open Library API documentation](https://openlibrary.org/dev/docs/api/lists#users-lists).

## Setup Instructions
1. Clone this repository.
2. Execute `yarn install` in the repository's directory.
3. Run `yarn dev`.
