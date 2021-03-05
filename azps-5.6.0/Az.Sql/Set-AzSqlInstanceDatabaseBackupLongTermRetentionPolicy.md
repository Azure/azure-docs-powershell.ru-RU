---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: b8284d4f2ac5b28baffed630e789fc002c2c7d9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015848"
---
# <span data-ttu-id="2a497-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2a497-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="2a497-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a497-102">SYNOPSIS</span></span>
<span data-ttu-id="2a497-103">Для долгосрочной политики хранения управляемой базы данных задана cmdlet **Set-AzSqlInstanceDatabaseLongTermRetentionBackup.**</span><span class="sxs-lookup"><span data-stu-id="2a497-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="2a497-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2a497-104">SYNTAX</span></span>

### <span data-ttu-id="2a497-105">WeeklyRetentionRequired (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a497-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a497-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="2a497-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a497-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="2a497-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a497-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="2a497-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a497-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a497-109">DESCRIPTION</span></span>
<span data-ttu-id="2a497-110">Cmdlet **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** задает политику хранения в долгосрочной перспективе для этой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="2a497-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="2a497-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2a497-111">EXAMPLES</span></span>

### <span data-ttu-id="2a497-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2a497-112">Example 1</span></span>
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

<span data-ttu-id="2a497-113">Настраивает еженедельную политику долгосрочного хранения базы данных на одну неделю.</span><span class="sxs-lookup"><span data-stu-id="2a497-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="2a497-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2a497-114">Example 2</span></span>
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

<span data-ttu-id="2a497-115">Эта команда удаляет из базы данных долгосрочные политики хранения.</span><span class="sxs-lookup"><span data-stu-id="2a497-115">This command removes the long term retention policy from the database.</span></span>

### <span data-ttu-id="2a497-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2a497-116">Example 3</span></span>

<span data-ttu-id="2a497-117">Этот Set-AzSqlInstanceDatabaseLongTermRetentionBackup задает долгосрочное хранение для управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="2a497-117">The Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet sets a managed database's long term retention policy.</span></span> <span data-ttu-id="2a497-118">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="2a497-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -DatabaseName target1 -InstanceName testInstance -MonthlyRetention P24W -ResourceGroupName testResourceGroup -WeekOfYear 26 -WeeklyRetention 'P1W' -YearlyRetention P10Y
```

## <span data-ttu-id="2a497-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a497-119">PARAMETERS</span></span>

### <span data-ttu-id="2a497-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2a497-120">-DatabaseName</span></span>
<span data-ttu-id="2a497-121">Имя управляемой базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="2a497-121">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="2a497-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a497-122">-DefaultProfile</span></span>
<span data-ttu-id="2a497-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a497-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a497-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="2a497-124">-InstanceName</span></span>
<span data-ttu-id="2a497-125">Имя управляемого экземпляра Azure, к которой относится база данных.</span><span class="sxs-lookup"><span data-stu-id="2a497-125">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="2a497-126">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="2a497-126">-MonthlyRetention</span></span>
<span data-ttu-id="2a497-127">Ежемесячное хранение.</span><span class="sxs-lookup"><span data-stu-id="2a497-127">The Monthly Retention.</span></span>
<span data-ttu-id="2a497-128">Если передать только число, а не строку ISO 8601, в качестве единицы будут считаться дни.</span><span class="sxs-lookup"><span data-stu-id="2a497-128">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="2a497-129">Минимальное значение — 7 дней, а максимальное — 10 лет.</span><span class="sxs-lookup"><span data-stu-id="2a497-129">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="2a497-130">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="2a497-130">-RemovePolicy</span></span>
<span data-ttu-id="2a497-131">При этом политика для базы данных будет очищена.</span><span class="sxs-lookup"><span data-stu-id="2a497-131">If provided, the policy for the database will be cleared.</span></span>

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

### <span data-ttu-id="2a497-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a497-132">-ResourceGroupName</span></span>
<span data-ttu-id="2a497-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a497-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="2a497-134">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="2a497-134">-WeeklyRetention</span></span>
<span data-ttu-id="2a497-135">Еженедельное хранение.</span><span class="sxs-lookup"><span data-stu-id="2a497-135">The Weekly Retention.</span></span>
<span data-ttu-id="2a497-136">Если передать только число, а не строку ISO 8601, в качестве единицы будет считаться число.</span><span class="sxs-lookup"><span data-stu-id="2a497-136">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="2a497-137">Минимальное значение — 7 дней, а максимальное — 10 лет.</span><span class="sxs-lookup"><span data-stu-id="2a497-137">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="2a497-138">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="2a497-138">-WeekOfYear</span></span>
<span data-ttu-id="2a497-139">Неделя года с 1 по 52 для сохранения за год.</span><span class="sxs-lookup"><span data-stu-id="2a497-139">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="2a497-140">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="2a497-140">-YearlyRetention</span></span>
<span data-ttu-id="2a497-141">Ежегодное хранение.</span><span class="sxs-lookup"><span data-stu-id="2a497-141">The Yearly Retention.</span></span>
<span data-ttu-id="2a497-142">Если передать только число, а не строку ISO 8601, в качестве единицы будут считаться дни.</span><span class="sxs-lookup"><span data-stu-id="2a497-142">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="2a497-143">Минимальное значение — 7 дней, а максимальное — 10 лет.</span><span class="sxs-lookup"><span data-stu-id="2a497-143">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="2a497-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a497-144">-Confirm</span></span>
<span data-ttu-id="2a497-145">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2a497-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a497-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a497-146">-WhatIf</span></span>
<span data-ttu-id="2a497-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a497-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a497-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2a497-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a497-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a497-149">CommonParameters</span></span>
<span data-ttu-id="2a497-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a497-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a497-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a497-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a497-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a497-152">INPUTS</span></span>

### <span data-ttu-id="2a497-153">System.String</span><span class="sxs-lookup"><span data-stu-id="2a497-153">System.String</span></span>

### <span data-ttu-id="2a497-154">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2a497-154">System.Int32</span></span>

## <span data-ttu-id="2a497-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2a497-155">OUTPUTS</span></span>

### <span data-ttu-id="2a497-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="2a497-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="2a497-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2a497-157">NOTES</span></span>

## <span data-ttu-id="2a497-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a497-158">RELATED LINKS</span></span>

[<span data-ttu-id="2a497-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2a497-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="2a497-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2a497-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="2a497-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2a497-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="2a497-162">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="2a497-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)