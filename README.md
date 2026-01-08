# 2025_PoC_AGI-frameworks (JULY.2025)

## Overview

This repository contains proof-of-concept implementations and research for multi-agent AGI frameworks, focusing on advanced orchestration, workflow management, and agent collaboration. The project explores various strategies for agent coordination, workflow execution, and optimization using CrewAI and Strands frameworks.

## Research Objectives

- **Multi-Agent Orchestration**: Explore different approaches to coordinate specialized AI agents
- **Advanced Workflow Management**: Implement graph-based swarm structures for enhanced coordination
- **Cost Optimization**: Implement cost-effective model selection based on task complexity
- **Culinary Excellence**: Ensure recipe adaptations maintain authentic flavors and textures
- **Dietary Compliance**: Strict adherence to dietary restrictions and preferences
- **Performance Optimization**: Balance cost, quality, and execution time
- **Predictable Execution**: Develop structured workflows with clear execution paths

## Framework Comparison

| Framework | Approach | Complexity | Use Case |
|-----------|----------|------------|----------|
| **CrewAI** | Sequential/Hierarchical | Medium | Production-ready orchestration |
| **Strands** | Swarm/Sequential | High | Experimental multi-agent collaboration |
| **Strands Graph** | Graph-Based Swarm | High | Advanced workflow orchestration |

## Directory Structure

```
2025_PoC_AGI-frameworks/
├── agno/
│   └── latest/
│       └── config/
│           ├── agents-sequential.yaml
│           ├── agents-teams.yaml
│           ├── config.yaml
│           ├── integration_config.yaml
│           ├── tasks-sequential.yaml
│           ├── tasks-teams.yaml
│           └── vacuum_config/
├── crew/
│   └── latest/
│       └── config/
│           ├── agent-coordinate/
│           │   ├── agents.yaml
│           │   ├── crew_config.yaml
│           │   ├── integration_config.yaml
│           │   └── tasks.yaml
│           ├── agent-sequential/
│           │   ├── agents.yaml
│           │   ├── crew_config.yaml
│           │   ├── integration_config.yaml
│           │   └── tasks.yaml
│           └── vacuum_config/
├── strands/
│   └── latest/
│       └── config/
│           ├── agents-sequential.yaml
│           ├── agents-swarm.yaml
│           ├── config.yaml
│           ├── integration_config.yaml
│           ├── tasks-sequential.yaml
│           ├── tasks-swarm.yaml
│           └── vacuum_config/
├── agno-agent-collaborate.ipynb
├── agno-agent-coordinate.ipynb
├── agno-agent-secuential.ipynb
├── agno-agent-workflow.ipynb
├── crew-agent-coordinate.ipynb
├── crew-agent-sequential.ipynb
├── strands-agent-sequential.ipynb
├── strands-multi-agent-collaborate.ipynb
├── strands-multi-agent-graph.ipynb
└── ...
```

## Agent Specializations

### Core Agents

1. **Culinary Coordinator**
   - Role: Master Chef & Project Manager
   - Goal: Orchestrate recipe adaptation ensuring maximum culinary excellence
   - Expertise: 20+ years in dietary adaptations and team coordination

2. **Ingredient Substitution Expert**
   - Role: Culinary and dietary substitutions specialist
   - Goal: Find optimal ingredient substitutions maintaining flavor and texture
   - Expertise: Culinary chemistry and flavor profile optimization

3. **Culinary Experience Optimizer**
   - Role: Gastronomic Enhancement Specialist
   - Goal: Maximize culinary experience through technique optimization
   - Expertise: Award-winning chef for extraordinary dining experiences

4. **Dietary Compliance Specialist**
   - Role: Nutritional and dietary restrictions expert
   - Goal: Ensure 100% compliance with dietary restrictions
   - Expertise: Certified nutritionist with allergy management

5. **Quality Assurance Chef**
   - Role: Final Validation & Presentation Expert
   - Goal: Ensure final recipe meets all quality standards
   - Expertise: Quality control and presentation excellence

## Model Selection Strategy

