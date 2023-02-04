# mahalanobisdistance
Mahalanobis Distance

# Calculating mahalanobis distance
import numphy as np

data = np.array([
[64, 580, 29],
[66, 570, 33],
[68, 590, 37],
[69, 660, 46],
[73, 600, 55]])

P1 = np.array([[66, 640, 44]])
m = np.mean([68, 600, 40])
print["Mean: ", m]

P1Mm = P1 - m
print["The difference with mean P1Mm: ", P1Mm]

data = np.transpose(data)
covM = np.cov(data, bias =False)
invCoveM = np.linalg.inv(covM)

tem1 = np.dot(P1Mm, invCoveM)
tem2 = np.dot(tem1, np.transpose(P1Mm))
print(tem1)
print(tem2)
MD = np.sqrt(tem2)

print("The Mahalanobis Distance: ", np.reshape(MD, -1))
