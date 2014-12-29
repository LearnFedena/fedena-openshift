
#Learn Fedena Instruction For Fedena-Openshift
Fedena-Openshift is original projectfedena school management system that has been preconfigured to be hosted on the popular openshift cloud platform.

No additional configuration is required. Just download to your local machine and push to openshift

#Installation 
1) Create a free account or login to an existing on openshift

2) open a terminal window or command prompt and enter the following command:
   `gem install rhc`

3) Create a ruby 1.8 application:

   `rhc app create <app-name> ruby-1.8 mysql-5.5`
 
4) Your openshift application will be cloned to your machine. Delete all the files and folders.

5) Use git to add and commit the changes file your directory:

   `git commit -a -m "deleted openshift temporary files and folders"`

6) Push your changes to openshift:

   `git push`

7) Clone or download and extract fedena-openshift to your local machine.

8) Copy all fedena-openshift files to `<app-name>`, your cloned from openshift

9) Use git to add and commit the changes file your directory:

   `git commit -a -m "added fedena-openshift files"`

10) Push your changes to openshift:

`git push`

11) SSH to your openshift application and change to the application root directory.

   `rhc ssh <app-name>`

12) Execute the following to populate your application database with tables:

   `bundle exec rake db:migrate RAILS_ENV="production"`

13) Populate your tables with initial data with the following command:

   `bundle exec rake db:seed RAILS_ENV="production"`

Your fedena school management should be fully deployed to openshift using fedena-openshift

#Default Login Details

 You can log in with following usernames and passwords:

  ` Username - admin, password - admin123`
    

#For detailed installation instruction

Visit  http://learnfedena.com/how-to-install-fedena-on-openshift 

#Community Support:

<a href = http://www.learnfedena.com >www.learnfedena.com</a> is a community driven Questions and Answers website which allows the open source community of Fedena school management software members gets advice and assistance from other members of the community.

#Fedena : Open source school management system

<a href= http://www.projectfedena.com>Project Fedena</a> is the open source school management system based on Ruby on Rails. It is developed by a team of developers at Foradian Technologies. The project was made open source by Foradian, and is now maintained by the open source community. Fedena is the ideal solution for schools and campuses that want an easy means to manage all campus records.


#License

Fedena is released under the Apache License 2.0.
