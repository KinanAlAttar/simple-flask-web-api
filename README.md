# A Simple Flask-based Web API
A simple web API implemented using Python3 and the Flask web framework.  

This is a based on the tutorial, [Creating Web APIs with Python and Flask](https://programminghistorian.org/en/lessons/creating-apis-with-python-and-flask).

# The Books.db Database
The database table `books` consists of 67 entries for each of the winners of the Hugo Award for best science fiction novel between 1953 and 2014 and consists of four columns: id, author,
published and first sentence. 

# How To Use

Using this is fairly simple, (make sure you have python3 and flask installed) all you need to do is startup the server, `python3 api.py`, and direct to, `localhost:5000`,
on your favorite web browser.

# The API
You can retrieve all the books in the database table with the request, `api/v1/resources/books/all`.

and, you can also filter out the data based on added queries on all the columns except for first sentence. For example, `/api/v1/resources/books?author=Connie+Willis`,
would return:

```
[
  {
    "author": "Connie Willis", 
    "first_sentence": "By noon Michael and Merope still hadn\u2019t returned from Stepney, and Polly was beginning to get really worried.", 
    "id": null, 
    "published": 2011, 
    "title": "Blackout, All Clear (Vol. 2 - Blackout)"
  }, 
  {
    "author": "Connie Willis", 
    "first_sentence": "There were five of us\u2014Carruthers and the new recruit and myself, and Mr. Spivens and the verger.", 
    "id": null, 
    "published": 1999, 
    "title": "To Say Nothing of the Dog"
  }, 
  {
    "author": "Connie Willis", 
    "first_sentence": "Mr. Dunworthy opened the door to the laboratory and his spectacles promptly steamed up.", 
    "id": null, 
    "published": 1993, 
    "title": "Doomsday Book"
  }
]
```
