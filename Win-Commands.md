# Powershell Web
## HTTP request
> Invoke-WebRequest -Uri http://localhost:8080/kpi/values/pcf

# Powershell Search
## String search
> netstat -aon | Select-String "8080"

# Powershell Task
## Task kill
> taskkill /F /PID <-PID->
