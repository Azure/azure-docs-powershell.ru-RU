---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 72118b8edd5f9816e14a5cfd19abbd5cabaca3dd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072955"
---
# <span data-ttu-id="57011-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="57011-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="57011-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="57011-102">SYNOPSIS</span></span>
<span data-ttu-id="57011-103">Выключает (закрывает) рекомендации по пометкам для столбцов в базе данных SQL, управляемой службой Azure.</span><span class="sxs-lookup"><span data-stu-id="57011-103">Disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="57011-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="57011-104">SYNTAX</span></span>

### <span data-ttu-id="57011-105">InputObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57011-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57011-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="57011-106">ColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57011-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="57011-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57011-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57011-108">DESCRIPTION</span></span>
<span data-ttu-id="57011-109">Командлет Disable-AzSqlInstanceDatabaseSensitivityRecommendation отключает (отправку) рекомендации по пометкам столбцов в базе данных SQL, управляемой с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="57011-109">The Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="57011-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="57011-110">EXAMPLES</span></span>

### <span data-ttu-id="57011-111">Пример 1: отключение рекомендаций по отметкам для заданного столбца в базе данных экземпляра SQL, управляемой с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="57011-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Disable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="57011-112">Пример 2. Отключите рекомендации по отметкам для столбцов, которые содержат рекомендации по пометкам в базе данных экземпляра Azure SQL Managed.</span><span class="sxs-lookup"><span data-stu-id="57011-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation
```

### <span data-ttu-id="57011-113">Пример 3. Отключите рекомендации по отметкам для определенного столбца в базе данных экземпляра SQL с управляемым управлением Azure с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="57011-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="57011-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="57011-114">PARAMETERS</span></span>

### <span data-ttu-id="57011-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57011-115">-AsJob</span></span>
<span data-ttu-id="57011-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="57011-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57011-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="57011-117">-ColumnName</span></span>
<span data-ttu-id="57011-118">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="57011-118">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57011-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="57011-119">-DatabaseName</span></span>
<span data-ttu-id="57011-120">Имя базы данных экземпляра SQL, управляемой с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="57011-120">The name of the Azure SQL managed instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57011-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="57011-121">-DatabaseObject</span></span>
<span data-ttu-id="57011-122">Объект базы данных экземпляра SQL, управляемый с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="57011-122">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57011-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57011-123">-DefaultProfile</span></span>
<span data-ttu-id="57011-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57011-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57011-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57011-125">-InputObject</span></span>
<span data-ttu-id="57011-126">Объект, представляющий классификацию чувствительности базы данных управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="57011-126">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57011-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="57011-127">-InstanceName</span></span>
<span data-ttu-id="57011-128">Имя экземпляра с управляемым SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="57011-128">Azure SQL managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57011-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57011-129">-PassThru</span></span>
<span data-ttu-id="57011-130">Указывает, следует ли выводить модель классификации чувствительности при завершении выполнения командлета</span><span class="sxs-lookup"><span data-stu-id="57011-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57011-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57011-131">-ResourceGroupName</span></span>
<span data-ttu-id="57011-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57011-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57011-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="57011-133">-SchemaName</span></span>
<span data-ttu-id="57011-134">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="57011-134">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57011-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="57011-135">-TableName</span></span>
<span data-ttu-id="57011-136">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="57011-136">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57011-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57011-137">-Confirm</span></span>
<span data-ttu-id="57011-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="57011-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57011-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57011-139">-WhatIf</span></span>
<span data-ttu-id="57011-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="57011-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57011-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="57011-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57011-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57011-142">CommonParameters</span></span>
<span data-ttu-id="57011-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="57011-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57011-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57011-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57011-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="57011-145">INPUTS</span></span>

### <span data-ttu-id="57011-146">Microsoft. Azure. Commands. SQL. Classification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="57011-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="57011-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="57011-147">OUTPUTS</span></span>

### <span data-ttu-id="57011-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="57011-148">System.Boolean</span></span>

## <span data-ttu-id="57011-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="57011-149">NOTES</span></span>

## <span data-ttu-id="57011-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57011-150">RELATED LINKS</span></span>

[<span data-ttu-id="57011-151">Дополнительные сведения об обнаружении и классификации данных в базе данных Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="57011-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)