# ngrok Traffic Policy Examples

[![ngrok](https://img.shields.io/badge/ngrok-enabled-blue.svg)](https://ngrok.com)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

A curated collection of production-ready Traffic Policy examples for ngrok endpoints. These policies demonstrate common patterns for traffic management, security, and optimization.

## 🚀 Quick Start

New to ngrok? [Sign up for a free account](https://ngrok.com/signup) and get started in minutes!

## 📖 About Traffic Policies

ngrok's [Traffic Policies](https://ngrok.com/docs/traffic-policy/) provide a powerful configuration language for managing traffic to your endpoints. With policies, you can:

- **🛡️ Security**: Block malicious traffic and validate requests
- **🔄 Routing**: Rewrite URLs and redirect traffic  
- **📊 Monitoring**: Log requests and add custom headers
- **⚡ Performance**: Cache responses and load balance
- **🎯 Targeting**: Route traffic based on conditions

Traffic policies can be scoped to specific endpoints, enabling teams to manage policies independently - API teams for internal services, DevOps for public endpoints.

## 📂 Repository Structure

This repository is organized to roughly mirror the [ngrok Traffic Policy Documentation](https://ngrok.com/docs/traffic-policy/examples/) structure for easy navigation

## 🛠️ Usage

### Method 1: Direct URL Reference

Use a policy directly from this repository:

```bash
# For local development
ngrok http 8080 --traffic-policy-url https://raw.githubusercontent.com/ngrok-samples/traffic-policy-examples/main/security/rate-limit.yaml

# For cloud endpoints
ngrok api endpoints create \
  --url your-domain.ngrok.app \
  --traffic-policy-url https://raw.githubusercontent.com/ngrok-samples/traffic-policy-examples/main/security/rate-limit.yaml
```

### Method 2: Local File

Clone the repository and reference local files:

```bash
# Clone the repository
git clone https://github.com/ngrok-samples/traffic-policy-examples.git
cd traffic-policy-examples

# Use with ngrok agent
ngrok http 8080 --traffic-policy-file ./security/rate-limit.yaml

# Use with cloud endpoints
ngrok api endpoints create \
  --url your-domain.ngrok.app \
  --traffic-policy-file ./security/rate-limit.yaml
```

### Method 3: Copy and Customize

Copy any policy configuration and modify it for your specific needs, then apply it through the [ngrok Dashboard](https://dashboard.ngrok.com) or API.

## 🤝 Contributing

We welcome contributions from the community! Here's how you can help:

### 💡 Suggesting New Examples

- [Open an issue](https://github.com/ngrok-samples/traffic-policy-examples/issues/new) describing the use case and policy you'd like to see
- Include details about the problem you're solving and expected behavior

### 📝 Adding New Policies

1. Fork this repository
2. Create a new branch for your policy
3. Add your policy file in the appropriate category directory
4. Include clear documentation and comments in the policy
5. Submit a pull request with a detailed description

### 📋 Policy Guidelines

- Use clear, descriptive filenames
- Include inline comments explaining complex logic
- Test your policy before submitting
- Follow the existing file structure and naming conventions

### 📞 Support

- For policy questions: [ngrok Discord](https://ngrok.com/discord)
- For documentation: [Traffic Policy Docs](https://ngrok.com/docs/traffic-policy/)
- For bugs or issues: [GitHub Issues](https://github.com/ngrok-samples/traffic-policy-examples/issues)

---

**Note**: Spam submissions will be closed and reported. Please ensure your contributions are relevant and helpful to the community.