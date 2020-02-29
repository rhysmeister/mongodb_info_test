# mongodb_info_test
Test for a MongoDB PR

Just a little test for the mongodb lookup plugin for PR: https://github.com/ansible/ansible/pull/67846

Get a test MongoBD instance running in docker with the following (no auth)...

```
docker run -tid --mount source=mongo,target=/var/lib/mongo --rm -p 27017:27017 --name mongodb rhyscampbell/dockermongodb
```


```
virtualenv venv
source venv/bin/activate
pip install ansible
ansible-playbook -l localhost test_mongodb_info.yml
```

Throws following error...


```
pip install pymongo
```

Now playbook run should work...

```
ansible-playbook -l localhost test_mongodb.yml
```
