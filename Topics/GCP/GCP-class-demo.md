# Lab

## Task 0: Click On list to activate them
1. Cloud Shell
2. VM instance
3. Memory store
4. IAM
5. Storage
6. IAM
7. Stack driver Logging

## Task 1: Cloud Shell

1. Run Dummy Application
2. Run below commands
```
npm install sails -g
git clone https://github.com/gmchowdary/gcp-sails-demo.git
cd gcp-sails-demo
sails lift --port 2019 --host 0.0.0.0
```
3. Preview on web console

## Task 2: Storage Service
1. Create storage
2. Insert data
3. Set permissions
	- Bucket Level
	- Object Level
	
##	Task 3: Compute Engine
1. Settings
	- set default Regions
2. Meta Data
	- ssh key
3. VM instance(Not network)
	- create
	- Bottom high cpu less memory

## Task 4: create VM
1. Create VM
2. Execute below Commands GCP ssh console
```
sudo apt update
sudo apt install -y apache2
echo $(date) > index.html
sudo mv ~/index.html /var/www/html
service apache2 start
```
3. show output on console
4. Enable HTTP firewall rule
5. See on browser

## Task 5 Instance Template
1. Create instance template
2. Confuguration
```
sudo apt update
sudo apt install -y apache2
echo $(date) > index.html
sudo mv ~/index.html /var/www/html
service apache2 start
```
3. Launch Instance

## Task 6 Instance Group
## Task 6.1: Unmanaged insances(Regiional)
1. Add and remove instance

## Task 6.2: Managed instances(Multizone and regional)
1. Impliment auto scaling
2. Script for Auto Scaling
```
sudo apt update
sudo apt install -y stress
sudo stress --cpu  1 --timeout 60
```

### Instance template immutable

## Task 7: Stackdirver logging

## Taks 8: IAM(Resource Autherization)
		Explain
			- Any one can do CRUD
			- Limited Previlages(Organisation or project or service level)
			- Permission 
				- Service.Resource.Verb
			- Role - Collection of permissions
				- roles/service.role
				- Premitive Roles are owner, editor, viewer
			- Members(A known identity to GCP)
				can be
					- User (Human or member who have access)
					- Service (To manage apps or services
					- Groups (named collection one or more Users or service)
					- domain(Domain Name managed by G-Suit)
					- allAuthenticatedUsers(Logged in by us Google account)
			- Policies 
				- A policy binds members to roles for scope of resources
				- Only Allow, No Deny
				- Child policy will not effect parent policy
				- One policy per resource
				
		Lab

## Task 9: 
	Networking
		- Routing(OSI 7 layer model)(Think about Data flow perspictive)(Decision Where data should go next)(Latency reduction)
		- Load Balancing
		- Global VPC and VPNs for connection, self learning
		
		- Subnets are static
		
	Databases



## Task 10:
MySQL
VM Instance
	Task 1 - Create VM instance with
		- GCP-SSH into VM
		- Install Apache2
			- sudo apt update
			- sudo apt install -y apache2
			- service apache2 start
			- echo $(date) > index.html
			- sudo mv ~/index.html /var/www/html
		- execute below commands
			- curl localhost
		- Try pasting Public IP on Browser does not work
		- Click on Instance ID > Edit VM instance > Check HTTP(Observe network tags)
		- Refresh web browser Worked BOOM!
		- Delete VM
	
	- Task 2 - Create Template

## Task 11: Load Balencing
```
sudo apt update
sudo apt install -y apache2
echo $(date) > index.html
sudo mv ~/index.html /var/www/html
service apache2 start
```

## Task 12: MemoryStore
1. Create redis (Wait)
2. Create VM
3. Install redis
```
sudo apt update
sudo apt install -y redis-server
```
4. connect to redis
```
redis-cli -h x.x.x.x
```
5. Insert Data
```
set x 10
get x
```

