---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 35f2bc63366a86501650af1808274a3a0403e77f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248473"
---
# <span data-ttu-id="1eb43-101">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1eb43-101">New-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="1eb43-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1eb43-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb43-103">Создание правила маскирования данных для базы данных.</span><span class="sxs-lookup"><span data-stu-id="1eb43-103">Creates a data masking rule for a database.</span></span>

## <span data-ttu-id="1eb43-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1eb43-104">SYNTAX</span></span>

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1eb43-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1eb43-105">DESCRIPTION</span></span>
<span data-ttu-id="1eb43-106">Командлет **New-AzSqlDatabaseDataMaskingRule** создает правило маскирования данных для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb43-106">The **New-AzSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="1eb43-107">Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации правила.</span><span class="sxs-lookup"><span data-stu-id="1eb43-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the rule.</span></span>
<span data-ttu-id="1eb43-108">Укажите *TableName* и *ColumnName* для указания целевого объекта правила и параметра *MaskingFunction* , определяющего способ маскирования данных.</span><span class="sxs-lookup"><span data-stu-id="1eb43-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="1eb43-109">Если *MaskingFunction* имеет значение число или текст, вы можете указать параметры *NumberFrom* и *NumberTo* , для масок номеров, а также *PrefixSize* , *ReplacementString* и *SuffixSize* для маскирования текста.</span><span class="sxs-lookup"><span data-stu-id="1eb43-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="1eb43-110">Если команда пройдет успешно и используется параметр *PassThru* , командлет возвращает объект, описывающий свойства правила масок данных в дополнение к идентификаторам правил.</span><span class="sxs-lookup"><span data-stu-id="1eb43-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="1eb43-111">Идентификаторы правила включают, но не ограничиваются, *ResourceGroupName* , *ServerName* , *DatabaseName* и *RuleID*.</span><span class="sxs-lookup"><span data-stu-id="1eb43-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>
<span data-ttu-id="1eb43-112">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb43-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1eb43-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1eb43-113">EXAMPLES</span></span>

### <span data-ttu-id="1eb43-114">Пример 1: Создание правила маскирования данных для числового столбца в базе данных</span><span class="sxs-lookup"><span data-stu-id="1eb43-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"  -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="1eb43-115">Эта команда создает правило маскировки данных для столбца с именем Column01 в таблице с именем Table01 в схеме с именем Schema01.</span><span class="sxs-lookup"><span data-stu-id="1eb43-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="1eb43-116">База данных с именем Database01 включает все эти элементы.</span><span class="sxs-lookup"><span data-stu-id="1eb43-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="1eb43-117">Правило — это правило маскирования чисел, использующее случайное число в интервале от 5 до 14 в качестве значения маски.</span><span class="sxs-lookup"><span data-stu-id="1eb43-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>

## <span data-ttu-id="1eb43-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1eb43-118">PARAMETERS</span></span>

### <span data-ttu-id="1eb43-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="1eb43-119">-ColumnName</span></span>
<span data-ttu-id="1eb43-120">Задает имя столбца, на которое указывает правило маскирования.</span><span class="sxs-lookup"><span data-stu-id="1eb43-120">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="1eb43-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1eb43-121">-DatabaseName</span></span>
<span data-ttu-id="1eb43-122">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="1eb43-122">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="1eb43-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb43-123">-DefaultProfile</span></span>
<span data-ttu-id="1eb43-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1eb43-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1eb43-125">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="1eb43-125">-MaskingFunction</span></span>
<span data-ttu-id="1eb43-126">Указывает функцию маскирования, используемую правилом.</span><span class="sxs-lookup"><span data-stu-id="1eb43-126">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="1eb43-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1eb43-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1eb43-128">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="1eb43-128">Default</span></span>
- <span data-ttu-id="1eb43-129">Маскировка</span><span class="sxs-lookup"><span data-stu-id="1eb43-129">NoMasking</span></span>
- <span data-ttu-id="1eb43-130">Текстовые</span><span class="sxs-lookup"><span data-stu-id="1eb43-130">Text</span></span>
- <span data-ttu-id="1eb43-131">Счетчик</span><span class="sxs-lookup"><span data-stu-id="1eb43-131">Number</span></span>
- <span data-ttu-id="1eb43-132">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="1eb43-132">SocialSecurityNumber</span></span>
- <span data-ttu-id="1eb43-133">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="1eb43-133">CreditCardNumber</span></span>
- <span data-ttu-id="1eb43-134">Адрес электронной почты по умолчанию используется значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1eb43-134">Email The default value is Default.</span></span>

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

