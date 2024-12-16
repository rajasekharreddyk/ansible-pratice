## Ansible Key components/terms
`Inventery`: List of nodes to which ansible controller server should communicate
   * By default location availiable at `/etc/ansible/hosts`, but we can pass our custom inventery as well by using `-i`.
     
`Modules`:
   *  Module is the smallest automation unit in ansible
   *  For every task we want perform, we need to check the relevant module from asnible.
   *  Based on the module selected, we need to pass the arguments.
     
`Task`:
   * Task in ansible will be consisting of Modules.

 `Play`:
   * Play in ansible will be consisting of multipile tasks.
     
`Playbook`:
   * Playbook in ansible will be consisting of one or more plays.
