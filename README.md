<br>

### Examples

For *\_\_pycache\_\_*:

```
find /cygdrive/j/library/briefings/sars -type d -name "__pycache__"
```

```
rm -r */*/__pycache__
rm -r */*/*/__pycache__
rm -r */*/*/*/__pycache__
rm -r */*/*/*/*/__pycache__
```

<br>

For *.ipynb_checkpoints*:

```
find /cygdrive/j/library/briefings/sars -type d -name ".ipynb_checkpoints"
```

```
rm -r */*/*/.ipynb_checkpoints
```
