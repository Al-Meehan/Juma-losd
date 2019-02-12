# Juma Editor (LOSD Version)

## Description

This is a version of the Juma Editor tool that has been specialised for use in the LOSD publication platform.

## Required Software

- MySQL Server v5.7
- Apache Maven v3.2.5 (or later)
- Java v1.7 (or later)

## Configuration and Running of Juma

How to configure and run Juma:
1. Extract Juma to desired directory.

2. You need to specify connection details to mysql server for Juma.
   Open the "../JUMA/juma-uplift-master/src/main/resources/hibernate.cfg.xml" file and specify your mysql connection url, username and password.
	 
3. To add users for Juma, edit the "../JUMA/juma-uplift-master/src/main/resources/shiro-users.properties" file.
   Each user must be on a separate line and the syntax to declare a new use is as follows: "user.name = password".
	 So for a user "foo" with password "bar" it would be specified as: "user.foo = bar".
	 
4. To Run Juma, navigate to "../JUMA/juma-uplift-master".
	 Run the following command: "mvn jetty:run", this will run Juma on the default port which is 8080.
	 To run Juma on a specific port, run the following command instead: "mvn jetty:run -Djetty.port=xxxx".

5. In a web browser, go to http://localhost:8080 (or to whatever port you specified).

## Dump File with Examlpe Mappings

The 'juma_TestUser_Mappings_dump.sql' file is a dump containing a number of example mappings for the conversion of HC55, LFS, and SILC statistical datasets. Simply import the the dump file to the mysql server and create a juma user with the name: 'TestUser'.

## License
This software is released under the [MIT license](http://opensource.org/licenses/MIT).
