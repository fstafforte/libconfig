# libxmlconfig
This is a C library that read configuration file in the following xml format.
Use a xsd schema file to validate configuratuon file.
You can add more then one file to the configuration file manager.
The xml file format is the following

<section name='section1'>
  <key name='key1'>
    <datum name='min' value='-20'>
    <datum name='max' value='20'>
  </key>
</section>
 

datum can be of the following types

boolean (literal string true or false)
64 bit integer;
double;
string (zero terminated charaters array)

Each key at least has a datum or more than one of the same type
Configuration file manager validates files usind configuration.xsd schema file 
that you can find in the configuration directory 
Users can retrive datum using configuartion file manager API or macros,
in case a datum value does not respect the desired type the default value is returned
and a message is printed out byte the logger set during library
initialization or on the standerd error if no logger has been set

Dependeces:
libxml2 vesrion 2.9.1 or higher







 






