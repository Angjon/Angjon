```python
class ReadMe:
    def __init__(self, username="Angjon", year=2023):
        self.username = username
        self.name = 'Jonas Angulski'
        self.education = {
            'engineering': ['Mechanical Engineering', 'PUCPR'],
            'data analysis': ['Data Analysis with Python', 'Free Code Camp'],
            'machine learning': ['Machine Learning A-Z', 'Ligency I Team']
        }
        self.employment = {
            'trainee': ['Renault do Brasil', 'São José dos Pinhais'],
            'engineer job rotation': ['Xingyu Automotive Lighting', ['Changzhou', 'China']],
            'all the above' : ['you': ['projects', 'anywhere']],
        }

    def doing(self, now=2023):
        today = self.year

        if now < today:
            experience = self.employment['engineer job rotation']
            return """
            I had the opportunity to be part of an intership in {large_firms} in {big_cities}.
            """.format(large_firms=experience[0], big_cities=experience[1])

        elif now = today:
            dream = self.education['machine learning']
            return """
            I am currently learning {code} at {code_institute}.
            """.format(code=dream[0], code_institute=dream[1])

        elif now > today:
            goal = self.employment['all the above']
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
