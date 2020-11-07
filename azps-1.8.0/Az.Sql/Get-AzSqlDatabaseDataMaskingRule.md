---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 5c43820c57531ca5a844e1ab429c26d85fecceee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729037"
---
# <span data-ttu-id="b75ab-101">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b75ab-101">Get-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="b75ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b75ab-102">SYNOPSIS</span></span>
<span data-ttu-id="b75ab-103">Получает правила маскирования данных из базы данных.</span><span class="sxs-lookup"><span data-stu-id="b75ab-103">Gets the data masking rules from a database.</span></span>

## <span data-ttu-id="b75ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b75ab-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b75ab-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b75ab-105">DESCRIPTION</span></span>
<span data-ttu-id="b75ab-106">Командлет **Get-AzSqlDatabaseDataMaskingRule** получает конкретное правило маскировки данных или все правила маскировки данных для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b75ab-106">The **Get-AzSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="b75ab-107">Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных, а параметр *RuleId* — для указания того, какое правило возвращает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b75ab-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="b75ab-108">Если вы не предоставляли *RuleId* , возвращаются все правила маскировки данных для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b75ab-108">If you do not provide *RuleId* , all the data masking rules for that Azure SQL database are returned.</span></span>
<span data-ttu-id="b75ab-109">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="b75ab-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b75ab-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b75ab-110">EXAMPLES</span></span>

### <span data-ttu-id="b75ab-111">Пример 1: получение всех правил маскирования данных из базы данных</span><span class="sxs-lookup"><span data-stu-id="b75ab-111">Example 1: Get all data masking rules from a database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :

DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table2
ColumnName        : column2
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

### <span data-ttu-id="b75ab-112">Пример 2: получение правила маскировки данных, определенного в схеме dbo, таблица "table1" и столбец "Столбец1".</span><span class="sxs-lookup"><span data-stu-id="b75ab-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

## <span data-ttu-id="b75ab-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b75ab-113">PARAMETERS</span></span>

### <span data-ttu-id="b75ab-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="b75ab-114">-ColumnName</span></span>
<span data-ttu-id="b75ab-115">Задает имя столбца, на которое указывает правило маскирования.</span><span class="sxs-lookup"><span data-stu-id="b75ab-115">Specifies the name of the column targeted by the masking rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b75ab-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b75ab-116">-DatabaseName</span></span>
<span data-ttu-id="b75ab-117">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="b75ab-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="b75ab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b75ab-118">-DefaultProfile</span></span>
<span data-ttu-id="b75ab-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b75ab-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b75ab-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b75ab-120">-ResourceGroupName</span></span>
<span data-ttu-id="b75ab-121">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="b75ab-121">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="b75ab-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="b75ab-122">-SchemaName</span></span>
<span data-ttu-id="b75ab-123">Указывает имя схемы.</span><span class="sxs-lookup"><span data-stu-id="b75ab-123">Specifies the name of a schema.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b75ab-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="b75ab-124">-ServerName</span></span>
<span data-ttu-id="b75ab-125">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="b75ab-125">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="b75ab-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="b75ab-126">-TableName</span></span>
<span data-ttu-id="b75ab-127">Указывает имя таблицы Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b75ab-127">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b75ab-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b75ab-128">-Confirm</span></span>
<span data-ttu-id="b75ab-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b75ab-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b75ab-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b75ab-130">-WhatIf</span></span>
<span data-ttu-id="b75ab-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b75ab-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b75ab-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b75ab-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b75ab-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b75ab-133">CommonParameters</span></span>
<span data-ttu-id="b75ab-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b75ab-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b75ab-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b75ab-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b75ab-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b75ab-136">INPUTS</span></span>

### <span data-ttu-id="b75ab-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b75ab-137">System.String</span></span>

## <span data-ttu-id="b75ab-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b75ab-138">OUTPUTS</span></span>

### <span data-ttu-id="b75ab-139">Microsoft. Azure. Commands. SQL. маскирует. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="b75ab-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="b75ab-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="b75ab-140">NOTES</span></span>

## <span data-ttu-id="b75ab-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b75ab-141">RELATED LINKS</span></span>

[<span data-ttu-id="b75ab-142">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="b75ab-142">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="b75ab-143">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b75ab-143">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b75ab-144">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b75ab-144">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b75ab-145">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="b75ab-145">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="b75ab-146">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b75ab-146">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


