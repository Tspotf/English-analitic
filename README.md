# English-analitic

serials_db = [ { "title": "Chronicles of the Galaxy", "genre": "Adventure", "seasons": 5, "rating": 8 },
               { "title": "Mystery Island", "genre": "Fantasy", "seasons": 3, "rating": 9 },
               { "title": "Epic Quest", "genre": "Fantasy", "seasons": 4, "rating": 7 },
               { "title": "Crime Files", "genre": "Crime Drama", "seasons": 6, "rating": 5},
               { "title": "Medical Miracles", "genre": "Medical Drama", "seasons": 2, "rating": 8 },
               { "title": "Time Travelers", "genre": "Adventure", "seasons": 4, "rating": 8 },
               { "title": "Comedy Central", "genre": "Comedy", "seasons": 7, "rating": 9 } ]

def surch_genre(Genre):
    serials_genre=[]
    for serial in serials_db:
        if serial['genre'].lower()==Genre.lower:
            serials_genre.append(serial)
    return serials_genre


def surch_rating(rating):
    serials_rating=[]
    for serial in serials_db:
        if serial['rating'].lower()==rating.lower:
            serials_rating.append(rating)
    return serials_rating


 #title genre, seasons, and rating



def view_all():
    for serial in serials_db:
        print(f'Title: {serial['title']}, Genre: {serial['genre']},Seasons: {serial['seasons']},Rating: {serial['rating']}. ')


matrix=[[17, 66, 74, 36, 42, 30, 44, 16, 5, 30],
        [14, 96, 94, 84, 84, 6, 12, 22, 21, 30],
        [16, 20, 66, 7, 64, 75, 83, 11, 37, 84],
        [2, 38, 8, 7, 45, 65, 80, 56, 12, 12],
        [17, 64, 26, 53, 86, 20, 75, 55, 90, 65],
        [80, 34, 62, 88, 36, 45, 52, 69, 84, 55],
        [82, 31, 18, 72, 27, 84, 6, 3, 92, 97],
        [86, 14, 45, 45, 55, 27, 5, 10, 35, 12],
        [32, 19, 95, 99, 51, 53, 25, 64, 65, 47],
        [95, 52, 80, 40, 81, 58, 74, 92, 78, 18]]
max=matrix[0][0]
min=matrix[0][0]
count=0
frequency={
}
for i in range(10):
    for c in range(10):
        count+=matrix[i][c]
        if matrix[i][c]<min:
            min=matrix[i][c]
        if matrix[i][c]>max:
            max=matrix[i][c]
        if matrix[i][c] in frequency:
            frequency[matrix[i][c]]+=1
        else:
            frequency[matrix[i][c]]=1
print(count,'sum of all numbers')
print(frequency,'frequency')
print(max,'max number')
print(min,'min number')
