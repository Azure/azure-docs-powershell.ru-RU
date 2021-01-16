---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 72118b8edd5f9816e14a5cfd19abbd5cabaca3dd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419532"
---
# <span data-ttu-id="dcba1-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="dcba1-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="dcba1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcba1-102">SYNOPSIS</span></span>
<span data-ttu-id="dcba1-103">Отключает (отключает) рекомендации по конфиденциальности для столбцов в базе SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dcba1-103">Disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="dcba1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dcba1-104">SYNTAX</span></span>

### <span data-ttu-id="dcba1-105">InputObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dcba1-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcba1-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcba1-106">ColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcba1-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcba1-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcba1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcba1-108">DESCRIPTION</span></span>
<span data-ttu-id="dcba1-109">Этот Disable-AzSqlInstanceDatabaseSensitivityRecommendation отключает (отключает) рекомендации по конфиденциальности для столбцов в базе SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dcba1-109">The Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="dcba1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dcba1-110">EXAMPLES</span></span>

### <span data-ttu-id="dcba1-111">Пример 1. Отключать рекомендации по конфиденциальности для данного столбца в базе данных azure SQL экземпляра.</span><span class="sxs-lookup"><span data-stu-id="dcba1-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Disable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="dcba1-112">Пример 2. Отключать рекомендации по конфиденциальности для столбцов, которые имеют рекомендации по конфиденциальности в базе данных azure SQL с Piping.</span><span class="sxs-lookup"><span data-stu-id="dcba1-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation
```

### <span data-ttu-id="dcba1-113">Пример 3. Отключать рекомендации по конфиденциальности для данного столбца в базе SQL Azure SQL с Piping.</span><span class="sxs-lookup"><span data-stu-id="dcba1-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="dcba1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcba1-114">PARAMETERS</span></span>

### <span data-ttu-id="dcba1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcba1-115">-AsJob</span></span>
<span data-ttu-id="dcba1-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="dcba1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dcba1-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="dcba1-117">-ColumnName</span></span>
<span data-ttu-id="dcba1-118">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="dcba1-118">Name of column.</span></span>

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

### <span data-ttu-id="dcba1-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dcba1-119">-DatabaseName</span></span>
<span data-ttu-id="dcba1-120">Имя базы данных экземпляра Azure SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dcba1-120">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="dcba1-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="dcba1-121">-DatabaseObject</span></span>
<span data-ttu-id="dcba1-122">Объект базы SQL экземпляра Azure.</span><span class="sxs-lookup"><span data-stu-id="dcba1-122">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="dcba1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcba1-123">-DefaultProfile</span></span>
<span data-ttu-id="dcba1-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dcba1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcba1-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcba1-125">-InputObject</span></span>
<span data-ttu-id="dcba1-126">Объект, представляющий SQL классификации конфиденциальности базы данных управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="dcba1-126">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="dcba1-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="dcba1-127">-InstanceName</span></span>
<span data-ttu-id="dcba1-128">Azure SQL управляемым именем экземпляра.</span><span class="sxs-lookup"><span data-stu-id="dcba1-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="dcba1-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dcba1-129">-PassThru</span></span>
<span data-ttu-id="dcba1-130">Указывает, нужно ли выводить модель классификации конфиденциальности в конце выполнения cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcba1-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="dcba1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcba1-131">-ResourceGroupName</span></span>
<span data-ttu-id="dcba1-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dcba1-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="dcba1-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="dcba1-133">-SchemaName</span></span>
<span data-ttu-id="dcba1-134">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="dcba1-134">Name of schema.</span></span>

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

### <span data-ttu-id="dcba1-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="dcba1-135">-TableName</span></span>
<span data-ttu-id="dcba1-136">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="dcba1-136">Name of table.</span></span>

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

### <span data-ttu-id="dcba1-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcba1-137">-Confirm</span></span>
<span data-ttu-id="dcba1-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcba1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcba1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcba1-139">-WhatIf</span></span>
<span data-ttu-id="dcba1-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcba1-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dcba1-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dcba1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcba1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcba1-142">CommonParameters</span></span>
<span data-ttu-id="dcba1-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcba1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcba1-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dcba1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcba1-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dcba1-145">INPUTS</span></span>

### <span data-ttu-id="dcba1-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="dcba1-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="dcba1-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dcba1-147">OUTPUTS</span></span>

### <span data-ttu-id="dcba1-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dcba1-148">System.Boolean</span></span>

## <span data-ttu-id="dcba1-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dcba1-149">NOTES</span></span>

## <span data-ttu-id="dcba1-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcba1-150">RELATED LINKS</span></span>

[<span data-ttu-id="dcba1-151">Дополнительные сведения об обнаружении и классификации SQL базе данных Azure</span><span class="sxs-lookup"><span data-stu-id="dcba1-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)