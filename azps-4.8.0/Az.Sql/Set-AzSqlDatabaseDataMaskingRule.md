---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 544db2f0e23cb510c81fb64898b6bcf856e760e5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243885"
---
# <span data-ttu-id="becad-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="becad-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="becad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="becad-102">SYNOPSIS</span></span>
<span data-ttu-id="becad-103">Задает свойства правила маскирования данных для базы данных.</span><span class="sxs-lookup"><span data-stu-id="becad-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="becad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="becad-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="becad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="becad-105">DESCRIPTION</span></span>
<span data-ttu-id="becad-106">Командлет **Set-AzSqlDatabaseDataMaskingRule** задает правило маскирования данных для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="becad-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="becad-107">Чтобы использовать командлет, укажите параметры *ResourceGroupName* , *ServerName* , *DatabaseName* и *RuleId* , чтобы определить правило.</span><span class="sxs-lookup"><span data-stu-id="becad-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="becad-108">Вы можете предоставить любой из параметров *SchemaName* , *TableName* и *ColumnName* , чтобы перенацелить правило.</span><span class="sxs-lookup"><span data-stu-id="becad-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="becad-109">Укажите параметр *MaskingFunction* , чтобы изменить способ маскирования данных.</span><span class="sxs-lookup"><span data-stu-id="becad-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="becad-110">Если вы задаете значение числа или текста для *MaskingFunction* , вы можете указать параметры *NumberFrom* и *NumberTo* для масок номеров, а также параметры *PrefixSize* , *ReplacementString* и *SuffixSize* для маскирования текста.</span><span class="sxs-lookup"><span data-stu-id="becad-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="becad-111">Если команда выполнена успешно, а параметр *PassThru* указан, командлет возвращает объект, описывающий свойства правила масок данных и идентификаторы правил.</span><span class="sxs-lookup"><span data-stu-id="becad-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="becad-112">Идентификаторы правила включают, но не ограничиваются, **ResourceGroupName** , **ServerName** , **DatabaseName** и **RuleId**.</span><span class="sxs-lookup"><span data-stu-id="becad-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>
<span data-ttu-id="becad-113">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="becad-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="becad-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="becad-114">EXAMPLES</span></span>

### <span data-ttu-id="becad-115">Пример 1: изменение диапазона правила маскировки данных в базе данных</span><span class="sxs-lookup"><span data-stu-id="becad-115">Example 1: Change the range of a data masking rule in a database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="becad-116">Эта команда изменяет правило маскировки данных с ИДЕНТИФИКАТОРом Rule17.</span><span class="sxs-lookup"><span data-stu-id="becad-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="becad-117">Это правило работает в базе данных с именем Database01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="becad-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="becad-118">Эта команда изменяет границы интервала, в течение которого случайное число генерируется как маскированное значение.</span><span class="sxs-lookup"><span data-stu-id="becad-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="becad-119">Новый диапазон находится в диапазоне от 23 до 42.</span><span class="sxs-lookup"><span data-stu-id="becad-119">The new range is between 23 and 42.</span></span>

### <span data-ttu-id="becad-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="becad-120">Example 2</span></span>

<span data-ttu-id="becad-121">Задает свойства правила маскирования данных для базы данных.</span><span class="sxs-lookup"><span data-stu-id="becad-121">Sets the properties of a data masking rule for a database.</span></span> <span data-ttu-id="becad-122">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="becad-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## <span data-ttu-id="becad-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="becad-123">PARAMETERS</span></span>

### <span data-ttu-id="becad-124">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="becad-124">-ColumnName</span></span>
<span data-ttu-id="becad-125">Задает имя столбца, на которое указывает правило маскирования.</span><span class="sxs-lookup"><span data-stu-id="becad-125">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="becad-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="becad-126">-DatabaseName</span></span>
<span data-ttu-id="becad-127">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="becad-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="becad-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="becad-128">-DefaultProfile</span></span>
<span data-ttu-id="becad-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="becad-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="becad-130">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="becad-130">-MaskingFunction</span></span>
<span data-ttu-id="becad-131">Указывает функцию маскирования, используемую правилом.</span><span class="sxs-lookup"><span data-stu-id="becad-131">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="becad-132">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="becad-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="becad-133">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="becad-133">Default</span></span>
- <span data-ttu-id="becad-134">Маскировка</span><span class="sxs-lookup"><span data-stu-id="becad-134">NoMasking</span></span>
- <span data-ttu-id="becad-135">Текстовые</span><span class="sxs-lookup"><span data-stu-id="becad-135">Text</span></span>
- <span data-ttu-id="becad-136">Счетчик</span><span class="sxs-lookup"><span data-stu-id="becad-136">Number</span></span>
- <span data-ttu-id="becad-137">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="becad-137">SocialSecurityNumber</span></span>
- <span data-ttu-id="becad-138">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="becad-138">CreditCardNumber</span></span>
- <span data-ttu-id="becad-139">Адрес электронной почты по умолчанию используется значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="becad-139">Email The default value is Default.</span></span>

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

