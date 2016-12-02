---
layout: post
title:  "Object Models"
date:   2016-12-02 16:32:22 +0000
---

Three concepts are critical to understanding object models. They are:

**Data Abstraction**

Data abstraction is the process of distilling data down to its essentials. It is the reduction of a particular body of data to a simplified representation of the whole. 

Abstraction is the process of recognizing and focusing on important characteristics of a situation or object and leaving/filtering out the un-wanted characteristics of that situation or object. Lets take a person as example and see how that person is abstracted in various situations

A doctor sees (abstracts) the person as patient.  The doctor is interested in name, height, weight, age, blood group,  previous or existing diseases etc of a person
An employer sees (abstracts) a person as Employee. The employer is interested in name, age,  health, degree of study, work experience etc of a person.  
So, you see that Abstraction is the basis for software development.  Its through abstraction we define the essential aspects of a system.  The process of identifying the abstractions for a given system is called as Modelling  (or object modelling).

In the above example, the doctor may not be interested in characteristics of a person on which the employer is interested in and vice versa.   Both employer and doctor will not be interested in all the characteristics of a person (like the color of dress the person wears on a particular day, the food the person takes, the relatives of the person etc).  But however some elements are common to both doctor and the employer (like name, age, height etc).  


**Encapsulation**

Encapsulation is the object model concept of including processing or behavior with the object instances defined by the class. Encapsulation allows code and data to be packaged together.
The definition of methods for a class is an integral part of encapsulation. A method is programming code that performs the behavior an object instance can exhibit. Calculating the age of a person would be an example of such behavior. The figure shows a way of looking at encapsulating the age method with an instance object. The code for the age method is "attached" to or encapsulated with the object rather than part of the application.


**Inheritance**

Inheritance in the object model is a means of defining one class in terms of another. This is common usage for most of us. For example, a conifer is a type of tree. There are certain characteristics that are true for all trees, yet there are specific characteristics for conifers.
Note that in an object model, there is no distinction in usage between system pre-defined types and user-defined types. This is known as extensibility. So it is possible to define a type as a sub-type of a system type or as a sub-type of a user-define type.
In this example, a Student is a type of Person. Likewise, a Employee is a type of Person. Both Student and Employee inherit all the attributes and methods of Person. Student has a locally defined student ID attribute. Employee has a locally defined employee ID attribute.
So, if you would look at a Student object, you would see attributes of name, date of birth, parents, children, and student ID.
