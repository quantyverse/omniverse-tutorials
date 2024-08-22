# Setting Up Your Development Environment

This guide will help you set up your development environment for working with the Omniverse Kit App Template. Following these steps will ensure that your environment is properly configured for building, testing, and deploying applications using Nvidia Omniverse.

## 1. Clone the Kit App Template Repository

Start by cloning the Kit App Template repository from GitHub to your local machine:

    git clone https://github.com/NVIDIA-Omniverse/kit-app-template.git

Navigate into the cloned repository:

    cd kit-app-template

## 2. Set Up the Required Tools

- **Install Dependencies**: Ensure your development environment is equipped with the latest version of Python. The Kit App Template is optimized for use with Visual Studio Code, though other IDEs like PyCharm can also be used.
- **NVIDIA RTX GPU**: Make sure your development machine has an NVIDIA RTX GPU with the latest drivers installed. This hardware is essential for running Omniverse applications efficiently.

## 3. Build the Project

To build the project, use the provided scripts according to your operating system:

- **Windows**: 
      
      .\repo.bat build
  
- **Linux**:
  
      ./repo.sh build

This command compiles the necessary components and prepares your environment for running the Omniverse applications.

## 4. Launch the Application

After building the project, you can launch the application:

- **Windows**:
      
      .\repo.bat launch
  
- **Linux**:
  
      ./repo.sh launch

During the launch process, you'll be prompted to select the `.kit` file associated with your application, typically located in the `_build` directory.

## 5. Explore and Customize

- **Extension Manager**: After launching, open the Extension Manager by navigating to `Window > Extensions` to explore and enable various extensions. This allows you to extend the functionality of your application.
- **Customization**: Start by exploring and customizing the reference applications included in the template, such as the USD Explorer. This will help you understand how to configure and modify Kit-based applications.

## 6. Additional Resources

For more detailed instructions and advanced configuration options, refer to the official [Omniverse Kit App Template documentation](https://docs.omniverse.nvidia.com/kit/docs/kit-app-template/latest/docs/intro.html). You can also configure your environment to use community-developed extensions by adjusting the registry settings.

---

By following these steps, you'll have a fully functional development environment for creating and customizing applications within Nvidia Omniverse using the Kit SDK.
