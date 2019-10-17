# MySQL Migration from Iaas to Paas

## Table of contents

[Overview](#Overview)

[Pre-Requisites](#Pre-requisites)

[Creating MySQL Server in Azure Portal](#creating-mysql-server-in-azure-portal)

[MySQL Migration using Workbench](#mysql-migration-using-workbench)

## Overview

**** need to provide the overview of the lab *******

##  Pre-requisites

*   Azure portal Access.
*   Familiar with Azure portal.

**Note**: Azure Portal access is provided as part of the Lab environment

## Creating MySQL Server in Azure Portal

1.Using the Chrome browser, login into Azure portal with the below details.

```
Azure Username: {{ Azure Portal Username }}

Azure Password: {{ Azure Portal Password }}

```

![alt text](https://qloudableassets.blob.core.windows.net/microsoft-learning/Az900/Lab4-Web%20Apps%20and%20cloud%20services/portal1.png?st=2019-08-22T11%3A08%3A20Z&se=2020-08-23T11%3A08%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=fm%2BDTeOkr2f0%2BS344uOTMlPzHxDsCisvhsf4Jo1LzmY%3D)

![alt text](https://qloudableassets.blob.core.windows.net/microsoft-learning/Az900/Lab4-Web%20Apps%20and%20cloud%20services/portal2.png?st=2019-08-22T11%3A09%3A36Z&se=2020-08-23T11%3A09%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=ONwSsJE%2B5ENkff6wqI098VfdvzB77ezY7PxjamtqBgQ%3D)

![alt text](https://qloudableassets.blob.core.windows.net/microsoft-learning/Az900/Lab4-Web%20Apps%20and%20cloud%20services/portal3.png?st=2019-08-22T11%3A09%3A59Z&se=2020-08-23T11%3A09%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=5JhMvyxOF4PJSrB3u4M9KLit%2B9IqG6MrVjUObzyLaGg%3D)

![alt text](https://qloudableassets.blob.core.windows.net/microsoft-learning/Az900/Lab4-Web%20Apps%20and%20cloud%20services/portal4.png?st=2019-08-22T11%3A10%3A23Z&se=2020-08-23T11%3A10%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=QKaTSjnXbhdQ1wkIajvEAwwAJvuUfoQn7NBkmBQa2C4%3D)

Click on **+Create** a resource -> **Databases** -> **Azure DB For MySQL** 

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/1.png?st=2019-10-17T10%3A25%3A40Z&se=2022-10-18T10%3A25%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=PW1yXIRT9hYVj6AVG6UFuhbDWPR%2FJHEr6L47jOyQ1Tc%3D)

Enter the following details to configure the database

```
    Server name: any friendly unique server name
    Subscription: select teh default Subscription
    Resource Group: {{ ResourceGroup }}
    Select Source : Blank
    Server admin login name : testadmin or any friendly name
    Password : Qwerty@123456
    Location : {{ Location }}
    Version: 5.7
    Pricing Tier : Click on the link and Select Basic

```
Click on Create to provision the database.

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/2.png?st=2019-10-17T10%3A26%3A16Z&se=2022-10-18T10%3A26%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=qV3LP8EuOZO%2Bk22XKiXeg3Yls2DdYpXJ5pFxDqsdr0I%3D)

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/3.png?st=2019-10-17T10%3A26%3A39Z&se=2022-10-18T10%3A26%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=tGX3c0YU7iOIVdZ3wewfGd9eq6J8tStBZemFty9NiEg%3D)

## MySQL Migration using Workbench 
 
Download and Install MySQL Workbench from the following URL.
 
https://dev.mysql.com/downloads/workbench/
 
Install by **double-clicking** the installation file and follow the steps as below by clicking **Next** where ever applicable.
 
![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/4.png?st=2019-10-17T10%3A27%3A09Z&se=2022-10-18T10%3A27%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=qxdgCiHA7VOAftk%2BVe%2FFpuuaE7OzbabRa4Oac%2B%2Bguo4%3D)

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/5.png?st=2019-10-17T10%3A27%3A30Z&se=2022-10-18T10%3A27%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=C2zUb2L961vOC5c23gm6U6sXI0DQtCglA821GYH9WGc%3D)

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/6.png?st=2019-10-17T10%3A28%3A29Z&se=2022-10-18T10%3A28%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=keoad7Yd%2Bfx3Oq2GKD13HMoZ47sx2Z%2Bgd8JXW6A%2B%2F0U%3D)

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/7.png?st=2019-10-17T10%3A28%3A46Z&se=2022-10-18T10%3A28%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=0OifJJmJJWJns8M3uNjZUKZeFadyjXYKJuJ%2FmMcPSkU%3D)

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/8.png?st=2019-10-17T10%3A29%3A03Z&se=2022-10-18T10%3A29%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=CWBvmGJOSfgqeybhjwPkDccBR%2FsK4DTxbEzOSaYUNKs%3D) 
 
 
Open **Workbench** from **Start Menu** after installing it.

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/9.png?st=2019-10-17T10%3A29%3A24Z&se=2022-10-18T10%3A29%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=u77A%2FwT9x%2FzL0Mm%2B7GmJwIvd9CFwDmg3b6UIrV9%2FyY0%3D)
 
