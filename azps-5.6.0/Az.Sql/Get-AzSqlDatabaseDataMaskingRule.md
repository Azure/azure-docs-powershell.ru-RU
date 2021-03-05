---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: ab6bdaac71e13cfe62c054c5dbc01686760505ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967475"
---
# <span data-ttu-id="2f13e-101">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2f13e-101">Get-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="2f13e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f13e-102">SYNOPSIS</span></span>
<span data-ttu-id="2f13e-103">Получает правила маскровки данных из базы данных.</span><span class="sxs-lookup"><span data-stu-id="2f13e-103">Gets the data masking rules from a database.</span></span>

## <span data-ttu-id="2f13e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2f13e-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f13e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f13e-105">DESCRIPTION</span></span>
<span data-ttu-id="2f13e-106">Для **этого** можно получить определенное правило или все правила маскровки данных для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2f13e-106">The **Get-AzSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="2f13e-107">Чтобы использовать этот cmdlet, используйте *параметры ResourceGroupName,* *ServerName* и *DatabaseName,* чтобы идентифицировать базу данных, и параметр *RuleId,* чтобы указать, какое правило возвращает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f13e-107">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="2f13e-108">Если не предоставить *RuleId,* возвращаются все правила маскровки данных для базы SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2f13e-108">If you do not provide *RuleId*, all the data masking rules for that Azure SQL database are returned.</span></span>
<span data-ttu-id="2f13e-109">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="2f13e-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="2f13e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2f13e-110">EXAMPLES</span></span>

### <span data-ttu-id="2f13e-111">Пример 1. Получить все правила маскровки данных из базы данных</span><span class="sxs-lookup"><span data-stu-id="2f13e-111">Example 1: Get all data masking rules from a database</span></span>
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

### <span data-ttu-id="2f13e-112">Пример 2. Получите правило маскровки данных, определенное в схеме "dbo", таблица "таблица1" и столбец "столбец1".</span><span class="sxs-lookup"><span data-stu-id="2f13e-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
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

## <span data-ttu-id="2f13e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f13e-113">PARAMETERS</span></span>

### <span data-ttu-id="2f13e-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="2f13e-114">-ColumnName</span></span>
<span data-ttu-id="2f13e-115">Указывает имя столбца, для которого задано правило маскровки.</span><span class="sxs-lookup"><span data-stu-id="2f13e-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="2f13e-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2f13e-116">-DatabaseName</span></span>
<span data-ttu-id="2f13e-117">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="2f13e-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="2f13e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f13e-118">-DefaultProfile</span></span>
<span data-ttu-id="2f13e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2f13e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f13e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f13e-120">-ResourceGroupName</span></span>
<span data-ttu-id="2f13e-121">Имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="2f13e-121">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="2f13e-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="2f13e-122">-SchemaName</span></span>
<span data-ttu-id="2f13e-123">Указывает имя схемы.</span><span class="sxs-lookup"><span data-stu-id="2f13e-123">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="2f13e-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2f13e-124">-ServerName</span></span>
<span data-ttu-id="2f13e-125">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="2f13e-125">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="2f13e-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="2f13e-126">-TableName</span></span>
<span data-ttu-id="2f13e-127">Указывает имя таблицы Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2f13e-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="2f13e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f13e-128">-Confirm</span></span>
<span data-ttu-id="2f13e-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f13e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f13e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f13e-130">-WhatIf</span></span>
<span data-ttu-id="2f13e-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f13e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f13e-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2f13e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f13e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f13e-133">CommonParameters</span></span>
<span data-ttu-id="2f13e-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f13e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f13e-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f13e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f13e-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f13e-136">INPUTS</span></span>

### <span data-ttu-id="2f13e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2f13e-137">System.String</span></span>

## <span data-ttu-id="2f13e-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2f13e-138">OUTPUTS</span></span>

### <span data-ttu-id="2f13e-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="2f13e-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="2f13e-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2f13e-140">NOTES</span></span>

## <span data-ttu-id="2f13e-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f13e-141">RELATED LINKS</span></span>

[<span data-ttu-id="2f13e-142">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="2f13e-142">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="2f13e-143">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2f13e-143">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2f13e-144">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2f13e-144">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2f13e-145">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="2f13e-145">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="2f13e-146">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2f13e-146">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


