pipeline{

    agent any
    tools{
      maven 'mymaven'
    }
//parameters are used to store data, these parameters can be used in step
//parameters have values which can be of type string,inetegr,boolean,secrret,password
    //synatx of parameter
    //dataType(name:'give name',defaultValue:'value',description:'describe the parameter')
    
    parameters{

        choice(name:'ENV',choices:["","Dev","QA"])

    }
}