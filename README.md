# Troubleshooting-Kubernetes-Volume-Mounts-with-Nginx-and-PHP-FPM
In this task, I encountered an issue with volume mounts in a Kubernetes cluster while working on a Nginx and PHP-FPM based setup. The pod, named 'nginx-phpfpm', had been functioning properly until a team member made a change that caused the application to stop working.

Upon investigation, I discovered that the issue was related to the configuration of the volume mount. The Nginx server was expected to serve files from the shared volume mounted at '/var/www/html', but the path mounted on the pod was different. This discrepancy prevented the successful copying of the '/home/thor/index.php' file to the container.

To resolve the issue, I corrected the mount path on the pod to match the expected path of '/var/www/html'. After making this correction, I was able to copy the 'index.php' file to the Nginx container. Subsequently, the application started working as expected.

Attached is a screenshot that demonstrates the completed task, showing the successful resolution of the issue and the website accessible through the 'Website' button on the top bar.
![IMG_8326](https://github.com/boltpius/Troubleshooting-Kubernetes-Volume-Mounts-with-Nginx-and-PHP-FPM-/assets/127052041/48cf7e9b-1e7e-4272-9188-fc16c3ba3eee)
![IMG_8324](https://github.com/boltpius/Troubleshooting-Kubernetes-Volume-Mounts-with-Nginx-and-PHP-FPM-/assets/127052041/39e6909b-fe7d-4cc4-bcb0-35db6591d561)
![IMG_8328](https://github.com/boltpius/Troubleshooting-Kubernetes-Volume-Mounts-with-Nginx-and-PHP-FPM-/assets/127052041/f6b7c879-dbff-401f-a72e-1ca840309193)
![IMG_8329](https://github.com/boltpius/Troubleshooting-Kubernetes-Volume-Mounts-with-Nginx-and-PHP-FPM-/assets/127052041/9e830a34-8b1b-4b83-aa28-85a55625187b)
<img width="1509" alt="Screenshot 2023-09-06 at 21 08 41" src="https://github.com/boltpius/Troubleshooting-Kubernetes-Volume-Mounts-with-Nginx-and-PHP-FPM-/assets/127052041/8a503f7f-3eef-445a-959e-072ed11eb1b2">

