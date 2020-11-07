---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: e21bf168093d2589321d6952ca45af7e9f8c0cbe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912612"
---
# <span data-ttu-id="04205-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="04205-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="04205-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="04205-102">SYNOPSIS</span></span>
<span data-ttu-id="04205-103">Включает рекомендации по пометкам для столбцов (рекомендации включены по умолчанию во всех столбцах) в базе данных SQL Server с управляемым экземпляром Azure.</span><span class="sxs-lookup"><span data-stu-id="04205-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="04205-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="04205-104">SYNTAX</span></span>

### <span data-ttu-id="04205-105">InputObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="04205-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04205-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="04205-106">ColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04205-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="04205-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04205-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04205-108">DESCRIPTION</span></span>
<span data-ttu-id="04205-109">Командлет Enable-AzSqlInstanceDatabaseSensitivityRecommendation включает рекомендации по отметкам для столбцов в базе данных экземпляра SQL, управляемой службой Azure.</span><span class="sxs-lookup"><span data-stu-id="04205-109">The Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="04205-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="04205-110">EXAMPLES</span></span>

### <span data-ttu-id="04205-111">Пример 1: Включите рекомендации по чувствительности для определенного столбца в базе данных экземпляра SQL, управляемой с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="04205-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Enable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="04205-112">Пример 2: Включите рекомендации по отметкам для определенного столбца в базе данных экземпляра SQL с управляемой службой Azure с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="04205-112">Example 2: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="04205-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="04205-113">PARAMETERS</span></span>

### <span data-ttu-id="04205-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04205-114">-AsJob</span></span>
<span data-ttu-id="04205-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="04205-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04205-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="04205-116">-ColumnName</span></span>
<span data-ttu-id="04205-117">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="04205-117">Name of column.</span></span>

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

### <span data-ttu-id="04205-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="04205-118">-DatabaseName</span></span>
<span data-ttu-id="04205-119">Имя базы данных экземпляра SQL, управляемой с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="04205-119">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="04205-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="04205-120">-DatabaseObject</span></span>
<span data-ttu-id="04205-121">Объект базы данных экземпляра SQL, управляемый с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="04205-121">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="04205-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04205-122">-DefaultProfile</span></span>
<span data-ttu-id="04205-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="04205-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04205-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04205-124">-InputObject</span></span>
<span data-ttu-id="04205-125">Объект, представляющий классификацию чувствительности базы данных управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="04205-125">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="04205-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="04205-126">-InstanceName</span></span>
<span data-ttu-id="04205-127">Имя экземпляра с управляемым SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="04205-127">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="04205-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04205-128">-PassThru</span></span>
<span data-ttu-id="04205-129">Указывает, следует ли выводить модель классификации чувствительности при завершении выполнения командлета</span><span class="sxs-lookup"><span data-stu-id="04205-129">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="04205-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04205-130">-ResourceGroupName</span></span>
<span data-ttu-id="04205-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="04205-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="04205-132">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="04205-132">-SchemaName</span></span>
<span data-ttu-id="04205-133">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="04205-133">Name of schema.</span></span>

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

### <span data-ttu-id="04205-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="04205-134">-TableName</span></span>
<span data-ttu-id="04205-135">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="04205-135">Name of table.</span></span>

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

### <span data-ttu-id="04205-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04205-136">-Confirm</span></span>
<span data-ttu-id="04205-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="04205-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04205-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04205-138">-WhatIf</span></span>
<span data-ttu-id="04205-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="04205-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04205-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="04205-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04205-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04205-141">CommonParameters</span></span>
<span data-ttu-id="04205-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="04205-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04205-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04205-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04205-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="04205-144">INPUTS</span></span>

### <span data-ttu-id="04205-145">Microsoft. Azure. Commands. SQL. Classification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="04205-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="04205-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="04205-146">OUTPUTS</span></span>

### <span data-ttu-id="04205-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04205-147">System.Boolean</span></span>

## <span data-ttu-id="04205-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="04205-148">NOTES</span></span>

## <span data-ttu-id="04205-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04205-149">RELATED LINKS</span></span>

[<span data-ttu-id="04205-150">Дополнительные сведения об обнаружении и классификации данных в базе данных Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="04205-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)