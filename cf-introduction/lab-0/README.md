# Registration at CloudFoundry.com

If you don't already have an account at CloudFoundry.com, you can sign
up at [www.cloudfoundry.com](http://www.cloudfoundry.com).

When your registration is approved, install `vmc` and test that you
can log in.  If you have Linux or Windows with Cygwin you can follow
the instructions below (Mac users probably OK too).  See
[installation instructions on Cloud Foundry](http://cf-docs-deprecated.cloudfoundry.com/tools/vmc/installing-vmc.html)
for more detailed instructions with platform differences.

Installing vmc is easy once you have installed Ruby and RubyGems on
your computer.  You may find it useful to install them using
[`rvm`](http://beginrescueend.com/rvm/install/):

    $ \curl -L https://get.rvm.io | bash -s stable
    $ source ~/.bash_profile
    $ rvm requirements
    $ rvm install 1.9.3

Open a terminal (Linux) and execute the following command (use `sudo` on Linux if you are not using `rvm`):

    $ gem install vmc --no-ri --no-rdoc -v 0.3.18

Execute the `vmc target` command to specify the Cloud Foundry target to which you will deploy your applications.  The following command targets the Cloud Foundry PaaS:

    $ vmc target api.cloudfoundry.com

To determine your current target, execute the `vmc target` command without any parameters:

    $ vmc target

Login using the user credentials you received via email after you registered with Cloud Foundry. Your username is typically your email address.

    $ vmc login

Ensure you have successfully logged in by retrieving information about your account:

    $ vmc info

