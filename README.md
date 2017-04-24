#######################
1. Ruby 2.2.0 is required. puppet 4 server/agent installation and r10k/hiera gem installation
2. Update /etc/puppetlabs/r10k/r10k.yaml with below content an change the ownership of the file to 'puppet:'
---
cachedir: '/var/cache/r10k'
sources:
  production:
    remote: 'https://github.com/srimandarbha/production'
    basedir: '/etc/puppetlabs/code/environments'
    environments: 'production'
3. Run "r10k deploy environment pv"
