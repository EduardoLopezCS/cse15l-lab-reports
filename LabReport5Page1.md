# **Lab Report 5**
by Eduardo Lopez

## Part 1:
## 1.1(Student Question): 
![Image](image1.1.png)

Hello my name is Eduardo, I am having trouble figureing out what's creating this failure on my code. The Junit test says my ```ListExamples.java``` file is failing a test relating to a ```TestTimedOutException```. I have a feeling it's related to the merge method where something isn't adding up or merging correctly resulting in the Junit test timing out. 

## 1.2(TA Response):
Hello Eduardo, thank you for making your question private. From the looks of the symptom, there is a timeout error meaning a possible while loop condition isn't being met, resulting in an infinite loop. With that in mind, take a look at your while loops. What would need to be done in order for the while loop or loops to eventually break(conditions met) and return the proper results.

## 1.3(Student Response):
![Image](image1.22.png)
![Image](image1.3.png)

Thank you. I found the bug. It makes sense why there would be a timeout error. The condition of my last while loop in my method would have never been met because instead of updating ```index2``` of ```list2``` for the loop, I was updating the ```index1``` which was already being done with the while loop above it. That's why the loop never broke because the proper indeces weren't even being incremented for the loop to move onto the next index on ```list2```. 

## 1.4(Information):

File and directory structure:

![Image](image1.5.png)
![Image](image1.4.png)

Contents of each file before fixing bug:

ListExamples.java:
```
import java.util.ArrayList;
import java.util.List;

interface StringChecker { boolean checkString(String s); }

class ListExamples {

  // Returns a new list that has all the elements of the input list for which
  // the StringChecker returns true, and not the elements that return false, in
  // the same order they appeared in the input list;
  static List<String> filter(List<String> list, StringChecker sc) {
    List<String> result = new ArrayList<>();
    for(String s: list) {
      if(sc.checkString(s)) {
        result.add(0, s);
      }
    }
    return result;
  }


  // Takes two sorted list of strings (so "a" appears before "b" and so on),
  // and return a new list that has all the strings in both list in sorted order.
  static List<String> merge(List<String> list1, List<String> list2) {
    List<String> result = new ArrayList<>();
    int index1 = 0, index2 = 0;
    while(index1 < list1.size() && index2 < list2.size()) {
      if(list1.get(index1).compareTo(list2.get(index2)) < 0) {
        result.add(list1.get(index1));
        index1 += 1;
      }
      else {
        result.add(list2.get(index2));
        index2 += 1;
      }
    }
    while(index1 < list1.size()) {
      result.add(list1.get(index1));
      index1 += 1;
    }
    while(index2 < list2.size()) {
      result.add(list2.get(index2));
      index1 += 1;
    }
    return result;
  }

}
```

ListExamplesTests.java:
```
import static org.junit.Assert.*;
import org.junit.*;
import java.util.*;
import java.util.ArrayList;


public class ListExamplesTests {
	@Test(timeout = 500)
	public void testMerge1() {
    		List<String> l1 = new ArrayList<String>(Arrays.asList("x", "y"));
		List<String> l2 = new ArrayList<String>(Arrays.asList("a", "b"));
		assertArrayEquals(new String[]{ "a", "b", "x", "y"}, ListExamples.merge(l1, l2).toArray());
	}
	
	@Test(timeout = 500)
        public void testMerge2() {
		List<String> l1 = new ArrayList<String>(Arrays.asList("a", "b", "c"));
		List<String> l2 = new ArrayList<String>(Arrays.asList("c", "d", "e"));
		assertArrayEquals(new String[]{ "a", "b", "c", "c", "d", "e" }, ListExamples.merge(l1, l2).toArray());
        }

}
```

test.sh:
```
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
```

Commands ran to trigger bug(test command):
```
bash test.sh
```

What to edit to fix bug:

To fix the bug, the programmer would have to edit line 43 in the ```ListExamples.java``` file, changing ```index1``` to ```index2``` in order for the while loop's conditions to be met and not timeout since incrementing ```index1``` wasn't for ```list2``` but instead, ```list1```. It's a simple and common bug that can cause a confusing symptom but thanks to the Junit test, it made it much easier to locate it in the code. 

## Part 2:
Something that I find not just very useful for future programming and file text editing but interesting and fun at the same is the command ```vim```. With ```vim```, you can fully edit any type of file without using an IDE because it's almost like an integrated IDE inside the terminal itself. It has very useful commands to navigate through text, edit, and search for anything like a word or character. Not just for any normal text file, but for coding as well. Like in CSE 30 when programming with C, ```vim``` helps to program C in a file without using an outside IDE that may require additional extensions. The only downside to it is if it's used by a programmer that doesn't have much experience with it, it may be more difficult and time consuming to edit a file with it compared to just using an IDE because they may not have the knowledge of the shortcut commands ```vim``` has to offer.
