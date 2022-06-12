# Net Ninja Typescript Tutorial

Youtube typescript tutorial code-along with my personal notes and experiments.

Youtube URL: https://www.youtube.com/watch?v=2pZmKW9-I_k&list=PL4cUxeGkcC9gUgr39Q_yD6v-bSyMwKPUI&index=2

### Acknowledgements

[The Net Ninja](https://github.com/iamshaunjp/typescript-tutorial)

### Setup

Install the typescript NPM package locally to this project's node_modules folder by running the following in the project folder's cli:

npm i typescript --save-dev

### Basic workflow:

Create a file called index.ts and write some ts in it. Then, in the cli, run 'tsc index.ts'. This compiles the ts in index.ts into js into a new file that is automatically called index.js in the same directory.

The command 'tsc index.ts' is short for 'tsc index.ts index.js', which compiles ts into a new js file of the same name. If you want the js output file name to be something other than 'index.js', you can specify it like this: 'tsc index.ts somefile.js'

The watch mode recompiles on every save: 'tsc index.ts -w'

### tsconfig workflow:

The previous workflow is fine if you have a simple html, css, and ts file structure, but if you have a /src file and a bundled output file like /public (or /dist or whatever), you need to use a tsconfig.json file and run the 'tsc' commands with it.

Create one by running 'tsc --init' and in it, inside "compilerOptions", set "rootDir" to "./src" and "outDir" to "./public". And outside of "compilerOptions", use "'include':["src"]" to only compile things from inside the src folder. Otherwise, any ts files even from outside/src will be compiled into /public.

Now running 'tsc' (or better yet, 'tsc -w') will compile the ts files in /src and output them into js file in /public.