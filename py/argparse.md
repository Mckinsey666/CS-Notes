# Argparse

## Require at least one optional argument
*Solution* : None! **argparse** has no guard for empty optinal arguments. 
   
*Possible remedy*
```python
if not(args.a or args.b or ...):
    parser.error("At least one optional argument is required!")
```