
# Rails Virtual Development Environment on Vagrant

Configuration files to automatically set up a basic and customizable Vagrant box with the required tools to develop Rails projects.


## Usage

1. Install in your computer the software listed the "Prerequisites" section.
2. Clone the repository into your machine.
3. Tweak the provider and the options in the `Vagrantfile`.
4. Run `vagrant up` and wait for the machine to be built, then `vagrant reload`.
5. When the machine is ready, run `vagrant ssh` and move to the synced folder with `cd /vagrant`.
6. You may now start a new Rails project with `rails new .` or adjust the Ruby and gems settings with RVM to match an existent code base.


## Prerequisites

* [Vagrant][0]
* [Virtualbox][1] and the extension pack.

If you notice that there are delays with the synchronization of shared folders with `virtualbox` as the `type`, a better option is to use [SSHFS][2] or [NFS][3]. But usually it works well enough.


## Out of the Box Included Software

* **[Ubuntu Bionic][4]**: This Linux distribution is closer to the one used on the Heroku-18 stack.

* **Ruby 2.5.x (with [RVM][5])**: Programming language that supports the Rails framework. The Ruby Version Manager allows to easily use different Ruby versions and gems per project.

* **[Rails][11]**: And other gems to aid the development of web apps. (Current gem distributions):
  - RSpec
  - Cucumber
  - Mailcatcher
  - Pry-Byebug
  - PG
  - Redis-Rails
  - Webpacker
  - Bundler

* **[Yarn][12] and [Webpacker][13]**: For Rails projects with heavy use of JavaScript.

* **[Node.js][6]**: Server side JavaScript runtime. (Current stable version).

* **[Postgres][7]**: Advanced SQL database. (Current Bionic distribution).

* **[Redis][8]**: In-memory data structure store. (Current Bionic distribution).

* **[Heroku CLI][9]**: Create and manage Heroku apps from the command line.

* **[AWS CLI][16]**: Create and manage AWS apps from the command line.

* **[Ngrok][15]**: Exposes local servers behind NATs and firewalls to the public internet over secure tunnels.

* **ZSH Shell (With [Oh-My-Zsh!][14])** Tools to improve the experience of working with the shell.

---
[0]: https://www.vagrantup.com/downloads.html
[1]: https://www.virtualbox.org/wiki/Downloads
[2]: https://fedoramagazine.org/vagrant-sharing-folders-vagrant-sshfs/
[3]: https://www.vagrantup.com/docs/synced-folders/nfs.html
[4]: https://app.vagrantup.com/ubuntu/boxes/bionic64
[5]: https://rvm.io/
[6]: https://nodejs.org/en/
[7]: https://www.postgresql.org/
[8]: https://redis.io/
[9]: https://devcenter.heroku.com/articles/heroku-cli
[10]: https://www.heroku.com/
[11]: https://rubyonrails.org/
[12]: https://yarnpkg.com/
[13]: https://github.com/rails/webpacker
[14]: http://ohmyz.sh/
[15]: https://ngrok.com/
[16]: https://aws.amazon.com/
