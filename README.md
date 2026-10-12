
import re
from collections import Counter


def word_frequency(text):
    words = re.findall(r"\b[a-zA-Z]+\b", text.lower())
    return Counter(words).most_common(10)


if __name__ == "__main__":
    sample = """
    Python makes automation easier.
    Automation saves time, and Python saves effort.
    """

    for word, count in word_frequency(sample):
        print(f"{word}: {count}")
