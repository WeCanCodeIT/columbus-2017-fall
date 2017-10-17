## Sorting a collection can be a necessary task
- putting things in aplhabetical order
- sort items by amount

## ArrayList does not have a sort method
- but they are fast (first in, first out) and this concept is easy to grasp

### For example

```bash
ArrayList<String> words = new ArrayList<String>();
		words.add("hello");
		words.add("hola");
		words.add("world");
		words.add("mundo");

		System.out.println(words);
```

- How is this list printed?

## Using the Collections Class
- there is a `sort()` method in the Collections class
- It accepts a `List` param and since `ArrayList` **implements**  the `List` interface...well then
- try it...it will sort an `ArrayList` of `Strings`
- what happens if we change the type on our list to be an object?
