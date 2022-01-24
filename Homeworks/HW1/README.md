## Week 1 Homework

In this homework we'll prepare the environment 
and practice with terraform and SQL

## Question 1. Google Cloud SDK

Install Google Cloud SDK. What's the version you have? 

To get the version, run `gcloud --version`

**Answer** = 369.0.0

## Google Cloud account 

Create an account in Google Cloud and create a project.

- Project name: My First Project
- Project number:280442394302
- Project ID:elite-thunder-339103

## Question 2. Terraform 

Now install terraform and go to the terraform directory (`week_1_basics_n_setup/1_terraform_gcp/terraform`)

After that, run

* `terraform init`
* `terraform plan`
* `terraform apply` 

Apply the plan and copy the output (after running `apply`) to the form.

It should be the entire output - from the moment you typed `terraform init` to the very end.

## Prepare Postgres 

Run Postgres and load data as shown in the videos

We'll use the yellow taxi trips from January 2021:

```bash
wget https://s3.amazonaws.com/nyc-tlc/trip+data/yellow_tripdata_2021-01.csv
```

You will also need the dataset with zones:

```bash 
wget https://s3.amazonaws.com/nyc-tlc/misc/taxi+_zone_lookup.csv
```

Download this data and put it to Postgres

## Question 3. Count records 

How many taxi trips were there on January 15?

Consider only trips that started on January 15.

![img](https://github.com/gialkady/de_zoomcamp/blob/main/Homeworks/HW1/images/Question%203.%20Count%20records.png)

**Answer** = 53024

## Question 4. Largest tip for each day

Find the largest tip for each day. 
On which day it was the largest tip in January?

Use the pick up time for your calculations.

(note: it's not a typo, it's "tip", not "trip")

![img](https://github.com/gialkady/de_zoomcamp/blob/main/Homeworks/HW1/images/Question%204.%20Largest%20tip%20for%20each%20day.png)

**Answer** = 2021-01-20

## Question 5. Most popular destination

What was the most popular destination for passengers picked up 
in central park on January 14?

Use the pick up time for your calculations.

Enter the zone name (not id). If the zone name is unknown (missing), write "Unknown" 

![img](https://github.com/gialkady/de_zoomcamp/blob/main/Homeworks/HW1/images/Question%205.%20Most%20popular%20destination.png)

## Question 6. Most expensive locations

What's the pickup-dropoff pair with the largest 
average price for a ride (calculated based on `total_amount`)?

Enter two zone names separated by a slash

For example:

"Jamaica Bay / Clinton East"

If any of the zone names are unknown (missing), write "Unknown". For example, "Unknown / Clinton East". 

![img](https://github.com/gialkady/de_zoomcamp/blob/main/Homeworks/HW1/images/Question%206.%20Most%20expensive%20locations.png)

