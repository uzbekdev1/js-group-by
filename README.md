# JavaScript group an array of objects by key

const cars = [{
make: "audi",
model: "r8",
year: "2012"
},
{
make: "audi",
model: "rs5",
year: "2013"
},
{
make: "ford",
model: "mustang",
year: "2012"
},
{
make: "ford",
model: "fusion",
year: "2015"
},
{
make: "kia",
model: "optima",
year: "2012"
}];

let group = cars.reduce((r, a) => {
 console.log("a", a);
 console.log('r', r);
 r[a.make] = [...r[a.make] || [], a];
 return r;
}, {});

console.log("group", group);

lodash.groupBy(cars, 'make')
