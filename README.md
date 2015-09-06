# vcluster
a CLI for generating vagrantfiles and running cross platform clustered unittests from the command line


## How it works
So the way this app works is you can open `settings.yaml` in order to create a list of all of the vagrant images you want to build for. 

Then you specify what shell command you want to run on the VM. 

You should have a list that looks something like this.

```yaml
systems:
      - "hashicorp/precise32"
      - "ubuntu/trusty64"
      - "puphpet/centos65-x64"


command: "cat /dev/random"
```

Then when you run `python vcluster.py`, you should be able to watch the tests run on the different VMs, if anything is logged to standard error the output will appear in red. 

## Built at PennApps XII

![](http://2014s.pennapps.com/build/images/logo/dark1.png)

![](https://mlh.io/brand-assets/logo-grayscale/mlh-logo-grayscale-small.png)
