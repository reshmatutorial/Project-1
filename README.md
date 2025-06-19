import time

def stopwatch():
    print("Stopwatch started. Press ENTER to stop.")
    start_time = time.time()
    input()
    end_time = time.time()
    elapsed = end_time - start_time
    print(f"Elapsed time: {time.strftime('%H:%M:%S', time.gmtime(elapsed))}")

def digital_clock():
    try:
        while True:
            current_time = time.strftime('%H:%M:%S')
            print(f"
