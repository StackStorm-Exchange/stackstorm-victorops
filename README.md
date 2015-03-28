#Victorops
This action enables the integration of Victorops into stackstorm. It is capable of performing the following actions
1. List all the open incidents on PD for a subdomain
2. Send acknowledgment of any incident or you can even send ACK for multiple incidents using comma seprated values
3. Close and open incident or you can even close multiple open incidents by providing comma sperated values
4. Launch an incident by giving its details and description

# Confgiuration

You need the following parameters to be in the config.yaml file
`api_key:` API-KEY
`routing_key:` ROUTING-KEY

##How to get API key
Once you sign in to your Victorops account go to the settings tab and click in Integrations button. A table will come at the right side, click on REST endpoint, It will spit out a Post URL, you just need to copy the part after `generic` becuase the first part is same for all. Copy and paste that part of API key in the config.yaml file.
![Alt text](/st2contrib/_images/api_key.png?raw=true "add API key")



##How to get Routing Key
Now to get the routing key you need to scroll down and you will see `Incident Routing` section. Click on `Add Rule`, then add the name of routing key and select the team to which you want to route the incident to. Once thats done copy the name that you just gave in routing key and paste it into the `config.yaml` file. The following images illustrate the steps.
![Alt text](/st2contrib/_images/add_rule.png?raw=true "add Rule")
![Alt text](/st2contrib/_images/routing_key.png?raw=true "add routing key")
![Alt text](/st2contrib/_images/done.png?raw=true "select team to route the incidents to")
