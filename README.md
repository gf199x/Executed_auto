# Executed_auto
Executed_auto_code_EG

/* quickly assign means name-fixing */
%macro Means (dataset = 
			,stats_list = );

	proc means data= &dataset &stats_list;
		title "MEANS of &dataset";
	run;

%mend Means;


/*eg: %Means(dataset=sashelp.class,stats_list= n nmiss);*/
%Means(dataset=sashelp.class, stats_list =n nmiss);
***********************;
/*compress=yes*/
options compress=yes reuse=yes;
*****************************;
