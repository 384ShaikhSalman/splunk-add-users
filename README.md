# Splunk-add-users
👤 Splunk: Creating a Second User
Welcome to this guide for adding a second user in Splunk. This README is designed to help Splunk admins create additional users with appropriate roles and permissions for team collaboration, monitoring, or dashboard access.
________________________________________
📌 Prerequisites
Before proceeding, ensure you have:
•	✅ A working Splunk installation (e.g., Splunk Enterprise or Free)
•	✅ Admin credentials for Splunk Web Interface or CLI
•	✅ Port 8000 open if accessing via web (http://localhost:8000)
________________________________________
🛠️ Step-by-Step: Create a New Splunk User
1. 🔐 Login to Splunk Web
•	Navigate to: http://<your-splunk-ip>:8000
•	Login using your admin credentials
________________________________________
2. ⚙️ Navigate to User Management
•	Click on Settings (top right corner)
•	Under Users and Authentication, click Access Controls
•	Select Users
________________________________________
3. ➕ Add New User
•	Click "New User"
•	Fill in the required details:
Field	Value (Example)
Username	analyst_user
Full Name	Security Analyst
Password	StrongPassword123!
Email	user@example.com
Roles	user, power, or custom
💡 Choose roles carefully. power has more access than user. Use admin only if needed.
________________________________________
4. 💾 Save User
•	Click "Save" to create the new user
•	New user can now log in using:
makefile
CopyEdit
Username: analyst_user  
URL: http://<your-splunk-ip>:8000
________________________________________
🔄 Optional: Create a Custom Role
If you want fine-grained access control:
1.	Go to Access Controls → Roles
2.	Click New Role
3.	Assign:
o	Indexes to search
o	Capabilities (like search, edit_dashboards, etc.)
4.	Assign this role to the new user
________________________________________
🚨 Best Practices
•	🔑 Use strong passwords
•	🧪 Test role permissions before giving wide access
•	📊 Limit access to only necessary dashboards or indexes
________________________________________
📁 File-Based (CLI) Method (Optional)
You can also create users via users.conf:
ini
CopyEdit
[user1]
password = changeme123
roles = user
email = user@example.com
•	Location: $SPLUNK_HOME/etc/system/local/users.conf
Restart Splunk after editing:
bash
CopyEdit
$ splunk restart
________________________________________
✅ Final Check
Once setup is complete, test login as the new user and verify:
•	Access to correct dashboards
•	Search permissions
•	Alerting capabilities (if assigned)
________________________________________
📚 Resources
•	Official Splunk Docs – User Management
•	Role-based Access Control

Author : Shaikh Salman Kaleem
384shaikhsalman@gmail.com
🎯 SOC Analyst in Training
🔐 Focus: Threat Detection | Splunk | IDS/IPS | Linux Security | Real-World Projects