### <span data-ttu-id="1eb43-135">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="1eb43-135">-NumberFrom</span></span>
<span data-ttu-id="1eb43-136">Задает меньшую границу интервала, из которого выделено случайное значение.</span><span class="sxs-lookup"><span data-stu-id="1eb43-136">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="1eb43-137">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Number.</span><span class="sxs-lookup"><span data-stu-id="1eb43-137">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="1eb43-138">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="1eb43-138">The default value is 0.</span></span>

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

### <span data-ttu-id="1eb43-139">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="1eb43-139">-NumberTo</span></span>
<span data-ttu-id="1eb43-140">Задает верхнюю границу интервала, из которого выделено случайное значение.</span><span class="sxs-lookup"><span data-stu-id="1eb43-140">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="1eb43-141">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Number.</span><span class="sxs-lookup"><span data-stu-id="1eb43-141">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="1eb43-142">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="1eb43-142">The default value is 0.</span></span>

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

### <span data-ttu-id="1eb43-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1eb43-143">-PassThru</span></span>
<span data-ttu-id="1eb43-144">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="1eb43-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1eb43-145">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1eb43-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1eb43-146">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="1eb43-146">-PrefixSize</span></span>
<span data-ttu-id="1eb43-147">Указывает число знаков в начале текста, для которого не задана маска.</span><span class="sxs-lookup"><span data-stu-id="1eb43-147">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="1eb43-148">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="1eb43-148">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="1eb43-149">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="1eb43-149">The default value is 0.</span></span>

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

### <span data-ttu-id="1eb43-150">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="1eb43-150">-ReplacementString</span></span>
<span data-ttu-id="1eb43-151">Указывает число знаков в конце текста, которые не были скрыты.</span><span class="sxs-lookup"><span data-stu-id="1eb43-151">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="1eb43-152">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="1eb43-152">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="1eb43-153">Значением по умолчанию является пустая строка.</span><span class="sxs-lookup"><span data-stu-id="1eb43-153">The default value is an empty string.</span></span>

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

### <span data-ttu-id="1eb43-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eb43-154">-ResourceGroupName</span></span>
<span data-ttu-id="1eb43-155">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="1eb43-155">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="1eb43-156">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="1eb43-156">-SchemaName</span></span>
<span data-ttu-id="1eb43-157">Указывает имя схемы.</span><span class="sxs-lookup"><span data-stu-id="1eb43-157">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="1eb43-158">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="1eb43-158">-ServerName</span></span>
<span data-ttu-id="1eb43-159">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="1eb43-159">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="1eb43-160">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="1eb43-160">-SuffixSize</span></span>
<span data-ttu-id="1eb43-161">Задает количество символов в конце текста, которые не были скрыты.</span><span class="sxs-lookup"><span data-stu-id="1eb43-161">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="1eb43-162">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="1eb43-162">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="1eb43-163">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="1eb43-163">The default value is 0.</span></span>

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

### <span data-ttu-id="1eb43-164">-TableName</span><span class="sxs-lookup"><span data-stu-id="1eb43-164">-TableName</span></span>
<span data-ttu-id="1eb43-165">Указывает имя таблицы базы данных, которая содержит столбец с маскированием.</span><span class="sxs-lookup"><span data-stu-id="1eb43-165">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="1eb43-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1eb43-166">-Confirm</span></span>
<span data-ttu-id="1eb43-167">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1eb43-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1eb43-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eb43-168">-WhatIf</span></span>
<span data-ttu-id="1eb43-169">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1eb43-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1eb43-170">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1eb43-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1eb43-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb43-171">CommonParameters</span></span>
<span data-ttu-id="1eb43-172">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1eb43-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb43-173">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1eb43-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb43-174">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1eb43-174">INPUTS</span></span>

### <span data-ttu-id="1eb43-175">System. String</span><span class="sxs-lookup"><span data-stu-id="1eb43-175">System.String</span></span>

### <span data-ttu-id="1eb43-176">System. Nullable "1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1eb43-176">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1eb43-177">System. Nullable "1 [[System. Double, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1eb43-177">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1eb43-178">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1eb43-178">OUTPUTS</span></span>

### <span data-ttu-id="1eb43-179">Microsoft. Azure. Commands. SQL. маскирует. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="1eb43-179">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="1eb43-180">Пуск</span><span class="sxs-lookup"><span data-stu-id="1eb43-180">NOTES</span></span>

## <span data-ttu-id="1eb43-181">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1eb43-181">RELATED LINKS</span></span>

[<span data-ttu-id="1eb43-182">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1eb43-182">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="1eb43-183">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1eb43-183">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="1eb43-184">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1eb43-184">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="1eb43-185">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="1eb43-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


