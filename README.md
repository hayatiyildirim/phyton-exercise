# phyton-exercise
import math

# 1. Noktaların Tanımlanması
points = [(1, 2), (4, 6), (7, 8), (3, 5)]

# 2. Öklid Mesafesi İçin Fonksiyon
def euclideanDistance(point1, point2):
    # Öklid mesafesi formülü: √((x2 - x1)² + (y2 - y1)²)
    x1, y1 = point1
    x2, y2 = point2
    return math.sqrt((x2 - x1)**2 + (y2 - y1)**2)

# 3. Mesafelerin Hesaplanması
distances = []
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        dist = euclideanDistance(points[i], points[j])
        distances.append(dist)

# 4. Minimum Mesafenin Bulunması
min_distance = min(distances)
print(f"Minimum mesafe: {min_distance}")
