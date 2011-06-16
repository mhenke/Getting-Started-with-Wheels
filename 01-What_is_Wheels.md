## *What is Wheels?*

Wheels is a ColdFusion framework using object oriented processes while
not forcing you to know oo. It does this by guiding you into writing
more maintainable and reusable code. Wheels is not a direct port of Ruby
on Rails (RoR).

### Wheels Philosophies

Wheels philosophies include:

Simplicity
- Full Stack
- Object Relational Mapping

Convention Over Configuration
Model-View-Controller
Object Relational Mapping

#### Simplicity

The simplicity of Wheels is a major reason I have become a fan. The
simplicity derives from convention over configuration. You follow the
conventions and you are golden. If you need to override a convention,
you can. The model objects have no getters or setters, another
simplicity feature. The properties are attached to the object in the
THIS scope. To get a column you would use #myModelObject.myColumn#.
There are no XML configuration files which keeps Wheels simple. One
simplicity feature is Wheels is one cohesive solution called a "Full
Stack" framework.

##### Full Stack

"Full stack" incorporates multiple features for developers into one
cohesive, fully functional solution. Per Djumner
http://cfwheels.org/user/profile/2, former lead developer for Wheels,
describes this as Wheels is "meant to be used without needing any other
frameworks. Compared with other ColdFusion frameworks where it's more
expected the developer will use some other framework" like Transfer for
Object Relation Mapping and ColdSpring for Inversion of control (IoC).
Wheels "full stack" includes validation, caching, and an Object
Relational Mapping solution.

##### Object Relational Mapping

The Object Relational Mapping (ORM) in Wheels will reduce the need to
create repetitive, basic SQL statements. Wheels implements the Active
Record design pattern to accomplish this. One detail of Active Record is
the database defines your model objects. Your model object will have
classes to interact with the data. With Active Record, encapsulation
occurs by hiding the SQL statement but not the data structure.

 You may have heard a lot about ORMs recently with Adobe ColdFusion 9
integrating Hibernate. The problem an ORM is trying to solve is
converting two incompatible data types: your relational database and
object-oriented code. Think of squares trying to fit into circles. The
ORM solves this problem. Hibernate takes a slightly different approach
from Wheels. Hiberate uses the Data Mapper design pattern. For more
information on different approaches to access data, readAdobe ColdFusion
Anthology Chapter 21 "Beans and DAOs and Gateways, Oh My!" by Sean
Corfield.

#### Convention Over Configuration

Sensible defaults are important to Wheels. I use sensible defaults and
convention over configuration (CoC) interchangeably. CoC is a software
design idea. CoC allows the developer to focus on coding instead of
worrying about for mapping between a functions, a databases and URL
requests. The developer only needs to configure the extraordinary, not
the ordinary. CoC decreases the number of decisions, while increasing
simplicity and maintaining flexibility.

I describe CoC with this story. In the mornings, I have a bacon, egg,
and cheese croissant sandwich with a coffee. I walk into the cafe and
when the cook sees me, we nod at each other. I grab my coffee and at the
cash register, my sandwich is waiting for me. We are using CoC. The cook
assumes I want my ordinary order, if I wanted something extraordinary I
would have to say so. Some conventions are based on how Wheels is
orgainized using the Model-View-Controller (MVC) architecture.

#### Model-View-Controller

MVC architecture purpose is organizing your code and promoting
simplicity. It should be clear where different types of code belong. In
Wheels, the file and folder structure should be very intuitive. Models
go in the models folder, Views go in the views folder and so on. Another
goal of MVC is promoting DRY (Don't Repeat Yourself) code.

Here is a simple explanation for each piece of MVC.

##### Model

The model is the data. In Wheels, a CFC in the models folder represents
a table in your database.

##### View

The view is what is presented to the user. It could be HTML, XML, JSON,
or other forms of content. In Wheels, the views will be a cfm file.

##### Controller

The controller is the brains of your Wheels application. It tells the
application what to get, what to do with it, and how to give it to the
user. In Wheels, the controller will be a CFC located in the controllers
folder.

As you read, Wheels borrows philosophies from RoR and implements them
in ColdFusion friendly, simple ways. Wheels coding and flow should not
be much different then when you first learned CFML from Ben Forta's
books. Wheels will guides you to better, more maintainable code. Let's
create a Wheels applications.