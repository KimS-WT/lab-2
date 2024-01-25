## Your Name:

# CIDM 3312 Lab 2: Review of Classes and Objects

The goal of this lab exercise to review your knowledge of classes, objects and namespaces in C#. Read the instructions in this file, `README.md`, below. You can view them in VS Code by pressing Ctrl+Shift+V or Cmd+Shift+V.

Need Help? Don't hesitate to reach out -

- Join our slack channel. Details are on WTClass.
- Email or call me.

## Task 0
1. Watch the Week 2 video and the read lecture notes on WTClass in our Week 2 folder.
2. Clone your repository in VS Code.

## Task 1
This repository does not have any starting code. You must create a new C# console application from the Terminal.
1. From the VS Code Terminal, type `dotnet new console`. Make sure you are in the correct folder.
2. Click on the newly created `Program.cs` file in VS Code, wait a few seconds, and click Yes on the popup asking you to Add "Required assets to build and debug".

## Task 2
1. Create a new file in the same folder as `Program.cs` called `Widget.cs`. This file is your class. It will be empty initially.
2. Fill in `Widget.cs` the following template code that serves as the basis of most new classes in C#:
  ```
  using System;

  namespace lab2_starter
  {
      public class Widget
      {

      }
  }
  ```

## Task 3
1. Give your Widget Class some properties. Remember, when we get to EF Core every class will have a primary key that will uniquely identify each instance of that class. We will give our Widget Class a primary key and a name:
  ```
  using System;

  namespace lab2_starter
  {
      public class Widget
      {
          public int WidgetId {get; set;}
          public string Name {get; set;} = string.Empty;
      }
  }
  ```

## Task 4
1. In 'Program.cs', bring in your Widget class namespace with the `using` keyword:
```
using lab2_starter;
```
2. In `Program.cs`, create a new object from the Widget class:
```
Widget widgetOne = new Widget();
```
3. Give `widgetOne` a name and display that name to the console.
```
widgetOne.Name = "Example Name";
Console.WriteLine($"widgetOne.Name = {widgetOne.Name}");
```
4. Create a second widget, give it a different name, and print it out to the console.

## Task 4
In larger applications, it can be helpful to have a hierarchy of namespaces. Right now `Widget.cs` has a namespace of `lab2_starter`. You can further separate namespaces within an application using the dot operator.
1. Change the namespace of the Widget class to `lab2_starter.Models`.
2. Notice how `Program.cs` now has errors. It can't find the Widget class anymore because it is in a different namespace. You need to use the `using` directive to bring in your Widget class.
3. Change the `using` directive in `Program.cs` to bring in the new namespace.

## Task 5
1. Save your program and run it. At the terminal prompt, type `dotnet run`.
2. Edit `README.md` and put your name at the top.
3. Push your changes to GitHub:
    - Click the source control icon in VS Code
    - Type in a commit message
    - Click the checkbox icon to commit. (Click yes on the message box to stage your commit)
    - Click the 3 dots icon (...) for more actions and click Push.
4. Or you can push your changes to GitHub using the Terminal:
    ```
    git add -A
    git commit -m "Your commit message"
    git push
    git status
    ```
4. Verify that your changes are on GitHub.
6. Congratulations! Your lab 2 assignment is complete.