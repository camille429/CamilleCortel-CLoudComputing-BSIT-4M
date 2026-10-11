# Reflection

1. **Why is using a `docker-compose.yml` file easier than running separate `docker run` commands?**
   - Everything is defined in one single, readable file. It is repeatable, shareable, and version-controlled. You do not need to remember or type long, complex commands every time.

2. **Why use environment variables instead of hardcoding settings in a Dockerfile?**
   - It keeps configuration separate from the application code. You can change passwords or settings without rebuilding the image. It is also more secure because sensitive values are not baked into the image itself.

3. **How did we get a fully functional Nextcloud stack running in just a few minutes?**
   - We used pre-built official images from Docker Hub — no need to manually install web servers, databases, or dependencies. Docker Compose automatically connects and configures the services to work together.

4. **How has your understanding of Cloud Computing changed since Lesson 1?**
   - I have learned that cloud computing is not just about storing files online. It is about building and deploying complete systems that are portable, scalable, and consistent across any environment. Containers make it possible to run the exact same application locally or in the cloud with minimal effort.
