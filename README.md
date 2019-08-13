## React


### Refreshing Array Functions
(((-Các lệnh gán trong react thì chỉ sao chép địa chỉ con trỏ chứ không sao chép giá trị vì lẽ đó khi thay đổi giá trị tại địa chỉ thì đối tượng mới cũng thay đổi. Nên nếu muốn sao chép thực sự thì ta phải tạo một đối tượng hoàn toàn mới và sao chép giá trị của đối tượng cũ chứ không phải hoàn toàn đối tượng. với systax sau: const secondPerson={...person};)))

Now over the last lectures I introduced you to some of the most important next generation javascript

features which you're going to see in those course.

There are two other things I know definitely.

Also want to cover.

They're not next generation javascript but they are features you might have missed or forgotten and

they're super important to keep in mind.

The first feature or concept of javascript I'm talking about is the fact that you have reference and

primitive types.

If I create a number like this, then this is a primitive type.

That means if I create a second number num2 and set it equal to this number then it will actually

create a real copy of number so num2 of course.

Now if I log this, it will also be one.

But it will have copied that value one into num2.

Now numbers, strings, booleans, these are so-called primitive types whenever you reassign or you store

a variable in another variable.

It will copy the value, objects and arrays are reference types.

Though let me show you what I mean.

I create my personal object which just has a name here and I now create a secondPerson and assigned

person as a value here.

If I console log.

secondPerson and hit run, it will print the same value as the first person but it will not actually have

copied the person instead.

Person the object is stored in memory and in the constant person we store a pointer to that place in memory.

And if we then assign person to secondPerson that pointer will be copied.

We can see that this is the case if we changed person.name after having it copied.

With that you would expect to print Max here still a person with name Max because we copied person, stored

it in secondPerson and thereafter changed the name.

However if I clear and run you will see name.

Manu here even though I'm printing the secondperson so for secondPerson the name also changed

the reason for it is that it just copied the pointer and points to the exact same object in memory as

person does.

So if we change name on person we automatically change it for secondPerson.

Now that's important.

Keep in mind and it's the same for arrays.

If you copy in quotation marks.

An array like this.

And you then change an array element.

It will all change in the so-called copied array.

This will become important in React because it can lead to unexpected behaviors.

If you copy objects or arrays like this because you then may manipulate one object in one place in the

app and accidentally manipulate another usage of the same object in another place of the app.

Therefore we will learn techniques to copy this in an immutable way which means we copy that by really

copying the object and not just a pointer for that we can use this spread operator.

Now we can simply create a new person object here and spread the person properties.

This will pull out the properties and the values of the properties from the object and add it to this

newly created object here and we do create a new one with the curly braces.

Now if I hit clear and run we still print an object with name Max even though we changed the name to

Manu here because now we really created a real copy.

This is a technique I will also come back to later in this course.

It's just important to realize and to keep in mind that objects and arrays are reference types.

If you reassign them you're copying the pointer not the value.

Therefore if you want to do this in a real copy way, you will have to create a new object and just copy

the properties and not the entire object.

That's something very important to keep in mind for this course.


## Refret Array Function
((Việc thực hiện các hàm trong mảng bằng Map
systax:   const newNum=num.map((n)=>{ 
return n*2;} )  ))

In the last lecture we had a look at reference of primitive types something super important to keep

in mind when working with javascript.

Another thing you will see quite a lot in this course are array functions.

We already saw filter a couple of lectures ago.

We also got sort, map and so on.

Let me quickly show you what I mean.

The good old numbers array with 1, 2 and 3.

Now let's say we want to turn this into an array where each number is doubled.

So we have to doubleNumArray, something like that we can use an array function for this.

We can take the numbers array and call map.

Map is a built-in array method.

And there are many of these methods.

I will use quite a lot of them and they're not.

Next generation javascript all these methods work in the same way though they take a function as an

input and this function which is an arrow function here but could be a normal function is then simply

executed on each element in the array here.

So on each element in the numbers array, on 1 and 2 and 3.

So therefore what we get in this arrow function is a number in the end.

But you can name this argument whatever you want here.

We can then simply return something.

And what you have to do in this internal function depends on which area of function you are using.

Check the docs in places like d Mozilla Developer Network docs to learn more about the available array

functions.

So in the map function we have to return the new value we want to turn the old one into so we could

return num * 2 and since this is executed on every element here.

It will return 2, 4 and 6 and conveniently map all the returns a new array.

So a real new array which is then stored in doubleNumArray.

So now if I output numbers and thereafter doubleNumArray like this and then I'll hit run you'll see

the old one is unchanged but the new one holds double the values and I will explain what these functions

do when we use them in the course.

I just want to bring them to your attention right now.

Explain that they always have this function which gets executed on each element and that they are not

next generation javascript but normal javascript actually, be prepared to meet them.

I will explain what they do when we see them and always feel free to dive into docs like the Mozilla

developer network to learn more about them.
## Wrap up

With that I want to conclude this module. We've learned a lot about next generation javascript and some

important javascript concepts.

In general you will meet a lot of the things you'll learn about in this module throughout the course.

Don't be confused by it.

It's still javascript.

Just using some more modern features.

That's just how we write React apps.

The next module will now start with React.

Now I will show you how to quickly create a project set up where we can use all these features while

still shipping code that works in older browsers too.

With that you're well prepared.

Always feel free to go back to this module and have a look at a given feature if you forgot how it

worked and you meet it in the course and want to refresh your knowledge.

And with that let's dive into React.
