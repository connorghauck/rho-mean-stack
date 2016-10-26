In this assignment, we were told to add "hometown" and "favorite movie" input fields to the form, which will add it to the Person object in the MongoDB.

First, I went into the index.html file and added in list items for {{person.hometown}} and {{person.movie}}. I then wrapped those in <p> tags within <li> tags. After, we needed input fields for them inside of the form, so those were added just below the Person input field. I then added ng-model ctrl.hometown and ctrl.movie in reference to the people controller.
Next, I went into the scripts/people.controller.js file and added in the hometown.controller and movie.controller to the addPerson function. This way, they would be added into the Person data via POST request from the people.js file.

In the routes/people.js file, I created variables for hometown and movie to go alongside the name variable, then made the new Person take in the req.body. This would take all of the data I added to the body of the Person object in mongo and save it. Then it would send it back out as a response.

I had, at first, forgotten to add the hometown/movie Strings to the Person in my models/person.js file. This resulted in nothing being done when I added people with the button in the HTML, because mongoose was assuming the person model was just the String of the name of the Person and none of the other strings we were creating. Once I added those in, it printed out perfectly fine.
