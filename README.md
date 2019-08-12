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