### Complexity-Based Model Assignment

| Complexity Level | Model | Use Case | Cost |
|------------------|-------|----------|------|
| **High** | `amazon.nova-premier-v1:0` | Complex culinary analysis | High |
| **Medium** | `amazon.nova-pro-v1:0` | Recipe adaptation, substitutions | Medium |
| **Low** | `amazon.nova-lite-v1:0` | Validation, quality checks | Low |
| **Ultra-Low** | `amazon.nova-micro-v1:0` | Simple tasks, basic validation | Minimal |

### Agent-Model Mapping

```yaml
agent_model_mapping:
  "Culinary Coordinator": "medium_complexity"
  "Ingredient Substitution Expert": "medium_complexity"
  "Culinary Experience Optimizer": "medium_complexity"
  "Dietary Compliance Specialist": "low_complexity"
  "Quality Assurance Chef": "low_complexity"
```

## Implementation Approaches

### 1. CrewAI Sequential Approach

**File**: `crew-agent-sequential.ipynb`

**Characteristics**:
- Linear workflow execution
- Predictable execution path
- Easy to debug and monitor
- Cost-effective for simple adaptations

**Workflow**:
1. Initial Recipe Analysis → Culinary Coordinator
2. Dietary Compliance Validation → Dietary Compliance Specialist
3. Ingredient Substitution Strategy → Ingredient Substitution Expert
4. Culinary Experience Enhancement → Culinary Experience Optimizer
5. Final Quality Assurance → Quality Assurance Chef

### 2. CrewAI Hierarchical Approach

**File**: `crew-agent-hieralquical.ipynb`

**Characteristics**:
- Tree-based workflow execution
- Parallel task processing
- Complex decision trees
- Suitable for complex adaptations

**Workflow**:
- Coordinator manages multiple parallel streams
- Agents can spawn sub-tasks
- Dynamic workflow adaptation

### 3. Strands Sequential Approach

**File**: `strands-agent-sequential.ipynb`

**Characteristics**:
- Agent-to-agent handoffs
- Message-based communication
- Flexible conversation flow
- Real-time adaptation

### 4. Strands Swarm Approach

**File**: `strands-multi-agent-swam.ipynb`

**Characteristics**:
- Collaborative multi-agent execution
- Dynamic task delegation
- Emergent behavior
- Maximum flexibility

**Configuration**:
```python
swarm = Swarm(
    agents=[coordinator, substitution_expert, optimizer],
    max_handoffs=45,
    max_iterations=15,
    execution_timeout=180.0,
    node_timeout=30.0,
    repetitive_handoff_detection_window=8,
    repetitive_handoff_min_unique_agents=3
)
```

### 5. Strands Graph-Based Swarm Approach

**File**: `strands-multi-agent-hierarchical.ipynb`

**Characteristics**:
- **Directed Acyclic Graph (DAG)** workflow structure
- **Conditional Routing** based on context and requirements
- **Decision Points** for intelligent workflow branching
- **Structured Execution** with predictable paths
- **Enhanced Monitoring** with detailed metrics
- **Result Merging** from multiple execution paths

**Key Features**:
- **WorkflowNode Types**: Start, Agent, Decision, Merge, End
- **Conditional Edges**: Dynamic routing based on context
- **Execution Tracking**: Detailed path visualization
- **Performance Analytics**: Comprehensive metrics collection
- **Error Handling**: Robust error recovery mechanisms

**Workflow Structure**:
```
START → Culinary Coordinator → Decision Point → [Branch 1/2] → Merge → END
                                    ↓
                              [Agent Execution]
                                    ↓
                              [Quality Check]
```

**Benefits Over Basic Swarm**:
- **Predictable Execution**: Clear workflow paths instead of random handoffs
- **Better Resource Management**: Optimized agent utilization and cost efficiency
- **Enhanced Monitoring**: Detailed tracking and performance analytics
- **Flexible Routing**: Conditional execution paths based on context
- **Improved Results**: Better coordination and consistent output quality

## Configuration Files

### Integration Configuration (`integration_config.yaml`)

