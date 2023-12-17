# Powershell HTTP request
Invoke-WebRequest -Uri http://localhost:8080/kpi/values/pcf

# Powershell string search
netstat -aon | Select-String "8080"

# Powershell task kill
taskkill /F /PID <-PID->
