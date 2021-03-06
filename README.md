anodeDraw
=========

A NodeJS Multiplayer Drawing Space. The app will let users draw on the page by dragging and moving their mice, and will display the results on a large canvas element. What sets is apart from all the other similar experiments though, is that people will see each other in real time as they do so. To achieve this, we will leverage the socket.io library for node.js, which uses a range of technologies from websockets to AJAX long polling to give us a real time data channel. Because of this, the example works in all modern browsers.


Installing node.js
===================

To run the game you will need to install node.js. It shouldn’t take more than a few minutes and is fairly straightforward.
If you are on Windows, you can go ahead and download the installer from its official site. If you are on Linux or OSX, 
you will need to run this set of commands in your terminal :-

>
echo 'export PATH=$HOME/local/bin:$PATH' >> ~/.bashrc
. ~/.bashrc
mkdir ~/local
mkdir ~/node-latest-install
cd ~/node-latest-install
curl http://nodejs.org/dist/node-latest.tar.gz | tar xz --strip-components=1
./configure --prefix=~/local
make install # ok, fine, this step probably takes more than 30 seconds...
curl https://npmjs.org/install.sh | sh

After you finish installing, you will also get access to npm, or node package manager. 
With this utility you can install useful libraries and bits of code that you can import into your node.js scripts. 
For this example, we will need the socket.io library I mentioned above, and node-static, which will serve the HTML, 
CSS and JS files of the drawing application. Again, open up your terminal (or a new command prompt window if you 
are on Windows) and write the following command:

npm install socket.io node-static
This shouldn’t take more than a few minutes to complete.

Running the Application
=========================

Navigate to the folder in command prompt and then type :-
>node app.js
