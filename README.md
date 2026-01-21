# net-ai-project-template

A .NET AI project template designed for seamless integration with AI-powered IDEs (Kilo Code, Roo AI, Kiro Amazon). This template provides a structured foundation for building AI-enhanced applications with comprehensive documentation, testing strategies, and AI IDE support.

Inspired by [Full AI Coding Assistant Workflow](https://docs.google.com/document/d/12ATcyjCEKh8T-MPDZ-VMiQ1XMa9FUvvk2QazrsKoiR8/edit?tab=t.0)

## 🚀 Quick Start

```bash
# Clone the repository
git clone https://github.com/your-repo/net-ai-project-template.git
cd net-ai-project-template

# Initialize your project
# Replace $YourProjectName$ placeholders in documentation files
# Start implementing your features in the src/ directory
```

## 📁 Project Structure

```
net-ai-project-template/
├── .gitignore                          # Git ignore rules
├── README.md                           # Project documentation (this file)
├── AGENTS.md                           # Main AI Rules 
├── .kilocode/                         # Kilo Code AI configuration
│   └── rules/
│       └── rules.md                   # Kilo-specific rules and guidelines
├── .kiro/                             # Kiro AI configuration
│   ├── specs/                         # Kiro specifications
│   └── steering/                      # Kiro steering documents
├── .roo/                              # Roo AI configuration
│   ├── mcp.json                       # MCP server configuration
│   └── rules/
│       └── rules.md                   # Roo-specific rules and guidelines
├── docs/                              # Comprehensive project documentation
│   ├── coding.md                      # C# coding standards and best practices
│   ├── domain.md                      # Domain-specific rules and business logic
│   ├── product.md                     # Product description and features
│   ├── roadmap.md                     # Project roadmap and milestones
│   ├── structure.md                   # Project architecture and structure
│   └── tech.md                        # Technical stack and dependencies
├── src/                               # Source code directory
│   └── .gitkeep                       # Placeholder (remove when adding code)
└── test/                              # Test files directory
    └── .gitkeep                       # Placeholder (remove when adding tests)
```

## AI Agents

This project uses AGENTS.md as the single source of truth
for AI agent behavior and coding rules.

## 📚 File and Folder Descriptions

### 🤖 AI IDE Configuration Files

The project includes comprehensive configuration for three AI-powered IDEs:

#### **`.kilocode/` - Kilo Code AI Configuration**

- **`rules/rules.md`**: Contains Kilo-specific guidelines

#### **`.roo/` - Roo AI Configuration**

- **`mcp.json`**: MCP (Model Context Protocol) server configuration
- **`rules/rules.md`**: Roo-specific guidelines

#### **`.kiro/` - Kiro Amazon AI Configuration**

- **`steering/`**: Contains Kiro steering specific documents

### 📖 Documentation Files (`docs/`)

The `docs/` directory contains comprehensive project documentation:

- **`coding.md`**: C# coding standards including:
  - Modern C# (.NET 6+) requirements
  - Async/await best practices
  - XML documentation standards
  - Structured logging requirements
  - Testing discipline (TDD approach)

- **`domain.md`**: Domain-specific rules and business logic
  - Core entity definitions and relationships
  - Business rules and constraints

- **`product.md`**: Product overview and vision
  - Target users and use cases
  - Key product principles
  - Business goals and success metrics

- **`roadmap.md`**: Project development roadmap
  - Phase-based development plan
  - Milestones and deliverables

- **`structure.md`**: Architectural guidance
  - Dependency rules and layer separation
  - Naming conventions and versioning strategy
  - Project layout and organization

- **`tech.md`**: Technical stack specification
  - C# (.NET 10+) and ASP.NET Core
  - Data formats (JSON with schema validation)
  - Cloud and infrastructure requirements
  - Security and observability considerations

### 🗃️ Source and Test Directories

- **`src/`**: Main source code directory
  - Currently contains `.gitkeep` placeholder
  - Designed for modular organization by feature/domain
  - Follows structure defined in `docs/structure.md`

- **`test/`**: Test files directory
  - Designed to mirror `src/` structure
  - Supports both unit tests and property-based tests
  - Currently contains `.gitkeep` placeholder

## 🎯 AI IDE Integration Features

This template is optimized for AI-powered development with:

### ✅ Kilo Code AI Support

- **Code Analysis**: Automatic code structure validation
- **Refactoring Tools**: Built-in refactoring capabilities
- **Project Navigation**: Intelligent file and symbol navigation
- **Context7 Integration**: Automatic library documentation lookup

### ✅ Roo AI Support

- **Rule-Based Guidance**: Context-aware development suggestions
- **MCP Protocol**: Model Context Protocol for extended capabilities
- **Documentation Assistance**: Automatic documentation generation
- **Testing Strategy**: Built-in testing pattern enforcement

### ✅ Kiro Amazon AI Support

- **Steering Documents**: AI-guided development workflows
- **Consistency Checks**: Cross-document validation
- **Best Practice Enforcement**: Automatic code quality checks

## 🛠️ Development Guidelines

### Project Setup

1. Replace all `$YourProjectName$` placeholders in documentation
2. Initialize your Git repository if not already done
3. Set up your preferred AI IDE (Kilo, Roo, or Kiro)
4. Configure MCP servers as needed (see `.roo/mcp.json`)

## 🤝 Contributing

1. **Fork the repository** and create your feature branch
2. **Follow coding standards** in `docs/coding.md`
3. **Write comprehensive tests** for all new features
4. **Update documentation** as needed
5. **Submit pull request** with clear description of changes

## 📝 License

[Specify your license here - MIT, Apache 2.0, etc.]

## 🙏 Acknowledgments

- AI IDE providers (Kilo, Roo, Kiro)
- Context7 for MCP server capabilities
- .NET community for modern C# development tools

---

> **Note**: This template is designed to work seamlessly with AI-powered IDEs. The configuration files in `.kilocode/`, `.roo/`, and `.kiro/` directories provide AI-specific guidance while maintaining consistency with the main documentation in `docs/`.

For optimal AI assistance, ensure your IDE is properly configured to recognize and utilize these configuration files.
