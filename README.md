# Cool Store Microservice Demo

This repo uses our [openshift-applier Ansible role](https://github.com/redhat-cop/casl-ansible/tree/master/roles/openshift-applier) to automate the deployment of the [Cool Store Microservice Demo](https://github.com/jbossdemocentral/coolstore-microservice). If you are unfamiliar with the Cool Store, [this OpenShift Common video](https://blog.openshift.com/openshift-commons-briefing-64-modern-application-architecture-beyond-microservices-full-stack-demo/) will bring you up to speed. As of now, this automation does not include the CI / CD components of the demo, just the deployments.


## Usage

1. clone the repository
    - `git clone https://github.com/rht-labs/coolstore-microservice-demo.git`
2. install the Ansible role via galaxy, preferably in the local directory as shown below
    - `ansible-galaxy install -r requirements.yml -p roles
3. run a playbook provided by the Ansible role with the inventory provided here
    - `ansible-playbook -i inventory/ --connection=local roles/casl-ansible/playbooks/openshift-cluster-seed.yml`

For details on the demo itself, please see [Cool Store Microservice Demo README](https://github.com/jbossdemocentral/coolstore-microservice/blob/1.1.x/README.md)
