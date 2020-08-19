npm init
npm install --save electron

package.json -> "start": "electron ."


Note #1
--------
Menu creation note:

On Mac, 
#1 it seems that the menu item must have submenu otherwise Mac will bypass it
#2 on Mac the first menu item is occupied by Electron, so you have to use unshift funciton. But don't know why mainMenuTemplate.unshift({}) didn't work, but mainMenuTemplate.unshift({label: ''});


Note #2
--------
Electron Uncaught ReferenceError: require is not defined発生時の対処法
https://teratail.com/questions/220803

        webPreferences: {
            nodeIntegration: true,
        }


Noet# 3
--------
npm install --save-dev electron-packager
npm run package-mac