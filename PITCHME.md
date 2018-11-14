---?color=linear-gradient(to right, #c02425, #f0cb35)
@title[Introduction]

@snap[west headline text-white span-70]
C#<br>*Fundamentals*
@snapend

@snap[south-west byline  text-white]
From Basic to Craft Code.
@snapend

---?image=template/img/bg/purple.jpg&position=top&size=100% 20%
@title[Course Outline]

@snap[north text-white span-100]
@size[1.5em](Course Outline)
@snapend

@snap[center span-100]
@ol[bullet-green](false)
- Array
- Generic
- Collection
@olend
<br><br>
@snapend

---?image=template/img/pencils.jpg
@title[Array]

## @color[black](Array)

@fa[arrow-down text-black]

@snap[south docslink span-50]
[The Ref Docs](https://guide.freecodecamp.org/csharp/array)
@snapend


+++?image=template/img/bg/pink.jpg&position=left&size=70% 100%
@title[Array Rules]

@snap[east split-screen-heading text-pink span-50]
Array<br>Rules
@snapend

@snap[west text-white span-65]
@ul[split-screen-list](false)
- Arrays start from zero. That is to say that the first element of an array is indexed as 0, the second element is 1, the third element 2, and so on.
- Arrays must be of the same data type. You can use any data type in an array (e.g. int, double, float, string, enum, List, People, etc.)
- A new Array must first be declared and initialised before it can be called and accessed.
@ulend
@snapend


+++?color=lavender
@title[Array Declaration]

### Declaring an *Array*

Use the following format for declaring arrays:

```csharp
dataType [] nameOfArray;
```


+++?color=lavender
@title[Array Initialization]

### Initializing an *Array*

Use the following format for initialising an array. This method also declares the array and states how many values are to be stored into the array.

```csharp
dataType [] nameOfArray = new nameOfArray[numberOfElements];
```


+++?color=lavender
@title[Array Assignment]

### Assigning *Values*

You can assign a value into an element directly by using the format below:

```csharp
nameOfArray[2] = 50;
```

You can assign multiple values at once while declaring the array using the format below:

```csharp
dataType [] nameOfArray = {5, 17, 19, 92};
```

+++?color=lavender
@title[Array Assignment 2]

```csharp
dataType [] nameOfArray = {5, 17, 19, 92};
```

<table>
  
  <tr>
    <th>Position</th>
    <th>Element</th>
  </tr>
  <tr>
    <td>[0]</td>
    <td>5</td> 
  </tr>
  
  <tr>
    <td>[1]</td>
    <td>17</td> 
  </tr>
  
  <tr>
    <td>[2]</td>
    <td>19</td> 
  </tr>
  
  <tr>
    <td>[3]</td>
    <td>92</td> 
  </tr>

</table>

+++?color=lavender
@title[Array Assignment 3]

### Assigning *Values* cont.

You can declare, initilise and assign values in the array all at once by using the format below:

```csharp
dataType [] nameOfArray = new dataType[numberOfElements]
{
    value1, value2, value3, value4
};
```

or simply:

```csharp
var nameOfArray = new dataType {value1, value2, value3, value4};
```

+++?image=https://www.geeksforgeeks.org/wp-content/uploads/gq/2015/05/Arrays.png&size=contain
@title[Array Elements]

@snap[south-west template-note text-gray]
Images from GeeksForGeeks
@snapend

note:
https://www.geeksforgeeks.org/arrays-in-c-cpp/


+++
@title[Array Example]

## Example

```csharp
int[] array = { 1, 2, 3, 4, 5 };
for (int i = 0; i < array.Length; i++)
{
	Console.WriteLine("Item on index {0} is {1}", i, array[i]);
}
```

## Output:

```bash
> Item on index 0 is 1
> Item on index 1 is 2
> Item on index 2 is 3
> Item on index 3 is 4
> Item on index 4 is 5
```

+++?image=template/img/bg/orange.jpg&position=right&size=50% 100%
@title[Array Pros and Cons]

@snap[west text-orange span-50]

@ol[split-screen-list](false)
Advantages
* Can be easily accessed in a random manner
* Can be easily manipulated
@olend
@snapend

@snap[east text-white span-45]
Disadvantages
@ol[split-screen-list](false)
* The only disadvantage is that the size of an array is fixed. (Hence, a list can be used in case of a dynamic sizing.)
@olend
@snapend


---?image=template/img/pencils.jpg
@title[Generic]

## @color[black](Generic)

@fa[arrow-down text-black]

@snap[south docslink span-50]
[The Ref Docs](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/generics/)
@snapend


+++?image=template/img/bg/pink.jpg&position=left&size=70% 100%
@title[Generic Overview]

@snap[east text-pink span-50]
Generic<br>Overview
@snapend

@snap[west text-white span-65]
@ul[split-screen-list](false)

- Use generic types to maximize code reuse, type safety, and performance.
- The most common use of generics is to create collection classes.
- You can create your own generic interfaces, classes, methods, events and delegates.  
- Generic classes may be constrained to enable access to methods on particular data types.  

@ulend
@snapend


+++?color=lavender
@title[Generic Code]

```csharp
// Declare the generic class.
public class GenericList<T>
{
    public void Add(T input) { }
}
class TestGenericList
{
    private class ExampleClass { }
    static void Main()
    {
        // Declare a list of type int.
        GenericList<int> list1 = new GenericList<int>();
        list1.Add(1);

        // Declare a list of type string.
        GenericList<string> list2 = new GenericList<string>();
        list2.Add("");

        // Declare a list of type ExampleClass.
        GenericList<ExampleClass> list3 = new GenericList<ExampleClass>();
        list3.Add(new ExampleClass());
    }
}
```

@[1-5](Declarint the Generic Type.)
@[6-10](Using Generic.)
@[11-14](Using Generic.)
@[15-18](Using Generic.)
@[19-21](Using Generic.)


+++?image=template/img/einstein.png&position=left&size=60% auto
@title[Array is Generic]

@snap[north-east span-60]
@quote[Array is also a Generic.]
@snapend

+++

```csharp
int[] intArray;



Array<int> arrayOfInt;
```

---
@title[Slide Markdown]

### Each slide in this presentation is provided as a *template*.

<br><br>

1. Select only the slide templates that you need.
1. Customize the template _markdown content_.
1. Optionally, override template _styles_ and _settings_.
1. Then present and publish with GitPitch @fa[smile-o]
<br><br>


---
@title[Tip! Fullscreen]

![TIP](template/img/tip.png)
<br>
For the best viewing experience, press F for fullscreen.

---?include=template/md/split-screen/PITCHME.md

---?include=template/md/sidebar/PITCHME.md

---?include=template/md/list-content/PITCHME.md

---?include=template/md/image/PITCHME.md

---?include=template/md/sidebox/PITCHME.md

---?include=template/md/code-presenting/PITCHME.md

---?include=template/md/header-footer/PITCHME.md

---?include=template/md/quotation/PITCHME.md

---?include=template/md/announcement/PITCHME.md

---?include=template/md/about/PITCHME.md

---?include=template/md/wrap-up/PITCHME.md

---
@title[The Template Docs]

@snap[west headline span-100]
GitPitch<br>*The Template @css[text-orange](End) ;)*
@snapend

@snap[south docslink span-100]
For supporting documentation see the [The Template Docs](https://gitpitch.com/docs/the-template)
@snapend
