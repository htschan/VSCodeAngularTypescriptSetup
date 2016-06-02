## Steps to setup a Web client project using Visual Studio Code, Angular 1.x, Typescript   

The following tools are required:
* NodeJS
* Bower
* NPM
* TSC Typescript compiler
* TSD Typescript definition manager
* Visual Studio Code
* live-server (NPM) to serve the files to the browser


These are the steps to setup a project:

1. Install Nodejs
2. Install Bower: ```npm install bower -g```
3. Goto Folder <myproject>
4. ```bower init```
5. Ceate subfolder "app"
6. Create .bowerrc
        {
            "directory": "app/bower_components"
        }
7. Install Typescript: ```npm install typescript -g```
8. Install TSD: 

    ```npm install tsd -g```

    ```tsd query angular```
    
    ```tsd install angular angular-material --save```
9. Install Angular: ```bower install angular-material --save```
10. Create folder _src_ and _dist_ below _app_
11. Create an __all.ts_ in _src_ and put all your references in it
```
    // <reference path="../../typings/tsd.d.ts" />
    /// <reference path="boot.ts" />
    ```
12. Create a _tsconfig.json_ file in _src_
13. Compile in _src_ with ```tsc.cmd -w``` to watch and compile
14. Install Server: ```npm install live-server -g```

The resulting folder structure looks like this
```
--<<myproject>>-+-<<app>>------+--<<bower_components>>

                |              +--<<dist>>
            
                |              +--<<src>>
            
                |              +--index.html
            
                |
            
                +-<<typings>>
            
                +-.bowerrc
            
                +-bower.json
            
                +-Readme.md
            
                +-tsd.json
```
    

        
    