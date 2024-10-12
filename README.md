# SWE_2021_41_2024_2_week_6

## Week 4 Assignment
> ### Repository
> > https://github.com/LoftSpace/SWE_2021_41_2024_2_week4.git

> ### Code
```python
  def isHappy(n: int) -> bool:
    def get_next(number):
        total_sum = 0
        while number > 0:
            digit = number % 10
            total_sum += digit * digit
            number //= 10
        return total_sum

    seen = set()
    while n != 1 and n not in seen:
        seen.add(n)
        n = get_next(n)

    return n == 1
    
```
> ### Description
> > A happy number is defined as a number that reaches 1 when replaced by the sum of the squares of its digits repeatedly. If this process return 1, the number is happy and if the process is in infinite loop, the number is unhappy.


## Week 5 Assignment
>  #### Command 1
>  docker exec ossp-container cat /etc/os-release
>  #### Output 1
>   PRETTY_NAME="Ubuntu 24.04.1 LTS"\
NAME="Ubuntu"\
VERSION_ID="24.04"\
VERSION="24.04.1 LTS (Noble Numbat)"\
VERSION_CODENAME=noble\
ID=ubuntu\
ID_LIKE=debian\
HOME_URL="https://www.ubuntu.com/"\
SUPPORT_URL="https://help.ubuntu.com/"\
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"\
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"\
UBUNTU_CODENAME=noble\
LOGO=ubuntu-logo\

> #### Command 2
> <code> docker exec ossp-container git --version <code>
  
> #### Output 2
> git version 2.43.0

> #### Command 3
> docker exec ossp-container python3 --version
> #### Output 3
> Python 3.12.3

> #### Command 4
> docker inspect --format="{{.HostConfig.Binds }}" ossp-container
> #### Output 4
> [/Users/hyj/ossp_host_dir:/mnt/osp_container_dir]
  
