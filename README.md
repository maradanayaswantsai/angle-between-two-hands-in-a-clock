# angle-between-two-hands-in-a-clock
by this you can know the angle between small hand and big hand in the clock
def findAngle(h,m):
    h = h % 12
    h1 = (h * 360) // 12 + (m * 360) // (12 * 60)
    m1 = (m * 360) // (60)
    angle = abs(h1 - m1)
    if angle > 180:
        angle = 360 - angle
    return angle

h = int(input("hour:"))
m = int(input("minute:"))
print("Angle between two hands is %d degrees"%findAngle(h,m))
