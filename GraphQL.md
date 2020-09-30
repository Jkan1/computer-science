# GraphQL

* GQL Mutation Requests - Insert/Update/Delete
* Not related with using any database

* Graph theory - (Nodes)books/items & (Lines/Edge)Relationships

* Limited Scope and exposed

* Server side GQL layer validates GQL queries

* Querry 
  * Scaler values (Constants / Static / String. Integer)
  * References complex data types used with sub-selections (not used with scaler types)

* Query calls its resolver function (same name)

* Data Types / TypeDef (Fields and Return types)

	* Imperative approach
	* Graphql and npm
  * Declarative approach
  * GraphQL SDL (Schema Definition Language) + GQL-tools - Exposable Types used in GraphQL

* One to One relation btw GQL Query and Resolver Function
* Bind them together into a GraphQL Schema using GQL-tools
* Then Execute Query against the schema

* GQL Doesn’t care how query is sent to GQL Server
* “query” is the most common root type in schema definition

* Like Old Technology - RPC (Remote Procedure Calls)

* GQL Explicit queries

* 5 Scaler Data Types in GQL - String, Integer, Float, Boolean, ID. Can create your own (custom Types)

* ! => Non Nullable Field

* Depth and Nesting should not be avoided, it does not overkill Database as it looks

* Query Params passed inside “( )”, i.e  (page : 1, first : 10)
* ! (Non Nullable) parameter means it’s Required
* Order of Params do Not Matter, As Parameters are passed By Name

* GQL is Version-less API

* GQL on client-side  with String manipulation is messy so GQL Variables are used.

* “query” -> called Operation Type (can also be provided a Operation Name )

* GQL Variables $name i.e. query Name ($name : <TYPE>) { }
* Define in Query Variables Panel

* GQL Common Fields shared btw different Types - Interface (List of Field Types)
* Other Types can implement Interfaces


* Alias used to separate same type of data : { book1 : Book(id :1) {} }

* Fragment : List of fields for a specific type (different than Interface as this is specific)

* Fragment : For Consuming API from Client 
* Interface : Modelling API on Server

* fragment  someName on Book { id title }

* Use : query BooksQuery { books { …someName } } 

* Union Types : union SearchResult = Author | Book | Review

* Inline Fragments : { … on Book { title author id}}

* Directives : include & skip
* Directives start with @
* Example : @include(if : Boolean) , @skip(if: Boolean)

* Mutation - all Queries resolver functions are called sequentially to prevent race conditions (Previously REST API were used in place of mutation)
* Example : 
  mutation AddUser{
  addUser(user:{firstName: "James", lastName:"Moore"}){
    id
    firstName
    lastName
  }
} (user is an InputType i.e Object)

* REST API response is either 100% Failure or 100% Success
* In GQL we can get Mixture of errors and results

* But if GQL Query is invalid, then GQL Validator returns error without calling any Resolver Functions
* So GQL Server could only return mixtures if Resolver functions are called.

* Case when more than one GQL query is sent to Server,  operationName property is required with the name of the query to execute.

