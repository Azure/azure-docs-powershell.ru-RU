---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 2bae2753861f182943e4ced142f6a2b3ac84bb1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222081"
---
# <span data-ttu-id="e2985-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e2985-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="e2985-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2985-102">SYNOPSIS</span></span>
<span data-ttu-id="e2985-103">Задает политику хранения на сервере в течение долгого времени.</span><span class="sxs-lookup"><span data-stu-id="e2985-103">Sets a server long term retention policy.</span></span>

## <span data-ttu-id="e2985-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e2985-104">SYNTAX</span></span>

### <span data-ttu-id="e2985-105">WeeklyRetentionRequired (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2985-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2985-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="e2985-106">RemovePolicy</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2985-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="e2985-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2985-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="e2985-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2985-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2985-109">DESCRIPTION</span></span>
<span data-ttu-id="e2985-110">Для этой базы данных задана долгосрочная политика хранения **Set-AzSqlDatabaseBackupLongTermRetentionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="e2985-110">The **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="e2985-111">Политика — это ресурс резервной копии Azure, используемый для определения политики резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e2985-111">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="e2985-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e2985-112">EXAMPLES</span></span>

### <span data-ttu-id="e2985-113">Пример 1. Настройка еженедельного хранения для текущей версии долгосрочной политики хранения</span><span class="sxs-lookup"><span data-stu-id="e2985-113">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="e2985-114">В этом случае политика долгосрочного хранения базы данных01 сохраняет еженедельную полную резервную копию в течение 2 недель.</span><span class="sxs-lookup"><span data-stu-id="e2985-114">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="e2985-115">Пример 2. Настройка ежемесячного хранения для текущей версии долгосрочной политики хранения</span><span class="sxs-lookup"><span data-stu-id="e2985-115">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="e2985-116">В этом случае политика долгосрочного хранения базы данных01 сохраняет первую полную резервную копию каждого месяца в течение 5 лет.</span><span class="sxs-lookup"><span data-stu-id="e2985-116">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="e2985-117">Пример 3. Настройка ежегодного хранения для текущей версии долгосрочной политики хранения</span><span class="sxs-lookup"><span data-stu-id="e2985-117">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="e2985-118">В этом случае для сохранения полной резервной копии, сделанных на 26-й неделе года, в течение 10 лет устанавливается политика хранения в долгосрочной перспективе.</span><span class="sxs-lookup"><span data-stu-id="e2985-118">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="e2985-119">Пример 4. Настройка каждого хранения для текущей версии долгосрочной политики хранения</span><span class="sxs-lookup"><span data-stu-id="e2985-119">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="e2985-120">В этом случае в базе данных01 создается политика долгосрочного хранения, которая сохраняет полную резервную копию в течение 14 дней, первую полную резервную копию каждого месяца в течение 24 недель, а также полную резервную копию за 26-ю неделю года в течение 10 лет.</span><span class="sxs-lookup"><span data-stu-id="e2985-120">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="e2985-121">Пример 5. Удаление долгосрочной политики хранения</span><span class="sxs-lookup"><span data-stu-id="e2985-121">Example 5: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="e2985-122">Удаляет политику для базы данных01, чтобы больше не сохранять резервные копии хранения в долгосрочной перспективе.</span><span class="sxs-lookup"><span data-stu-id="e2985-122">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="e2985-123">Это не повлияет на уже сделанные резервные копии</span><span class="sxs-lookup"><span data-stu-id="e2985-123">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="e2985-124">Пример 6. Удаление долгосрочной политики хранения</span><span class="sxs-lookup"><span data-stu-id="e2985-124">Example 6: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="e2985-125">Это еще один способ удаления политики для базы данных01, чтобы она больше не сохраняет резервные копии хранения в долгосрочной перспективе.</span><span class="sxs-lookup"><span data-stu-id="e2985-125">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="e2985-126">Это не повлияет на уже сделанные резервные копии</span><span class="sxs-lookup"><span data-stu-id="e2985-126">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="e2985-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2985-127">PARAMETERS</span></span>

