# gha-ssh-agent

GitHub Action to configure SSH agent for CI/CD pipelines. This action allows you to set up an SSH agent in your GitHub Actions workflow, enabling secure access to private repositories and servers during your CI/CD processes.

## Usage

To use this action in your GitHub Actions workflow, add the following step to your workflow YAML file:

```yaml
- name: Set up SSH Agent
  uses: gha-ssh-agent@v1.0.0
  with:
    ssh-key: ${{ secrets.SSH_PRIVATE_KEY }}
    hosts: |-
      github.com
      gitlab.com
    ssh-key-types: "rsa,ed25519"
    known-hosts: |-
      github.com ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEA...
      gitlab.com ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAI...
    command-line-interpreter: bash
```

## Contributing

Check out the [CONTRIBUTING](CONTRIBUTING.md) file for guidelines on how to contribute to this project.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
