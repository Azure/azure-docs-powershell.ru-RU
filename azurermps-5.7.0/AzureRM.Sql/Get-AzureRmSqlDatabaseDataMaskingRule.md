---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 0c04697f36558c7eb4c296e2837595541381a3d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557091"
---
# <span data-ttu-id="4c6e7-101">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="4c6e7-101">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="4c6e7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c6e7-102">SYNOPSIS</span></span>
<span data-ttu-id="4c6e7-103">Получает правила маскирования данных из базы данных.</span><span class="sxs-lookup"><span data-stu-id="4c6e7-103">Gets the data masking rules from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c6e7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c6e7-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c6e7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c6e7-105">DESCRIPTION</span></span>
<span data-ttu-id="4c6e7-106">Командлет **Get-AzureRmSqlDatabaseDataMaskingRule** получает конкретное правило маскировки данных или все правила маскировки данных для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4c6e7-106">The **Get-AzureRmSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="4c6e7-107">Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных, а параметр *RuleId* — для указания того, какое правило возвращает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4c6e7-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="4c6e7-108">Если вы не предоставляли *RuleId* , возвращаются все правила маскировки данных для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4c6e7-108">If you do not provide *RuleId* , all the data masking rules for that Azure SQL database are returned.</span></span>

<span data-ttu-id="4c6e7-109">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="4c6e7-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4c6e7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c6e7-110">EXAMPLES</span></span>

### <span data-ttu-id="4c6e7-111">Пример 1: получение всех правил маскирования данных из базы данных</span><span class="sxs-lookup"><span data-stu-id="4c6e7-111">Example 1: Get all data masking rules from a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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

### <span data-ttu-id="4c6e7-112">Пример 2: получение правила маскировки данных, определенного в схеме dbo, таблица "table1" и столбец "Столбец1".</span><span class="sxs-lookup"><span data-stu-id="4c6e7-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
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

## <span data-ttu-id="4c6e7-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c6e7-113">PARAMETERS</span></span>

### <span data-ttu-id="4c6e7-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="4c6e7-114">-ColumnName</span></span>
<span data-ttu-id="4c6e7-115">Задает имя столбца, на которое указывает правило маскирования.</span><span class="sxs-lookup"><span data-stu-id="4c6e7-115">Specifies the name of the column targeted by the masking rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6e7-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4c6e7-116">-DatabaseName</span></span>
<span data-ttu-id="4c6e7-117">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="4c6e7-117">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c6e7-118">-DefaultProfile</span></span>
<span data-ttu-id="4c6e7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4c6e7-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6e7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c6e7-120">-ResourceGroupName</span></span>
<span data-ttu-id="4c6e7-121">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="4c6e7-121">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6e7-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="4c6e7-122">-SchemaName</span></span>
<span data-ttu-id="4c6e7-123">Указывает имя схемы.</span><span class="sxs-lookup"><span data-stu-id="4c6e7-123">Specifies the name of a schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6e7-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="4c6e7-124">-ServerName</span></span>
<span data-ttu-id="4c6e7-125">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="4c6e7-125">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6e7-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="4c6e7-126">-TableName</span></span>
<span data-ttu-id="4c6e7-127">Указывает имя таблицы Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4c6e7-127">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6e7-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c6e7-128">-Confirm</span></span>
<span data-ttu-id="4c6e7-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4c6e7-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6e7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c6e7-130">-WhatIf</span></span>
<span data-ttu-id="4c6e7-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4c6e7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c6e7-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4c6e7-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6e7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c6e7-133">CommonParameters</span></span>
<span data-ttu-id="4c6e7-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c6e7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c6e7-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c6e7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c6e7-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c6e7-136">INPUTS</span></span>

###  
<span data-ttu-id="4c6e7-137">Ничего.</span><span class="sxs-lookup"><span data-stu-id="4c6e7-137">None.</span></span>

## <span data-ttu-id="4c6e7-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c6e7-138">OUTPUTS</span></span>

### <span data-ttu-id="4c6e7-139">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="4c6e7-139">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="4c6e7-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c6e7-140">NOTES</span></span>

## <span data-ttu-id="4c6e7-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c6e7-141">RELATED LINKS</span></span>

[<span data-ttu-id="4c6e7-142">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="4c6e7-142">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="4c6e7-143">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="4c6e7-143">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="4c6e7-144">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="4c6e7-144">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="4c6e7-145">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="4c6e7-145">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="4c6e7-146">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="4c6e7-146">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)