Click **+** beside **MySQL Connections** to add a connection. Enter the following details.

``` 
    Connection Name: On-prem or whatever suits your needs
    Hostname : IP address or FQDN of your source DB
    Username : 
    Click on Store in Vault and enter the password and Click OK

```
![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/10.png?st=2019-10-17T10%3A29%3A56Z&se=2022-10-18T10%3A29%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=L1kF%2BcJdkaV8iFjh69o9grSXWVfRa7cqMnt6Dmf%2F%2FXk%3D)

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/11.png?st=2019-10-17T10%3A30%3A12Z&se=2022-10-18T10%3A30%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=DFGtUvI9Gb%2FMGPs%2Fb0SwxZnkLgeP1jnt1Di1HxsjdxI%3D)

 
Login to the **IaaS VM of the DB** using **Putty**. Connect to MySQL using the following command

``` 
    mysql -uroot -pWelcome123
``` 

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/12.png?st=2019-10-17T10%3A30%3A31Z&se=2022-10-18T10%3A30%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=tjzfS8ezsIKhL0jRO2WkNIaE24nwZycUTeF3zoHE9JM%3D)
 
Once connected to **MySQL**, enter the following command by **changing the IP to yout IP address**.
 
```
    grant all on *.* to root@<<IP You are connecting from>> IDENTIFIED BY ' Welcome123';
```

>   Note: you can get the ip of your machine by click on Test connection in Workbench.
	 
![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/13.png?st=2019-10-17T10%3A31%3A11Z&se=2022-10-18T10%3A31%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=cmy2fnqPJ%2BvfjUtyQsqMwanYbSjtB%2BeAArD5EjM9KM0%3D)

Click on **test connection** to ensure you entered all the details correctly .

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/14.png?st=2019-10-17T10%3A31%3A32Z&se=2022-10-18T10%3A31%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=UPLXB8tY%2Bf5NbFHJyS%2FY5Uwvl8r6sO%2FrTJMeak2iEM0%3D)


Open the **MySQL PaaS Database** in Azure Portal .

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/15.png?st=2019-10-17T10%3A32%3A28Z&se=2022-10-18T10%3A32%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=gkB4XA8ZC7H3uRK5IOEy1Pra%2FqvP%2BBbcm%2Fq%2FtBog%2F5c%3D)

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/16.png?st=2019-10-17T10%3A32%3A48Z&se=2022-10-18T10%3A32%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=7GSrZ%2BYvdajdiZRquAp8iAfarPX9AticeUQNI%2Bl%2FwZo%3D)

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/17.png?st=2019-10-17T10%3A33%3A11Z&se=2022-10-18T10%3A33%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=1lfR0hsmaUSwel8oFojBBbFNAclZiTFLwJmx1q8sZbs%3D)
  
