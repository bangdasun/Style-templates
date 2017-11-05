### Template for function definition

Standard of function naming, doc style.

* Python version
```
def get_power_sum(lst, p=2):
    """
    Get the sum of some power of all elements in list
    
    Parameters
    ----------
    lst: list object, int or float
        list of elements to be calculated.
    
    p: int, default 2
        power to be taken
    
    Returns
    -------
    s: int or float
        sum of power of elements in list
    
    Examples (optional)
    --------
    >>> get_power_sum([1, 2, 3], p=2)
    14
    """
    
    s = 0
    for val in lst:
        s += val**p
     
    return s
```
