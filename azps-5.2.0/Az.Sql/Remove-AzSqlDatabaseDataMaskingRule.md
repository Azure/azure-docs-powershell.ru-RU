---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 02a6090a98a80300f886e8bbbd8e2622aa7981d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322114"
---
# <span data-ttu-id="e4595-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e4595-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="e4595-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4595-102">SYNOPSIS</span></span>
<span data-ttu-id="e4595-103">Удаляет правило маскровки данных из базы данных.</span><span class="sxs-lookup"><span data-stu-id="e4595-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="e4595-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e4595-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4595-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4595-105">DESCRIPTION</span></span>
<span data-ttu-id="e4595-106">Для **удаления определенного** правила маскровки данных из базы данных Azure SQL удаляются определенные правила маскровки данных.</span><span class="sxs-lookup"><span data-stu-id="e4595-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="e4595-107">Удалить правило маскровки данных можно с помощью параметров *ResourceGroupName,* *ServerName,* *DatabaseName* и *RuleId,* чтобы определить правило, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4595-107">You can remove a data masking rule by using the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="e4595-108">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="e4595-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e4595-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e4595-109">EXAMPLES</span></span>

### <span data-ttu-id="e4595-110">Пример 1. Удаление правила маскровки данных базы данных</span><span class="sxs-lookup"><span data-stu-id="e4595-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="e4595-111">Эта команда удаляет правило "Правило01", определенное для базы данных Database01.</span><span class="sxs-lookup"><span data-stu-id="e4595-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="e4595-112">База данных расположена на сервере Server01 и назначена группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="e4595-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="e4595-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4595-113">PARAMETERS</span></span>

### <span data-ttu-id="e4595-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="e4595-114">-ColumnName</span></span>
<span data-ttu-id="e4595-115">Указывает имя столбца, для которого задано правило маскровки.</span><span class="sxs-lookup"><span data-stu-id="e4595-115">Specifies the name of the column targeted by the masking rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4595-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e4595-116">-DatabaseName</span></span>
<span data-ttu-id="e4595-117">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="e4595-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="e4595-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4595-118">-DefaultProfile</span></span>
<span data-ttu-id="e4595-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e4595-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4595-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e4595-120">-Force</span></span>
<span data-ttu-id="e4595-121">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e4595-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e4595-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4595-122">-PassThru</span></span>
<span data-ttu-id="e4595-123">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="e4595-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e4595-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e4595-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e4595-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4595-125">-ResourceGroupName</span></span>
<span data-ttu-id="e4595-126">Имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="e4595-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="e4595-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="e4595-127">-SchemaName</span></span>
<span data-ttu-id="e4595-128">Указывает имя схемы.</span><span class="sxs-lookup"><span data-stu-id="e4595-128">Specifies the name of a schema.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4595-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e4595-129">-ServerName</span></span>
<span data-ttu-id="e4595-130">Имя сервера, на котором размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="e4595-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="e4595-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="e4595-131">-TableName</span></span>
<span data-ttu-id="e4595-132">Указывает имя таблицы Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e4595-132">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4595-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4595-133">-Confirm</span></span>
<span data-ttu-id="e4595-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e4595-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4595-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4595-135">-WhatIf</span></span>
<span data-ttu-id="e4595-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4595-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4595-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e4595-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4595-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4595-138">CommonParameters</span></span>
<span data-ttu-id="e4595-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4595-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4595-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4595-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4595-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4595-141">INPUTS</span></span>

### <span data-ttu-id="e4595-142">System.String</span><span class="sxs-lookup"><span data-stu-id="e4595-142">System.String</span></span>

## <span data-ttu-id="e4595-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e4595-143">OUTPUTS</span></span>

### <span data-ttu-id="e4595-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="e4595-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="e4595-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e4595-145">NOTES</span></span>

## <span data-ttu-id="e4595-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4595-146">RELATED LINKS</span></span>

[<span data-ttu-id="e4595-147">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e4595-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="e4595-148">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e4595-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="e4595-149">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e4595-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="e4595-150">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="e4595-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


