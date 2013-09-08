## ASP.NET Identity / Membership Database

This is a seed project which you can use to create your custom ASP.NET Identity / Membership solution using
[Database First](http://msdn.microsoft.com/en-us/data/jj206878.aspx) development approach.

![ASP.NET Membership Database](http://i.imgur.com/whB1uCn.png)

### Prerequisites

 * [Visual Studio 2012.3](http://www.visualstudio.com) or [Visual Studio 2013 Preview](http://www.microsoft.com/visualstudio/eng/2013-preview#story-2013preview)
 * [SQL Server Data Tools](http://msdn.microsoft.com/en-us/data/tools.aspx) (already included in VS2013)

### How to deploy

Double-click on the ```.\Database\Publish Profiles\Local.publish.xml``` file in Solution Explorer which should open
a publishing dialog shown below and click [Publish].

![ASP.NET Membership Database Publish Dialog](http://i.imgur.com/QrT9MBp.png)

### Database naming conventions

The naming conventions in this project are the same used in the [AdventureWorks](https://msftdbprodsamples.codeplex.com/)
sample database created by Microsoft database professionals and demonstrate many best practices in terms of style.

To summarize:

 * Object names are easily understood
 * Table names are not pluralized ("User" table not "Users")
 * Abbreviations are few, but allowed (i.e. Qty, Amt, etc.)
 * PascalCase used exclusively with the exception of certain column names (i.e. rowguid)
 * No underscores
 * Certain keywords are allowed (i.e. Name)
 * Stored procedures are prefaced with "usp"
 * Functions are prefaced with "ufn"
 * Constraints are prefixed with DF, FK, UK, IX based on their types
 * Constraints contain table's name as well as a list of columns used in the constraint
   (i.e. PK_User_UserID, UK_User_UserName, DF_User_CreatedDate)

Each rule has a good reasoning behind it. For example, why table names should be singular? Because this way
there is less noise, such tables are easier to map to entity models using ORM tools, tables are more accurately
sorted alphabetically in your IDE, table names describe the data type rather than how much data it contains,
it's easier to come up with singular names, than with plural ones (with a few exceptions like News), easier to
spell correctly (especially for a non-native English language programmer).

For more info visit [AdventureWorks OLTP Database](http://msdn.microsoft.com/en-us/library/ms124659.aspx) at MSDN

### Learn more about SSDT

 * [SQL Server Data Tools Home Page](http://msdn.microsoft.com/en-us/data/tools.aspx) at Dev Center
 * [SQL Server Data Tools Documentation](http://msdn.microsoft.com/en-us/library/hh272686.aspx) at MSDN.
 * [SQL Server Data Tools Team Blog](http://blogs.msdn.com/b/ssdt/)
 * [SQL Server Data Tools Forums](http://social.msdn.microsoft.com/Forums/en-US/ssdt/threads)
 * [SQL Server Data Tools Questions](http://stackoverflow.com/questions/tagged/ssdt) at StackOverflow

### Credits

Brought to you by Konstantin Tarkus and is available under Apache License 2.0. Have questions? Email me at
[hello@tarkus.me](mailto:hello@tarkus.me)