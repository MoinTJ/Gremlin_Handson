# Gremlin_Handson
Gremlin Hands-on, on Windows Server with Free Gremlin Account

# Whats is Chaos Engineering ? 
"Chaos Engineering is the discipline of experimenting on a system in order to build confidence in the system’s capability to withstand turbulent conditions"

To specifically address the uncertainty of distributed systems at scale, Chaos Engineering can be thought of as the facilitation of experiments to uncover systemic weaknesses. These experiments follow four steps:

1) Start by defining ‘steady state’ as some measurable output of a system that indicates normal behavior.
2) Hypothesize steady state/Create a Hypothesis Scenarios
   Introduce variables that reflect real world events like servers that crash,Sudden CPU Spike,High Memory Consumption, hard drives that malfunction, network connections that are    severed, etc.
3) Run Experiments  / Automate Experiments to Run Continuously / Schedule as per the needs
4) Measure the BlastRadius & Analyze the behaviour 

Ulimate Goal : The harder it is to disrupt the steady state, the more confidence we have in the behavior of the system

There are number of tools avaiable in market : pls see the link with pros & cons 
https://www.gremlin.com/community/tutorials/chaos-engineering-tools-comparison/

# Before you begin this tutorial you need the following: Prerequisites 
1) Windows Server 2019 host
2) Gremlin account ( Free Sign up )


# Now Lets Play with Gremlin on Windows Server 

# 1 Create an Account / Register it  : https://app.gremlin.com/login  ( Click on "New to Gremlin? Sign up for free" Create an account)
![image](https://user-images.githubusercontent.com/55667819/127996374-de61e4c7-2c1d-46a5-acf8-8b4d334a98dc.png)

# 2 Once Account Created, Should be able to login & able to view dashboard page as below 
![image](https://user-images.githubusercontent.com/55667819/127996729-3c343c66-cb8f-46be-ab3f-580ac029a848.png)

# 3 Click on Profile Button (![image](https://user-images.githubusercontent.com/55667819/128007467-01e225b6-4c71-4cd1-b949-536cb08ee355.png))

Click on Team Settings --> Configuration Tab --> generate [Team ID,Secret Key,Certificates] 

![image](https://user-images.githubusercontent.com/55667819/128000688-7c4254d1-f63a-420e-897a-d4e1519c69b6.png)

# 4 Now Download the Gremlin Agent / Installer from below link & Install on Windows Server 
https://www.gremlin.com/community/tutorials/how-to-install-and-run-gremlin-on-windows/ 

![image](https://user-images.githubusercontent.com/55667819/128008746-ff9230a4-139d-4c5b-9a99-5e2dc5a766a4.png)


# 5 Once Installation completed --> Navigate to [C:\ProgramData\Gremlin\Agent\config.yaml]

Gremlin's configuration file on Windows is located at C:\ProgramData\Gremlin\Agent\config.yaml. Please note that ProgramData is a hidden folder. You can either type in the address on File Explorer or show hidden folders then navigate interactively.

you will see an example of this file at C:\ProgramData\Gremlin\Agent\config.yaml.example copy this file or remove to the .example suffix, and fill in the file with your desired configuration
Edit the Yaml file, Uncomment # & Give details of Team ID,Certificates Path for .Pem files  or Team ID & Secret Key or Through Enviroment varaibales as mentioned in Gremlin Agent link, follow only 

![image](https://user-images.githubusercontent.com/55667819/128011600-87e99e90-59b3-450d-b97e-e113b7ca745b.png)

# 6 Now Navigate to Services from Start Menu and --> "Navigate to Gremlin Daemon Agent " Restart the Gremlin Daemon Agent 

![image](https://user-images.githubusercontent.com/55667819/128013472-e1a60dfe-c2ba-4d23-b9be-f197d912896b.png)

# 7 On Dashboard Page of your free Gremlin Account : Click on "Create Attack" 
![image](https://user-images.githubusercontent.com/55667819/128015627-80e9ea87-e143-4b57-b925-b6db200ea422.png)

# 8 You will navigated to Attacks Tabs --> Click on Infra Tab --> You should be able to view 1 Hosts Available to Perform Chaos on it.
![image](https://user-images.githubusercontent.com/55667819/128016114-7b9cb993-c208-4887-bac1-80922039025f.png)

# 9 Click on Choose Hosts to Target  (Slide the Button to view the details)
![image](https://user-images.githubusercontent.com/55667819/128016397-337a23a5-5f19-46f1-a5e2-758b72ff5fe9.png)

# 10 Now scroll down little below to "Choose a Gremlin" Attack  | Understand your requirements w.r.t Category & Respective Attacks

![image](https://user-images.githubusercontent.com/55667819/128017224-8491a83d-8dc4-47dd-89f9-c9b4d6eaad08.png)

# 11 for Sample we will be selecting CPU Attacks under Category Resource : Provide the Attacks details like Length of test(seconds),CPU,Cores as shown below
![image](https://user-images.githubusercontent.com/55667819/128017502-2541ba1f-2ca6-4c37-909a-ee04ae4c93eb.png)

# 12 Now Click on "UnLeash Gremlin" Button 
![image](https://user-images.githubusercontent.com/55667819/128017761-e60c4aed-131c-4b51-a16a-514898ceafca.png)

# 13 Hurray !!!!!  You did Choas with CPU resource Utilization 
![image](https://user-images.githubusercontent.com/55667819/128017986-6b88d80c-33f6-4527-86b1-b0ba21fa936e.png)

![image](https://user-images.githubusercontent.com/55667819/128018015-f57c0e54-8de8-4b2b-91d0-5c6e7faabd88.png)

# 14 Now for Memory Go back to | Step 10 | --> Select Memory Attack
![image](https://user-images.githubusercontent.com/55667819/128018335-30a902bc-dca9-49d2-8034-3af27e9b2bde.png)


# 15 Observe the memory Consumtption during the chaos attacks 
![image](https://user-images.githubusercontent.com/55667819/128018614-3df37625-5f13-4eac-990a-0fbec100036b.png)

# 16 During the execution if you wnt to stop any test, due to any issues or any deviation just click on Halt Button

![image](https://user-images.githubusercontent.com/55667819/128018758-7e72c513-e6b2-4fe6-a07d-fab248fa7918.png)

# Hope this is Informative 
# Happy Chaosing  :)  



