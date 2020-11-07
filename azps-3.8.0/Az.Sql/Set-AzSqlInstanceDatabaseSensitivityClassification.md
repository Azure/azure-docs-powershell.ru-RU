---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: f524c8b30f609cb2fef3fb3f59550078b26b11b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912513"
---
# <span data-ttu-id="699f7-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="699f7-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="699f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="699f7-102">SYNOPSIS</span></span>
<span data-ttu-id="699f7-103">Задает типы сведений и метки чувствительности для столбцов в базе данных SQL, управляемой службой Azure.</span><span class="sxs-lookup"><span data-stu-id="699f7-103">Sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="699f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="699f7-104">SYNTAX</span></span>

### <span data-ttu-id="699f7-105">ClassificationObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="699f7-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="699f7-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="699f7-106">ColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="699f7-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="699f7-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlManagedDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="699f7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="699f7-108">DESCRIPTION</span></span>
<span data-ttu-id="699f7-109">Командлет Set-AzSqlInstanceDatabaseSensitivityClassification задает типы данных и метки чувствительности для столбцов в базе данных SQL, управляемой с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="699f7-109">The Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="699f7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="699f7-110">EXAMPLES</span></span>

### <span data-ttu-id="699f7-111">Пример 1: Настройка типа сведений и метки чувствительности для столбца в базе данных SQL, управляемой службой Azure.</span><span class="sxs-lookup"><span data-stu-id="699f7-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="699f7-112">Пример 2: Настройка рекомендуемых типов данных и меток чувствительности для столбцов в базе данных SQL, управляемой с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="699f7-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="699f7-113">Пример 3: Настройка типа сведений и метки чувствительности для столбца в базе данных SQL, управляемой службой Azure, с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="699f7-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL managed instance database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="699f7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="699f7-114">PARAMETERS</span></span>

### <span data-ttu-id="699f7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="699f7-115">-AsJob</span></span>
<span data-ttu-id="699f7-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="699f7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="699f7-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="699f7-117">-ClassificationObject</span></span>
<span data-ttu-id="699f7-118">Объект, представляющий классификацию чувствительности базы данных управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="699f7-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="699f7-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="699f7-119">-ColumnName</span></span>
<span data-ttu-id="699f7-120">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="699f7-120">Name of column.</span></span>

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

### <span data-ttu-id="699f7-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="699f7-121">-DatabaseName</span></span>
<span data-ttu-id="699f7-122">Имя базы данных экземпляра SQL, управляемой с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="699f7-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="699f7-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="699f7-123">-DatabaseObject</span></span>
<span data-ttu-id="699f7-124">Объект базы данных экземпляра SQL, управляемый с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="699f7-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="699f7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="699f7-125">-DefaultProfile</span></span>
<span data-ttu-id="699f7-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="699f7-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="699f7-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="699f7-127">-InformationType</span></span>
<span data-ttu-id="699f7-128">Имя, описывающее тип данных, хранящихся в столбце.</span><span class="sxs-lookup"><span data-stu-id="699f7-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="699f7-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="699f7-129">-InstanceName</span></span>
<span data-ttu-id="699f7-130">Имя экземпляра с управляемым SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="699f7-130">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="699f7-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="699f7-131">-PassThru</span></span>
<span data-ttu-id="699f7-132">Указывает, следует ли выводить модель классификации чувствительности при завершении выполнения командлета</span><span class="sxs-lookup"><span data-stu-id="699f7-132">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="699f7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="699f7-133">-ResourceGroupName</span></span>
<span data-ttu-id="699f7-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="699f7-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="699f7-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="699f7-135">-SchemaName</span></span>
<span data-ttu-id="699f7-136">Имя схемы.</span><span class="sxs-lookup"><span data-stu-id="699f7-136">Name of schema.</span></span>

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

### <span data-ttu-id="699f7-137">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="699f7-137">-SensitivityLabel</span></span>
<span data-ttu-id="699f7-138">Имя, которое описывает чувствительность данных, хранящихся в столбце.</span><span class="sxs-lookup"><span data-stu-id="699f7-138">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="699f7-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="699f7-139">-TableName</span></span>
<span data-ttu-id="699f7-140">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="699f7-140">Name of table.</span></span>

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

### <span data-ttu-id="699f7-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="699f7-141">-Confirm</span></span>
<span data-ttu-id="699f7-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="699f7-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="699f7-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="699f7-143">-WhatIf</span></span>
<span data-ttu-id="699f7-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="699f7-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="699f7-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="699f7-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="699f7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="699f7-146">CommonParameters</span></span>
<span data-ttu-id="699f7-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="699f7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="699f7-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="699f7-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="699f7-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="699f7-149">INPUTS</span></span>

### <span data-ttu-id="699f7-150">Microsoft. Azure. Commands. SQL. Classification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="699f7-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="699f7-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="699f7-151">OUTPUTS</span></span>

### <span data-ttu-id="699f7-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="699f7-152">System.Boolean</span></span>

## <span data-ttu-id="699f7-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="699f7-153">NOTES</span></span>

## <span data-ttu-id="699f7-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="699f7-154">RELATED LINKS</span></span>

[<span data-ttu-id="699f7-155">Дополнительные сведения об обнаружении и классификации данных в базе данных Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="699f7-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
