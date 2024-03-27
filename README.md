import sys

def find_epsilon_subtraction():
    epsilon = 1.0
    while 1.0 - epsilon != 1.0:
        epsilon /= 2
    return epsilon * 2

def find_epsilon_addition():
    epsilon = 1.0
    while 1.0 + epsilon != 1.0:
        epsilon /= 2
    return epsilon * 2

def find_max_representable_number():
    max_number = sys.float_info.max
    return max_number

def find_min_positive_number():
    min_positive = sys.float_info.min
    return min_positive

def main():
    epsilon_subtraction = find_epsilon_subtraction()
    epsilon_addition = find_epsilon_addition()
    max_representable_number = find_max_representable_number()
    min_positive_number = find_min_positive_number()

    print("Smallest epsilon for 1.0 - ε != 1.0:", epsilon_subtraction)
    print("Smallest epsilon for 1.0 + ε != 1.0:", epsilon_addition)
    print("Maximum representable number:", max_representable_number)
    print("Minimum representable positive number:", min_positive_number)

if __name__ == "__main__":
    main()
