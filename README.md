# This repo is to store Postman collections - pet projects for learning API testing.

## Implementation highlights:
- All CRUD operations used;
- Requests that cover functionality with and without authorization;
- Negative and positive scenarios;
- Security testing - editing or deleting other user's articles;
- Test data generation in the pre-request scripts tab - signing in, article and comment creation;
- Cleaning up after HTTP requests - test data deletion.

### Conduit
The repo currently contains 2 files - *Conduit.postman_collection.json* and *User1.postman_environment.json*.
Both files relate to the following website - *https://conduit.mate.academy*
The website is a simple platform where a user can:
- sign up, sign in and out, and edit their own profile;
- view other user's profiles;
- view, post, edit, and delete their own articles;
- view, comment, and like other user's articles.

### Collection
*Conduit.postman_collection.json* collection has folders in it, mainly:
- Signed out - for requests that don't require authorization;
- Signed in - for requests that require authorization;
  - Article - a subfolder within 'Signed in' that stores requests in corresponding folders for creating, editing, and deleting articles;
  - Comments - a subfolder within 'Signed in' that stores requests in corresponding folders for creating, editing, and deleting comments;

### Environment
All requests rely on variables from an environment - *User1.postman_environment.json*.
There is no need to use specifically the *User1.postman_environment.json* environment, you can create a brand new one with a few things to consider:
- Create a **'url'** variable with the value '**https://conduit.mate.academy**' (NOT '**https://conduit.mate.academy/**' with a **/** in the end);
- Create a **'password'** variable with any value (I used '1' for an easier sing in via the website UI).
- Other needed variables will be created during test executions.

### Running requests
1. Set your environment - import *User1.postman_environment.json* or create a new one with **url** and **password** variables;
2. Run **Sing up - myUser** and **Sing up - otherUser** to set the variables needed for other requests.
After this, all other requests should be independent from one another and can be executed at once.
3. Run any random test or folder, or the whole collection

