---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 544db2f0e23cb510c81fb64898b6bcf856e760e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504757"
---
# <span data-ttu-id="2b3a8-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2b3a8-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="2b3a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b3a8-102">SYNOPSIS</span></span>
<span data-ttu-id="2b3a8-103">Задает свойства правила маскровки данных для базы данных.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="2b3a8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2b3a8-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b3a8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b3a8-105">DESCRIPTION</span></span>
<span data-ttu-id="2b3a8-106">Cmdlet **Set-AzSqlDatabaseDataMaskingRule** задает правило маскровки данных для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="2b3a8-107">Чтобы использовать этот cmdlet, задате параметры *ResourceGroupName,* *ServerName,* *DatabaseName* и *RuleId,* чтобы определить правило.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-107">To use the cmdlet, provide the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="2b3a8-108">Вы можете предоставить любые параметры *SchemaName,* *TableName* и *ColumnName,* чтобы перенаправить правило.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-108">You can provide any of the parameters of *SchemaName*, *TableName*, and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="2b3a8-109">Укажите *параметр MaskingFunction,* чтобы изменить маскировать данные.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="2b3a8-110">Если указать значение "Число" или "Текст" для маскированияФункции, можно указать параметры *NumberFrom* и *NumberTo* для маскирования или *префикса,* *ReplacementString* и *SuffixSize* для маскирования текста. </span><span class="sxs-lookup"><span data-stu-id="2b3a8-110">If you specify a value of Number or Text for *MaskingFunction*, you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize*, *ReplacementString*, and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="2b3a8-111">Если команда добиться успеха и указать параметр *PassThru,* командлет возвратит объект, описывающий свойства правила маскровки данных и идентификаторы правил.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="2b3a8-112">Идентификаторы правил включают, но не ограничив их, **ResourceGroupName,** **ServerName,** **DatabaseName** и **RuleId.**</span><span class="sxs-lookup"><span data-stu-id="2b3a8-112">Rule identifiers include, but are not limited to, **ResourceGroupName**, **ServerName**, **DatabaseName**, and **RuleId**.</span></span>
<span data-ttu-id="2b3a8-113">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="2b3a8-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2b3a8-114">EXAMPLES</span></span>

### <span data-ttu-id="2b3a8-115">Пример 1. Изменение диапазона правила маскровки данных в базе данных</span><span class="sxs-lookup"><span data-stu-id="2b3a8-115">Example 1: Change the range of a data masking rule in a database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="2b3a8-116">Эта команда изменяет правило маскровки данных с правилом ID17.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="2b3a8-117">Это правило действует в базе данных Database01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="2b3a8-118">Эта команда изменяет границы интервала, в течение которого случайное число генерируется как маскировка.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="2b3a8-119">Новый диапазон — от 23 до 42.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-119">The new range is between 23 and 42.</span></span>

### <span data-ttu-id="2b3a8-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2b3a8-120">Example 2</span></span>

<span data-ttu-id="2b3a8-121">Задает свойства правила маскровки данных для базы данных.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-121">Sets the properties of a data masking rule for a database.</span></span> <span data-ttu-id="2b3a8-122">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="2b3a8-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## <span data-ttu-id="2b3a8-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b3a8-123">PARAMETERS</span></span>

### <span data-ttu-id="2b3a8-124">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="2b3a8-124">-ColumnName</span></span>
<span data-ttu-id="2b3a8-125">Указывает имя столбца, для которого задано правило маскровки.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-125">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="2b3a8-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2b3a8-126">-DatabaseName</span></span>
<span data-ttu-id="2b3a8-127">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="2b3a8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b3a8-128">-DefaultProfile</span></span>
<span data-ttu-id="2b3a8-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2b3a8-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b3a8-130">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="2b3a8-130">-MaskingFunction</span></span>
<span data-ttu-id="2b3a8-131">Указывает функцию маскровки, которая используется правилом.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-131">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="2b3a8-132">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="2b3a8-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2b3a8-133">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="2b3a8-133">Default</span></span>
- <span data-ttu-id="2b3a8-134">NoMasking</span><span class="sxs-lookup"><span data-stu-id="2b3a8-134">NoMasking</span></span>
- <span data-ttu-id="2b3a8-135">Текст</span><span class="sxs-lookup"><span data-stu-id="2b3a8-135">Text</span></span>
- <span data-ttu-id="2b3a8-136">Число</span><span class="sxs-lookup"><span data-stu-id="2b3a8-136">Number</span></span>
- <span data-ttu-id="2b3a8-137">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="2b3a8-137">SocialSecurityNumber</span></span>
- <span data-ttu-id="2b3a8-138">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="2b3a8-138">CreditCardNumber</span></span>
- <span data-ttu-id="2b3a8-139">Значение по умолчанию — "Отправить по электронной почте".</span><span class="sxs-lookup"><span data-stu-id="2b3a8-139">Email The default value is Default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b3a8-140">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="2b3a8-140">-NumberFrom</span></span>
<span data-ttu-id="2b3a8-141">Определяет нижнюю границу интервала, из которого выбирается случайное значение.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-141">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="2b3a8-142">Укажите этот параметр только в том случае, если укажите значение "Число" *для параметра MaskingFunction.*</span><span class="sxs-lookup"><span data-stu-id="2b3a8-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2b3a8-143">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-143">The default value is 0.</span></span>

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

