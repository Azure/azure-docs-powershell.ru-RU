---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: eb5e809b3f48403a6095f84643af0a169b2cecf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906605"
---
# <span data-ttu-id="a8e07-101">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a8e07-101">New-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="a8e07-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8e07-102">SYNOPSIS</span></span>
<span data-ttu-id="a8e07-103">Создание правила маскирования данных для базы данных.</span><span class="sxs-lookup"><span data-stu-id="a8e07-103">Creates a data masking rule for a database.</span></span>

## <span data-ttu-id="a8e07-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8e07-104">SYNTAX</span></span>

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8e07-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8e07-105">DESCRIPTION</span></span>
<span data-ttu-id="a8e07-106">Командлет **New-AzSqlDatabaseDataMaskingRule** создает правило маскирования данных для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a8e07-106">The **New-AzSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="a8e07-107">Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* , *DatabaseName* и *RuleId* , чтобы определить правило.</span><span class="sxs-lookup"><span data-stu-id="a8e07-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="a8e07-108">Укажите *TableName* и *ColumnName* для указания целевого объекта правила и параметра *MaskingFunction* , определяющего способ маскирования данных.</span><span class="sxs-lookup"><span data-stu-id="a8e07-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="a8e07-109">Если *MaskingFunction* имеет значение число или текст, вы можете указать параметры *NumberFrom* и *NumberTo* , для масок номеров, а также *PrefixSize* , *ReplacementString* и *SuffixSize* для маскирования текста.</span><span class="sxs-lookup"><span data-stu-id="a8e07-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="a8e07-110">Если команда пройдет успешно и используется параметр *PassThru* , командлет возвращает объект, описывающий свойства правила масок данных в дополнение к идентификаторам правил.</span><span class="sxs-lookup"><span data-stu-id="a8e07-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="a8e07-111">Идентификаторы правила включают, но не ограничиваются, *ResourceGroupName* , *ServerName* , *DatabaseName* и *RuleID*.</span><span class="sxs-lookup"><span data-stu-id="a8e07-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>
<span data-ttu-id="a8e07-112">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="a8e07-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a8e07-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8e07-113">EXAMPLES</span></span>

### <span data-ttu-id="a8e07-114">Пример 1: Создание правила маскирования данных для числового столбца в базе данных</span><span class="sxs-lookup"><span data-stu-id="a8e07-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="a8e07-115">Эта команда создает правило маскировки данных для столбца с именем Column01 в таблице с именем Table01 в схеме с именем Schema01.</span><span class="sxs-lookup"><span data-stu-id="a8e07-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="a8e07-116">База данных с именем Database01 включает все эти элементы.</span><span class="sxs-lookup"><span data-stu-id="a8e07-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="a8e07-117">Правило — это правило маскирования чисел, использующее случайное число в интервале от 5 до 14 в качестве значения маски.</span><span class="sxs-lookup"><span data-stu-id="a8e07-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>
<span data-ttu-id="a8e07-118">Правило называется Rule01.</span><span class="sxs-lookup"><span data-stu-id="a8e07-118">The rule is named Rule01.</span></span>

## <span data-ttu-id="a8e07-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8e07-119">PARAMETERS</span></span>

