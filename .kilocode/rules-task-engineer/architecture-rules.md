# Modular Monolith Boundaries
1. Code must be organized by domain modules, not technical layers.
2. You may not import internal functions from one domain module directly into another. You must use the 
   designated public interfaces/facades of that module.
3. Never store secrets in plain text.