### <span data-ttu-id="2b3a8-144">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="2b3a8-144">-NumberTo</span></span>
<span data-ttu-id="2b3a8-145">Определяет верхнюю границу интервала, из которого выбирается случайное значение.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-145">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="2b3a8-146">Укажите этот параметр только в том случае, если укажите значение "Число" *для параметра MaskingFunction.*</span><span class="sxs-lookup"><span data-stu-id="2b3a8-146">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2b3a8-147">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-147">The default value is 0.</span></span>

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

### <span data-ttu-id="2b3a8-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b3a8-148">-PassThru</span></span>
<span data-ttu-id="2b3a8-149">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-149">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2b3a8-150">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-150">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2b3a8-151">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="2b3a8-151">-PrefixSize</span></span>
<span data-ttu-id="2b3a8-152">Определяет количество знаков в начале текста, которые не маскирует.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-152">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="2b3a8-153">Укажите этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2b3a8-154">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-154">The default value is 0.</span></span>

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

### <span data-ttu-id="2b3a8-155">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="2b3a8-155">-ReplacementString</span></span>
<span data-ttu-id="2b3a8-156">Количество знаков в конце текста, которые не маскирует.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-156">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="2b3a8-157">Укажите этот параметр только в том случае, если для параметра *MaskingFunction задано* значение Text.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-157">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2b3a8-158">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-158">The default value is 0.</span></span>

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

### <span data-ttu-id="2b3a8-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b3a8-159">-ResourceGroupName</span></span>
<span data-ttu-id="2b3a8-160">Имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-160">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="2b3a8-161">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="2b3a8-161">-SchemaName</span></span>
<span data-ttu-id="2b3a8-162">Указывает имя схемы.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-162">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="2b3a8-163">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2b3a8-163">-ServerName</span></span>
<span data-ttu-id="2b3a8-164">Имя сервера, на котором размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-164">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="2b3a8-165">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="2b3a8-165">-SuffixSize</span></span>
<span data-ttu-id="2b3a8-166">Количество знаков в конце текста, которые не маскирует.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-166">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="2b3a8-167">Укажите этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-167">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2b3a8-168">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-168">The default value is 0.</span></span>

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

### <span data-ttu-id="2b3a8-169">-TableName</span><span class="sxs-lookup"><span data-stu-id="2b3a8-169">-TableName</span></span>
<span data-ttu-id="2b3a8-170">Указывает имя таблицы базы данных, которая содержит столбец с маской.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-170">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="2b3a8-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b3a8-171">-Confirm</span></span>
<span data-ttu-id="2b3a8-172">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b3a8-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b3a8-173">-WhatIf</span></span>
<span data-ttu-id="2b3a8-174">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b3a8-175">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b3a8-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b3a8-176">CommonParameters</span></span>
<span data-ttu-id="2b3a8-177">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b3a8-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b3a8-178">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b3a8-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b3a8-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b3a8-179">INPUTS</span></span>

### <span data-ttu-id="2b3a8-180">System.String</span><span class="sxs-lookup"><span data-stu-id="2b3a8-180">System.String</span></span>

### <span data-ttu-id="2b3a8-181">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2b3a8-181">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2b3a8-182">System.Nullable'1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2b3a8-182">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2b3a8-183">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2b3a8-183">OUTPUTS</span></span>

### <span data-ttu-id="2b3a8-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="2b3a8-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="2b3a8-185">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2b3a8-185">NOTES</span></span>

## <span data-ttu-id="2b3a8-186">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b3a8-186">RELATED LINKS</span></span>

[<span data-ttu-id="2b3a8-187">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2b3a8-187">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2b3a8-188">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2b3a8-188">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2b3a8-189">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2b3a8-189">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2b3a8-190">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="2b3a8-190">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


