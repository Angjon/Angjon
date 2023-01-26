```python
class ReadMe:
    def __init__(self, username="Angjon", year=2023):
        self.username = username
        self.name = 'Jonas Angulski'
        self.education = {
            'Engineering': ['Mechanical Engineering', 'PUCPR'],
            'Data Analysis': ['Data Analysis with Python', 'Free Code Camp'],
            'Machine Learning': ['Machine Learning A-Z', 'Ligency I Team']
        }
        self.employment = {
            'Trainee': ['Renault do Brasil', 'São José dos Pinhais'],
            'Engineer Job Rotation': ['Xingyu Automotive Lighting', ['Changzhou', 'China']],
            'All the above' : ['you': ['projects', 'anywhere']],
        }

    def doing(self, now=2023):
        today = self.year

        if now < today:
            experience = self.employment['engineer']
            return """
            I had the opportunity to be part of an intership in {large_firms} in {big_cities}.
            """.format(large_firms=experience[0], big_cities=experience[1])

        elif now = today:
            dream = self.education['Machine Learning']
            return """
            I am currently learning {code} at {code_institute}.
            """.format(code=dream[0], code_institute=dream[1])

        elif now > today:
            goal = self.employment['All the above']
            return """
            I am eager to collaborate with {teams} on {projects}.
            """.format(teams=goal[0], projects='software development')
        else:
            return """
            ### Hi there 👋
            """
        
    def collaborate(self, role, organization, location):
        opportunity = self.employment
        opportunity[role] = [organization, location]

me = ReadMe(2023)
```
