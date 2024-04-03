Challenge 2: Node.js Application with NGINX Reverse Proxy
Advancing to the second challenge, I aimed to deploy a dynamic Node.js application with NGINX as a reverse proxy. This task was more complex, involving multiple containers and a deeper dive into network configurations.

Encountered Issues and Resolutions
•	NGINX Configuration Error: The message "events directive is not allowed here" was a significant stumbling block, underscoring the critical nature of correct NGINX configuration and its sensitivity to context.
•	Application Not Reflecting Updates: After updating server.js, the changes were not reflected, teaching me about Docker's nature of container immutability and the need for rebuilding containers to apply code changes.
•	"Cannot GET /" Error: When I encountered this error when accessing the root URL through NGINX, I troubleshooted NGINX's proxy settings and Docker's networking, ensuring proper communication between containers.

Key Learnings
•	Deep Dive into NGINX: Through configuration errors and troubleshooting, I gained a profound understanding of how NGINX serves as a reverse proxy, including the nuances of its configuration files.
•	Docker Compose Mastery: Learned to orchestrate multi-container applications, emphasizing the utility and power of docker-compose.yml for defining and running complex applications.
•	Iterative Learning Through Troubleshooting: Each error encountered taught me patience and persistence, and I learned to troubleshoot, research iteratively, and systematically apply solutions.
Conclusion
•	Though filled with challenges, my journey through the Docker Challenges was immensely rewarding. Each error encountered was a doorway to deeper understanding, be it Docker's intricacies, NGINX's configuration, or the broader principles of web application deployment. This experience has bolstered my technical skills and instilled a resilient problem-solving mindset, ready to tackle future challenges in the ever-evolving tech landscape.

Enhanced Features in Dockerized Applications
As I navigated through the complexities of deploying applications with Docker, specific functionalities were integrated to demonstrate the dynamic capabilities of a Node.js application and system monitoring. These features are foundational to understanding how applications interact with users and the system environment. Below is a detailed examination of these crucial parts of my learning journey.

Search book by correct ID: http://localhost:8080/api/books/1
Display List of Book: http://localhost:8080/api/books
 
Memory Stats Retrieval
One of the standout features implemented was the Memory Stats Retrieval through the route /api/stats. This functionality leverages Node.js to read from the system's /proc/meminfo file, extracting and returning specific memory statistics such as MemFree and MemAvailable. The significance of this feature extends beyond mere data retrieval; it embodies the application's capacity to interact with and monitor the underlying system. It provided a practical demonstration of accessing system-level information from within a Dockerized application, underscoring the importance of understanding the operating environment.

Books Data Retrieval
The core functionality around Books Data Retrieval was designed to showcase basic data manipulation and routing within a Node.js application. This feature was divided into two main routes:
•	/api/books: Returns a static list of books, simulating a simple data retrieval operation commonly found in web applications. This route was instrumental in understanding how to handle HTTP GET requests and return JSON responses, laying the groundwork for building RESTful APIs.
•	/api/books/:id: This function retrieves a book by its unique identifier (ID), demonstrating how to implement parameterized routing to fetch specific records. This functionality is pivotal in creating dynamic web services where users can request data based on unique identifiers.

Reflections on Implemented Features
Integrating these features into the Docker challenges provided a multi-faceted learning experience. From a technical standpoint, it facilitated hands-on practice with Node.js, Express routing, and the nuances of Docker containerization. It highlighted the importance of application interaction with the user and the system on a conceptual level, illustrating how Dockerized applications can bridge complex back-end operations and front-end user requests.
