=====TO UPDATE NODE AND NPM============
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.2/install.sh | bash && nvm install stable --reinstall-packages-from=node
nvm install node && nvm use node

=====TO START and TEST PREVIEW=========
npm install && npm start

=====TO DEPLOY ON GITHUB==============
git remote remove origin
rm -rf .git
rm -rf build
npm install && npm run build
cd build
git init
git remote add origin https://github.com/hansfzlorenzana/hansfzlorenzana.github.io.git
git add .
git commit -m "Change"
git push origin main