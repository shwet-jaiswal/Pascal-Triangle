# Pascal-Triangle
Code for how to generate Pascal Triangle for n rows


/**
 * Function for generate Pascal Triangle for n rows
 * rows - Input to the function for number of rows
 * output - Returns a 2D array with the values
 **/
 
function createPascalTriangle(rows) {
    var pascalTriangleArray = [];
    var temp;

    for (var row = 0; row < rows; row++) {
        pascalTriangleArray[row] = [];

        for (var column = 0; column <= row, column++) {
            if (column === row) {
              pascalTriangleArray[row].push(1);
            }
            else {
              temp = (arr[row-1][column-1] ? arr[row-1][column-1] : 0) + 
                        (arr[row-1][column] ? arr[row-1][column] : 0);
              pascalTriangleArray[row].push(temp);
            }
        }
    }
    return pascalTriangleArray;
}
