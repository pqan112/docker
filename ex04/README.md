# Run React vite with container

1. Pull node image
2. Mapping local with container with volume
3. Create react vite app
4. npm i
5. add `"dev": "vite --host"` in `pakage.json`
6. add to dockerfile CMD ["npm", "run", "dev"]
7. run command `docker run -v .:/app/web -p 3000:5173 -it react:002`
