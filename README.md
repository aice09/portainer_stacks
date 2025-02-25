# Portainer Stacks

This repository contains a collection of **Portainer** stack configurations for deploying and managing containerized applications using **Docker** and **Portainer**.

## 📁 Repository Structure

```
portainer-stacks/
│
├── stack1.yml       # Example stack file
├── stack2.yml       # Another stack file
├── templates/       # Optional Portainer templates
└── README.md        # This file
```

## 🚀 Getting Started

### Prerequisites

- **Docker** installed on your system
- **Portainer** set up and running
- Access to the Portainer UI

### 📥 Importing a Stack into Portainer

1. Open the **Portainer** UI.
2. Navigate to **Stacks** → **Add Stack**.
3. Copy the contents of the desired `.yml` file or upload it directly.
4. Set a name for your stack.
5. Click **Deploy the Stack**.

### 📄 Example Deployment

```bash
docker stack deploy -c stack1.yml my_stack_name
```

### 🔄 Updating a Stack

If changes are made to a stack file:

1. Navigate to the stack in the Portainer UI.
2. Replace the existing configuration with the updated `.yml` file.
3. Click **Update the Stack**.

## ⚙️ Customization

- Modify environment variables, network settings, and volume paths in the `.yml` files to match your setup.
- Use the `templates/` directory for reusable Portainer templates.

## 📚 Documentation

- [Portainer Documentation](https://docs.portainer.io/)
- [Docker Compose Reference](https://docs.docker.com/compose/compose-file/)

## 🛡️ License

This project is licensed under the [MIT License](LICENSE).

