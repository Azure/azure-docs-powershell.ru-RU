---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: e21bf168093d2589321d6952ca45af7e9f8c0cbe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419479"
---
# <span data-ttu-id="e9e6d-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="e9e6d-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="e9e6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="e9e6d-103">Включает рекомендации по конфиденциальности для столбцов (они включены по умолчанию для всех столбцов) в базе данных azure SQL управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="e9e6d-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="e9e6d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e9e6d-104">SYNTAX</span></span>

### <span data-ttu-id="e9e6d-105">InputObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e9e6d-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9e6d-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9e6d-106">ColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9e6d-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9e6d-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9e6d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9e6d-108">DESCRIPTION</span></span>
<span data-ttu-id="e9e6d-109">Этот Enable-AzSqlInstanceDatabaseSensitivityRecommendation обеспечивает рекомендации по конфиденциальности для столбцов в базе SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e9e6d-109">The Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="e9e6d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e9e6d-110">EXAMPLES</span></span>

### <span data-ttu-id="e9e6d-111">Пример 1. Рекомендации по конфиденциальности для данного столбца в базе SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e9e6d-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Enable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="e9e6d-112">Пример 2. Включить рекомендации по конфиденциальности для данного столбца в базе SQL azure SQL с Piping.</span><span class="sxs-lookup"><span data-stu-id="e9e6d-112">Example 2: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="e9e6d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9e6d-113">PARAMETERS</span></span>

### <span data-ttu-id="e9e6d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9e6d-114">-AsJob</span></span>
<span data-ttu-id="e9e6d-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e9e6d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9e6d-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="e9e6d-116">-ColumnName</span></span>
<span data-ttu-id="e9e6d-117">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="e9e6d-117">Name of column.</span></span>

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

### <span data-ttu-id="e9e6d-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e9e6d-118">-DatabaseName</span></span>
<span data-ttu-id="e9e6d-119">Имя базы данных экземпляра Azure SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e9e6d-119">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="e9e6d-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="e9e6d-120">-DatabaseObject</span></span>
<span data-ttu-id="e9e6d-121">Объект базы SQL экземпляра Azure.</span><span class="sxs-lookup"><span data-stu-id="e9e6d-121">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="e9e6d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9e6d-122">-DefaultProfile</span></span>
<span data-ttu-id="e9e6d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9e6d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9e6d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9e6d-124">-InputObject</span></span>
<span data-ttu-id="e9e6d-125">Объект, представляющий SQL классификации конфиденциальности базы данных управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="e9e6d-125">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="e9e6d-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e9e6d-126">-InstanceName</span></span>
<span data-ttu-id="e9e6d-127">Azure SQL управляемым именем экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e9e6d-127">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="e9e6d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9e6d-128">-PassThru</span></span>
<span data-ttu-id="e9e6d-129">Указывает, нужно ли выводить модель классификации конфиденциальности в конце выполнения cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9e6d-129">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="e9e6d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9e6d-130">-ResourceGroupName</span></span>
<span data-ttu-id="e9e6d-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e9e6d-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="e9e6d-132">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="e9e6d-132">-SchemaName</span></span>
<span data-ttu-id="e9e6d-133">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="e9e6d-133">Name of schema.</span></span>

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

### <span data-ttu-id="e9e6d-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="e9e6d-134">-TableName</span></span>
<span data-ttu-id="e9e6d-135">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="e9e6d-135">Name of table.</span></span>

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

### <span data-ttu-id="e9e6d-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9e6d-136">-Confirm</span></span>
<span data-ttu-id="e9e6d-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e9e6d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9e6d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9e6d-138">-WhatIf</span></span>
<span data-ttu-id="e9e6d-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9e6d-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9e6d-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e9e6d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9e6d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9e6d-141">CommonParameters</span></span>
<span data-ttu-id="e9e6d-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9e6d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9e6d-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9e6d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9e6d-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9e6d-144">INPUTS</span></span>

### <span data-ttu-id="e9e6d-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="e9e6d-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="e9e6d-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e9e6d-146">OUTPUTS</span></span>

### <span data-ttu-id="e9e6d-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e9e6d-147">System.Boolean</span></span>

## <span data-ttu-id="e9e6d-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e9e6d-148">NOTES</span></span>

## <span data-ttu-id="e9e6d-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9e6d-149">RELATED LINKS</span></span>

[<span data-ttu-id="e9e6d-150">Дополнительные сведения об обнаружении и классификации SQL базе данных Azure</span><span class="sxs-lookup"><span data-stu-id="e9e6d-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)