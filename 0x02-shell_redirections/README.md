- echo "Hello, World" prints “Hello, World”, followed by a new line to the standard output

echo ""(Ôo)'" displays a confused smiley "(Ôo)'

cat /etc/passwd displays the content of the /etc/passwd file

cat /etc/passwd /etc/hosts displays the content of /etc/passwd and /etc/hosts

tail /etc/passwd displays the last 10 lines of /etc/passwd

head /etc/passwd displays the first 10 lines of /etc/passwd

head -n 3 iacta | tail -n 1 displays the third line of the file iacta

echo "Best School" >"*\'"Best School"'\*$?*****:)" creates a file named exactly *\'"Best School"'\*$?*****:) containing the text Best School ending by a new line

ls -la > ls_cwd_content writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it

tail -n 1 iacta >> iacta duplicates the last line of the file iacta

find . -type f -name "*.js" -delete deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders

find ./* -type d | wc -l counts the number of directories and sub-directories in the current directory

ls -t | head -n 10 that displays the 10 newest files in the current directory

sort | uniq -u takes a list of words as input and prints only words that appear exactly once

grep -e "root" /etc/passwd displays lines containing the pattern “root” from the file /etc/passwd

grep -c "bin" /etc/passwd displays the number of lines that contain the pattern “bin” in the file /etc/passwd

grep -A 3 "root" /etc/passwd displays lines containing the pattern “root” and 3 lines after them in the file /etc/passwd

grep -v "bin" /etc/passwd Display all the lines in the file /etc/passwd that do not contain the pattern “bin”

grep ^[a-zA-Z] /etc/ssh/sshd_config displays all lines of the file /etc/ssh/sshd_config starting with a letter

tr Ac Ze replaces all characters A and c from input to Z and e respectively

tr -d cC removes all letters c and C from input

rev reverse its input

cut -d":" -f1,6 /etc/passwd | sort displays all users and their home directories, sorted by users

find . -empty -printf '%f\n' finds all empty files and directories in the current directory and all sub-directories

find -type f -name "*.gif" | rev | cut -d "/" -f 1 | cut -d '.' -f 2- | rev | LC_ALL=C sort -f lists all the files with a .gif extension in the current directory and all its sub-director

cut -c 1 | paste -s -d '' decodes acrostics that use the first letter of each line

tail -n +2 | cut -f -1 | sort -k 1 | uniq -c | sort -rnk 1 | head -n 11 | rev | cut -d ' ' -f -1 | rev parses web servers logs in TSV format as input and displays the 11 hosts or IP addresses which did the most requests.
