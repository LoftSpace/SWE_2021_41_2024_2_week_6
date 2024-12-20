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
>  <code> docker exec ossp-container cat /etc/os-release </code> 
>  #### Output 1
```bash
PRETTY_NAME="Ubuntu 24.04.1 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.1 LTS (Noble Numbat)"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=noble
LOGO=ubuntu-logo
```

This command shows the contents of the /etc/os-release file inside the Docker container named ossp-container. 
> #### Command 2
> <code> docker exec ossp-container git --version </code>
> #### Output 2
> <code> git version 2.43.0 </code>

This command shows the version of Git installed in the ossp-container

> #### Command 3
> <code> docker exec ossp-container python3 --version </code>
> #### Output 3
> <code> Python 3.12.3 </code>

This command shows the version of Python 3 installed in the ossp-container

> #### Command 4
> <code> docker inspect --format="{{.HostConfig.Binds }}" ossp-container </code>
> #### Output 4
> <code> [/Users/hyj/ossp_host_dir:/mnt/osp_container_dir] </code>

This command shows the ossp-container and the bindings(mounting) between the host machine and the container
  
