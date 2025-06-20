# VPC Module
This module is developed for joindevops company. Projects inside joindevops follows this module to create their VPC.

# Inputs
* project (required) - Users should specify their project name
* environment (required) - Users should specify their environment
* cidr_block (optional) - Users can provide their CIDR block. Default is 10.0.0.0/16

# steps to create VPC Module

* create VPC
* create IGW
* attach VPC to IGW

* create 2 public subnets
* create 2 private subnets
* create 2 database subnets

* create public route table
* add internet as route through IGW
* attach to public-1a and public-1b

* create private route table
* attach to private-1a and private-1b

* create database route table
* attach to database-1a and database-1b

* create eip
* create nat gateway with eip

* add routes to private and db route table through NAT 0.0.0.0/0

* associated public rt with public subnets
* associated private rt with private subnets
* associated database rt with database subnets

* peering connection with default VPC
* add routes with destination of default VPC CIDR in roboshop route tables routes
* add routes with roboshop vpc CIDR as destination in default VPC main route table


