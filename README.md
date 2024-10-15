## Project Specification: **n3xa streams**

### 1. **Project Overview**
**n3xa streams** is a data flow automation platform inspired by Apache NIFI, developed by **n3xa**. Built using **React Flow**, the platform aims to provide a more user-friendly, extensible interface for managing complex data pipelines. It allows for real-time and batch processing of data through customizable processor nodes and can be extended with WebAssembly for high-performance requirements. The application will have a backend using **JavaScript** for orchestration and data management.

### 2. **Core Objectives**
- **User-friendly Interface**: An intuitive drag-and-drop interface using **React Flow** for managing data flows.
- **Built-in and Custom Processor Nodes**: Offer pre-built processor nodes with easy configuration and an extensibility model for developers to create new processors, possibly leveraging WebAssembly.
- **Backend for Performance**: Use a **JavaScript** backend for handling data orchestration, storage, and high-throughput processing.
- **Flexible Storage Options**: Leverage **ScyllaDB** for high throughput, with fallback to **PostgreSQL** for less intensive use cases.
- **Real-time and Batch Processing**: Support for both real-time data streams and batch operations.
  
### 3. **Key Features**
- **Processor Nodes**:
    - Built-in nodes for data ingestion, transformation, routing, filtering, and enrichment.
    - Configurable nodes with input/output formats, connection options, and customizable settings.
    - Support for asynchronous and parallel processing.
    - Real-time feedback for performance metrics (data rates, errors, processing time).
  
- **Extensibility**:
    - **Processor SDK** for developers to create new processors using JavaScript or WebAssembly for performance-critical tasks.
    - Simple guidelines for extending and deploying custom processors.
  
- **Flow Management**:
    - Visual creation and editing of data flows using drag-and-drop.
    - Node connection mechanisms for defining relationships between processors.
    - Real-time monitoring and debugging features, such as live logs and performance stats.
  
- **Storage**:
    - Use **ScyllaDB** for handling high throughput data streams or **PostgreSQL** for smaller-scale use cases.
    - Backend integration to persist flow configurations and states.

- **Error Handling**:
    - Real-time error alerts and logging for nodes and flows.
    - Visual indicators of node or flow failures.

- **Authentication & Access Control**:
    - Role-based access control for managing user permissions.
    - Authentication system for secured access to flows and processor configurations.

### 4. **Technical Architecture**
- **Frontend**:
    - **React.js** with **React Flow** for flow visualization and management.
    - **Vite** as the build tool for fast, optimized bundling.
    - **TailwindCSS** with **shadcn** for component styling.
    - **TypeScript** for type safety and maintainability.
    - **WebAssembly** integration for performance-critical processors.

- **Backend**:
    - **Node.js** (JavaScript) for handling orchestration, flow state management, and data processing.
    - **Express.js** or **Fastify** for the API layer to communicate between frontend and backend.
    - **ScyllaDB** as the primary database for high-throughput use cases, with fallback to **PostgreSQL** for smaller workloads.
  
- **Data Flow Engine**:
    - Orchestration layer for connecting processors and managing data flow asynchronously.
    - Support for both batch and real-time data processing.

### 5. **Project Phases**

#### Phase 1: Core Infrastructure and UI
- Set up **Vite** for React development and initialize **React Flow** for flow visualization.
- Build out the drag-and-drop interface for placing and connecting processors.
- Develop basic processor nodes (e.g., ingest, transform, route).
- Implement **TailwindCSS** with **shadcn** for styling and component consistency.

#### Phase 2: Backend and Processor Extensibility
- Set up a **Node.js** backend for flow orchestration and processor execution.
- Add **ScyllaDB** and **PostgreSQL** as storage backends depending on throughput needs.
- Implement the **Processor SDK** for developer extensibility (supporting JavaScript and WebAssembly processors).
  
#### Phase 3: Real-time Monitoring and Error Handling
- Build real-time monitoring features, such as live data rates, error logging, and flow health visualization.
- Implement user authentication and role-based access control for managing user permissions.

#### Phase 4: Testing, Documentation, and Optimization
- Unit and integration tests for both frontend and backend.
- Developer and user documentation for using and extending **n3xa streams**.
- Performance optimization, particularly focusing on WebAssembly execution and data flow orchestration.

### 6. **Success Criteria**
- **Intuitive Interface**: The platform should be easy to use, enabling both developers and non-developers to manage data flows effectively.
- **High Performance**: **n3xa streams** must handle high-throughput data flows efficiently, especially when using WebAssembly for performance-critical processors.
- **Extensibility**: Developers should find it straightforward to create and integrate custom processors.

---

### Additional Considerations
- **Performance Benchmarks**: Set performance goals based on specific use cases, such as processing large data streams in real-time. 
- **ScyllaDB Tuning**: If high throughput becomes a bottleneck, fine-tuning ScyllaDB to maximize performance should be a focus.
