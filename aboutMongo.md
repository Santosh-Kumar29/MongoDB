->MongoDB is an open-source document database and leading NoSQL database.

->Collection
	Collection is a group of MongoDB documents. It is the equivalent of an RDBMS table. A collection exists within a single database. Collections do not enforce a schema.

->Document
	A document is a set of key-value pairs
	
RDBMS	    	MongoDB
____________________________________________

Database		Database
Table			Collection
Tuple/Row		Document
column			Field
Table Join		Embedded Documents
Primary Key		Primary Key (Default key _id provided by MongoDB itself)

->MongoDB is a document-based non-relational database management system. It's also called an object-based system. It was designed to supplant the MySQL structure as an easier way to work with data. On the other hand, MySQL is a table-based system (or open-source relational database)


->Why Use MongoDB?
	#Document Oriented Storage − Data is stored in the form of JSON style documents.
	#Index on any attribute
	#Replication and high availability
	Professional support by MongoDB
	
->Data Model Design
	MongoDB provides two types of data models: — Embedded data model and Normalized data model
	
	-->Embedded Data Model
		In this model, you can have (embed) all the related data in a single document, it is also known as de-normalized data model
	-->
		{
			_id: ,
			Emp_ID: "10025AE336"
			Personal_details:{
				First_Name: "Radhika",
				Last_Name: "Sharma",
				Date_Of_Birth: "1995-09-26"
			},
			Contact: {
				e-mail: "radhika_sharma.123@gmail.com",
				phone: "9848022338"
			},
			Address: {
				city: "Hyderabad",
				Area: "Madapur",
				State: "Telangana"
			}
		}
	-->Normalized Data Model
		In this model, you can refer the sub documents in the original document, using references. For example, you can re-write the above document in the normalized model as:
		
		Employee:

				{
					_id: <ObjectId101>,
					Emp_ID: "10025AE336"
				}
		Personal_details:

			{
				_id: <ObjectId102>,
				empDocID: " ObjectId101",
				First_Name: "Radhika",
				Last_Name: "Sharma",
				Date_Of_Birth: "1995-09-26"
			}
			
		Contact:

			{
				_id: <ObjectId103>,
				empDocID: " ObjectId101",
				e-mail: "radhika_sharma.123@gmail.com",
				phone: "9848022338"
			}
			
			
			
