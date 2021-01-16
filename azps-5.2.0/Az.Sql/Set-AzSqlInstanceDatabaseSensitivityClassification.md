---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: f524c8b30f609cb2fef3fb3f59550078b26b11b9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402095"
---
# <span data-ttu-id="fc486-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="fc486-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="fc486-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc486-102">SYNOPSIS</span></span>
<span data-ttu-id="fc486-103">Задает типы данных и метки конфиденциальности столбцов в базе SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="fc486-103">Sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="fc486-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fc486-104">SYNTAX</span></span>

### <span data-ttu-id="fc486-105">ClassificationObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fc486-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc486-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc486-106">ColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc486-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc486-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlManagedDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc486-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc486-108">DESCRIPTION</span></span>
<span data-ttu-id="fc486-109">Этот Set-AzSqlInstanceDatabaseSensitivityClassification задает типы данных и метки конфиденциальности столбцов в базе SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="fc486-109">The Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="fc486-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fc486-110">EXAMPLES</span></span>

### <span data-ttu-id="fc486-111">Пример 1. Настройка типа данных и метки конфиденциальности столбца в базе данных azure SQL экземпляра.</span><span class="sxs-lookup"><span data-stu-id="fc486-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="fc486-112">Пример 2. Настройка рекомендуемых типов данных и меток конфиденциальности для столбцов в базе SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="fc486-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="fc486-113">Пример 3. Заведите тип данных и метку конфиденциальности столбца в базе данных управляемых экземпляров Azure SQL с помощью piping.</span><span class="sxs-lookup"><span data-stu-id="fc486-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL managed instance database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="fc486-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc486-114">PARAMETERS</span></span>

### <span data-ttu-id="fc486-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc486-115">-AsJob</span></span>
<span data-ttu-id="fc486-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fc486-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc486-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="fc486-117">-ClassificationObject</span></span>
<span data-ttu-id="fc486-118">Объект, представляющий SQL классификации конфиденциальности базы данных управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="fc486-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="fc486-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="fc486-119">-ColumnName</span></span>
<span data-ttu-id="fc486-120">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="fc486-120">Name of column.</span></span>

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

### <span data-ttu-id="fc486-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fc486-121">-DatabaseName</span></span>
<span data-ttu-id="fc486-122">Имя базы данных экземпляра Azure SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="fc486-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="fc486-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="fc486-123">-DatabaseObject</span></span>
<span data-ttu-id="fc486-124">Объект базы SQL экземпляра Azure.</span><span class="sxs-lookup"><span data-stu-id="fc486-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="fc486-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc486-125">-DefaultProfile</span></span>
<span data-ttu-id="fc486-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc486-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc486-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="fc486-127">-InformationType</span></span>
<span data-ttu-id="fc486-128">Имя, описыва которое описывает тип данных, хранимых в столбце.</span><span class="sxs-lookup"><span data-stu-id="fc486-128">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc486-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="fc486-129">-InstanceName</span></span>
<span data-ttu-id="fc486-130">Azure SQL управляемым именем экземпляра.</span><span class="sxs-lookup"><span data-stu-id="fc486-130">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="fc486-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc486-131">-PassThru</span></span>
<span data-ttu-id="fc486-132">Указывает, нужно ли выводить модель классификации конфиденциальности в конце выполнения cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc486-132">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="fc486-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc486-133">-ResourceGroupName</span></span>
<span data-ttu-id="fc486-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc486-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="fc486-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="fc486-135">-SchemaName</span></span>
<span data-ttu-id="fc486-136">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="fc486-136">Name of schema.</span></span>

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

### <span data-ttu-id="fc486-137">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="fc486-137">-SensitivityLabel</span></span>
<span data-ttu-id="fc486-138">Имя, которое описывает конфиденциальность данных в столбце.</span><span class="sxs-lookup"><span data-stu-id="fc486-138">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc486-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="fc486-139">-TableName</span></span>
<span data-ttu-id="fc486-140">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="fc486-140">Name of table.</span></span>

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

### <span data-ttu-id="fc486-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc486-141">-Confirm</span></span>
<span data-ttu-id="fc486-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc486-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc486-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc486-143">-WhatIf</span></span>
<span data-ttu-id="fc486-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc486-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc486-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fc486-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc486-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc486-146">CommonParameters</span></span>
<span data-ttu-id="fc486-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc486-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc486-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc486-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc486-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc486-149">INPUTS</span></span>

### <span data-ttu-id="fc486-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="fc486-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="fc486-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fc486-151">OUTPUTS</span></span>

### <span data-ttu-id="fc486-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fc486-152">System.Boolean</span></span>

## <span data-ttu-id="fc486-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fc486-153">NOTES</span></span>

## <span data-ttu-id="fc486-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc486-154">RELATED LINKS</span></span>

[<span data-ttu-id="fc486-155">Дополнительные сведения об обнаружении и классификации SQL базе данных Azure</span><span class="sxs-lookup"><span data-stu-id="fc486-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
