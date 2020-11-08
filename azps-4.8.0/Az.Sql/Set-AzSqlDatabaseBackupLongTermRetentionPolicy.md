---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 2bae2753861f182943e4ced142f6a2b3ac84bb1d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243889"
---
# <span data-ttu-id="2f983-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2f983-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="2f983-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f983-102">SYNOPSIS</span></span>
<span data-ttu-id="2f983-103">Настройка политики хранения для серверной долгосрочной настройки.</span><span class="sxs-lookup"><span data-stu-id="2f983-103">Sets a server long term retention policy.</span></span>

## <span data-ttu-id="2f983-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f983-104">SYNTAX</span></span>

### <span data-ttu-id="2f983-105">WeeklyRetentionRequired (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2f983-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f983-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="2f983-106">RemovePolicy</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f983-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="2f983-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f983-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="2f983-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f983-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f983-109">DESCRIPTION</span></span>
<span data-ttu-id="2f983-110">Командлет **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** задает политику долгосрочного хранения, зарегистрированную для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="2f983-110">The **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="2f983-111">Политика — это ресурс резервного копирования Azure, который используется для определения политики хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="2f983-111">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="2f983-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f983-112">EXAMPLES</span></span>

### <span data-ttu-id="2f983-113">Пример 1: Установка еженедельного хранения для текущей версии политики долгосрочного хранения</span><span class="sxs-lookup"><span data-stu-id="2f983-113">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="2f983-114">Таким образом, политика хранения для Database01 будет храниться в течение длительного полного резервного копирования в течение 2 недель.</span><span class="sxs-lookup"><span data-stu-id="2f983-114">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="2f983-115">Пример 2: Настройка месячного хранения для текущей версии политики долгосрочного хранения</span><span class="sxs-lookup"><span data-stu-id="2f983-115">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="2f983-116">Настройка политики хранения для Database01 для сохранения первой полной резервной копии каждого месяца в течение 5 лет.</span><span class="sxs-lookup"><span data-stu-id="2f983-116">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="2f983-117">Пример 3: Настройка ежегодного хранения для текущей версии политики долгосрочного хранения</span><span class="sxs-lookup"><span data-stu-id="2f983-117">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="2f983-118">Настройка политики хранения для Database01 для сохранения полной резервной копии, сделанной на 26 неделе года в течение 10 лет.</span><span class="sxs-lookup"><span data-stu-id="2f983-118">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="2f983-119">Пример 4: Настройка каждого хранения для текущей версии политики долгосрочного хранения</span><span class="sxs-lookup"><span data-stu-id="2f983-119">Example 4: Set each retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="2f983-120">Таким образом, политика хранения для Database01 будет хранить все полные резервные копии в течение 14 дней, из первых полных резервных копий каждого месяца в течение 24 недель и полной резервной копии, сделанной на 26 неделе года в течение 10 лет.</span><span class="sxs-lookup"><span data-stu-id="2f983-120">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="2f983-121">Пример 5: Удаление политики долгосрочного хранения</span><span class="sxs-lookup"><span data-stu-id="2f983-121">Example 5: Remove the long term retention policy</span></span>
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

<span data-ttu-id="2f983-122">Удаление политики для Database01, чтобы она больше не сохранила долгосрочные резервные копии хранения.</span><span class="sxs-lookup"><span data-stu-id="2f983-122">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="2f983-123">Это не повлияет на уже созданные резервные копии</span><span class="sxs-lookup"><span data-stu-id="2f983-123">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="2f983-124">Пример 6: Удаление политики долгосрочного хранения</span><span class="sxs-lookup"><span data-stu-id="2f983-124">Example 6: Remove the long term retention policy</span></span>
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

<span data-ttu-id="2f983-125">Это еще один способ удаления политики для Database01, чтобы больше не сохранять долгосрочные резервные копии хранения.</span><span class="sxs-lookup"><span data-stu-id="2f983-125">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="2f983-126">Это не повлияет на уже созданные резервные копии</span><span class="sxs-lookup"><span data-stu-id="2f983-126">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="2f983-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f983-127">PARAMETERS</span></span>

