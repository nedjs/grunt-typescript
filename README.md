grunt-typescript
================

Compile TypeScript

## Documentation
You'll need to install `grunt-typescript` first:

    npm install grunt-typescript

Then modify your `grunt.js` file by adding the following line:

    grunt.loadNpmTasks('grunt-typescript');

Then add some configuration for the plugin like so:

    grunt.initConfig({
        ...
        typescript: {
          base: {
            src: ['path/to/typescript/files/**/*.ts'],
            dest: 'where/you/want/your/js/files',
            options: {
              module: 'amd', //or commonjs
              target: 'es5', //or es3
              base_path: 'path/to/typescript/files'
            }
          }
        },
        ...
    });
   
If you want to create a js file that is a concatenation of all the ts file (like -out option from tsc), 
you should specify the name of the file with the '.js' extension to dest option.

    grunt.initConfig({
        ...
        typescript: {
          base: {
            src: ['path/to/typescript/files/**/*.ts'],
            dest: 'where/you/want/your/js/file.js',
            options: {
              module: 'amd', //or commonjs
            }
          }
        },
        ...
    });



※I'm sorry for poor English