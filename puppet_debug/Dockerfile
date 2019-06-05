FROM simonanderson/ssh:centos7

#install Puppet agent (for facter):
RUN sudo rpm -Uvh https://yum.puppet.com/puppet6/puppet6-release-el-7.noarch.rpm; echo "puppetlabs" | sudo yum -y install puppet-agent

#RUN yes y | /opt/puppetlabs/puppet/bin/gem install puppet-debugger


COPY Dockerfile / 
