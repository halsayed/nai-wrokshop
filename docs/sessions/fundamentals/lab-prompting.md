# Lab: Introduction to Prompting & Context

## Overview

In this lab, you'll gain hands-on experience with prompt engineering and understanding how context affects LLM responses. You'll experiment with different prompting techniques and see how they influence the quality and relevance of AI outputs.

## Prerequisites

- Access to the workshop environment
- Basic understanding of LLM concepts (covered in the previous session)

## Lab Environment

For this lab, we'll use a pre-deployed open-source LLM interface that allows you to experiment with different models and prompting techniques.

## Part 1: Basic Prompting

### Step 1: Access the LLM Interface

1. In your workshop environment, navigate to the LLM interface at:
   ```
   http://<your-cluster-ip>:8000/chat
   ```

2. You should see a chat interface where you can interact with the model.

### Step 2: Write Your First Prompts

Try the following prompts and observe the responses:

1. Simple question:
   ```
   What is a Kubernetes pod?
   ```

2. Ask for a specific format:
   ```
   List 5 best practices for Kubernetes security in bullet points.
   ```

3. Generic vs. specific:
   ```
   How to troubleshoot network issues?
   ```
   
   Then try:
   ```
   I'm a Nutanix administrator troubleshooting connectivity issues between Kubernetes pods. Give me a step-by-step procedure to diagnose and resolve the problem.
   ```

!!! tip
    Notice how being specific about your role and the exact problem leads to more relevant responses.

## Part 2: Advanced Prompting Techniques

### Step 1: Few-Shot Learning

Try using examples to guide the model:

```
Translate these Kubernetes commands into human-readable explanations:

Command: kubectl get pods -n kube-system
Explanation: List all pods running in the kube-system namespace

Command: kubectl describe deployment nginx
Explanation: Show detailed information about the nginx deployment

Command: kubectl logs -f pod-name
Explanation: 
```

### Step 2: Chain-of-Thought Prompting

Ask the model to reason step by step:

```
I need to deploy a stateful application on Kubernetes that requires persistent storage. Think through step by step what resources I'll need to create and in what order.
```

Then try adding:

```
Think step by step and explain your reasoning for each component.
```

### Step 3: Role Prompting

Ask the model to assume a specific role:

```
You are an experienced Nutanix infrastructure architect. I'm planning to deploy LLMs on our Nutanix cluster. What considerations should I keep in mind regarding resource allocation, networking, and storage?
```

## Part 3: Understanding Context Windows

### Step 1: Testing Context Length

1. Copy a long technical document (your instructor will provide this)
2. Paste it into the chat and ask:
   ```
   Summarize the key points from this document.
   ```

3. Then try:
   ```
   Reference specific details from paragraph 15 of the document above.
   ```

!!! note
    The model can only reference information that's within its context window.

### Step 2: Maintaining Context

Test how the model maintains context across a conversation:

1. Ask:
   ```
   I want to set up monitoring for my Kubernetes cluster on Nutanix. What tools would you recommend?
   ```

2. Follow up with:
   ```
   For the first tool you mentioned, how would I deploy it?
   ```

3. Continue with:
   ```
   What metrics should I be particularly concerned with?
   ```

## Part 4: RAG (Retrieval-Augmented Generation) Preview

In this section, you'll get a brief preview of Retrieval-Augmented Generation, which we'll explore in depth later.

1. Navigate to the RAG-enabled chat interface at:
   ```
   http://<your-cluster-ip>:8000/rag-chat
   ```

2. This interface has access to Nutanix documentation. Try:
   ```
   How do I configure high availability for NKP?
   ```

3. Notice how the model cites sources from the documentation.

## Validation

You have successfully completed this lab if you:

- [x] Created and tested various types of prompts
- [x] Observed how specificity affects response quality
- [x] Experimented with advanced prompting techniques
- [x] Understood the limitations of context windows
- [x] Previewed RAG capabilities

## Next Steps

Now that you understand the basics of prompting and context, you're ready to [deploy an LLM using Nutanix NAI](../deployment/index.md) in the next session.
