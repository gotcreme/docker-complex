This project was created for Stephen Grider's Udemy Course: Docker And Kubernetes: The Complete Guide

# Project Workflow

1. Push code to github master branch
2. Travis-ci automatically pulls repo
3. Travis builds a test image, tests code
4. Travis builds prod images
5. Travis pushes built prod images to docker Hub
6. Travis pushes project to AWS ElasticBeanstalk (just needs Dockerrun.aws.json file to kick off process)
7. EB pulls images from Docker Hub and deploys them using Dockerrun.aws.json file
