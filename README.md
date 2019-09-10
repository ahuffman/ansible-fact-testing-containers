# ansible-fact-testing-containers
The purpose of this repository is to house Dockerfile's for [ansible-fact](https://github.com/ahuffman/ansible-fact) automated testing.

## Repository Information
The repository contains a `.travis.yml` for automated builds of our test containers.

The `.travis.yml` launches travis.sh.

[travis.sh](travis.sh) launches the build-containers.yml Ansible playbook, which builds out our testing containers, pre-installed with Ansible and any Python dependencies required.

## License
[MIT](LICENSE)

## Authors
[Andrew J. Huffman](https://github.com/ahuffman)
