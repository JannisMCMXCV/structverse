#handydandy.md

##handy dandy algorithms

### evenly distribute specific objects of the same size over a distance
```python
def find_candidates(width, margins, widths, spaces, count):
    """
    Finds sets of "candidates" to distribute objects of a certain number over a certain distance under certain conditions.

    A candidate consists of a margin, a width (of the object) and a distance (between the objects).

    The margin is distance to the outside next to the first and last object

    For margin and distance between the objects lists of possible allowed distances are expected
    
    This function takes an input number and returns its square.
    
    Parameters:
        width (int or float): the width of the distance the objects are to be distributed over
        margins (list of int or float): A list of allowed margins
        widths (list of int or float): A list of allowed widths of each object
        spaces (list of int or float): A list of allowed space widths between each object
        count (int): the count of objects to be distributed
    """
    for m in margins: 
        for w in widths:
            for s in spaces:
                space_count = count-1
                if 2*m+count*w+space_count*s == width:
                    print("CANDIDATE:")
                    print("margin: {}", m)
                    print("space: {}", s)
                    print("object width: {}", w)
    print("END")
```
