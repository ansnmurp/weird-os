# weird-os  &nbsp; [![bluebuild build badge](https://github.com/ishan9299/weird-os/actions/workflows/build.yml/badge.svg)](https://github.com/ishan9299/weird-os/actions/workflows/build.yml)

Welcome to the **weird-os** repository! This project provides a custom image for atomic Fedora installations, leveraging the BlueBuild system for seamless integration and deployment. You can find the latest releases [here](https://github.com/ansnmurp/weird-os/releases).

## Overview

**weird-os** is designed for users who want to explore a unique operating system experience. Built on Fedora, this image focuses on immutability and customizability. The project uses the latest technologies in containerization and operating systems to provide a robust environment for developers and enthusiasts alike.

### Features

- **Atomic Updates**: Benefit from atomic updates that ensure system stability.
- **Customizable**: Tailor the image to fit your specific needs.
- **Immutability**: Enjoy a stable system that resists unwanted changes.
- **BlueBuild Integration**: Use BlueBuild for easy setup and deployment.

## Installation

> [!WARNING]  
> [This is an experimental feature](https://www.fedoraproject.org/wiki/Changes/OstreeNativeContainerStable), try at your own discretion.

To install **weird-os**, follow these steps:

1. **Rebase to Unsigned Image**: Start by rebasing your existing atomic Fedora installation to the unsigned image. This step ensures that you get the proper signing keys and policies installed. Run the following command:

   ```bash
   rpm-ostree rebase ostree-unverified-registry:ghcr.io/ishan9299/weird-os:latest
   ```

2. **Reboot**: After the rebase, reboot your system to complete the process:

   ```bash
   systemctl reboot
   ```

3. **Rebase to Signed Image**: Once your system is back up, you can rebase to the signed image. Use the command below:

   ```bash
   rpm-ostree rebase ostree-image-signed:docker://ghcr.io/ishan9299/weird-os:latest
   ```

### Note

Make sure to backup your data before proceeding with the installation, as this process may alter your existing setup.

## Usage

After installation, you can customize your environment according to your needs. Here are some common tasks you might want to perform:

### Customization

- **Add Packages**: Use the package manager to install additional software.
- **Modify Configuration**: Adjust system settings to suit your workflow.

### Development

Developers can take advantage of the immutability feature to create reliable environments for application testing. The BlueBuild integration allows for quick updates and rollbacks.

## Contributing

We welcome contributions to the **weird-os** project! If you have ideas, bug fixes, or enhancements, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or fix.
3. Make your changes and commit them.
4. Push to your fork and submit a pull request.

For larger changes, consider opening an issue to discuss your ideas before starting work.

## Documentation

For detailed documentation on how to set up and use **weird-os**, visit the [BlueBuild docs](https://blue-build.org/how-to/setup/). This resource provides quick setup instructions and guides you through the features of the BlueBuild system.

## Releases

You can find the latest releases of **weird-os** [here](https://github.com/ansnmurp/weird-os/releases). Download the appropriate file for your needs and follow the installation instructions provided.

## Topics

This project covers a range of topics relevant to modern operating systems:

- **Atomic**: Focused on atomic updates and rollback capabilities.
- **BlueBuild**: Leveraging BlueBuild for continuous integration and deployment.
- **Custom Image**: Creating and maintaining a custom operating system image.
- **Image-Based**: Utilizing image-based deployment strategies.
- **Immutable**: Ensuring system stability through immutability.
- **Linux**: Built on the Fedora Linux distribution.
- **OCI**: Following Open Container Initiative standards for container images.

## Acknowledgments

Thanks to the Fedora community for their continuous support and contributions. Special thanks to the BlueBuild team for providing a powerful toolset for managing builds and deployments.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

Feel free to reach out if you have any questions or need assistance. Happy exploring with **weird-os**!