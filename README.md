# Java-MVC-Structure :Basic Structure for Java MVC Project

First of all I would like to say that its **not the one and only or mandatory structure** to be followed for java mvc projects. You can use any structure, according to your requirements. I am going to give a description of the structure which I try to follow.

**And this structure is for those who are not going to use any frameworks for the MVC Web-project.**
 
# Pre-requisites before creating a web-project:
1. Java or JDK must be installed properly.
2. IDE(preferably Eclipse or Netbeans,...).
3. Server for executing your project(Apache Tomcat Server).
4. Database for execution of database functionality, (not required at the initial part for creating the structure of the project).
 
# A. Follow the basic instructions for understanding, of the above structure:

1.  **src - will contain all the classes,servlets within respective packages.**
     For the above demo structure, I have included 5 packages namely- 
a.  **com.bean** - for the Bean/POJO class,  
b.  **com.controller** - for the servlet class, 
c.  **com.dao** - for the DataAccessObjects class, for database operations, 
d.  **com.service** - (not required for small-projects) for the service class, to act as a bridge between servlet and dao. This class can be omitted,
e.  **com.util** - for the DatabaseUtil class which is for establishing and disconnecting a database connection. Again you can omit this, and include this methods in other             class.

2. **WebContent - this will contain the source files including JSP, HTML, CSS, Javascript pages.**
     I have created a separate folder css to keep the css files, and javascript folder to include the javascript source files. Again this can be avoided, and can be included      in the WebContent folder directly.
     
     Now, clone/download the above structure and follow the necessary steps, import it in your IDE, and you are ready to start with the mvc project.
     
# B. Follow the basic instructions those who want to create the project structure manually:(for ecipse IDE)

1. Open your ide, and create a Dynamic Web Project from File menu.
2. Enter the name --> Select Target runtime as Apache Tomcat server  --> select the latest Dynamic web module version  --> Next  --> Next -->
3. Check the box to include web.xml deployment descriptor file in your project (this is the most important step)  --> Finish
4. Your project is created. 
Now go through  **A. Follow the basic instructions for understanding, of the above structure:** to continue with your mvc web project and to add packages and source files.
**src folder is available within Java Resources.**


# Point to be Noted:
The web.xml file is generated by default.
So it contains some basic code by default and you need to change it according to your project.
For example- web.xml contains following code by default:

    <welcome-file-list>
    <welcome-file>index.html</welcome-file>
    <welcome-file>index.htm</welcome-file>
    <welcome-file>index.jsp</welcome-file>
    <welcome-file>default.html</welcome-file>
    <welcome-file>default.htm</welcome-file>
    <welcome-file>default.jsp</welcome-file>
    </welcome-file-list>

If your starting file for the project is index.html, then its well and good, you need not change. But if this is not the case, and suppose your starting file is **hello.jsp**,
 then the web.xml will be like:
 
    <welcome-file-list>
    <welcome-file>hello.jsp</welcome-file>   // here is the change
    </welcome-file-list>
By the way, keep the other default portion of the code as it is, you need to change only in case **welcome-file tag**.
 

