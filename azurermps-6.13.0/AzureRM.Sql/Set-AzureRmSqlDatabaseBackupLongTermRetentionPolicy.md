---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: a9389999bdbd93b332a3186ede1003c896552d1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560012"
---
# <span data-ttu-id="057eb-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="057eb-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="057eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="057eb-102">SYNOPSIS</span></span>
<span data-ttu-id="057eb-103">Настройка политики хранения для серверной долгосрочной настройки.</span><span class="sxs-lookup"><span data-stu-id="057eb-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="057eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="057eb-104">SYNTAX</span></span>

### <span data-ttu-id="057eb-105">WeeklyRetentionRequired (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="057eb-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="057eb-106">Предыдущ</span><span class="sxs-lookup"><span data-stu-id="057eb-106">Legacy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="057eb-107">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="057eb-107">RemovePolicy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="057eb-108">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="057eb-108">MonthlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="057eb-109">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="057eb-109">YearlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="057eb-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="057eb-110">DESCRIPTION</span></span>
<span data-ttu-id="057eb-111">Командлет **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** задает политику долгосрочного хранения, зарегистрированную для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="057eb-111">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="057eb-112">Политика — это ресурс резервного копирования Azure, который используется для определения политики хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="057eb-112">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="057eb-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="057eb-113">EXAMPLES</span></span>

### <span data-ttu-id="057eb-114">Пример 1: Установка еженедельного хранения для текущей версии политики долгосрочного хранения</span><span class="sxs-lookup"><span data-stu-id="057eb-114">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="057eb-115">Таким образом, политика хранения для Database01 будет храниться в течение длительного полного резервного копирования в течение 2 недель.</span><span class="sxs-lookup"><span data-stu-id="057eb-115">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="057eb-116">Пример 2: Настройка месячного хранения для текущей версии политики долгосрочного хранения</span><span class="sxs-lookup"><span data-stu-id="057eb-116">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="057eb-117">Настройка политики хранения для Database01 для сохранения первой полной резервной копии каждого месяца в течение 5 лет.</span><span class="sxs-lookup"><span data-stu-id="057eb-117">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="057eb-118">Пример 3: Настройка ежегодного хранения для текущей версии политики долгосрочного хранения</span><span class="sxs-lookup"><span data-stu-id="057eb-118">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="057eb-119">Настройка политики хранения для Database01 для сохранения полной резервной копии, сделанной на 26 неделе года в течение 10 лет.</span><span class="sxs-lookup"><span data-stu-id="057eb-119">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="057eb-120">Пример 4: Настройка каждого хранения для текущей версии политики долгосрочного хранения</span><span class="sxs-lookup"><span data-stu-id="057eb-120">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="057eb-121">Таким образом, политика хранения для Database01 будет хранить все полные резервные копии в течение 14 дней, из первых полных резервных копий каждого месяца в течение 24 недель и полной резервной копии, сделанной на 26 неделе года в течение 10 лет.</span><span class="sxs-lookup"><span data-stu-id="057eb-121">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="057eb-122">Пример 4: Удаление политики долгосрочного хранения</span><span class="sxs-lookup"><span data-stu-id="057eb-122">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="057eb-123">Удаление политики для Database01, чтобы она больше не сохранила долгосрочные резервные копии хранения.</span><span class="sxs-lookup"><span data-stu-id="057eb-123">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="057eb-124">Это не повлияет на уже созданные резервные копии</span><span class="sxs-lookup"><span data-stu-id="057eb-124">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="057eb-125">Пример 4: Удаление политики долгосрочного хранения</span><span class="sxs-lookup"><span data-stu-id="057eb-125">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="057eb-126">Это еще один способ удаления политики для Database01, чтобы больше не сохранять долгосрочные резервные копии хранения.</span><span class="sxs-lookup"><span data-stu-id="057eb-126">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="057eb-127">Это не повлияет на уже созданные резервные копии</span><span class="sxs-lookup"><span data-stu-id="057eb-127">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="057eb-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="057eb-128">PARAMETERS</span></span>

