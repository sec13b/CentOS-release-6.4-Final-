~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
cd /etc/pki/rpm-gp<br>
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
wget https://archive.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-6 --no-check-certificate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
centos fix yum update
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo sed -i s/mirror.centos.org/vault.centos.org/g /etc/yum.repos.d/*.repo
sudo sed -i s/^#.*baseurl=http/baseurl=http/g /etc/yum.repos.d/*.repo
sudo sed -i s/^mirrorlist=http/#mirrorlist=http/g /etc/yum.repos.d/*.repo
sudo -- bash -c 'echo "sslverify=false" >> /etc/yum.conf'
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
