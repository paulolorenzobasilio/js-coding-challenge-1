# js-coding-challenge-1
Moscord Javascript Coding Challenge 1

```javascript
const people = [
        {
            name: 'Arisa',
            department: 'BP',
            gender: 'F'
        },
        {
            name: 'Ham',
            department: 'IT',
            gender: 'F',
        },
        {
            name: 'Alice',
            department: 'IT',
            gender: 'F'
        },
        {
            name: 'Anna',
            department: 'DA',
            gender: 'F'
        },
        {
            name: 'Larry',
            department: 'Sales',
            gender: 'M'
        },
        {
            name: 'Ria',
            department: 'Sales',
            gender: 'F'
        },
        {
            name: 'JD',
            department: 'Sales',
            gender: 'M'
        },
        {
            name: 'Thor',
            department: 'Sales',
            gender: 'M'
        },
        {
            name: 'Karl',
            department: 'Sales',
            gender: 'M'
        },
        {
            name: 'Rachel',
            department: 'Sales',
            gender: 'F'
        }
    ]

    const listByGender = (gender => {
        return people.filter(person => person.gender === gender)
    })

    const groupByDepartment = (() => {
        return people.reduce((department, person) => {
            const personDepartment = person.department
            department[personDepartment] = department[personDepartment] || []
            department[personDepartment].push(person)
            return department
        }, {})
    })

    console.log('list by Gender Male', listByGender('M'))
    console.log('list by Gender Female', listByGender('F'))
    console.log('group by department', groupByDepartment())
```
