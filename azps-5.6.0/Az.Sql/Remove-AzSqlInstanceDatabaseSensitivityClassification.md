---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: 369a9f0f9bb475d27512eb13047a5a4ffe334573
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967443"
---
# <span data-ttu-id="3cdf0-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="3cdf0-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="3cdf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cdf0-102">SYNOPSIS</span></span>
<span data-ttu-id="3cdf0-103">Удаляет типы данных и метки конфиденциальности столбцов в базе данных azure SQL экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3cdf0-103">Removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="3cdf0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3cdf0-104">SYNTAX</span></span>

### <span data-ttu-id="3cdf0-105">ClassificationObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3cdf0-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cdf0-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cdf0-106">ColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cdf0-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cdf0-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cdf0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cdf0-108">DESCRIPTION</span></span>
<span data-ttu-id="3cdf0-109">Этот Remove-AzSqlInstanceDatabaseSensitivityClassification удаляет типы данных и метки конфиденциальности столбцов в базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3cdf0-109">The Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="3cdf0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3cdf0-110">EXAMPLES</span></span>

### <span data-ttu-id="3cdf0-111">Пример 1. Удаление типа данных и метки конфиденциальности столбца в базе данных azure SQL экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3cdf0-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="3cdf0-112">Пример 2. Удаление текущих типов данных и меток конфиденциальности столбцов в базе данных azure SQL экземпляра с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="3cdf0-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Remove-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="3cdf0-113">Пример 3. Удаление метки типа данных и конфиденциальности столбца в базе данных Azure SQL экземпляра с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="3cdf0-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="3cdf0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cdf0-114">PARAMETERS</span></span>

### <span data-ttu-id="3cdf0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cdf0-115">-AsJob</span></span>
<span data-ttu-id="3cdf0-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3cdf0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3cdf0-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="3cdf0-117">-ClassificationObject</span></span>
<span data-ttu-id="3cdf0-118">Объект, представляющий SQL классификации конфиденциальности базы данных управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="3cdf0-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cdf0-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="3cdf0-119">-ColumnName</span></span>
<span data-ttu-id="3cdf0-120">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="3cdf0-120">Name of column.</span></span>

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

### <span data-ttu-id="3cdf0-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3cdf0-121">-DatabaseName</span></span>
<span data-ttu-id="3cdf0-122">Имя базы данных экземпляра Azure SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3cdf0-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="3cdf0-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="3cdf0-123">-DatabaseObject</span></span>
<span data-ttu-id="3cdf0-124">Объект базы SQL экземпляра Azure.</span><span class="sxs-lookup"><span data-stu-id="3cdf0-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="3cdf0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cdf0-125">-DefaultProfile</span></span>
<span data-ttu-id="3cdf0-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3cdf0-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cdf0-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3cdf0-127">-InstanceName</span></span>
<span data-ttu-id="3cdf0-128">Azure SQL управляемым именем экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3cdf0-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="3cdf0-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cdf0-129">-PassThru</span></span>
<span data-ttu-id="3cdf0-130">Указывает, нужно ли выводить модель классификации конфиденциальности в конце выполнения cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cdf0-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="3cdf0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cdf0-131">-ResourceGroupName</span></span>
<span data-ttu-id="3cdf0-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3cdf0-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="3cdf0-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="3cdf0-133">-SchemaName</span></span>
<span data-ttu-id="3cdf0-134">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="3cdf0-134">Name of schema.</span></span>

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

### <span data-ttu-id="3cdf0-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="3cdf0-135">-TableName</span></span>
<span data-ttu-id="3cdf0-136">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="3cdf0-136">Name of table.</span></span>

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

### <span data-ttu-id="3cdf0-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cdf0-137">-Confirm</span></span>
<span data-ttu-id="3cdf0-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cdf0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cdf0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cdf0-139">-WhatIf</span></span>
<span data-ttu-id="3cdf0-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cdf0-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cdf0-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3cdf0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cdf0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cdf0-142">CommonParameters</span></span>
<span data-ttu-id="3cdf0-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cdf0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cdf0-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cdf0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cdf0-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3cdf0-145">INPUTS</span></span>

### <span data-ttu-id="3cdf0-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="3cdf0-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="3cdf0-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3cdf0-147">OUTPUTS</span></span>

### <span data-ttu-id="3cdf0-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3cdf0-148">System.Boolean</span></span>

## <span data-ttu-id="3cdf0-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3cdf0-149">NOTES</span></span>

## <span data-ttu-id="3cdf0-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3cdf0-150">RELATED LINKS</span></span>

[<span data-ttu-id="3cdf0-151">Дополнительные сведения об обнаружении и классификации SQL базе данных Azure</span><span class="sxs-lookup"><span data-stu-id="3cdf0-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