### <span data-ttu-id="e2985-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e2985-128">-DatabaseName</span></span>
<span data-ttu-id="e2985-129">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e2985-129">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2985-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2985-130">-DefaultProfile</span></span>
<span data-ttu-id="e2985-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2985-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2985-132">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="e2985-132">-MonthlyRetention</span></span>
<span data-ttu-id="e2985-133">Ежемесячное хранение.</span><span class="sxs-lookup"><span data-stu-id="e2985-133">The Monthly Retention.</span></span>
<span data-ttu-id="e2985-134">Если передать только число, а не строку ISO 8601, в качестве единицы будет считаться число.</span><span class="sxs-lookup"><span data-stu-id="e2985-134">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="e2985-135">Минимальное значение — 7 дней, а максимальное — 10 лет.</span><span class="sxs-lookup"><span data-stu-id="e2985-135">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2985-136">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="e2985-136">-RemovePolicy</span></span>
<span data-ttu-id="e2985-137">При этом политика для базы данных будет удалена.</span><span class="sxs-lookup"><span data-stu-id="e2985-137">If provided, the policy for the database will be removed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2985-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2985-138">-ResourceGroupName</span></span>
<span data-ttu-id="e2985-139">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2985-139">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2985-140">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e2985-140">-ServerName</span></span>
<span data-ttu-id="e2985-141">Имя azure, SQL Server находится в базе данных.</span><span class="sxs-lookup"><span data-stu-id="e2985-141">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2985-142">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="e2985-142">-WeeklyRetention</span></span>
<span data-ttu-id="e2985-143">Еженедельное хранение.</span><span class="sxs-lookup"><span data-stu-id="e2985-143">The Weekly Retention.</span></span>
<span data-ttu-id="e2985-144">Если передать только число, а не строку ISO 8601, в качестве единицы будет считаться число.</span><span class="sxs-lookup"><span data-stu-id="e2985-144">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="e2985-145">Минимальное значение — 7 дней, а максимальное — 10 лет.</span><span class="sxs-lookup"><span data-stu-id="e2985-145">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2985-146">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="e2985-146">-WeekOfYear</span></span>
<span data-ttu-id="e2985-147">Неделя года с 1 по 52 для сохранения в ежегодном хранении.</span><span class="sxs-lookup"><span data-stu-id="e2985-147">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2985-148">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="e2985-148">-YearlyRetention</span></span>
<span data-ttu-id="e2985-149">Ежегодное хранение.</span><span class="sxs-lookup"><span data-stu-id="e2985-149">The Yearly Retention.</span></span>
<span data-ttu-id="e2985-150">Если передать только число, а не строку ISO 8601, в качестве единицы будет считаться число.</span><span class="sxs-lookup"><span data-stu-id="e2985-150">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="e2985-151">Минимальное значение — 7 дней, а максимальное — 10 лет.</span><span class="sxs-lookup"><span data-stu-id="e2985-151">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2985-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2985-152">-Confirm</span></span>
<span data-ttu-id="e2985-153">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e2985-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2985-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2985-154">-WhatIf</span></span>
<span data-ttu-id="e2985-155">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2985-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2985-156">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e2985-156">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2985-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2985-157">CommonParameters</span></span>
<span data-ttu-id="e2985-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2985-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2985-159">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2985-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2985-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2985-160">INPUTS</span></span>

### <span data-ttu-id="e2985-161">System.String</span><span class="sxs-lookup"><span data-stu-id="e2985-161">System.String</span></span>

### <span data-ttu-id="e2985-162">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e2985-162">System.Int32</span></span>

## <span data-ttu-id="e2985-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e2985-163">OUTPUTS</span></span>

### <span data-ttu-id="e2985-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e2985-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="e2985-165">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e2985-165">NOTES</span></span>

## <span data-ttu-id="e2985-166">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2985-166">RELATED LINKS</span></span>

[<span data-ttu-id="e2985-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e2985-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="e2985-168">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="e2985-168">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="e2985-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="e2985-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="e2985-170">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="e2985-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)