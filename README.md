# django_interview_questions
#### Difference between Flask and Django?

| Comparison Factor     | Django    | Flask   |
| :------------- | :----------: | :----------- |
|  Project Type | Supports Large Projects| Built for smaller projects |
| Templates,Admin, ORM  | Built in  | Needs to be installed |
| Flexibility  | Allows complete web development without the need for third-party tools| More flexible as the user can select any third-party tools according to their choice and requirements |
| Visual Debugging |	Does not support Visual Debug	| Supports Visual Debug |
| Type of framework |	Batteries included |	Simple, lightweight |
|Bootstrapping-tool |	Built-it|	Not available | 
<br>
Nb: Batteries are libraries and tools that are required for common use cases and ORM is the object relational mapping layer which is used to interact with other relational databases.<br>

#### What is  Django?
Django is a Python-based free and open-source web framework that follows the model-template-view architectural pattern.It was also named after Django Reinhardt who was a jazz guitarist from the 1930s.<br>

#### Which companies use Django?
Pinterest, Instagram, Coursera, Udemy, Spotify, Youtube, Bitbucket, Mozilla,Eventbrite, Dropbox [others](https://stackshare.io/django)<br>

#### What are the features of Django?
SEO Optimized -as from the name it means that adding your website to the search engine such that it appears in the top results. This is because Django maintains the built website through URLs rather than the IP addresses on the server, which makes it easy for SEO engineers to add the website to the server while the web-developer doesn’t have to convert the URL into some numeric code.<br>
Rapid Development -Django was designed with the intention to make a framework which takes less time to build web application. The project implementation phase is takes time  but Django creates it rapidly.<br>
Fully loaded framework -Django includes various helping task modules and libraries which can be used to handle common Web development tasks. Django takes care of user authentication, content administration, site maps, RSS feeds etc.<br>
High security -thereby helping developers avoid common security mistakes such as cross-site request forgery (csrf), clickjacking, cross-site scripting, etc
It is exceptionally scalable which in turn helps meet the heaviest traffic demands<br>
Versatile -The logical project structure and MVT architecture of Django provides us with a solid foundation which can then be used to make whichever application we want to create.<br>
Scalability -Django is scalable in nature and has ability to quickly and flexibly switch from small to large scale application project.<br>

#### How do you check the Django version installed in a PC?
Open CMD command prompt and type python -m django --version <br> 
You can also try to import Django and use the get_version() method as follows:<br>
```python
import django
print(django.get_version())
```
#### What are the advantages of using Django?
Django is called a loosely coupled framework because of its Model View Template architecture. It helps in separating the server code from the client-related code. <br>
Django’s models and views take care of the code that needs to be run on the server like getting records from database, etc., and the templates are mostly HTML and CSS that just need data from models passed in by the views to render them. Since these components are independent of each other, Django is called a loosely coupled framework.<br>
Allows rapid development of websites.<br>
Follows the DRY or the Don’t Repeat Yourself Principle which means, one concept or a piece of data should live in just one place.<br>
Consistent at low as well as high levels.<br>
SQL statements are not executed too many times and are optimized internally.<br>
Can easily drop into raw SQL whenever required.<br>
Flexibility while using URL’s.<br>

#### Explain Django architecture? 
Django follows the MVT (Model View Template architecture) which is based on the MVC (Model View Controller architecture). The main difference between these two is that Django itself takes care of the controller part.<br>
<img src="https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2019/10/mvt.png">
<br>
MVT separates the code into three parts.<br>
Model, View, and Template. <br>
The Model contains the system responsible for dealing with data and databases; <br>
View deals with the design pattern; that is, it decides what data should be displayed, <br>
Template specifies a structure for output.<br>
Data can be populated in a template using placeholders. It defines how the information is presented. An example is a Generic list view that we can use to display a set of records from the database. <br>

#### Give a brief about "django-admin"?
django-admin is the command-line utility of Django for administrative tasks. Using the django-admin you can perform a number of tasks as shown below:<br>
| Task   | Command |
| :------------- | :---------- |
| To display the usage information and the list of the commands provided by each application | django-admin help |
| To display the list of available commands | django-admin help –command |
| To display the description of a given command and the list of its available options | django-admin help <command> |
| Determining the version of Django | django-admin version |
| Creating new migrations based on the changes made in models | django-admin makemigrations |
| Synchronizing the database state with the current set of models and migrations | django-admin migrate |
| Starting the development server | django-admin runserver |
| Sending a test email in order to confirm the email sending through Django is working | django-admin sendtestemail |
| To start the Python interactive interpreter | django-admin shell |
| To show all the migrations in your project | django-admin showmigrations |
<br>

#### How do you connect your django project to the database?
Django comes with a default database which is SQLite. <br>
To connect your project to this database, use the following commands:<br>
```python manage.py migrate ``` (migrate command looks at the INSTALLED_APPS settings and creates database tables accordingly) <br>
```python manage.py makemigrations``` (tells Django you have created/ changed your models)<br>
```python manage.py sqlmigrate <name of the app followed by the generated id>``` (sqlmigrate takes the migration names and returns their SQL)<br>

#### What are the various files that are created when you create a Django Project? Explain briefly.
After you create a project using the startproject command, the following files will be created: <br>
| File Name  | Description |
| :------------- | :---------- |
| manage.py | A command-line utility that allows you to interact with your Django project |
| __init__.py | An empty file that tells Python that the current directory should be considered as a Python package |
| settings.py | Consists of the settings for the current project |
| urls.py | Contains the URL’s for the current project |
| wsgi.py | This is an entry-point for the web servers to serve the project you have created |
<br>

#### What are ‘Models’?
Models are a single and definitive source for information about your data. It consists of all the essential fields and behaviors of the data you have stored. Often, each model will map to a single specific database table. <br>
In Django, models serve as the abstraction layer that is used for structuring and manipulating your data. <br> 
Django models are a subclass of the ```django.db.models.Model``` class and the attributes in the models represent database fields. <br>

#### What are ‘views’?
Django views serve the purpose of encapsulation.<br>
They encapsulate the logic liable for processing a user’s request and for returning the response back to the user.<br> 
Views in Django either return an HttpResponse or raise an exception such as Http404.<br> 
HttpResponse contains the objects that consist of the content that is to be rendered to the user. Views can also be used to perform tasks such as read records from the database, delegate to the templates, generate a PDF file, etc.<br>

#### What are ‘templates’?
Django’s template layer renders the information to be presented to the user in a designer-friendly format. <br>
Using templates, you can generate HTML dynamically. The HTML consists of both static as well as dynamic parts of the content. You can have any number of templates depending on the requirement of your project. It is also fine to have none of them.<br>
Django has its own template system called the Django template language (DTL). Regardless of the backend, you can also load and render templates using Django’s standard admin.<br>

#### What is the difference between a Project and an App?
An app is basically a Web Application that is created to do something for example, a database of student records. A project, on the other hand, is a collection of apps of some particular website. Therefore, a single project can consist of ‘n’ number of apps and a single app can be in multiple projects. <br>

#### What are the different inheritance styles in Django?
Django has three possible inheritance styles:<br>
| Inheritance style | 	Description |
| :------------- | :---------- |
| Abstract base classes | Used when you want to use the parent class to hold information that you don’t want to type for each child model. Here, the parent class is never used in solitude |
| Multi-table inheritance | Used when you have to subclass an existing model and want each model to have its own database table |
| Proxy models | Used if you only want to modify the Python-level behavior of a model, without changing the ‘models’ fields in any way |
<br>

#### What are static files?
Static files in Django are those files that serve the purpose of additional files such as the CSS, images or JavaScript files. These files are managed by ```django.contrib.staticfiles```. These files are created within the project app directory by creating a subdirectory named as static. <br>

#### What are ‘signals’?
Django includes a “signal dispatcher” which helps allow decoupled applications get notified when actions occur elsewhere in the framework.<br>
Signals allow certain senders to notify a set of receivers that some action has taken place. They’re especially useful when many pieces of code may be interested in the same events.<br>
Some of the signals are as follows:
| Signal	| Description |
| :-------- | :------- |
| django.db.models.signals.pre_save   django.db.models.signals.post_save | Sent before or after a model’s save() method is called |
| django.db.models.signals.pre_delete  django.db.models.signals.post_delete |Sent before or after a model’s delete() method or queryset’s delete() method is called |
| django.db.models.signals.m2m_changed | Sent when a ManyToManyField on a model is changed.|
| django.core.signals.request_started  django.core.signals.request_finished | Sent when Django starts or finishes an HTTP request.|
<br>

#### Briefly explain Django Field Class.
‘Field’ is basically an abstract class that actually represents a column in the database table. <br>
The Field class, is in turn, a subclass of  RegisterLookupMixin. In Django, these fields are used to create database tables (db_type()) which are used to map Python types to the database using ```get_prep_value()``` and vice versa using ```from_db_value()``` method. Therefore, fields are fundamental pieces in different Django APIs such as models and querysets.

####  How do you create a Django project?
To create a Django project, cd into the directory where you would like to create your project and type the following command:<br>
```django-admin startproject Vee ```
NOTE: Here, Vee is the name of the project. You can give any name that you desire.<br>

#### What is mixin?
Mixin is a type of multiple inheritance wherein you can combine behaviors and attributes of more than one parent class.<br>
Mixins provide an excellent way to reuse code from multiple classes. For example, generic class-based views consist of a mixin called TemplateResponseMixin whose purpose is to define ```render_to_response()``` method. When this is combined with a class present in the View, the result will be a TemplateView class.<br>
One drawback of using these mixins is that it becomes difficult to analyze what a child class is doing and which methods to override in case of its code being too scattered between multiple classes.




























