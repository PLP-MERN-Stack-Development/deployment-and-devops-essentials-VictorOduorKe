# backend deploy
1. Create a render account using github account
2. At the top right select new to initilaze new project
3. Connect your project repository and follow the instructions
4. Dont forget to add the following environment variables

 ```bash
JWT_SECRET=YOUR_SUPER_SECRET_JWT_KEY
CLIENT_URL=front_end_live_url
LIVE_MONGODB_URI=your_live_mongo_uri
 ```
 5. deploy your project and if there is no error it should indicate live and be given backend url, copy it to be used in frontend

# Frontend deploy
1. Create an account in vercel using github
2. nitialize new poject suing the Add new button
3. configure the repo with your poject
4. folllow the remaining steps to setup project
5. Add the environment variables

```bash
VITE_API_BASE_URL=your_live_backend_url
```
6. deploy your project and if successfull you will receive a domain url to navigate to the project




## 🌐 Deployment Links
- Frontend (Vercel): https://blog-post-ecru.vercel.app
- Backend (Render): https://deployment-and-devops-essentials-985a.onrender.com

## ⚙️ CI/CD Pipeline
This project uses GitHub Actions for Continuous Integration:
- On every push or pull request, both the client and server are built and tested.
- Vercel and Render handle automatic deployment on successful merges.

### Workflow File
See `.github/workflows/ci.yml`.

## 🩺 Monitoring
- Health check endpoint: `/api/health`
- Monitoring via Render dashboard logs and uptime checks
- health check image

[Health check image](./images/health.png)
