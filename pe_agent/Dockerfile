FROM simonanderson/ssh:centos7
RUN sudo rpm -Uvh https://yum.puppet.com/puppet5/puppet5-release-el-7.noarch.rpm; echo "puppetlabs" | sudo yum -y install puppet-agent
# RUN curl -kO http://enterprise.delivery.puppetlabs.net/2018.1/ci-ready/puppet-enterprise-2018.1.5-rc1-148-gaf610b5-el-7-x86_64.tar

#    "puppet-master" = [
      # Autosign nodes from domain
#      "echo '*.${var.domain}' | sudo tee /etc/puppetlabs/puppet/autosign.conf",

      # Download the Puppet Enterprise installer
#      "while : ; do",
#      "  until curl --max-time 300 -o pe-installer.tar.gz \"https://pm.puppetlabs.com/cgi-bin/download.cgi?dist=el&rel=7&arch=x86_64&ver=latest:\"; do sleep 1; done",
#      "  tar -xzf pe-installer.tar.gz && break",
#      "done",

      # Install Puppet enterprise
 #     "cat > pe.conf <<-EOF",
 #     "${var.pe_conf}",
 #     "EOF",
 #     "sudo ./puppet-enterprise-*/puppet-enterprise-installer -c pe.conf",

      # Run Puppet a few times to finalise installation
 #     "until sudo /opt/puppetlabs/bin/puppet agent -t; do sleep 1; done",


COPY Dockerfile / 
