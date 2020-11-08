---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: c594a9bf247355201bc08e438af1d9dff8cd3f7d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235784"
---
# <span data-ttu-id="cac92-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="cac92-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="cac92-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cac92-102">SYNOPSIS</span></span>
<span data-ttu-id="cac92-103">Удаляет типы сведений и метки чувствительности для столбцов в базе данных экземпляра SQL, управляемой с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="cac92-103">Removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="cac92-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cac92-104">SYNTAX</span></span>

### <span data-ttu-id="cac92-105">ClassificationObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cac92-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cac92-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="cac92-106">ColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cac92-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="cac92-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cac92-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cac92-108">DESCRIPTION</span></span>
<span data-ttu-id="cac92-109">Командлет Remove-AzSqlInstanceDatabaseSensitivityClassification удаляет типы данных и метки чувствительности столбцов в базе данных экземпляра SQL, управляемой с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="cac92-109">The Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="cac92-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cac92-110">EXAMPLES</span></span>

### <span data-ttu-id="cac92-111">Пример 1: Удаление типа данных и метки чувствительности для столбца в базе данных экземпляра SQL с управляемой службой Azure.</span><span class="sxs-lookup"><span data-stu-id="cac92-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="cac92-112">Пример 2: Удаление текущих типов данных и меток секретности столбцов в базе данных экземпляра SQL с управляемой службой Azure с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="cac92-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Remove-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="cac92-113">Пример 3: Удаление типа данных и метки чувствительности для столбца в базе данных управляемого экземпляра Azure SQL с конвейером.</span><span class="sxs-lookup"><span data-stu-id="cac92-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="cac92-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cac92-114">PARAMETERS</span></span>

### <span data-ttu-id="cac92-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cac92-115">-AsJob</span></span>
<span data-ttu-id="cac92-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cac92-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cac92-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="cac92-117">-ClassificationObject</span></span>
<span data-ttu-id="cac92-118">Объект, представляющий классификацию чувствительности базы данных управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="cac92-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="cac92-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="cac92-119">-ColumnName</span></span>
<span data-ttu-id="cac92-120">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="cac92-120">Name of column.</span></span>

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

### <span data-ttu-id="cac92-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cac92-121">-DatabaseName</span></span>
<span data-ttu-id="cac92-122">Имя базы данных экземпляра SQL, управляемой с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="cac92-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="cac92-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="cac92-123">-DatabaseObject</span></span>
<span data-ttu-id="cac92-124">Объект базы данных экземпляра SQL, управляемый с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="cac92-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="cac92-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cac92-125">-DefaultProfile</span></span>
<span data-ttu-id="cac92-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cac92-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cac92-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="cac92-127">-InstanceName</span></span>
<span data-ttu-id="cac92-128">Имя экземпляра с управляемым SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="cac92-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="cac92-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cac92-129">-PassThru</span></span>
<span data-ttu-id="cac92-130">Указывает, следует ли выводить модель классификации чувствительности при завершении выполнения командлета</span><span class="sxs-lookup"><span data-stu-id="cac92-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="cac92-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cac92-131">-ResourceGroupName</span></span>
<span data-ttu-id="cac92-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cac92-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="cac92-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="cac92-133">-SchemaName</span></span>
<span data-ttu-id="cac92-134">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="cac92-134">Name of schema.</span></span>

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

### <span data-ttu-id="cac92-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="cac92-135">-TableName</span></span>
<span data-ttu-id="cac92-136">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="cac92-136">Name of table.</span></span>

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

### <span data-ttu-id="cac92-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cac92-137">-Confirm</span></span>
<span data-ttu-id="cac92-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cac92-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cac92-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cac92-139">-WhatIf</span></span>
<span data-ttu-id="cac92-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cac92-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cac92-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cac92-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cac92-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cac92-142">CommonParameters</span></span>
<span data-ttu-id="cac92-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cac92-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cac92-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cac92-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cac92-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cac92-145">INPUTS</span></span>

### <span data-ttu-id="cac92-146">Microsoft. Azure. Commands. SQL. Classification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="cac92-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="cac92-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cac92-147">OUTPUTS</span></span>

### <span data-ttu-id="cac92-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cac92-148">System.Boolean</span></span>

## <span data-ttu-id="cac92-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="cac92-149">NOTES</span></span>

## <span data-ttu-id="cac92-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cac92-150">RELATED LINKS</span></span>

[<span data-ttu-id="cac92-151">Дополнительные сведения об обнаружении и классификации данных в базе данных Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="cac92-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)