Click on **Connection Security** and add a **firewall rule** as below and hit save.

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/18.png?st=2019-10-17T10%3A33%3A30Z&se=2022-10-18T10%3A33%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=z1y0iRd6BbQOs009FTN7XIfh68bplRPj1s8%2Bld1MX6E%3D)
   
Add this connection to **MySQL Workbench** just as we did for the on-prem connection. Give a **connection name, enter the Hostname, Username and Password of the MySQL PaaS**.
 
Open the **MySQL Overview page** in Azure portal to obtain the **username and server name**. You can **reset the password here** and use it to connect.

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/19.png?st=2019-10-17T10%3A33%3A53Z&se=2022-10-18T10%3A33%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=VFboD%2FBaWPW13ZwQx0ktHM7QfrB1BpdNPVhAwCOck8Q%3D)

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/20.png?st=2019-10-17T10%3A34%3A14Z&se=2022-10-18T10%3A34%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=Ft1YDDLXKU8BnkTNhhPiYLR7dGLw2hKLIo3AyZstvto%3D)

Click on **test connection** to ensure connectivity.
 
![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/21.png?st=2019-10-17T10%3A34%3A31Z&se=2022-10-18T10%3A34%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=1AFOTVDZI55Tdhki1GXVUdR0Q0jpNr0ra0ZCGSuY%2BaI%3D) 
 
You should see the **2 connections** in Workbench's dashboard as below.
 
![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/22.png?st=2019-10-17T10%3A35%3A37Z&se=2022-10-18T10%3A35%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=CR6iKrEjZ0Z%2B0MUx0pp7IUFAJhEaMQnPZ%2B85%2BaKohNU%3D)

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/23.png?st=2019-10-17T10%3A35%3A54Z&se=2022-10-18T10%3A35%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=6ol2Ione0JZWPYT451Bh9%2BzhAzMUMtKI5eKI2Tu0VNU%3D)
  
Click on **Database -> Migration Wizard** to begin the migration.

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/24.png?st=2019-10-17T10%3A36%3A11Z&se=2022-10-18T10%3A36%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=Atpbzh%2BhQ5DIL%2Ff0WxKCwZFxs6og7HEb7Utdn9SqPbY%3D)
 
Click on **start Migration**.

Select the **Source Database --> On-prem** in this case and click **Next**.

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/25.png?st=2019-10-17T10%3A36%3A30Z&se=2022-10-18T10%3A36%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=TvWZ9A4pygQPegOsQB%2Fk5PXRReHffstmm%2Fh5brEbrKE%3D)
 
Select the **target database --> Azure** in this case and click **next**.
 
![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/26.png?st=2019-10-17T10%3A36%3A48Z&se=2022-10-18T10%3A36%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=5Wr3Ow7xEXOZ%2FUJO2oezCHpu18yDTq7VfzpM5dEi9Dk%3D)
 
The wizard validates **connectivity** and then click **next**.

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/27.png?st=2019-10-17T10%3A37%3A07Z&se=2022-10-18T10%3A37%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=cRyTdj0DjF853ugQYUBBcUSuTs5v%2F%2FVHOVt2vRyw%2FBY%3D) 
 
Select the Schema to be migrated. **Demo_DB** in this case.

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/28.png?st=2019-10-17T10%3A37%3A25Z&se=2022-10-18T10%3A37%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=tjMUpb6K3gbqM0CtpF%2BMQe2uEev8xKVGFbRR9k7S6gE%3D)

Wizard with perform the required steps and once validated, click **Next**.
 
