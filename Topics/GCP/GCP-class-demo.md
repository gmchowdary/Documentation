Lab
	Cloud Shell
		- Run Dummy Application
```
npm install sails -g
git clone https://github.com/gmchowdary/gcp-sails-demo.git
cd gcp-sails-demo
sails lift --port 2019 --host 0.0.0.0
```

		- Preview on web console
	Storage
		- create storage
		- insert data
		- set permissions
	
	Compute Engine
		Settings
			Regione
		Meta Data
			ssh key
		VM instance(Not network)
			create
			Bottom high cpu less memory
		Instance Group
			Managed instances(Multizone and regional)
				auto scaling
			unmanaged insances(Regiional)
				Add and remove instance
		Instance template immutable

	stackdirver logging

	IAM(Resource Autherization)
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
				- 
				
		Lab

	Networking
		- Routing(OSI 7 layer model)(Think about Data flow perspictive)(Decision Where data should go next)(Latency reduction)
		- Load Balancing
		- Global VPC and VPNs for connection, self learning
		
		- Subnets are static
		
	Databases




MySQL
VM Instance
	Task 1 - Create VM instance with
		- GCP-SSH into VM
		- Install Apache2
			- sudo apt update
			- sudo apt install apache2
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

Script for Auto Scaling
```
sudo apt update
sudo apt install stress
sudo stress --cpu  1 --timeout 60
```

Script for Load Balencing
```
sudo apt update
sudo apt install apache2
echo $(date) > index.html
sudo mv ~/index.html /var/www/html
service apache2 start
```

Storage

Memory Store
	- Create redis (Wait)
	- Create VM
	- Install redis
		sudo apt update
		sudo apt install redis-server
	- connect to redis
		redis-cli -h x.x.x.x
	- Insert Data
		set x 10
		get x

