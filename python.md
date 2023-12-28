# JavaScript

## Make File Runnable as Script or When Imported/Called by Another File

Add the `if __name__ == '__main__'...` block so that your code can be run when imported and called from another file or
when called directly as `$ python my_script.py`.

```python
def main():
    print("Hello world!")

if __name__ == '__main__':
    main()
```

Reference: [YouTube video "You should put this in all your Python scripts | if __name__ == '__main__': ..."](https://www.youtube.com/watch?v=g_wlZ9IhbTs)
