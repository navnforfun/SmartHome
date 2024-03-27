﻿dotnet ef dbcontext scaffold -o Models/Entity -f -d "Data Source=localhost;Initial Catalog=SmartHome;User Id=sa;Password=123456;Trust Server Certificate=true" "Microsoft.EntityFrameworkCore.SqlServer"
dotnet aspnet-codegenerator controller -name SecurityLogs -namespace App.Controllers.SecurityLogs -m SmartHome.Models.Entity.SecurityLog -udl -dc App.AppDbContex
dotnet aspnet-codegenerator controller -name Account -namespace App.Controllers.Account -m SmartHome.Models.Entity.User -udl -dc SmartHome.Models.Entity.SmartHomeContext