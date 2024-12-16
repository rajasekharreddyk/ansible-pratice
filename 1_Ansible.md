## Pull and Push based
* In pull based CM, on the worker nodes we need to install a `software agent` of the CM server w is responsible for communication, and making sure the desired state is met,
* In `Push` based CM, there will be `no agents` required on the nodes,
* In push based CM. the CM server needs to have the below onces.
     * List of all the nodes communicate, ans make the desred state met
     * the credentials to communicate to the nodes
     * IT will use protocals SSH/Winrm to communicate to the nodes.
* CM tools like chef,pupet are pull base CM.
* Ansible is the push based CM.
* the agents on the pull based periodically check for any configuration changes from the central server.
* 