Contains AWS Bedrock model configurations and API endpoints:

```yaml
aws_bedrock:
  high_complexity_model:
    model_id: "bedrock/amazon.nova-premier-v1:0"
    model_kwargs:
      temperature: 0.7
      top_p: 0.9
      max_tokens: 8000
  # ... other model configurations
```

### Agent Configuration (`agents-*.yaml`)

Defines agent personalities, goals, and expertise:

```yaml
"Culinary Coordinator":
  name: "Culinary Coordinator"
  role: "Master Chef & Project Manager"
  goal: "Orchestrate recipe adaptation ensuring maximum culinary excellence"
  backstory: "Executive chef with 20+ years experience in dietary adaptations"
  prompt: "You are an expert culinary coordinator..."
```

### Task Configuration (`tasks-*.yaml`)

Defines task objectives and expected outputs:

```yaml
"Enhance Recipe":
  name: "Enhance Recipe"
  description: "Transform the requested recipe to be 100% compliant..."
  expected_output:
    - "Normalized recipe and instructions"
    - "Validation status for Quality checks"
```

## Usage Examples

### Running CrewAI Sequential

```python
from crewai import Crew, Agent, Task
import yaml

# Load configuration
with open('researches/crew/latest/config/agent-sequencial/crew_config.yaml', 'r') as f:
    config = yaml.safe_load(f)

# Create agents and tasks
# ... implementation details

# Run the crew
crew = Crew(agents=agents, tasks=tasks, verbose=True)
result = crew.kickoff()
```

### Running Strands Swarm

```python
from strands import Agent
from strands.multiagent import Swarm
import yaml

# Load configuration
with open('researches/strands/latest/config/config.yaml', 'r') as f:
    config = yaml.safe_load(f)

# Create agents
agents = [create_agent(config) for config in agent_configs]

# Create swarm
swarm = Swarm(agents, max_handoffs=45, max_iterations=15)

# Run swarm
result = swarm("Enhance this recipe with dietary restrictions...")
```

## Performance Metrics

### Cost Optimization

- **Model Selection**: Complexity-based model assignment
- **Token Usage**: Tracked per agent and task
- **Execution Time**: Monitored for optimization
- **Quality Metrics**: User satisfaction tracking


## Best Practices

### 1. Model Selection
- Use appropriate complexity models for each task
- Monitor cost vs. quality trade-offs
- Implement fallback strategies

### 2. Error Handling
- Implement retry mechanisms
- Log errors for analysis
- Provide graceful degradation

### 3. Performance Optimization
- Monitor execution times
- Optimize agent handoffs
- Balance parallel vs. sequential execution

### 4. Quality Assurance
- Validate dietary compliance
- Ensure culinary authenticity
- Track user satisfaction

## Troubleshooting

### Common Issues

1. **Swarm Timeout**
   - Increase `execution_timeout`
   - Reduce `max_handoffs`
   - Optimize agent communication

2. **High Token Usage**
   - Use lower complexity models
   - Optimize prompts
   - Implement caching

3. **Poor Quality Results**
   - Increase model complexity
   - Improve agent prompts
   - Add validation steps

### Debug Mode

Enable debug logging:

```python
import logging
logging.getLogger("strands.multiagent").setLevel(logging.DEBUG)
logging.basicConfig(
    format="%(levelname)s | %(name)s | %(message)s",
    handlers=[logging.StreamHandler()]
)
```


## Research Status

### Completed Implementations ✅

- **CrewAI Sequential**: Production-ready linear workflow
- **CrewAI Hierarchical**: Tree-based parallel processing
- **Strands Sequential**: Agent-to-agent handoffs
- **Strands Basic Swarm**: Collaborative multi-agent execution
- **Strands Graph-Based Swarm**: Advanced DAG workflow orchestration
- **AGNO Sequential**: AGNO agent sequential workflow experiments
- **AGNO Team/Collaborative**: AGNO multi-agent team and collaboration experiments
- **AGNO Workflow**: AGNO workflow orchestration and coordination experiments