### <span data-ttu-id="becad-140">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="becad-140">-NumberFrom</span></span>
<span data-ttu-id="becad-141">Задает меньшую границу интервала, из которого выделено случайное значение.</span><span class="sxs-lookup"><span data-stu-id="becad-141">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="becad-142">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Number.</span><span class="sxs-lookup"><span data-stu-id="becad-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="becad-143">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="becad-143">The default value is 0.</span></span>

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

### <span data-ttu-id="becad-144">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="becad-144">-NumberTo</span></span>
<span data-ttu-id="becad-145">Задает верхнюю границу интервала, из которого выделено случайное значение.</span><span class="sxs-lookup"><span data-stu-id="becad-145">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="becad-146">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Number.</span><span class="sxs-lookup"><span data-stu-id="becad-146">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="becad-147">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="becad-147">The default value is 0.</span></span>

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

### <span data-ttu-id="becad-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="becad-148">-PassThru</span></span>
<span data-ttu-id="becad-149">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="becad-149">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="becad-150">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="becad-150">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="becad-151">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="becad-151">-PrefixSize</span></span>
<span data-ttu-id="becad-152">Указывает число знаков в начале текста, для которого не задана маска.</span><span class="sxs-lookup"><span data-stu-id="becad-152">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="becad-153">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="becad-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="becad-154">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="becad-154">The default value is 0.</span></span>

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

### <span data-ttu-id="becad-155">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="becad-155">-ReplacementString</span></span>
<span data-ttu-id="becad-156">Задает количество символов в конце текста, которые не были скрыты.</span><span class="sxs-lookup"><span data-stu-id="becad-156">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="becad-157">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="becad-157">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="becad-158">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="becad-158">The default value is 0.</span></span>

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

### <span data-ttu-id="becad-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="becad-159">-ResourceGroupName</span></span>
<span data-ttu-id="becad-160">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="becad-160">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="becad-161">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="becad-161">-SchemaName</span></span>
<span data-ttu-id="becad-162">Указывает имя схемы.</span><span class="sxs-lookup"><span data-stu-id="becad-162">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="becad-163">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="becad-163">-ServerName</span></span>
<span data-ttu-id="becad-164">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="becad-164">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="becad-165">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="becad-165">-SuffixSize</span></span>
<span data-ttu-id="becad-166">Задает количество символов в конце текста, которые не были скрыты.</span><span class="sxs-lookup"><span data-stu-id="becad-166">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="becad-167">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="becad-167">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="becad-168">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="becad-168">The default value is 0.</span></span>

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

### <span data-ttu-id="becad-169">-TableName</span><span class="sxs-lookup"><span data-stu-id="becad-169">-TableName</span></span>
<span data-ttu-id="becad-170">Указывает имя таблицы базы данных, которая содержит столбец с маскированием.</span><span class="sxs-lookup"><span data-stu-id="becad-170">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="becad-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="becad-171">-Confirm</span></span>
<span data-ttu-id="becad-172">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="becad-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="becad-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="becad-173">-WhatIf</span></span>
<span data-ttu-id="becad-174">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="becad-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="becad-175">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="becad-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="becad-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="becad-176">CommonParameters</span></span>
<span data-ttu-id="becad-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="becad-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="becad-178">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="becad-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="becad-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="becad-179">INPUTS</span></span>

### <span data-ttu-id="becad-180">System. String</span><span class="sxs-lookup"><span data-stu-id="becad-180">System.String</span></span>

### <span data-ttu-id="becad-181">System. Nullable "1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="becad-181">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="becad-182">System. Nullable "1 [[System. Double, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="becad-182">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="becad-183">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="becad-183">OUTPUTS</span></span>

### <span data-ttu-id="becad-184">Microsoft. Azure. Commands. SQL. маскирует. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="becad-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="becad-185">Пуск</span><span class="sxs-lookup"><span data-stu-id="becad-185">NOTES</span></span>

## <span data-ttu-id="becad-186">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="becad-186">RELATED LINKS</span></span>

[<span data-ttu-id="becad-187">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="becad-187">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="becad-188">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="becad-188">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="becad-189">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="becad-189">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="becad-190">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="becad-190">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