### <span data-ttu-id="a8e07-120">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="a8e07-120">-ColumnName</span></span>
<span data-ttu-id="a8e07-121">Задает имя столбца, на которое указывает правило маскирования.</span><span class="sxs-lookup"><span data-stu-id="a8e07-121">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="a8e07-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a8e07-122">-DatabaseName</span></span>
<span data-ttu-id="a8e07-123">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="a8e07-123">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="a8e07-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8e07-124">-DefaultProfile</span></span>
<span data-ttu-id="a8e07-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a8e07-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8e07-126">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="a8e07-126">-MaskingFunction</span></span>
<span data-ttu-id="a8e07-127">Указывает функцию маскирования, используемую правилом.</span><span class="sxs-lookup"><span data-stu-id="a8e07-127">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="a8e07-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a8e07-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a8e07-129">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8e07-129">Default</span></span>
- <span data-ttu-id="a8e07-130">Маскировка</span><span class="sxs-lookup"><span data-stu-id="a8e07-130">NoMasking</span></span>
- <span data-ttu-id="a8e07-131">Текстовые</span><span class="sxs-lookup"><span data-stu-id="a8e07-131">Text</span></span>
- <span data-ttu-id="a8e07-132">Счетчик</span><span class="sxs-lookup"><span data-stu-id="a8e07-132">Number</span></span>
- <span data-ttu-id="a8e07-133">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="a8e07-133">SocialSecurityNumber</span></span>
- <span data-ttu-id="a8e07-134">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="a8e07-134">CreditCardNumber</span></span>
- <span data-ttu-id="a8e07-135">Адрес электронной почты по умолчанию используется значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a8e07-135">Email The default value is Default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e07-136">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="a8e07-136">-NumberFrom</span></span>
<span data-ttu-id="a8e07-137">Задает меньшую границу интервала, из которого выделено случайное значение.</span><span class="sxs-lookup"><span data-stu-id="a8e07-137">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="a8e07-138">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Number.</span><span class="sxs-lookup"><span data-stu-id="a8e07-138">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a8e07-139">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="a8e07-139">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e07-140">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="a8e07-140">-NumberTo</span></span>
<span data-ttu-id="a8e07-141">Задает верхнюю границу интервала, из которого выделено случайное значение.</span><span class="sxs-lookup"><span data-stu-id="a8e07-141">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="a8e07-142">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Number.</span><span class="sxs-lookup"><span data-stu-id="a8e07-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a8e07-143">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="a8e07-143">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e07-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8e07-144">-PassThru</span></span>
<span data-ttu-id="a8e07-145">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="a8e07-145">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a8e07-146">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a8e07-146">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a8e07-147">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="a8e07-147">-PrefixSize</span></span>
<span data-ttu-id="a8e07-148">Указывает число знаков в начале текста, для которого не задана маска.</span><span class="sxs-lookup"><span data-stu-id="a8e07-148">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="a8e07-149">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="a8e07-149">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a8e07-150">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="a8e07-150">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e07-151">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="a8e07-151">-ReplacementString</span></span>
<span data-ttu-id="a8e07-152">Указывает число знаков в конце текста, которые не были скрыты.</span><span class="sxs-lookup"><span data-stu-id="a8e07-152">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="a8e07-153">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="a8e07-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a8e07-154">Значением по умолчанию является пустая строка.</span><span class="sxs-lookup"><span data-stu-id="a8e07-154">The default value is an empty string.</span></span>

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

### <span data-ttu-id="a8e07-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8e07-155">-ResourceGroupName</span></span>
<span data-ttu-id="a8e07-156">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="a8e07-156">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a8e07-157">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="a8e07-157">-SchemaName</span></span>
<span data-ttu-id="a8e07-158">Указывает имя схемы.</span><span class="sxs-lookup"><span data-stu-id="a8e07-158">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="a8e07-159">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="a8e07-159">-ServerName</span></span>
<span data-ttu-id="a8e07-160">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="a8e07-160">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="a8e07-161">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="a8e07-161">-SuffixSize</span></span>
<span data-ttu-id="a8e07-162">Задает количество символов в конце текста, которые не были скрыты.</span><span class="sxs-lookup"><span data-stu-id="a8e07-162">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="a8e07-163">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="a8e07-163">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a8e07-164">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="a8e07-164">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e07-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="a8e07-165">-TableName</span></span>
<span data-ttu-id="a8e07-166">Указывает имя таблицы базы данных, которая содержит столбец с маскированием.</span><span class="sxs-lookup"><span data-stu-id="a8e07-166">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="a8e07-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8e07-167">-Confirm</span></span>
<span data-ttu-id="a8e07-168">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a8e07-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8e07-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8e07-169">-WhatIf</span></span>
<span data-ttu-id="a8e07-170">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a8e07-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8e07-171">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a8e07-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8e07-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8e07-172">CommonParameters</span></span>
<span data-ttu-id="a8e07-173">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8e07-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8e07-174">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8e07-174">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8e07-175">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8e07-175">INPUTS</span></span>

### <span data-ttu-id="a8e07-176">System. String</span><span class="sxs-lookup"><span data-stu-id="a8e07-176">System.String</span></span>

### <span data-ttu-id="a8e07-177">System. Nullable "1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a8e07-177">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a8e07-178">System. Nullable "1 [[System. Double, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a8e07-178">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a8e07-179">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8e07-179">OUTPUTS</span></span>

### <span data-ttu-id="a8e07-180">Microsoft. Azure. Commands. SQL. маскирует. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="a8e07-180">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="a8e07-181">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8e07-181">NOTES</span></span>

## <span data-ttu-id="a8e07-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8e07-182">RELATED LINKS</span></span>

[<span data-ttu-id="a8e07-183">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a8e07-183">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a8e07-184">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a8e07-184">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a8e07-185">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a8e07-185">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a8e07-186">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="a8e07-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


