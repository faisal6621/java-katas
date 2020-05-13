= Java Time API - A Code kata

image::docs/DukeTime.png[alt="Java Duke Date Time Logo", align="center", height=420]

== Table of Contents
* [What is a Code Kata](#WhatIsACodeKata)
** [How does one go about with this kata?](#HowToSolveKata)
** [Mission](#Mission)
** [Requirements](#Requirements)
* [Project Structure](#ProjectStructure)
* [Java Time API](#JavaTime)
* [Solutions to the Katas](#Solutions)
* [Take Away](#TakeAway)

Most, if not all Java developers need to rely on Java date and time libraries. 

[#WhatIsACodeKata]
== What is a Code-Kata

A code-kata is a coding exercise that builds muscle memory by a practice of programming to arrive 
at a known solution.

[#HowToSolveKata]
=== How does one go about with this code kata?

The essence of the exercise (presentation material and code kata) is to demonstrate the  
usage patterns for dates and times.

This set of code katas rely on fixing broken tests. The tests may have multiple solutions, the 
intent is to learn and experiment. 

The project contains several JUnit tests that fail as `org.opentest4j.AssertionFailedError`. 

<span style="color:green;">**Here are simple steps to use this kata**</span>:

1. Run the test class(es).
2. One or more tests will fail with the test failure message.
3. Fix the failing tests by taking hints from the `TODO`s.
4. Repeat above steps until all tests pass.
5. Check the solutions to see if there are other ways to solve. 
(Remember, the solution may be less performant than yours)
6. Rinse and repeat (delete and checkout again, then back to Step 1) to build muscle memory.

[#Mission]
=== Mission
> ***Your mission**, should you choose to accept it, will be to fix the JUnit tests. This 
message will self-destruct in* **NaN** *minutes*

[#Requirements]
=== Requirements
How to prepare for coding along

This kata is developed as a Java maven project. Ensure that you have:

1. Apache Maven 3.3.x or above. _Tested with Apache Maven 3.5.0_.
    Link: https://maven.apache.org/download.cgi

1. JDK 11. _Tested with OpenJDK 11_
    Link: http://jdk.java.net/11/

1. Your favorite Java IDE. _IntelliJ IDEA Ultimate was used to develop this kata_.
 
[#ProjectStructure]
== Project Structure

The structure of the project:
```
|____pom.xml
|____README.md
|
|____src
| |
| |____test                    <------------------- Kata Tests
| | |____java
| |   |____none
| |     |____cvg
| |       |____datetime
| |
| |____main                    <------------------- Shared ErrorMessages & DemoClass
| | |____java
| |   |____none
| |     |____cvg
| |       |____datetime
| |
| |____solutions               <------------------- Solutions 
| | |____java
| |   |____none
| |     |____cvg
| |       |____datetime
```

[#JavaTime]
== Java Time API

The JUnit tests listed below are setup to utilize the Java Time API features.

=== Tests Included

==== Java Date Time

1. ==== xref:src/test/java/none/cvg/datetime/TestKata1InstantAndDateInterop.java[TestKata1InstantAndDateInterop.java]

   The tests in this class show interoperability between `java.util.Date` and the newer `java.time.Instant`. 

2. ==== xref:src/test/java/none/cvg/datetime/TestKata2LocalAndZonedDateTimes.java[TestKata2LocalAndZonedDateTimes.java] 

   The tests in this class show the usage of `java.time.LocalDate`, `java.time.LocalTime`, `java.time.LocalDateTime` and `java.time.ZonedDateTime`. 
   In addition, this class introduces a `java.time.Clock` that is extremely handy in writing tests. 

3. ==== xref:src/test/java/none/cvg/datetime/TestKata3PeriodsAndDurations.java[TestKata3PeriodsAndDurations.java]

   The tests in this class show the usage of DateTime ranges: Period, Duration tests. 

4. ==== xref:src/test/java/none/cvg/datetime/TestKata4DateTimePartials.java[TestKata4DateTimePartials.java]

   The tests in this class show the usage of DateTime partials: Month, MonthDay, Year, YearMonth and DayOfWeek tests. 

5. ==== xref:src/test/java/none/cvg/datetime/TestKata5StreamsInDateTime.java[TestKata5StreamsInDateTime.java]

   The tests in this class show the usage of DateTime in Java `stream()` lazy iterations. 

[#Solutions]
== Solutions

Solutions for each test:

Kata Test | Solution
------------ | -------------
[TestKata1InstantAndDateInterop.java](src/test/java/none/cvg/datetime/TestKata1InstantAndDateInterop.java) | [TestSolution1InstantAndDateInterop.java](src/solutions/java/none/cvg/datetime/TestSolution1InstantAndDateInterop.java)
[TestKata2LocalAndZonedDateTimes.java](src/test/java/none/cvg/datetime/TestKata2LocalAndZonedDateTimes.java) | [TestSolution2LocalAndZonedDateTimes.java](src/solutions/java/none/cvg/datetime/TestSolution2LocalAndZonedDateTimes.java)
[TestKata3PeriodsAndDurations.java](src/test/java/none/cvg/datetime/TestKata3PeriodsAndDurations.java) | [TestSolution3PeriodsAndDurations.java](src/solutions/java/none/cvg/datetime/TestSolution3PeriodsAndDurations.java)
[TestKata4DateTimePartials.java](src/test/java/none/cvg/datetime/TestKata4DateTimePartials.java) | [TestSolution4DateTimePartials.java](src/solutions/java/none/cvg/datetime/TestSolution4DateTimePartials.java)
[TestKata5StreamsInDateTime.java](src/test/java/none/cvg/datetime/TestKata5StreamsInDateTime.java) | [TestSolution5StreamsInDateTime.java](src/solutions/java/none/cvg/datetime/TestSolution5StreamsInDateTime.java)
    
[#TakeAway]
== Take Away

The key take-away from this kata is a solid understanding of the Java Time API.
