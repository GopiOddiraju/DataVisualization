# HW 2 - CS 625, Fall 2023

Gopi Oddiraju  
Due: September 20, 2023



### Part 1. Data Cleaning

Created a new project in OpenRefine using PetNames.tsv dataset as shown below.

![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/6a65e0b4-4c0a-4626-86b6-849058c92cf4)




Cleared leading and trailing white spaces in all cells in all columns using Edit cells > Common transforms > trim leading and trailing spaces option.

![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/e975a0bb-6c2d-4b54-917d-bdbe91d1cf48)


Renamed the columns with appropriate names using the edit column> rename column option.

![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/0ffff94b-6320-4175-beeb-cfba36810844)



#### Kind of Pet Column
Created a text facet for "Kind of Pet" column. Using the cluster option, merged each kind of species with different names into one (used different methods along with different keying functions.). There were 69 different kinds of pets at first. 

![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/f9acf8f7-6740-473c-8712-c1586666f75f)

![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/364bc521-fa5a-4840-bba4-eeb3afd619cf)


Manually corrected a few of them which could not be done using the cluster option. ex: God as Dog, Car as Cat, Dlg as Dog, Sog as Dog. (By selecting the type and clicking on the edit option). Identified a few blank fields as Dogs based on their breed. Changed a few others based on my knowledge ( Bunny as Rabbit, beta fish as fish). There was a row with the value "dog, dog, dog, cat". Using split muti-valued cells options ("," as separator), divided into multiple records as below.

![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/61b3321a-212e-477a-8f7f-f96867f7ffa0)


After making all these changes, finally, there are 30 different kinds of pets left including blank as a type. ( Kept Human, Virus as it is). 

![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/c377a56a-b04a-489d-8180-6fbf6fc93640)


#### Pet's full name column
Then, I moved on to the Pet's full name column. Applied a text facet and used clusters with different types of keying functions. 

![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/9344066a-d98d-487c-b6b2-4906979d43dd)

![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/cb1692b1-41b6-4cb7-b0f3-ce0be9234431)

As Names are Nouns, I kept most of them as it is ( for eg: I considered Scarlett and Scarlet as different names. ) Used clusters mostly for removing case sensitivity and merged them.


#### Pet's everyday name column

I followed the same procedure for this as Pet's full name column.

![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/e76d77dc-27cc-42d1-b137-2608833c8deb)



#### Pet's Age column

There were a lot of inconsistencies in this column's data format. At first, created a text facet and found out that there are 204 different choices.

![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/4ea1d494-8154-4fe0-8e41-e2c99afb3573)

Using value.replace("~", "") expression removed approximations. Here, selected only one record for the purpose of screenshot and made changes at all places.
![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/fd2957d0-1ce4-4d28-b4f2-d89c7e01e6f1)


Removed non-numeric values using the below expressions. Kept Deceased as deceased even when the age was known. Blanks and some symbols were considered Unknown.

![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/5e4b8e34-c59a-453d-a5ce-aeb358181a70)

![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/e3c78e61-baed-42b8-a588-74bfd0b74a67)


Converted months/weeks into years. Changed the column datatype from text to Number.

![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/2811ce76-49ab-4147-851a-acd5a70eae50)

![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/2a750134-5556-49a5-96ad-5019992a3695)





#### Pet's breed column

Followed the same steps such as removing leading and trailing spaces, and merging the same kind of breeds into one using clusters. 




### Part 2. Analyze Cleaned Data

1. How many types (kinds) of pets are there?

   There are 30 kinds of Pets. We can see that by creating a text facet to the kind of pet column.

   ![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/da5049c7-c1ff-42a5-86ae-7b255e6d9a10)

1. How many cats?

   500 Cats. We can see the number beside the type of pet.
   
1. How many breeds of cats?

   91 types. We can find out that by applying text facets to both the kind of pet and pet breed columns and selecting the cat. Then we can the total number of choices as shown below.

   ![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/f3111a0f-8ccb-41c0-92bf-842648540fce)

   
1. What's the most popular cat breed? How many cats are in that breed?

   **Domestic short-hair** breed. There are 69 such cats. We can find out by sorting them based on the count.

   ![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/efc0cfd0-cf99-4008-8fe9-ac2cad503c6d)

1. What's the age range of the cats?

   The age range of cats is from 0.1 years to 24 years. This can be found out by sorting the pet's age column after filtering the type of pet to the cat.

   
1. What's the age range of the rabbits? (*Don't forget to look for the bunny, too.*)

   The age range of cats is from 1.75 years to 13 years. This can be found out by sorting the pet's age column after filtering the type of pet to Rabbit( I already changed Bunnys to Rabbit).
   
1. What is the oldest pet? Give the pet's name, kind, and age.

   The oldest pet is a cat. The pet's full name is **Bruce Springsteen** and the pet's breed as per the given data is a cat, Its age is 24.

   
1. What are the top 5 most popular dog breeds? List the breed and number.

   The top 5 most popular dog breeds are **Golder Retriever**, **Mutt**, **Labrador Retriever**, **Border Collie**, **German Shepherd**. Apply text facets to the kind of pet and pet breed columns then select the dog in the kind of pet text facet, sort the pet breed facet by the count, and look for the first 5 breeds.

   ![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/75a52e0c-4b20-4b58-b99d-fe5d0c67b918)

1. What's the most popular everyday name for a dog?

   **Daisy** is the most popular everyday name for a dog. Apply text facets to the kind of pet and pet's everyday name columns, select the dog in the kind of pet facet, and then sort the most popular everyday name facet by the count.

   ![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/f9978dd3-caaa-49b0-94dc-4012df27bddd)


   
1. What's the most popular full name any pet?

   **Sophie** is the most popular full name for any pet. Apply text facet to the pet's full name column. Sort it by the count.

   ![image](https://github.com/odu-cs625-datavis/fall23-mcw-GopiOddiraju/assets/112833939/9961c171-dab2-4ef4-be68-82429eae4a47)


## References

https://www.youtube.com/watch?v=B70J_H_zAWM&list=PL737054C67FCC0741


https://vickysteeves.gitlab.io/2018-uutah-repro/cleaning-data.html

