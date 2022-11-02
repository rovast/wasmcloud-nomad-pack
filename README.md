# wasmcloud-nomad-pack

## Features

- Update vargant use ustc mirror ubuntu repository to speed up installing packages
- Update the nomad-pack repo to here

### Environment

I have placed a vagrant file in this directory just so everyone can share the 
same environment during development.  

Install [vagrant](https://github.com/hashicorp/vagrant#quick-start)

`vagrant up`

This should expose Nomad and Consul UIs

[http://localhost:4646](http://localhost:4646)   
[http://localhost:8500](http://localhost:8500)

### Install `nomad-pack`

Per [repo](https://github.com/hashicorp/nomad-pack) instructions

```bash
wget https://github.com/hashicorp/nomad-pack/releases/download/nightly/nomad-pack_0.0.1.techpreview.4-1_amd64.deb
dpkg -i nomad-pack_0.0.1.techpreview.4-1_amd64.deb
```

### Add registry

`nomad-pack registry add wasmcloud github.com/rovast/wasmcloud-nomad-pack`

### Launch wasmcloud pack

`nomad-pack run --registry=wasmcloud wasmcloud-host`

### Hit washboard

[http://localhost:4000](http://localhost:4000)

## More

If you want play on a nomad cluster, see [rovast/nomad-cluster-demo](https://github.com/rovast/nomad-cluster-demo) for demo.
