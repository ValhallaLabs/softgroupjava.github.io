---
layout: post
title: Code Conventions
---

В цілому код має відповідати [Java Code Conventions](http://www.oracle.com/technetwork/java/codeconventions-150003.pdf) із не значними змінами, описаними нижче. **Але** якщо ми працюємо над legacy проектом, то щоб не вносити плутанини потрібно підлаштовуватися під наявний стиль коду.

## Java

#### General

 - __No tabs__ in source code - only spaces.
 - Max line length - __120 symbols__.
 - Use 4 spaces for indentation.
 - Java source files shouldn't be large, you should try to make them not more than 500 lines.

#### Classes & Methods and other stuff

 - If there is an abbreviation in class name, you should use camel style for them as well. E.g. *UserDao*, not *UserDAO*.
 - If you can't imagine any adequate name for implementation of some interface, name it *InterfaceNameImpl*.
 - Interfaces shouldn't use I at the start, and abstract classes shouldn't start with A. Bad style: *IFigure*, *ARoundFigure*.
- Both classes and methods should be named in a self-explanatory way. If the name is too long, you could shorten it and add more information to JavaDocs, but you should think thorought about these names, they are very important.
 - If you have a method with an empty body and you don't want/can implement it, you must throw *UnsupportedOperationException* in its body.

#### Comments

 - JavaDocs should be present at next levels: packages, classes, methods, constants. Private methods might be an exception, but only if it's name and functions are really self-explanatory and they do not throw any unchecked exceptions, in other cases - you have to write full JavaDocs.
 - When you create a class or make serious amendmends, you should always put/add yourself as the author, use your first name and family name for these purpose.
 - If you implement/override some method and you follow the contract that is described by parent's JavaDocs, you should put {@inheritDoc} directive in JavaDocs of this new method. If you deviate from the contract, you should write full JavaDoc for it.
 - Do not use excessively simple Java comments inside methods body, - only for places where there is a real need.

#### Packages

 - Package name shouldn't contain any BIG letters or underscores.
 - Don't put a lot of classes in a single package, 20 is okay, 100 is too much.
 - Try to avoid circle dependencies between packages.

## XML
 - Use 2 spaces for indentation
 - If you deal with such short tags: <something attribute1="value" />, you should put a space between last attribute and slash.

## Database

 - Columns, constraints, tables should not use CamelStyle, nor they should contain small letters. This is how they should be named: COLUMN_NAME, TABLE_NAME, FK_NAME

## Resource Bundle

 - No camel case, use underscore to separate words (recent_activity=Recent Activity).
 - Use dots to separate places where the label is used, but don't use dots just to separate words (profile.comment_count=Comment Count).
 - Use placeholders to finish the phrase within the text: (header.welcome_user=Welcome, {0}).

## Example

```java
package ua.softgroup.project;

import ua.softgroup.project.core.SomeClass;

/**
 * Class  description  goes  here.
 *
 * @author Firstname Lastname
 * @author Firstname1 Lastname1
 */
public class Blah extends SomeClass {
    /**
     * classVar1 documentation comment
     */
    public static int classVar1;
    /**
     * classVar2  documentation  comment  that  happens  to  be
     * more  than  one  line  long
     */
    private static Object classVar2;
    /**
     * instanceVar1 documentation comment
     */
    public Object instanceVar1;
    /**
     * instanceVar2 documentation comment
     */
    protected int instanceVar2;
    /**
     * instanceVar3 documentation comment
     */
    private Object[] instanceVar3;

    /**
     * ...constructor  Blah  documentation  comment...
     */
    public Blah() {
      //  ...implementation  goes  here...
    }

    /**
     * ...method  doSomething  documentation  comment...
     */
    public void doSomething() {
       //  ...implementation  goes  here...
    }

    /**
     * ...method  doSomethingElse  documentation  comment...
     *
     * @param someParam description
     * @return description
     * @throws SomeRuntimeException when ....
     */
    public Object doSomethingElse(Object someParam) {
       //  ...implementation  goes  here...
    }

}
```
