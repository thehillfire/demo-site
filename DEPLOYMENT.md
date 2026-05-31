# Deployment Guide

This document provides step-by-step instructions for deploying the demo-site to Netlify and Render.

## Netlify Deployment

### Prerequisites
- GitHub account with this repository
- - Netlify account (free tier available)
 
  - ### Steps
 
  - 1. **Connect GitHub to Netlify**
    2.    - Go to https://app.netlify.com
          -    - Click "New site from Git"
               -    - Connect your GitHub account
                    -    - Select the `thehillfire/demo-site` repository
                     
                         - 2. **Configure Build Settings**
                           3.    - Build command: (leave empty for static site)
                                 -    - Publish directory: `.` (root directory)
                                      -    - The `netlify.toml` file will handle advanced configuration
                                       
                                           - 3. **Deploy**
                                             4.    - Click "Deploy site"
                                                   -    - Wait for build to complete
                                                        -    - Your site will be available at `[site-name].netlify.app`
                                                         
                                                             - ### Automatic Deployments
                                                             - After initial connection, any push to the `main` branch will automatically trigger a new deployment.
                                                         
                                                             - ## Render Deployment
                                                         
                                                             - ### Prerequisites
                                                             - - GitHub account with this repository
                                                               - - Render account (free tier available)
                                                                
                                                                 - ### Steps
                                                                
                                                                 - 1. **Connect to Render**
                                                                   2.    - Go to https://dashboard.render.com
                                                                         -    - Click "New +" → "Static Site"
                                                                              -    - Connect your GitHub account
                                                                                   -    - Select the `thehillfire/demo-site` repository
                                                                                    
                                                                                        - 2. **Configure Settings**
                                                                                          3.    - Name: `demo-site` (or preferred name)
                                                                                                -    - Build Command: (leave empty)
                                                                                                     -    - Publish Directory: `.`
                                                                                                      
                                                                                                          - 3. **Deploy**
                                                                                                            4.    - Click "Create Static Site"
                                                                                                                  -    - Wait for deployment to complete
                                                                                                                       -    - Your site will be available at `[site-name].onrender.com`
                                                                                                                        
                                                                                                                            - ## Custom Domains
                                                                                                                        
                                                                                                                            - Both platforms support custom domains:
                                                                                                                        
                                                                                                                            - **Netlify**: Add domain in Site Settings → Domain Management
                                                                                                                            - **Render**: Add domain in Settings → Custom Domains
                                                                                                                        
                                                                                                                            - ## Environment Variables
                                                                                                                        
                                                                                                                            - If you need environment variables:
                                                                                                                        
                                                                                                                            - **Netlify**: Add in Site Settings → Build & Deploy → Environment
                                                                                                                            - **Render**: Add in Environment in the site settings
                                                                                                                        
                                                                                                                            - ## Continuous Integration
                                                                                                                        
                                                                                                                            - Both platforms automatically:
                                                                                                                            - - Detect changes pushed to GitHub
                                                                                                                              - - Run builds automatically
                                                                                                                                - - Deploy to production
                                                                                                                                  - - Provide preview URLs for pull requests
                                                                                                                                   
                                                                                                                                    - ## Troubleshooting
                                                                                                                                   
                                                                                                                                    - ### Build Fails
                                                                                                                                    - - Check build logs in the platform dashboard
                                                                                                                                      - - Verify `netlify.toml` configuration
                                                                                                                                        - - Ensure all dependencies are listed
                                                                                                                                         
                                                                                                                                          - ### Site Shows 404
                                                                                                                                          - - Verify publish directory is correct
                                                                                                                                            - - Check that `index.html` is in the root directory
                                                                                                                                             
                                                                                                                                              - ### Custom Domain Not Working
                                                                                                                                              - - Allow 24-48 hours for DNS propagation
                                                                                                                                                - - Verify DNS records are correctly configured
                                                                                                                                                  - - Check platform's domain documentation
                                                                                                                                                   
                                                                                                                                                    - ## Performance Optimization
                                                                                                                                                   
                                                                                                                                                    - The site includes:
                                                                                                                                                    - - Cache headers in `netlify.toml`
                                                                                                                                                      - - Optimized asset serving
                                                                                                                                                        - - CDN distribution (included with both platforms)
                                                                                                                                                         
                                                                                                                                                          - ## Support
                                                                                                                                                         
                                                                                                                                                          - - **Netlify Docs**: https://docs.netlify.com
                                                                                                                                                            - - **Render Docs**: https://render.com/docs
                                                                                                                                                              - - **GitHub Pages**: Alternative free option
                                                                                                                                                                - 