![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/29.png?st=2019-10-17T10%3A37%3A42Z&se=2022-10-18T10%3A37%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=BzHDOm8q31CkwbNrd9frC2AYEjKd7iOJ6nM2tHClal4%3D)
 
Click on **Show Selection** to see the tables being migrated. Click **Next**.

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/30.png?st=2019-10-17T10%3A38%3A04Z&se=2022-10-18T10%3A38%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=H1nElYIB8pnjFDTxU1MHKmI%2FWs0CaeVmWHzsnCFAWKM%3D) 
 
Click **Next**.

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/31.png?st=2019-10-17T10%3A38%3A28Z&se=2022-10-18T10%3A38%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=9J5fXXA5zo%2BeC%2BCXVzbypzGCG%2F3%2BNbuss6pnZ611ufc%3D) 
 
The wizard will show **any Warnings or Errors here**. Click on **Next**.

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/32.png?st=2019-10-17T10%3A38%3A45Z&se=2022-10-18T10%3A38%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=8SGRmfrac2XcipOEzbwNX1GdnPxq5M4N%2Bp%2FzeLNreJg%3D)
 
Select **Create Schema in Target RDBMS** since we are migration to a **blank database**. Click **Next**.
 
![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/33.png?st=2019-10-17T10%3A39%3A03Z&se=2022-10-18T10%3A39%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=fZSs6AfqOeLFk7tE1kfk60FrsRDndtvH0sPOpdAMQ%2Fs%3D)
 
Click **Next**.
 
![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/34.png?st=2019-10-17T10%3A39%3A20Z&se=2022-10-18T10%3A39%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=e6QVo8QQ4lkqyEFjeBmKMk78eCUIRrJ8j4wabpHEIoo%3D)

Wizard will **show the SQL Statements** for objects being migrated. Click **Next**.

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/35.png?st=2019-10-17T10%3A39%3A37Z&se=2022-10-18T10%3A39%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=HwWGYOwqDzE3fSU9hEvwnLyFYylvqon%2Bv5jwG8QDE8g%3D) 
 
Use **Online Copy** since the VM has connectivity to both databases. Click **Next**.

![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/36.png?st=2019-10-17T10%3A39%3A59Z&se=2022-10-18T10%3A39%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=njV%2F%2ButQAV6qTzvgRk4zhoufraIBCRmKoRbZIs26%2Bz8%3D)
 
Click **Next**.
 
![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/37.png?st=2019-10-17T10%3A40%3A17Z&se=2022-10-18T10%3A40%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=u1N6iVFvPlUOypuAU8xGX4L78OFb59MngL5ujZAzPCo%3D)
 
After Successful Migration, the wizard gives you the summary. Click **Finish**.
 
![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/38.png?st=2019-10-17T10%3A40%3A36Z&se=2022-10-18T10%3A40%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=1GvzCfuH0D%2FJN3iKFPKGd32VQWSx44%2B2DsBcRnwKQ4g%3D) 
 
Connect to the databases to validate successful migration.
 
Use the following Queries to validate. Execute them sequentially.

```
    Use Demo_DB;
    Show Tables;
    Select count(*) from wp_options;

```
![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/39.png?st=2019-10-17T10%3A40%3A54Z&se=2022-10-18T10%3A40%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=11X%2BDI6XK1a1GeIhHH6PCikBKqM%2BurYJJ%2BGYeXi3oNY%3D)

Run same commands on **Azure** and you should see the same output.
 
```
    Use Demo_DB;
    Show Tables;
    Select count(*) from wp_options;
```
![alt text](https://qloudableassets.blob.core.windows.net/migration-labs/My%20Sql%20Migration%20from%20Iaas%20to%20Paas/40.png?st=2019-10-17T10%3A41%3A11Z&se=2022-10-18T10%3A41%3A00Z&sp=rl&sv=2018-03-28&sr=b&sig=pShJ493ntJtI82JNrV7VjBIvLh16vS%2BOry1l54mZM7w%3D)
