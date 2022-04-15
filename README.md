# JS Core Homework 1

1. https://www.codewars.com/kata/reviews/563b814cc41198306a000132/groups/563bacb3cd883097e000008f
2. https://www.codewars.com/kata/reviews/56bcf9bc8698152aba000015/groups/56befb08b5106ebc950005b7
3. https://www.codewars.com/kata/reviews/51f2d1cafc9c0f745c000380/groups/5215a98623e94f50d50000f7
4. https://www.codewars.com/kata/reviews/5418ac811d3bf3216b000236/groups/61f1eea0fe5122000185581c
5. https://www.codewars.com/kata/reviews/5d1607f3fdfc750001fd46a4/groups/5d4db23019da5c00014fd368

(З 5 якась помилка, воно здається не моє показує, тому напишу код яким я виконав:

function sortString(string,ordering) {
  const uniqueOrder = [... new Set(ordering.split(''))]
  let lettersLeft = string

  return uniqueOrder.reduce((acc, letter) => {
    const regex = new RegExp(letter, 'g')
    acc.push(...(string.match(regex) || []))
    lettersLeft = lettersLeft.replace(regex, '')
    return acc
  }, []).join('') + lettersLeft
}

)