# pymd5-collisions
Two sample python programs with the same md5 hash to illustrate collision vulnerability.

# Explanation:
These python scripts illustrate a significant vulnerability in the MD5 hashing algorithm. Each of these programs have the same MD5 hash, but do different things. good.py and evil.py each contain a binary blob generated using Marc Stevens' MD5 collision generation tool fastcoll. This blob has the same MD5 hash, but differing SHA256 hashes. This fact is used to differentiate the behavior of the two programs.

The file "explanation.txt" contains pseudo-code describing the behavior of the two programs. Because "good.py" and "evil.py" contain binary blobs, github's text viewer cannot encode the files. Download and cat the files from a terminal prompt to view. 

# Usage:
user$ python good.py #prints "good" output
user$ python bad.py #prints "bad" output

To view hashes:
user$ openssl dgst -md5 good.py evil.py
user$ openssl dgst -sha256 good.py evil.py
