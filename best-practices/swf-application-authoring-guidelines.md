# Best practices - SWF application authoring guidelines

## About SWF application guidelines

The best way to create Flash Pro applications depends on the application you
create and the technology that you are using to build the application.

An online application lets a user influence a website by interacting with it.
For example, the application might collect information from the user (such as a
username and password for a registration), information might be added to the
site (such as in a forum), or the user might interact in real time with other
site visitors (such as a chat room or interactive white board). Results from the
server often appear in the SWF file, depending on the interaction. These
examples are applications that involve the user and different kinds of server
interaction. A website that does not use visitor information or data is not an
application (for example, a portfolio, cartoon animation, or static
informational site). Flash Pro applications involve an interactive process
between the user, a web application, and a server. The basic process is as
follows:

1.  A user enters information into a SWF file.

2.  The information is converted into data.

3.  The data is formatted and sent to a web server.

4.  The data is collected by the web server and sent to an application server
    (for example, ColdFusion, PHP, or ASP).

5.  The data is processed and sent back to the web server.

6.  The web server sends the results to the SWF file.

7.  The SWF file receives the formatted data.

8.  Your ActionScript processes the data so the application can use it.

When you build an application, you must select a protocol for transferring data.
The protocol alerts the application when data is sent or received, in what
format the data is transferred, and how it handles a server's response. After
data is received in the SWF file, it must be manipulated and formatted. If you
use a protocol, you do not have to worry about data being in an unexpected
format. When you transfer data using name-value pairs, you can check how the
data is formatted. Check that the data is formatted correctly, so you do not
receive XML formatted data and so the SWF file knows what data to expect and
work with.

## Collecting and formatting data

Applications depend on user interaction with the SWF file. Frequently, it
depends on the user entering data into forms. Flash Pro provides many ways you
can enter and format data in Flash Pro applications. This flexibility exists
because of the capabilities you have with animation and creative control over
the interface, and error checking and validation you can perform using
ActionScript.

Benefits from using Flash Pro to build forms to collect data include the
following:

- Increased design control.

- Decreased or no need for page refreshing.

- Reuse of common assets.

  ![](../img/tip_help.png) To save information that you collect from the user,
  save it in a shared object on the user's computer. Shared objects let you
  store data on a user's computer, which is similar to using a cookie. For more
  information on Shared objects, see the sharedObject class in ActionScript 2.0
  Language Reference or ActionScript 3.0 Language and Components Reference.

## Sending and processing data

You must typically process information before you send it to the server, so it's
formatted in a way that the server understands. When the server receives the
data, it can be manipulated in any number of ways and sent back to the SWF file
in a format that it can accept, which can range from name-value pairs to complex
objects.

> **Note:** Your application server must have the MIME type of its output set to
> `application/x-www-urlform-encoded`. If that MIME type is missing, the result
> is usually unusable when it reaches Flash Pro. The following table shows you
> several options for sending data to a server and receiving data using Flash
> Pro:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Send data</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><samp>LoadVars.send</samp> and
<samp>LoadVars.sendAndLoad</samp></p></td>
<td><p>Sends name-value pairs to a server-side script for processing.
<samp>LoadVars.send</samp> sends variables to a remote script and
ignores any response. <samp>LoadVar.sendAndLoad</samp> sends name-value
pairs to a server and loads or parses the response into a target
<samp>LoadVars</samp> object.</p></td>
</tr>
<tr class="even">
<td><p><samp>XML.send</samp> and <samp>XML.sendAndLoad</samp></p></td>
<td><p>Similar to <samp>LoadVars</samp>, but <samp>XML.send</samp> and
<samp>XML.sendAndLoad</samp> send XML packets instead of name-value
pairs.</p></td>
</tr>
<tr class="odd">
<td><p><samp>getURL</samp></p></td>
<td><p>Using the <samp>getURL()</samp> function or
<samp>MovieClip.getURL</samp> method, you can send variables from Flash
Pro to a frame or pop‑up window.</p></td>
</tr>
<tr class="even">
<td><p>Flash Remoting</p></td>
<td><p>Lets you easily exchange complex information between Flash Pro
and ColdFusion, ASP.NET, Java, and more. You can also use Flash Remoting
to consume web services.</p></td>
</tr>
<tr class="odd">
<td><p>Web services</p></td>
<td><p>Adobe® Flash® Professional CS5 includes the WebServiceConnector
component that lets you connect to remote web services, send and receive
data, and bind results to components. This lets Flash Pro developers
quickly create Rich Internet Applications without having to write a
single line of ActionScript.</p>
<p>You can consume remote web services by using WebServiceClasses, which
can require writing complex ActionScript.</p></td>
</tr>
</tbody>
</table>

## Adding data loading and validation

Validate any information you retrieve before you send that data to a server.
This reduces strain on the remote server, because it does not handle as many
requests when users do not fill in required fields. Never rely solely on
client-side validation in any application; server-side validation must also
occur.

Even if you build a simple registration or login form, check that the user has
entered their name and password. Perform this validation before sending the
request to the remote server-side script and waiting for a result. Do not rely
only on server-side validation. If a user enters only a username, the
server-side script must receive the request, validate the data being sent, and
return an error message to the Flash Pro application, stating that it requires
both the username and password. Likewise, if validation is performed only on the
client side (within the SWF file), a user might hack the SWF file, bypass the
validation, and send data to your server in an attempt to post the bad data.

Client-side validation can be as simple as making sure that a form field is at
least one character long, or that the user entered a numeric value and not a
string. To validate an e‑mail address, for example, check that the text field in
Flash Pro isn't empty and contains at least the at sign (`@`) and dot (`.`)
characters. For the server-side validation, add more complex validation and
check that the e‑mail address belongs to a valid domain.

