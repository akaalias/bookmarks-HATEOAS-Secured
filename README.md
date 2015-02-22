# Bookmarks REST + HATEOAS Implementation
A simple Spring Boot Application persisting Users and Bookmarks to a Hibernate DB and providing a RESTful, HATEOAS-enabled interface

## To run in STS:

Right-click the project folder -> Run as... -> Spring Boot App

## To run test suite:

Right-click the project folder -> Run as... -> JUnit Test

## To try it out

``` curl http://localhost:8080/jhoeller/bookmarks/4 | python -m json.tool ```

```
{
    "bookmark": {
        "description": "A description",
        "id": 4,
        "uri": "http://bookmark.com/2/dsyer"
    },
    "links": [
        {
            "href": "http://bookmark.com/2/dsyer",
            "rel": "bookmark-uri"
        },
        {
            "href": "http://localhost:8080/dsyer/bookmarks",
            "rel": "bookmarks"
        },
        {
            "href": "http://localhost:8080/dsyer/bookmarks/4",
            "rel": "self"
        }
    ]
}```