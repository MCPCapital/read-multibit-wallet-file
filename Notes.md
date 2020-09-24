@MCPCapital - I built/used this tool almost 2 years ago, so I forget the exact hoops I jumped through in order to get it to build. That being said, I still have that build on my linux box, so I pushed the generated files (plus an NPM shrinkwrap file, which is just a publishable version of package.lock) to my fork. So if you run:

 npm i -g git+https://github.com/DavidKDeutsch/read-multibit-wallet-file.git
then it will install it directly from my fork, you should just be able to run it without building (if you already have the official one installed, you may want to uninstall it first). Note that during install you may see a bunch of errors regarding not being able to find Visual Studio and whatnot related to node-gyp, but if towards the end you see something saying "Pure JS implementation will be used," then the failures should not matter; it just means it could not create an optimized build, and when you run mbexport it will simply run the js that was installed instead of an executable binary.

I tried it out on the test wallet files in the source code and it seemed to work (I don't have my old wallets around to test), so give it a shot and let me know how it works out.

—
