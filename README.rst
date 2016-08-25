How to run this demo
====================

Step: 1
-------

Install vagrant and required plugin for your host:

- https://github.com/projectatomic/adb-atomic-developer-bundle/blob/master/docs/installing.rst

Step: 2
-------

Use docker vagrant file for `vagrant up`

- https://github.com/projectatomic/adb-atomic-developer-bundle/blob/master/components/centos/centos-docker-base-setup/Vagrantfile

Step: 3
-------

Install eclipse for your host ( tested this project on Version: Neon Release-4.6.0 )

- https://eclipse.org/downloads/

Step: 4
-------

Install Eclipse Docker Tooling plugin-2.0.0 from Eclipse Marketplace.
(Help => Eclipse Marketplace)

Step: 5
-------

Get details of Docker daemon info which is running by vagrant box

`vagrant service-manager env docker`

Step: 6
-------

Click `Open Perspective` from right hand side top corner and select `Docker Tooling`.

- Select `TCP Connection` on popup window when you add a docker connection.
- Put a `Connection Name` can be anything like `mytest_Connection`
- URI: output from Step: 5 should be like `tcp://172.28.128.8:2376`
- Click on Enable authentication and put path from output of step-5, should be
  like `/Users/prkumar/work/vagrant/adb/.vagrant/machines/default/virtualbox/docker`

Step: 7
-------

- Clone this repo and export it to your eclipse workspace.
- Then select Dockerfile and then run it as `Docker Image Build`.

After build successful you have a container running which can be checked in
Docker explore tooling window.
