---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: cf7cf1dcd91bc1c9f703e4fc5ca613ad6407e575
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235762"
---
# <span data-ttu-id="8ade0-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8ade0-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="8ade0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ade0-102">SYNOPSIS</span></span>
<span data-ttu-id="8ade0-103">Командлет **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** задает долгосрочную политику хранения для управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="8ade0-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="8ade0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ade0-104">SYNTAX</span></span>

### <span data-ttu-id="8ade0-105">WeeklyRetentionRequired (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ade0-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ade0-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="8ade0-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ade0-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="8ade0-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ade0-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="8ade0-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ade0-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ade0-109">DESCRIPTION</span></span>
<span data-ttu-id="8ade0-110">Командлет **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** задает политику хранения долгосрочной безопасности для этой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="8ade0-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="8ade0-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ade0-111">EXAMPLES</span></span>

### <span data-ttu-id="8ade0-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8ade0-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -WeeklyRetention "P1W"


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P1W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="8ade0-113">Настройка политики еженедельного хранения для базы данных в течение одной недели.</span><span class="sxs-lookup"><span data-stu-id="8ade0-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="8ade0-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8ade0-114">Example 2</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName target1 -RemovePolicy


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : target1
WeeklyRetention     : PT0S
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="8ade0-115">Эта команда удаляет политику долгосрочного хранения из базы данных.</span><span class="sxs-lookup"><span data-stu-id="8ade0-115">This command removes the long term retention policy from the database.</span></span>

### <span data-ttu-id="8ade0-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8ade0-116">Example 3</span></span>

<span data-ttu-id="8ade0-117">Командлет Set-AzSqlInstanceDatabaseLongTermRetentionBackup задает долгосрочную политику хранения для управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="8ade0-117">The Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet sets a managed database's long term retention policy.</span></span> <span data-ttu-id="8ade0-118">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="8ade0-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -DatabaseName target1 -InstanceName testInstance -MonthlyRetention P24W -ResourceGroupName testResourceGroup -WeekOfYear 26 -WeeklyRetention 'P1W' -YearlyRetention P10Y
```

## <span data-ttu-id="8ade0-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ade0-119">PARAMETERS</span></span>

### <span data-ttu-id="8ade0-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8ade0-120">-DatabaseName</span></span>
<span data-ttu-id="8ade0-121">Имя управляемой базы данных Azure, которую вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="8ade0-121">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="8ade0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ade0-122">-DefaultProfile</span></span>
<span data-ttu-id="8ade0-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ade0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ade0-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="8ade0-124">-InstanceName</span></span>
<span data-ttu-id="8ade0-125">Имя экземпляра, управляемого Azure, к которому относится база данных.</span><span class="sxs-lookup"><span data-stu-id="8ade0-125">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="8ade0-126">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="8ade0-126">-MonthlyRetention</span></span>
<span data-ttu-id="8ade0-127">Месячный срок хранения.</span><span class="sxs-lookup"><span data-stu-id="8ade0-127">The Monthly Retention.</span></span>
<span data-ttu-id="8ade0-128">Если вместо строки ISO 8601 передается только число, дни будут считаться единицами.</span><span class="sxs-lookup"><span data-stu-id="8ade0-128">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="8ade0-129">Не менее 7 дней и не более 10 лет.</span><span class="sxs-lookup"><span data-stu-id="8ade0-129">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="8ade0-130">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="8ade0-130">-RemovePolicy</span></span>
<span data-ttu-id="8ade0-131">Если он указан, политика для базы данных будет очищена.</span><span class="sxs-lookup"><span data-stu-id="8ade0-131">If provided, the policy for the database will be cleared.</span></span>

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

### <span data-ttu-id="8ade0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ade0-132">-ResourceGroupName</span></span>
<span data-ttu-id="8ade0-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ade0-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="8ade0-134">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="8ade0-134">-WeeklyRetention</span></span>
<span data-ttu-id="8ade0-135">Сохранение в неделю.</span><span class="sxs-lookup"><span data-stu-id="8ade0-135">The Weekly Retention.</span></span>
<span data-ttu-id="8ade0-136">Если вместо строки ISO 8601 передается только число, дни будут считаться единицами.</span><span class="sxs-lookup"><span data-stu-id="8ade0-136">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="8ade0-137">Не менее 7 дней и не более 10 лет.</span><span class="sxs-lookup"><span data-stu-id="8ade0-137">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="8ade0-138">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="8ade0-138">-WeekOfYear</span></span>
<span data-ttu-id="8ade0-139">Неделя года, от 1 до 52, которую нужно сохранить для ежегодного хранения.</span><span class="sxs-lookup"><span data-stu-id="8ade0-139">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="8ade0-140">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="8ade0-140">-YearlyRetention</span></span>
<span data-ttu-id="8ade0-141">Ежегодное хранение.</span><span class="sxs-lookup"><span data-stu-id="8ade0-141">The Yearly Retention.</span></span>
<span data-ttu-id="8ade0-142">Если вместо строки ISO 8601 передается только число, дни будут считаться единицами.</span><span class="sxs-lookup"><span data-stu-id="8ade0-142">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="8ade0-143">Не менее 7 дней и не более 10 лет.</span><span class="sxs-lookup"><span data-stu-id="8ade0-143">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="8ade0-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ade0-144">-Confirm</span></span>
<span data-ttu-id="8ade0-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8ade0-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ade0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ade0-146">-WhatIf</span></span>
<span data-ttu-id="8ade0-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8ade0-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ade0-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8ade0-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ade0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ade0-149">CommonParameters</span></span>
<span data-ttu-id="8ade0-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ade0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ade0-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ade0-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ade0-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ade0-152">INPUTS</span></span>

### <span data-ttu-id="8ade0-153">System. String</span><span class="sxs-lookup"><span data-stu-id="8ade0-153">System.String</span></span>

### <span data-ttu-id="8ade0-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8ade0-154">System.Int32</span></span>

## <span data-ttu-id="8ade0-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ade0-155">OUTPUTS</span></span>

### <span data-ttu-id="8ade0-156">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="8ade0-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="8ade0-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ade0-157">NOTES</span></span>

## <span data-ttu-id="8ade0-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ade0-158">RELATED LINKS</span></span>

[<span data-ttu-id="8ade0-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8ade0-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="8ade0-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8ade0-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="8ade0-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8ade0-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="8ade0-162">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="8ade0-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)