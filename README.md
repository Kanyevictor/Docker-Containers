Docker Load Balancer with Nginx

A Docker-based load balancing solution that demonstrates horizontal scaling and traffic distribution using Nginx as a reverse proxy/load balancer.
📋 Project Overview

This project sets up a complete load balancing environment with:

    Two backend web servers (container1 & container2) serving custom HTML content

    Nginx load balancer distributing traffic using weighted round-robin algorithm

    Docker Compose for orchestration and easy deployment

🏗️ Architecture
text

┌─────────────────────────────────────┐
│         Load Balancer (Nginx)       │
│            Port: 8080               │
│        Weighted Distribution:       │
│        • Server A: 75% (weight=3)   │
│        • Server B: 25% (weight=1)   │
└───────────────┬─────────────────────┘
                │
        ┌───────┴───────┐
        ▼               ▼
┌─────────────┐ ┌─────────────┐
│  Server A   │ │  Server B   │
│  container1 │ │  container2 │
│  Port: 80   │ │  Port: 80   │
└─────────────┘ └─────────────┘

🚀 Quick Start
Prerequisites

    Docker

    Docker Compose

Installation

    Clone the repository:

bash

git clone https://github.com/Kanyevictor/Docker-Containers.git
cd Docker-Containers
