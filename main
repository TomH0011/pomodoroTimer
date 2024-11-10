import time
import datetime

class pomodoro():

    def times(self):
        print("How many study sessions would you like?: ")
        try:
            y = int(input())
            if y < 0 or y > 10:
                raise ValueError
        except:
            print("Invalid amount, please pick between 0 and 10 minutes inclusive")
            return None

        print("How long would you like the study section to last?: ")
        try:
            x = int(input())
            if x < 0 or x > 60:
                raise ValueError
        except:
            print("Invalid timing, please pick between 0 and 60 minutes inclusive")
            raise ValueError
        if x and y:
            return x, y
        else:
            print("Invalid inputs, please try again")
            return None

    def timer(self, x, y):

        while y > 0:

            total_time = x * 60
            rest_time = (x // 2) * 60

            while total_time > 0:
                # work_Timer represents time left on countdown
                work_timer = datetime.timedelta(seconds=total_time)

                # Prints the time left on the timer
                print(f"\rStudy Time Remaining: {work_timer}", end="")

                # Delays the program one second
                time.sleep(1)

                # Reduces total time by one second
                total_time -= 1

                if total_time == 0:
                    while rest_time > 0:
                        # rest_Timer represents time left on countdown
                        rest_timer = datetime.timedelta(seconds=rest_time)

                        # Prints the time left on the timer
                        print(f"\rBreak Time Remaining: {rest_timer}", end="")

                        # Delays the program one second
                        time.sleep(1)

                        # Reduces total time by one second
                        rest_time -= 1
            print("\nBreak over. Back to study!")
            y-=1


        print("Bzzzt! The countdown is at zero seconds! Study session has concluded")


pomodoro = pomodoro()
times_result = pomodoro.times()

if times_result is not None:
    x, y = times_result
    pomodoro.timer(x, y)
else:
    print("Failed to start the timer due to invalid inputs.")