You must write ActionScript to handle the data that loads into the SWF file from
the server. After you finish loading data into a SWF file, the data can be
accessed from that location. Use ActionScript to check whether the data is fully
loaded. You can use callback functions or listeners to send a signal that the
data is loaded into the document. When you load data, it can be formatted in
several ways:

- You might load XML, in which case you use the XML class methods and properties
  to parse the data and use it. If you use name-value pairs, the pairs turn into
  variables and you can manipulate them as variables.

- You might receive data from a web service or from Flash Remoting. In both
  cases, you could receive complex data structures, such as arrays, objects, or
  record sets, which you must parse and bind appropriately.

## Using error handling and debugging

Your application needs to be robust enough to anticipate certain errors and
handle them accordingly.

One of the best ways to perform error handling in ActionScript 2.0 is to use the
`try-catch-finally` blocks that let you throw and catch custom errors. By
creating custom error classes, you can reuse code throughout your application
without having to rewrite error handling code. For more information on throwing
custom errors, see the `Error` class in _ActionScript 2.0 Language Reference_.
For more information on `try-catch-finally` blocks, see `try..catch..finally` in
_ActionScript 2.0 Language Reference_.

In ActionScript 3.0, use the `flash.errors` class to catch errors.

For more information, see "Handling synchronous errors in an application" in
_Programming ActionScript 3.0_.

## Organizing files and storing code

Consider the following guidelines before you start organizing files and storing
code:

- Do you divide the SWF file into multiple SWF files, and, if so, how should
  they interact?

- What assets can you share across SWF files?

- What files do you dynamically load?

- How and where do you store ActionScript?

  When you develop an application, store your server-side code and files in a
  logical directory structure, similar to those in an ActionScript package.
  Arrange your code this way to keep it well organized and reduce the risk of
  the code being overwritten.

  For larger applications, encapsulate client-server communication and services
  in classes. When you use classes, you benefit in the following ways:

- You can reuse the code in more than one SWF file.

- You can edit code in a central place, and update all SWF files by republishing
  them.

- You can create a single API that can manipulate different UI elements or other
  assets that perform similar functions.

## Using the MVC design pattern

The MVC design pattern is used to separate the information, output, and data
processing in the application. The application is divided into three elements:
model, view, and controller; each element handles a different part of the
process.

The model  
Incorporates the data and rules of the application. Much of the application's
processing occurs in this part of the design pattern. The model also contains
any components (such as CFCs, EJBs, and web services), and the database. Data
returned is not formatted for the interface (or front end) of the application in
this part of the process. The returned data can be used for different interfaces
(or views).

The view  
Handles the front end of the application (the interface with which the user
interacts), and renders the model's contents. The interface specifies how the
model's data is presented and outputs the view for the user to use, and lets the
user access or manipulate the application's data. If the model changes, the view
updates to reflect those changes by either pushing or pulling data (sending or
requesting data). If you create a hybrid web application (for example, one that
includes Flash Pro interacting with other applications on the page), consider
the multiple interfaces as part of the view in the design pattern. The MVC
design pattern supports handling a variety of views.

The controller  
Handles the requirements of the model and view to process and display data, and
typically contains a lot of code. It calls any part of the model, depending on
user requests from the interface (or view), and contains code that's specific to
the application. Because this code is specific to the application, it is usually
not reusable. However, the other components in the design pattern are reusable.
The controller does not process or output any data, but it takes the request
from the user and decides what part of the model or view components it needs to
call, and determines where to send the data and what formatting is applied to
the returned data. The controller ensures that views have access to parts of the
model data that they must display. The controller typically transmits and
responds to changes that involve the model and view.

Each part of the model is built as a self-contained component in the overall
process. If you change one part of the model (for example, you might rework the
interface), the other parts of the process do not usually need modification,
which reduces problems. If your design pattern is created correctly, you can
change the view without reworking the model or controller. If your application
does not use MVC, making changes anywhere can cause a rippling effect across all
your code, which requires many more changes than if you were using a specific
design pattern.

An important reason to use the MVC pattern is to separate data and logic from
the user interface. By separating these parts of the process, you can have
several different graphical interfaces that use the same model and unformatted
data. This means that you can use your application with different Flash Pro
interfaces, such as an interface for the web, one for Pocket PC, a version for
cell phones, and perhaps an HTML version that doesn't use Flash Pro at all.
Separating data from the rest of the application can greatly reduce the time it
takes to develop, test, and even update more than one client interface.
Similarly, adding new front ends for the same application is easier if you have
an existing model to use.

Only use MVC if you build a large or complex application, such as an e‑commerce
website or an e‑learning application. Using the architecture requires planning
and understanding how Flash Pro and this design pattern work. Carefully consider
how the different pieces interact with each other; this typically involves
testing and debugging. When you use MVC, testing and debugging are more involved
and difficult than in typical Flash Pro applications. If you build an
application in which you need the additional complexity, consider using MVC to
organize your work.

## Creating secure applications

Dishonest users might try to hack your application, whether you build a small
portal site where users can log in and read articles or a large e‑commerce
store. For this reason, consider the following steps to secure your application.

- Post data to HTTPS for data that needs to be secured. Encrypt values in Flash
  Pro before sending them to a remote server to be processed.

  > **Important:** Never store any information or code in a SWF file that you
  > don't want users to see. It is easy to disassemble SWF files and view their
  > contents using third-party software.

- Add a cross-domain policy, which prevents unauthorized domains from accessing
  your assets.
