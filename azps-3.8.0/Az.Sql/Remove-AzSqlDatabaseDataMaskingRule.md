---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 02a6090a98a80300f886e8bbbd8e2622aa7981d4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912125"
---
# <span data-ttu-id="719b7-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="719b7-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="719b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="719b7-102">SYNOPSIS</span></span>
<span data-ttu-id="719b7-103">Удаление правила маскирования данных из базы данных.</span><span class="sxs-lookup"><span data-stu-id="719b7-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="719b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="719b7-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="719b7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="719b7-105">DESCRIPTION</span></span>
<span data-ttu-id="719b7-106">Командлет **Remove-AzSqlDatabaseDataMaskingRule** удаляет конкретное правило маскировки данных из базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="719b7-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="719b7-107">Вы можете удалить правило маскировки данных с помощью параметров *ResourceGroupName* , *ServerName* , *DatabaseName* и *RuleId* , чтобы определить правило, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="719b7-107">You can remove a data masking rule by using the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="719b7-108">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="719b7-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="719b7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="719b7-109">EXAMPLES</span></span>

### <span data-ttu-id="719b7-110">Пример 1: Удаление правила маскирования данных в базе данных</span><span class="sxs-lookup"><span data-stu-id="719b7-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="719b7-111">Эта команда удаляет имя правила Rule01 определенного для Database01 базы данных.</span><span class="sxs-lookup"><span data-stu-id="719b7-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="719b7-112">База данных находится в Server01 и назначена группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="719b7-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="719b7-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="719b7-113">PARAMETERS</span></span>

### <span data-ttu-id="719b7-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="719b7-114">-ColumnName</span></span>
<span data-ttu-id="719b7-115">Задает имя столбца, на которое указывает правило маскирования.</span><span class="sxs-lookup"><span data-stu-id="719b7-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="719b7-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="719b7-116">-DatabaseName</span></span>
<span data-ttu-id="719b7-117">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="719b7-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="719b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="719b7-118">-DefaultProfile</span></span>
<span data-ttu-id="719b7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="719b7-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="719b7-120">-Force</span><span class="sxs-lookup"><span data-stu-id="719b7-120">-Force</span></span>
<span data-ttu-id="719b7-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="719b7-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="719b7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="719b7-122">-PassThru</span></span>
<span data-ttu-id="719b7-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="719b7-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="719b7-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="719b7-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="719b7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="719b7-125">-ResourceGroupName</span></span>
<span data-ttu-id="719b7-126">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="719b7-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="719b7-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="719b7-127">-SchemaName</span></span>
<span data-ttu-id="719b7-128">Указывает имя схемы.</span><span class="sxs-lookup"><span data-stu-id="719b7-128">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="719b7-129">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="719b7-129">-ServerName</span></span>
<span data-ttu-id="719b7-130">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="719b7-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="719b7-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="719b7-131">-TableName</span></span>
<span data-ttu-id="719b7-132">Указывает имя таблицы Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="719b7-132">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="719b7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="719b7-133">-Confirm</span></span>
<span data-ttu-id="719b7-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="719b7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="719b7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="719b7-135">-WhatIf</span></span>
<span data-ttu-id="719b7-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="719b7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="719b7-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="719b7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="719b7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="719b7-138">CommonParameters</span></span>
<span data-ttu-id="719b7-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="719b7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="719b7-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="719b7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="719b7-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="719b7-141">INPUTS</span></span>

### <span data-ttu-id="719b7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="719b7-142">System.String</span></span>

## <span data-ttu-id="719b7-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="719b7-143">OUTPUTS</span></span>

### <span data-ttu-id="719b7-144">Microsoft. Azure. Commands. SQL. маскирует. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="719b7-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="719b7-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="719b7-145">NOTES</span></span>

## <span data-ttu-id="719b7-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="719b7-146">RELATED LINKS</span></span>

[<span data-ttu-id="719b7-147">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="719b7-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="719b7-148">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="719b7-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="719b7-149">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="719b7-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="719b7-150">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="719b7-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


