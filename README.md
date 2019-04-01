# PL/SQL Trigger


Triggers are stored programs, which are automatically executed or fired when some events occur. 

Triggers are written to be executed in response to any of the following events −

A database manipulation (DML) statement (DELETE, INSERT, or UPDATE)

A database definition (DDL) statement (CREATE, ALTER, or DROP)

A database operation (SERVERERROR, LOGON, LOGOFF, STARTUP, or SHUTDOWN)


Benefits of Triggers
----

Generating some derived column values automatically

Enforcing referential integrity

Event logging and storing information on table access

Auditing

Synchronous replication of tables

Imposing security authorizations

Preventing invalid transactions


Create Trigger
------

    CREATE [OR REPLACE ] TRIGGER trigger_name  
    {BEFORE | AFTER | INSTEAD OF }  
    {INSERT [OR] | UPDATE [OR] | DELETE}  
    [OF col_name]  
    ON table_name  
    [REFERENCING OLD AS o NEW AS n]  
    [FOR EACH ROW]  
    WHEN (condition)   
    DECLARE 
       Declaration-statements 
    BEGIN  
       Executable-statements 
    EXCEPTION 
       Exception-handling-statements 
    END; 
    
  
