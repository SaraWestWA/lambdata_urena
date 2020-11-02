Code clear and easy to follow.
Doc strings are useful.

isit_float  - functions as described, misspelled integer on line 15

datetime_columns - accidentally mixed the year & month into one column, it will work as expected if corrected.

Dead_poets_society - very creative

The '__repr__' and '__string__' methods have the same output, they are intended to be different, this link explains:
https://pythonprogramming.net/__str__-__repr__-intermediate-python-tutorial/#:~:text=The%20__str__%20method,descriptive%20of%20that%20exact%20object.
(new informtion for me, too).

Import and run pylint & pydocstyle for pep8 compliance details. I also like to use this site: http://pep8online.com/

Here is some useful code for testing within your py file, something I learned in SaraW Unit 3 v 1.0.

    if __name__ == '__main__':

        j = isit_float('jane')
        print(j)

        # Setup DataFrame to test datetime_columns method
        data = ([['11/16/2020', 'May 6, 1979', 'Nov 3, 1860', '10 Jun 1945', '10/02/1996', '1/1/03', 'June 1960', '03/3/1985'],
                [2, 2, 1, 0, 1, 6, 6, 2]])

        names = ['dates', 'int']

        df = pd.DataFrame(data, index=names).T

        print (df, '\n')

    # Make class variable
    dft = datetime_columns(df, 'dates')
    print(dft, '\n')

    print(poem5)
