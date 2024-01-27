## Getting Started

Welcome to the VS Code JavaFx world. Here is a guideline to help you get started to write Java and use JavaFx code in Visual Studio Code.

## Folder Structure

The workspace contains two folders by default, where:

- `src`: the folder to maintain sources
- `lib`: the folder to maintain dependencies

Meanwhile, the compiled output files will be generated in the `bin` folder by default.

> If you want to customize the folder structure, open `.vscode/settings.json` and update the related settings there.

## Dependency Management

The `JAVA PROJECTS` view allows you to manage your dependencies. More details can be found [here](https://github.com/microsoft/vscode-java-dependency#manage-dependencies).

## Install JavaFx

In first time, install the folders in [JavaFx](https://openjfx.io/openjfx-docs/#introduction).
Create `LocalApps->OpenJFX` and store the foldres in `OpenJFX`.
Then, in VsCode install the extention pack: `Extension Pack for Java` by Microsoft.

In Vscode, use command: `ctrl+shift+p` and typing `Java: Create Java Project...`

If you have Maven:

- Select `JavaFx`, this create JavaFx project with Maven

If you don't have Maven:

- Select `No build tools`
- Select folder for store you project
- Choose name for your project
- This create simply Java project
- Go to your Java project 
- In lib, paste the files .jar 

Where are the jar files ? 

- In zip or dezip file JavaFx that you have installed
- Go to `LocalApps->OpenJFX->lib`
- Slect all jar file and paste in `lib` folder in your Java project

Then, in your project, go to `src` folder, usually they is `App.java` here.
Open `App.java` and copy/paste this code : 

```java
import javafx.application.Application;
import javafx.stage.Stage;

public class App extends Application{

    @Override
    public void start(Stage primaryStage) throws Exception
    {
        primaryStage.show();
    }
    public static void main(String[] args) throws Exception {
        launch(args);
    }
}
```

I don't explain the code but the goal is create and display the window with JavaFx. 

## Last step
In your terminal, go to your project and execute this command in src folder:

1- Compilate the code :
```bash
javac --module-path D:/LocalApps/OpenJfx/lib --add-modules javafx.controls App.java
```
The `D:/LocalApps/OpenJfx/lib` is an exemple, write the path where are installed JavaFx.

2- Execute the program:
```bash
java --module-path D:/LocalApps/OpenJfx/lib --add-modules javafx.controls App
```

With this command, you should have a windin open, 
Congratulation, you have create your first Window with Java and JavaFx.