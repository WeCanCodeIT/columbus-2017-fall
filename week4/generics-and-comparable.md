## Sorting a collection can be a necessary task
- Recommended Reading: Head First Java 529-554
- putting things in order
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
```bash
ArrayList<Word> words = new ArrayList<Word>();
		words.add(new Word("hello"));
		words.add(new Word("hola"));
		words.add(new Word("world"));
		words.add(new Word("mundo"));

		
		Collections.sort(words);
		System.out.println(words);
```

## The sort() method declaration
### `public static <T extends Comparable<? super T>> void sort List<T> List)`
- When you see < > this mean generics, a feature of Java 5
- Generics means more type safety
	- This assures more issues happen during compile time and not run time
	- Before generics, an `ArrayList` could contain a collection of any object
		- Soccerballs, fish, cars and guitars could all be housed in the same collection
		- With generics you type-safe collections...so only one particular object will belong in a collection
		- Therefore you will not find a pumpkin in a collection of cars
		- With generics objects go in and out of the same type
		
		
## Re-visiting our sort() method
- `sort()` can only take lists of comparable objects (like Strings)
- `Word` is not a subtype of `Comparable` so we cannot sort this particular object...but
- `Word` can implement `Comparable` and we can pass `ArrayList<Word>` to the `sort()` method like this...
	- `public class Word implements Comparable<Word>`
- And now we can build out our `compareTo(T o)` like this...
```bash
	@Override
	public int compareTo(Word word) {
		return this.word.compareTo(word.getWord());
	}
```
- Woah no errors! But output needs fixed...what is happening, how do we do this?
- Ahh yes, you have had plenty of experience with this haven't you.

###  Ahh lets change our list of words to be names
- What if I want to sort by first name?
	- There is a custom `Comparator` for that

```bash
class CompareFirst implements Comparator<Name>{
		public int compare(Name one, Name another) {
			return one.getFirstName().compareTo(another.getFirstName());
		}
	}
```
And in the App class

```bash
CompareFirst firstName = new CompareFirst();
	Collections.sort(names, firstName);
	
	System.out.println(names);