### <span data-ttu-id="2f983-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2f983-128">-DatabaseName</span></span>
<span data-ttu-id="2f983-129">Имя базы данных SQL Azure, которую нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="2f983-129">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="2f983-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f983-130">-DefaultProfile</span></span>
<span data-ttu-id="2f983-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f983-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f983-132">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="2f983-132">-MonthlyRetention</span></span>
<span data-ttu-id="2f983-133">Месячный срок хранения.</span><span class="sxs-lookup"><span data-stu-id="2f983-133">The Monthly Retention.</span></span>
<span data-ttu-id="2f983-134">Если вместо строки ISO 8601 передается только число, дни будут считаться единицами.</span><span class="sxs-lookup"><span data-stu-id="2f983-134">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="2f983-135">Не менее 7 дней и не более 10 лет.</span><span class="sxs-lookup"><span data-stu-id="2f983-135">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="2f983-136">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="2f983-136">-RemovePolicy</span></span>
<span data-ttu-id="2f983-137">Если он указан, политика для базы данных будет удалена.</span><span class="sxs-lookup"><span data-stu-id="2f983-137">If provided, the policy for the database will be removed.</span></span>

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

### <span data-ttu-id="2f983-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f983-138">-ResourceGroupName</span></span>
<span data-ttu-id="2f983-139">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2f983-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="2f983-140">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="2f983-140">-ServerName</span></span>
<span data-ttu-id="2f983-141">Имя сервера Azure SQL Server, в котором находится база данных.</span><span class="sxs-lookup"><span data-stu-id="2f983-141">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="2f983-142">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="2f983-142">-WeeklyRetention</span></span>
<span data-ttu-id="2f983-143">Сохранение в неделю.</span><span class="sxs-lookup"><span data-stu-id="2f983-143">The Weekly Retention.</span></span>
<span data-ttu-id="2f983-144">Если вместо строки ISO 8601 передается только число, дни будут считаться единицами.</span><span class="sxs-lookup"><span data-stu-id="2f983-144">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="2f983-145">Не менее 7 дней и не более 10 лет.</span><span class="sxs-lookup"><span data-stu-id="2f983-145">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="2f983-146">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="2f983-146">-WeekOfYear</span></span>
<span data-ttu-id="2f983-147">Неделя года, от 1 до 52, которую нужно сохранить для ежегодного хранения.</span><span class="sxs-lookup"><span data-stu-id="2f983-147">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="2f983-148">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="2f983-148">-YearlyRetention</span></span>
<span data-ttu-id="2f983-149">Ежегодное хранение.</span><span class="sxs-lookup"><span data-stu-id="2f983-149">The Yearly Retention.</span></span>
<span data-ttu-id="2f983-150">Если вместо строки ISO 8601 передается только число, дни будут считаться единицами.</span><span class="sxs-lookup"><span data-stu-id="2f983-150">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="2f983-151">Не менее 7 дней и не более 10 лет.</span><span class="sxs-lookup"><span data-stu-id="2f983-151">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="2f983-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f983-152">-Confirm</span></span>
<span data-ttu-id="2f983-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2f983-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f983-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f983-154">-WhatIf</span></span>
<span data-ttu-id="2f983-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2f983-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f983-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2f983-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f983-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f983-157">CommonParameters</span></span>
<span data-ttu-id="2f983-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f983-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f983-159">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f983-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f983-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f983-160">INPUTS</span></span>

### <span data-ttu-id="2f983-161">System. String</span><span class="sxs-lookup"><span data-stu-id="2f983-161">System.String</span></span>

### <span data-ttu-id="2f983-162">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2f983-162">System.Int32</span></span>

## <span data-ttu-id="2f983-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f983-163">OUTPUTS</span></span>

### <span data-ttu-id="2f983-164">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="2f983-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="2f983-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f983-165">NOTES</span></span>

## <span data-ttu-id="2f983-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f983-166">RELATED LINKS</span></span>

[<span data-ttu-id="2f983-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2f983-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="2f983-168">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2f983-168">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="2f983-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2f983-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="2f983-170">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="2f983-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)