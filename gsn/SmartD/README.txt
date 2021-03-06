
SmartD version 1.0 29.12.2013

Installation and running from Eclipse:
======================================
1. Create a new database and call it "gsn"
   NOTE: we use database server MySQL for this project.
   If you do not familiar with SQL commands, see README-mysql-related.txt

2. Set the username equal to "gsn" and the password equal to "gsnpassword"

3. Go to /tables

	a. Extract electric_data_small_11.sql.zip, 

	b. Import the tables: 
	   - electric_data_small_11.sql
	   - ireland_survey_answer_small_11.sql 
	   - ireland_survey_answer_options.sql
	   - ireland_survey_question.sql
	   to the gsn database.
	   NOTE: electric_data_small_11 and ireland_survey_answer_small_11 contains only
		     a (very small) subset of the dataset that we used for the demo 
		     (we took randomly 11 ids and anonymize them).
		     The original dataset that we used is the CER dataset: 
		     CER smart metering project:   
		     https://www.ucd.ie/issda/data/commissionforenergyregulationcer/
		     Please contact them to obtain the full dataset.

	c. rename table electric_data_small_11 to electric_data
	   rename table ireland_survey_answer_small_11 to ireland_survey_answer

	d. apply the sql script on file remove-qid-1-and-2.sql to remove question 
       ID 1 and 2 (which seem to be irrelevant for our inferencing)
       (you can simply copy/paste each line to the mysql console)

	e. NOTE: for all these tables, we used MyISAM engine. Depending on what you 
	   want, you might want to change it to InnoDB. There are a lot of 
	   documentation/forum discussed their difference (just in case you do not 
	   understand their differences)

NOTE: this step 4 below assumes that you have already gsn in your eclipse (and 
      you understand how to run gsn). If not, please check 
      README-gsn-related.txt (then you will understand step 4-6 easily).

4. Choose Java 1.6 in your eclipse

5. Right click on the build.xml, choose "Run As" and choose [2 Ant Build...].
   There are a lot of check boxes. First, to build GSN, choose build (default) 
   and run it.

6. To start GSN, choose check box "gsn", and run it. If you still have "build" 
   checked, uncheck it.

SmartD can be reached at:
web site : http://localhost:22001/SmartDindex.html


2014.05.30
==========
To be able to run the forecasting capability as in the demo, see the README in
../../smartd-forecasting/README


