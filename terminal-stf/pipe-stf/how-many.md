how many iter the whole rust compiler used?

`$ rg -c 'iter' compiler | awk -F ':' '{ print $2 }' | paste -sd+ - | bc`

`$ rg -c 'iter' compiler | awk -F ':' '{ print $2 }' | awk '{s+=$1} END {print s}'`