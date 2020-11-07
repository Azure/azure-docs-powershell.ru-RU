---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 5d734836f822b61ac37ca0ba567eda4473e0292e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912522"
---
# <span data-ttu-id="4b456-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4b456-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="4b456-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4b456-102">SYNOPSIS</span></span>
<span data-ttu-id="4b456-103">Командлет **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** задает долгосрочную политику хранения для управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="4b456-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="4b456-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4b456-104">SYNTAX</span></span>

### <span data-ttu-id="4b456-105">WeeklyRetentionRequired (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4b456-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b456-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="4b456-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b456-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="4b456-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b456-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="4b456-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b456-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b456-109">DESCRIPTION</span></span>
<span data-ttu-id="4b456-110">Командлет **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** задает политику хранения долгосрочной безопасности для этой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="4b456-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="4b456-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4b456-111">EXAMPLES</span></span>

### <span data-ttu-id="4b456-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4b456-112">Example 1</span></span>
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

<span data-ttu-id="4b456-113">Настройка политики еженедельного хранения для базы данных в течение одной недели.</span><span class="sxs-lookup"><span data-stu-id="4b456-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="4b456-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4b456-114">Example 2</span></span>
```
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


<span data-ttu-id="4b456-115">Эта команда удаляет политику долгосрочного хранения из базы данных.</span><span class="sxs-lookup"><span data-stu-id="4b456-115">This command removes the long term retention policy from the database.</span></span>
## <span data-ttu-id="4b456-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4b456-116">PARAMETERS</span></span>

### <span data-ttu-id="4b456-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4b456-117">-DatabaseName</span></span>
<span data-ttu-id="4b456-118">Имя управляемой базы данных Azure, которую вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="4b456-118">The name of the Azure Managed Database to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b456-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b456-119">-DefaultProfile</span></span>
<span data-ttu-id="4b456-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b456-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b456-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4b456-121">-InstanceName</span></span>
<span data-ttu-id="4b456-122">Имя экземпляра, управляемого Azure, к которому относится база данных.</span><span class="sxs-lookup"><span data-stu-id="4b456-122">The name of the Azure Managed Instance the database belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b456-123">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="4b456-123">-MonthlyRetention</span></span>
<span data-ttu-id="4b456-124">Месячный срок хранения.</span><span class="sxs-lookup"><span data-stu-id="4b456-124">The Monthly Retention.</span></span>
<span data-ttu-id="4b456-125">Если вместо строки ISO 8601 передается только число, дни будут считаться единицами.</span><span class="sxs-lookup"><span data-stu-id="4b456-125">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="4b456-126">Не менее 7 дней и не более 10 лет.</span><span class="sxs-lookup"><span data-stu-id="4b456-126">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b456-127">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="4b456-127">-RemovePolicy</span></span>
<span data-ttu-id="4b456-128">Если он указан, политика для базы данных будет очищена.</span><span class="sxs-lookup"><span data-stu-id="4b456-128">If provided, the policy for the database will be cleared.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b456-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b456-129">-ResourceGroupName</span></span>
<span data-ttu-id="4b456-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4b456-130">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b456-131">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="4b456-131">-WeeklyRetention</span></span>
<span data-ttu-id="4b456-132">Сохранение в неделю.</span><span class="sxs-lookup"><span data-stu-id="4b456-132">The Weekly Retention.</span></span>
<span data-ttu-id="4b456-133">Если вместо строки ISO 8601 передается только число, дни будут считаться единицами.</span><span class="sxs-lookup"><span data-stu-id="4b456-133">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="4b456-134">Не менее 7 дней и не более 10 лет.</span><span class="sxs-lookup"><span data-stu-id="4b456-134">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b456-135">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="4b456-135">-WeekOfYear</span></span>
<span data-ttu-id="4b456-136">Неделя года, от 1 до 52, которую нужно сохранить для ежегодного хранения.</span><span class="sxs-lookup"><span data-stu-id="4b456-136">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b456-137">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="4b456-137">-YearlyRetention</span></span>
<span data-ttu-id="4b456-138">Ежегодное хранение.</span><span class="sxs-lookup"><span data-stu-id="4b456-138">The Yearly Retention.</span></span>
<span data-ttu-id="4b456-139">Если вместо строки ISO 8601 передается только число, дни будут считаться единицами.</span><span class="sxs-lookup"><span data-stu-id="4b456-139">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="4b456-140">Не менее 7 дней и не более 10 лет.</span><span class="sxs-lookup"><span data-stu-id="4b456-140">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b456-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b456-141">-Confirm</span></span>
<span data-ttu-id="4b456-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4b456-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b456-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b456-143">-WhatIf</span></span>
<span data-ttu-id="4b456-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4b456-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b456-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4b456-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b456-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b456-146">CommonParameters</span></span>
<span data-ttu-id="4b456-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4b456-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b456-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b456-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b456-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4b456-149">INPUTS</span></span>

### <span data-ttu-id="4b456-150">System. String</span><span class="sxs-lookup"><span data-stu-id="4b456-150">System.String</span></span>

### <span data-ttu-id="4b456-151">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4b456-151">System.Int32</span></span>

## <span data-ttu-id="4b456-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b456-152">OUTPUTS</span></span>

### <span data-ttu-id="4b456-153">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="4b456-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="4b456-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="4b456-154">NOTES</span></span>

## <span data-ttu-id="4b456-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b456-155">RELATED LINKS</span></span>

[<span data-ttu-id="4b456-156">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4b456-156">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="4b456-157">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="4b456-157">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="4b456-158">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="4b456-158">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="4b456-159">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="4b456-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)