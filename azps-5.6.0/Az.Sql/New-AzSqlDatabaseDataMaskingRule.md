---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: b453c11d7a6e63e5365bca5cd186002f66ed13cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995865"
---
# <span data-ttu-id="75b1c-101">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="75b1c-101">New-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="75b1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75b1c-102">SYNOPSIS</span></span>
<span data-ttu-id="75b1c-103">Создает правило маскровки данных для базы данных.</span><span class="sxs-lookup"><span data-stu-id="75b1c-103">Creates a data masking rule for a database.</span></span>

## <span data-ttu-id="75b1c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="75b1c-104">SYNTAX</span></span>

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75b1c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75b1c-105">DESCRIPTION</span></span>
<span data-ttu-id="75b1c-106">Для базы данных Azure SQL создается правило маскровки данных с SQL **AzSqlDataBaseDataMaskingRule.**</span><span class="sxs-lookup"><span data-stu-id="75b1c-106">The **New-AzSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="75b1c-107">Чтобы использовать этот cmdlet, определите правило с помощью параметров *ResourceGroupName,* *ServerName* и *DatabaseName.*</span><span class="sxs-lookup"><span data-stu-id="75b1c-107">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the rule.</span></span>
<span data-ttu-id="75b1c-108">Укажите *ИмяТаблицы* и Имя Столбца, чтобы указать целевой объект для правила и параметр *MaskingFunction,* чтобы определить маскировать данные. </span><span class="sxs-lookup"><span data-stu-id="75b1c-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="75b1c-109">Если *maskingFunction* имеет значение "Число" или "Текст", можно указать параметры *NumberFrom* и *NumberTo,* для маскирования номеров или *prefixSize,* *ReplacementString* и *SuffixSize* для маскирования текста.</span><span class="sxs-lookup"><span data-stu-id="75b1c-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize*, *ReplacementString*, and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="75b1c-110">Если команда прошла успешно и используется параметр *PassThru,* командлет возвращает объект, описывающий свойства правила маскровки данных в дополнение к идентификаторам правил.</span><span class="sxs-lookup"><span data-stu-id="75b1c-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="75b1c-111">К идентификаторам правил относятся, но не ограничив их, *ResourceGroupName,* *ServerName,* *DatabaseName* *и RuleID.*</span><span class="sxs-lookup"><span data-stu-id="75b1c-111">Rule identifiers include, but are not limited to, *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleID*.</span></span>
<span data-ttu-id="75b1c-112">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="75b1c-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="75b1c-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="75b1c-113">EXAMPLES</span></span>

### <span data-ttu-id="75b1c-114">Пример 1. Создание правила маскровки данных для числового столбца в базе данных</span><span class="sxs-lookup"><span data-stu-id="75b1c-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"  -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="75b1c-115">Эта команда создает правило маскровки данных для столбца "Столбец01" таблицы "Таблица01" схемы "Схема01".</span><span class="sxs-lookup"><span data-stu-id="75b1c-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="75b1c-116">База данных с именем Database01 содержит все эти элементы.</span><span class="sxs-lookup"><span data-stu-id="75b1c-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="75b1c-117">Правило — это правило маскровки, в качестве значения маски в качестве значения маски используется случайное число от 5 до 14.</span><span class="sxs-lookup"><span data-stu-id="75b1c-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>

## <span data-ttu-id="75b1c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75b1c-118">PARAMETERS</span></span>

### <span data-ttu-id="75b1c-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="75b1c-119">-ColumnName</span></span>
<span data-ttu-id="75b1c-120">Указывает имя столбца, для которого задано правило маскровки.</span><span class="sxs-lookup"><span data-stu-id="75b1c-120">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="75b1c-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="75b1c-121">-DatabaseName</span></span>
<span data-ttu-id="75b1c-122">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="75b1c-122">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="75b1c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75b1c-123">-DefaultProfile</span></span>
<span data-ttu-id="75b1c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="75b1c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75b1c-125">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="75b1c-125">-MaskingFunction</span></span>
<span data-ttu-id="75b1c-126">Указывает функцию маскровки, которая используется правилом.</span><span class="sxs-lookup"><span data-stu-id="75b1c-126">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="75b1c-127">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="75b1c-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="75b1c-128">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="75b1c-128">Default</span></span>
- <span data-ttu-id="75b1c-129">NoMasking</span><span class="sxs-lookup"><span data-stu-id="75b1c-129">NoMasking</span></span>
- <span data-ttu-id="75b1c-130">Текст</span><span class="sxs-lookup"><span data-stu-id="75b1c-130">Text</span></span>
- <span data-ttu-id="75b1c-131">Число</span><span class="sxs-lookup"><span data-stu-id="75b1c-131">Number</span></span>
- <span data-ttu-id="75b1c-132">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="75b1c-132">SocialSecurityNumber</span></span>
- <span data-ttu-id="75b1c-133">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="75b1c-133">CreditCardNumber</span></span>
- <span data-ttu-id="75b1c-134">Значение по умолчанию — "Отправить по электронной почте".</span><span class="sxs-lookup"><span data-stu-id="75b1c-134">Email The default value is Default.</span></span>

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

