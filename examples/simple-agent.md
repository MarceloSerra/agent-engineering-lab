# Simple Agent Example

## Basic Research Assistant Implementation

```python
import asyncio
from typing import List, Dict

class ResearchAgent:
    def __init__(self):
        self.tools = ["search", "read_file", "summarize"]
        self.memory = []
        
    async def execute_task(self, query: str) -> Dict:
        """Execute research task using available tools."""
        # Step 1: Search for relevant information
        search_results = await self._search(query)
        
        # Step 2: Read most promising sources
        documents = [await self._read(source) for source in search_results[:3]]
        
        # Step 3: Synthesize findings into summary
        summary = await self._summarize(documents)
        
        # Store result in memory for future reference
        self.memory.append({"query": query, "result": summary})
        
        return {"answer": summary, "sources": search_results}
    
    async def _search(self, query: str) -> List[str]:
        """Mock search implementation."""
        return ["source_1.md", "source_2.md", "source_3.md"]
    
    async def _read(self, source: str) -> str:
        """Mock file reading implementation."""
        return f"Content from {source}"
    
    async def _summarize(self, documents: List[str]) -> str:
        """Mock summarization implementation."""
        return "Synthesized summary of provided documents."

# Usage example
agent = ResearchAgent()
result = asyncio.run(agent.execute_task("How does MCP work?"))
print(f"Answer: {result['answer']}")
```

## Key Concepts Demonstrated

- **Tool Registration:** Explicit list of available capabilities
- **Memory Persistence:** Results stored for future context retrieval
- **Async Execution:** Non-blocking operations enable efficient processing
- **Structured Workflow:** Defined sequence of tool invocations per task type

## Next Steps

1. Replace mock implementations with actual API calls and file system access
2. Add error handling for failed searches, unreadable files, summarization failures
3. Implement memory retrieval strategies: recency weighting, relevance scoring
4. Create specialized sub-agents for different research domains

---

*Related: [Agents Overview](../agents/README.md) | [Planning Agents](../agents/planning-agents/README.md)*