### <span data-ttu-id="057eb-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="057eb-129">-DatabaseName</span></span>
<span data-ttu-id="057eb-130">Имя базы данных SQL Azure, которую нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="057eb-130">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="057eb-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="057eb-131">-DefaultProfile</span></span>
<span data-ttu-id="057eb-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="057eb-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="057eb-133">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="057eb-133">-MonthlyRetention</span></span>
<span data-ttu-id="057eb-134">Месячный срок хранения.</span><span class="sxs-lookup"><span data-stu-id="057eb-134">The Monthly Retention.</span></span>
<span data-ttu-id="057eb-135">Если вместо строки ISO 8601 передается только число, дни будут считаться единицами.</span><span class="sxs-lookup"><span data-stu-id="057eb-135">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="057eb-136">Minumum в течение 7 дней и максимум 10 лет.</span><span class="sxs-lookup"><span data-stu-id="057eb-136">There is a minumum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="057eb-137">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="057eb-137">-RemovePolicy</span></span>
<span data-ttu-id="057eb-138">Если он указан, политика для базы данных будет удалена.</span><span class="sxs-lookup"><span data-stu-id="057eb-138">If provided, the policy for the database will be removed.</span></span>

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

### <span data-ttu-id="057eb-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="057eb-139">-ResourceGroupName</span></span>
<span data-ttu-id="057eb-140">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="057eb-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="057eb-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="057eb-141">-ResourceId</span></span>
<span data-ttu-id="057eb-142">Идентификатор ресурса для политики краткосрочного хранения резервной копии.</span><span class="sxs-lookup"><span data-stu-id="057eb-142">The Resource ID of the backup long term retention policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Legacy
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="057eb-143">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="057eb-143">-ServerName</span></span>
<span data-ttu-id="057eb-144">Имя сервера Azure SQL Server, в котором находится база данных.</span><span class="sxs-lookup"><span data-stu-id="057eb-144">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="057eb-145">-State</span><span class="sxs-lookup"><span data-stu-id="057eb-145">-State</span></span>
<span data-ttu-id="057eb-146">Состояние длительного резервного копирования хранения, "включено" или "отключено"</span><span class="sxs-lookup"><span data-stu-id="057eb-146">The state of the long term retention backup policy, 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: Legacy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="057eb-147">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="057eb-147">-WeeklyRetention</span></span>
<span data-ttu-id="057eb-148">Сохранение в неделю.</span><span class="sxs-lookup"><span data-stu-id="057eb-148">The Weekly Retention.</span></span>
<span data-ttu-id="057eb-149">Если вместо строки ISO 8601 передается только число, дни будут считаться единицами.</span><span class="sxs-lookup"><span data-stu-id="057eb-149">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="057eb-150">Minumum в течение 7 дней и максимум 10 лет.</span><span class="sxs-lookup"><span data-stu-id="057eb-150">There is a minumum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="057eb-151">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="057eb-151">-WeekOfYear</span></span>
<span data-ttu-id="057eb-152">Неделя года, от 1 до 52, которую нужно сохранить для ежегодного хранения.</span><span class="sxs-lookup"><span data-stu-id="057eb-152">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="057eb-153">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="057eb-153">-YearlyRetention</span></span>
<span data-ttu-id="057eb-154">Ежегодное хранение.</span><span class="sxs-lookup"><span data-stu-id="057eb-154">The Yearly Retention.</span></span>
<span data-ttu-id="057eb-155">Если вместо строки ISO 8601 передается только число, дни будут считаться единицами.</span><span class="sxs-lookup"><span data-stu-id="057eb-155">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="057eb-156">Minumum в течение 7 дней и максимум 10 лет.</span><span class="sxs-lookup"><span data-stu-id="057eb-156">There is a minumum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="057eb-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="057eb-157">-Confirm</span></span>
<span data-ttu-id="057eb-158">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="057eb-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="057eb-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="057eb-159">-WhatIf</span></span>
<span data-ttu-id="057eb-160">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="057eb-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="057eb-161">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="057eb-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="057eb-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="057eb-162">CommonParameters</span></span>
<span data-ttu-id="057eb-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="057eb-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="057eb-164">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="057eb-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="057eb-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="057eb-165">INPUTS</span></span>

### <span data-ttu-id="057eb-166">System. String</span><span class="sxs-lookup"><span data-stu-id="057eb-166">System.String</span></span>

### <span data-ttu-id="057eb-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="057eb-167">System.Int32</span></span>

## <span data-ttu-id="057eb-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="057eb-168">OUTPUTS</span></span>

### <span data-ttu-id="057eb-169">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="057eb-169">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="057eb-170">Пуск</span><span class="sxs-lookup"><span data-stu-id="057eb-170">NOTES</span></span>

## <span data-ttu-id="057eb-171">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="057eb-171">RELATED LINKS</span></span>

[<span data-ttu-id="057eb-172">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="057eb-172">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="057eb-173">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="057eb-173">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="057eb-174">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="057eb-174">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="057eb-175">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="057eb-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
