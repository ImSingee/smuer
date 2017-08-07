
# smuer

![py35][py35]

smuer is an open source api for smu digital platform. Acessing your personal account through smuer in python has never been easier.




## Installation

smuer can be installed with this little one-line command:

```python
pip install smuer
```

## Quick start
    
    from smuer import Smuer
    
    #create a smuer
    student = Smuer(username='', password='')
    
    # query card info
    info = student.get_card_info()
    print(info)
    
    # query 2nd semester courses arrangement
    table2 = student.get_courses_table(2)
    print(table2)
    
    # query 1st semester grade info
    table = student.get_grade_table(1)
    print(table)
    
    # caculate the acerage point of 1st semester
    
    av1 = student.caculate_grade(1)
    print(av1)
    
    # caculate the average point of 2nd and 3rd semester
    av2_3 = student.caculate_grade(2,3)
    print(av2_3)

## Api

    def get_card_info(self):
    ''' return a string contaning e-card balance info'''
    
    def get_courses_table(self, semester_id):
    '''return a list contaning several dicts . 
       every course ' s info was structured,  
       and save into a dic'''
    
    def get_grade_table(self, semester_id):
    '''return a list contaning several dicts . 
       every course ' s grade_info was structured,  
       and save into a dic'''
    
    def caculate_grade(self, *semester_id):
    ''' return the averge point of the semesters'''

## Todoist

- [ ]  Tiezi read and post  
- [ ] get library info
- [ ] evaluate teaching



## FAQ

 none yet



## See also

[csvwolf/smu-jwc-api][smu-jwc-api]: SMU digital APi  

[evercx/SMU_WebService][SMU_WebService]: a set of restful Api of SMU digital platform  

[SnakeHacker/SMUHack][SMUHack]: SmuLoginPassword_blasting

[SMUHack]: https://github.com/SnakeHacker/SMUHack

[smu-jwc-api]: https://github.com/csvwolf/smu-jwc-api

[py35]: https://img.shields.io/badge/python-3.5-red.svg

[SMU_WebService]: https://github.com/evercx/SMU_WebService