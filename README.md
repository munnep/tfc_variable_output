# tfc_variable_output
tfc variable output

# Example: Using variables with TFC

Within TFC and TFE you can add variable definitions add different levels [See documentation](https://www.terraform.io/cloud-docs/workspaces/variables#special-environment-variables) 

In the following step by step you will see the impact on what the variables do at different levels

# How to

- Clone/Fork this repository to your own VCS
- Within TFC make a new workspace that points to this repository  
- Run it for the first time. You will see the following output     
![](media/2022-03-11-10-42-24.png)  
- On the workspace level add a variable with something different for default_variable  
![](media/2022-03-11-10-44-04.png)  
- run a new plan  
![](media/2022-03-11-10-45-05.png)  
- go to settings --> variable sets --> new variable set  
 ![](media/2022-03-11-10-47-34.png)  
- Make a new run  
![](media/2022-03-11-10-50-23.png)  

What happens when we add a global variables with the intention of changing the workspace variable and default variable?
- add 2 variables to your global variable settings    
![](media/2022-03-11-10-53-07.png)  
- we see that only the default variable of the code is overwritten  
![](media/2022-03-11-10-54-56.png)  
- change the global_variable at workspace level  
![](media/2022-03-11-10-56-02.png)  
- You see in the bottem it gets overwritten  
![](media/2022-03-11-10-57-04.png)  
- Realize where you set your variables

