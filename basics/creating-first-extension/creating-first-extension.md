# Creating your first extension in Nvidia Omniverse

This guide will help you to create your first extension in the App you just created here [Create Frist App / Setting up Environment](basics/setting-up-environment/setting-up-environment.md)


## 1. Create and Configure New Extension From Template

Run the following command to initiate the configuration wizard:

**Linux:**

```bash
./repo.sh template new
```

**Windows:**

```batch
.\repo.bat template new
```


Follow the prompt instructions:

* **? Select with arrow keys what you want to create:** Extension
* **? Select with arrow keys your desired template:** Basic Python Extension
* **? Enter name of application .kit file [name-spaced, lowercase, alphanumeric]:** [set extension name]
* **? Enter application_display_name:** [set extension display name]
* **? Enter version:** [set extension version]

> **Note:** You can choose between different Extension types like pure Python extension or Python UI extension which will have pre generated content tailored for the specific type. I recommend to have a look at these extensions.


## 2. Build the Extension

So the extension to be added to your app you have to build the application again, use the provided scripts according to your operating system:

- **Windows**: 
      
      .\repo.bat build
  
- **Linux**:
  
      ./repo.sh build

This command compiles the necessary components and prepares your environment for running the Omniverse applications with your new extension.

## 3. Launch the Application

After building the project, you can launch the application and see if your extension was created as expected:

- **Windows**:
      
      .\repo.bat launch
  
- **Linux**:
  
      ./repo.sh launch

During the launch process, you'll be prompted to select the `.kit` file associated with your application, typically located in the `_build` directory.

## 4. Start your Extension

- **Extension Manager**: After launching, open the Extension Manager by navigating to `Window > Extensions` to explore and enable various extensions. Type the name of your extension you just created and start it.

## 5. Additional Resources

For more detailed instructions and advanced configuration options, refer to the official [Omniverse Kit App Template documentation](https://docs.omniverse.nvidia.com/kit/docs/kit-app-template/latest/docs/intro.html).

---

By following these steps, you'll have a fully functional extension you can now use to develop. Check out the other chapters on how to fill the extension with content.
