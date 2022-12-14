DjangoListField comes with built in resolver which returns all the posts
but for graphene.List() we have to write our own resolver

```
import graphene

from graphene_django import DjangoObjectType,DjangoListField

from .models import Book

  

class BookType(DjangoObjectType):
	
	class Meta:
	
		model = Book
		
		fields = "__all__"

  

class Query(graphene.ObjectType):

all_books = graphene.List(BookType)

book = graphene.Field(BookType,book_id=graphene.Int())

  

def resolve_all_books(self,info, **kwargs):

return Book.objects.all()

def resolve_book(self,info,book_id):

return Book.objects.get(pk=book_id)
```

Changes

import graphene

from graphene_django import DjangoObjectType, DjangoListField 
from .models import Book 


class BookType(DjangoObjectType): 
    class Meta:
        model = Book
        fields = "__all__"


class Query(graphene.ObjectType):
    all_books = graphene.List(BookType)
    book = graphene.Field(BookType, book_id=graphene.Int())

    def resolve_all_books(self, info, **kwargs):
        return Book.objects.all()

    def resolve_book(self, info, book_id):
        return Book.objects.get(pk=book_id)