### <span data-ttu-id="75b1c-135">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="75b1c-135">-NumberFrom</span></span>
<span data-ttu-id="75b1c-136">Определяет нижнюю границу интервала, из которого выбирается случайное значение.</span><span class="sxs-lookup"><span data-stu-id="75b1c-136">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="75b1c-137">Укажите этот параметр только в том случае, если укажите значение "Число" *для параметра MaskingFunction.*</span><span class="sxs-lookup"><span data-stu-id="75b1c-137">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="75b1c-138">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="75b1c-138">The default value is 0.</span></span>

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

### <span data-ttu-id="75b1c-139">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="75b1c-139">-NumberTo</span></span>
<span data-ttu-id="75b1c-140">Определяет верхнюю границу интервала, из которого выбирается случайное значение.</span><span class="sxs-lookup"><span data-stu-id="75b1c-140">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="75b1c-141">Укажите этот параметр только в том случае, если укажите значение "Число" *для параметра MaskingFunction.*</span><span class="sxs-lookup"><span data-stu-id="75b1c-141">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="75b1c-142">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="75b1c-142">The default value is 0.</span></span>

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

### <span data-ttu-id="75b1c-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75b1c-143">-PassThru</span></span>
<span data-ttu-id="75b1c-144">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="75b1c-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="75b1c-145">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="75b1c-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="75b1c-146">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="75b1c-146">-PrefixSize</span></span>
<span data-ttu-id="75b1c-147">Определяет количество знаков в начале текста, которые не маскируется.</span><span class="sxs-lookup"><span data-stu-id="75b1c-147">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="75b1c-148">Укажите этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="75b1c-148">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="75b1c-149">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="75b1c-149">The default value is 0.</span></span>

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

### <span data-ttu-id="75b1c-150">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="75b1c-150">-ReplacementString</span></span>
<span data-ttu-id="75b1c-151">Определяет количество символов в конце текста, которые не маскируете.</span><span class="sxs-lookup"><span data-stu-id="75b1c-151">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="75b1c-152">Укажите этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="75b1c-152">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="75b1c-153">Значением по умолчанию является пустая строка.</span><span class="sxs-lookup"><span data-stu-id="75b1c-153">The default value is an empty string.</span></span>

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

### <span data-ttu-id="75b1c-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75b1c-154">-ResourceGroupName</span></span>
<span data-ttu-id="75b1c-155">Имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="75b1c-155">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="75b1c-156">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="75b1c-156">-SchemaName</span></span>
<span data-ttu-id="75b1c-157">Указывает имя схемы.</span><span class="sxs-lookup"><span data-stu-id="75b1c-157">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="75b1c-158">-ServerName</span><span class="sxs-lookup"><span data-stu-id="75b1c-158">-ServerName</span></span>
<span data-ttu-id="75b1c-159">Имя сервера, на котором размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="75b1c-159">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="75b1c-160">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="75b1c-160">-SuffixSize</span></span>
<span data-ttu-id="75b1c-161">Количество знаков в конце текста, которые не маскирует.</span><span class="sxs-lookup"><span data-stu-id="75b1c-161">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="75b1c-162">Укажите этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="75b1c-162">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="75b1c-163">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="75b1c-163">The default value is 0.</span></span>

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

### <span data-ttu-id="75b1c-164">-TableName</span><span class="sxs-lookup"><span data-stu-id="75b1c-164">-TableName</span></span>
<span data-ttu-id="75b1c-165">Указывает имя таблицы базы данных, которая содержит столбец с маской.</span><span class="sxs-lookup"><span data-stu-id="75b1c-165">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="75b1c-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75b1c-166">-Confirm</span></span>
<span data-ttu-id="75b1c-167">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75b1c-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75b1c-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75b1c-168">-WhatIf</span></span>
<span data-ttu-id="75b1c-169">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75b1c-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75b1c-170">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="75b1c-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75b1c-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b1c-171">CommonParameters</span></span>
<span data-ttu-id="75b1c-172">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75b1c-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b1c-173">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75b1c-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b1c-174">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75b1c-174">INPUTS</span></span>

### <span data-ttu-id="75b1c-175">System.String</span><span class="sxs-lookup"><span data-stu-id="75b1c-175">System.String</span></span>

### <span data-ttu-id="75b1c-176">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="75b1c-176">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="75b1c-177">System.Nullable'1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="75b1c-177">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="75b1c-178">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="75b1c-178">OUTPUTS</span></span>

### <span data-ttu-id="75b1c-179">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="75b1c-179">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="75b1c-180">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="75b1c-180">NOTES</span></span>

## <span data-ttu-id="75b1c-181">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75b1c-181">RELATED LINKS</span></span>

[<span data-ttu-id="75b1c-182">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="75b1c-182">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="75b1c-183">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="75b1c-183">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="75b1c-184">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="75b1c-184">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="75b1c-185">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="75b1c-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


