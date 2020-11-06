---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 1a26cc83bfd42ba63f2ae914ea6c288b862ccaf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559424"
---
# <span data-ttu-id="28fce-101">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="28fce-101">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="28fce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28fce-102">SYNOPSIS</span></span>
<span data-ttu-id="28fce-103">Задает свойства правила маскирования данных для базы данных.</span><span class="sxs-lookup"><span data-stu-id="28fce-103">Sets the properties of a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28fce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28fce-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28fce-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28fce-105">DESCRIPTION</span></span>
<span data-ttu-id="28fce-106">Командлет **Set-AzureRmSqlDatabaseDataMaskingRule** задает правило маскирования данных для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="28fce-106">The **Set-AzureRmSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="28fce-107">Чтобы использовать командлет, укажите параметры *ResourceGroupName* , *ServerName* , *DatabaseName* и *RuleId* , чтобы определить правило.</span><span class="sxs-lookup"><span data-stu-id="28fce-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="28fce-108">Вы можете предоставить любой из параметров *SchemaName* , *TableName* и *ColumnName* , чтобы перенацелить правило.</span><span class="sxs-lookup"><span data-stu-id="28fce-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="28fce-109">Укажите параметр *MaskingFunction* , чтобы изменить способ маскирования данных.</span><span class="sxs-lookup"><span data-stu-id="28fce-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>

<span data-ttu-id="28fce-110">Если вы задаете значение числа или текста для *MaskingFunction* , вы можете указать параметры *NumberFrom* и *NumberTo* для масок номеров, а также параметры *PrefixSize* , *ReplacementString* и *SuffixSize* для маскирования текста.</span><span class="sxs-lookup"><span data-stu-id="28fce-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="28fce-111">Если команда выполнена успешно, а параметр *PassThru* указан, командлет возвращает объект, описывающий свойства правила масок данных и идентификаторы правил.</span><span class="sxs-lookup"><span data-stu-id="28fce-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="28fce-112">Идентификаторы правила включают, но не ограничиваются, **ResourceGroupName** , **ServerName** , **DatabaseName** и **RuleId**.</span><span class="sxs-lookup"><span data-stu-id="28fce-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>

<span data-ttu-id="28fce-113">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="28fce-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="28fce-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28fce-114">EXAMPLES</span></span>

### <span data-ttu-id="28fce-115">Пример 1: изменение диапазона правила маскировки данных в базе данных</span><span class="sxs-lookup"><span data-stu-id="28fce-115">Example 1: Change the range of a data masking rule in a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="28fce-116">Эта команда изменяет правило маскировки данных с ИДЕНТИФИКАТОРом Rule17.</span><span class="sxs-lookup"><span data-stu-id="28fce-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="28fce-117">Это правило работает в базе данных с именем Database01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="28fce-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="28fce-118">Эта команда изменяет границы интервала, в течение которого случайное число генерируется как маскированное значение.</span><span class="sxs-lookup"><span data-stu-id="28fce-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="28fce-119">Новый диапазон находится в диапазоне от 23 до 42.</span><span class="sxs-lookup"><span data-stu-id="28fce-119">The new range is between 23 and 42.</span></span>

## <span data-ttu-id="28fce-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28fce-120">PARAMETERS</span></span>

### <span data-ttu-id="28fce-121">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="28fce-121">-ColumnName</span></span>
<span data-ttu-id="28fce-122">Задает имя столбца, на которое указывает правило маскирования.</span><span class="sxs-lookup"><span data-stu-id="28fce-122">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="28fce-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="28fce-123">-DatabaseName</span></span>
<span data-ttu-id="28fce-124">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="28fce-124">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="28fce-125">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="28fce-125">-MaskingFunction</span></span>
<span data-ttu-id="28fce-126">Указывает функцию маскирования, используемую правилом.</span><span class="sxs-lookup"><span data-stu-id="28fce-126">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="28fce-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="28fce-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="28fce-128">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="28fce-128">Default</span></span>
- <span data-ttu-id="28fce-129">Маскировка</span><span class="sxs-lookup"><span data-stu-id="28fce-129">NoMasking</span></span>
- <span data-ttu-id="28fce-130">Текстовые</span><span class="sxs-lookup"><span data-stu-id="28fce-130">Text</span></span>
- <span data-ttu-id="28fce-131">Счетчик</span><span class="sxs-lookup"><span data-stu-id="28fce-131">Number</span></span>
- <span data-ttu-id="28fce-132">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="28fce-132">SocialSecurityNumber</span></span>
- <span data-ttu-id="28fce-133">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="28fce-133">CreditCardNumber</span></span>
- <span data-ttu-id="28fce-134">Отправить по электронной почте</span><span class="sxs-lookup"><span data-stu-id="28fce-134">Email</span></span>

<span data-ttu-id="28fce-135">По умолчанию используется значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="28fce-135">The default value is Default.</span></span>

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

### <span data-ttu-id="28fce-136">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="28fce-136">-NumberFrom</span></span>
<span data-ttu-id="28fce-137">Задает меньшую границу интервала, из которого выделено случайное значение.</span><span class="sxs-lookup"><span data-stu-id="28fce-137">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="28fce-138">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Number.</span><span class="sxs-lookup"><span data-stu-id="28fce-138">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="28fce-139">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="28fce-139">The default value is 0.</span></span>

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

### <span data-ttu-id="28fce-140">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="28fce-140">-NumberTo</span></span>
<span data-ttu-id="28fce-141">Задает верхнюю границу интервала, из которого выделено случайное значение.</span><span class="sxs-lookup"><span data-stu-id="28fce-141">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="28fce-142">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Number.</span><span class="sxs-lookup"><span data-stu-id="28fce-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="28fce-143">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="28fce-143">The default value is 0.</span></span>

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

### <span data-ttu-id="28fce-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28fce-144">-PassThru</span></span>
<span data-ttu-id="28fce-145">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="28fce-145">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="28fce-146">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="28fce-146">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="28fce-147">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="28fce-147">-PrefixSize</span></span>
<span data-ttu-id="28fce-148">Указывает число знаков в начале текста, для которого не задана маска.</span><span class="sxs-lookup"><span data-stu-id="28fce-148">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="28fce-149">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="28fce-149">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="28fce-150">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="28fce-150">The default value is 0.</span></span>

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

### <span data-ttu-id="28fce-151">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="28fce-151">-ReplacementString</span></span>
<span data-ttu-id="28fce-152">Задает количество символов в конце текста, которые не были скрыты.</span><span class="sxs-lookup"><span data-stu-id="28fce-152">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="28fce-153">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="28fce-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="28fce-154">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="28fce-154">The default value is 0.</span></span>

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

### <span data-ttu-id="28fce-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28fce-155">-ResourceGroupName</span></span>
<span data-ttu-id="28fce-156">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="28fce-156">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="28fce-157">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="28fce-157">-SchemaName</span></span>
<span data-ttu-id="28fce-158">Указывает имя схемы.</span><span class="sxs-lookup"><span data-stu-id="28fce-158">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="28fce-159">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="28fce-159">-ServerName</span></span>
<span data-ttu-id="28fce-160">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="28fce-160">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="28fce-161">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="28fce-161">-SuffixSize</span></span>
<span data-ttu-id="28fce-162">Задает количество символов в конце текста, которые не были скрыты.</span><span class="sxs-lookup"><span data-stu-id="28fce-162">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="28fce-163">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="28fce-163">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="28fce-164">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="28fce-164">The default value is 0.</span></span>

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

### <span data-ttu-id="28fce-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="28fce-165">-TableName</span></span>
<span data-ttu-id="28fce-166">Указывает имя таблицы базы данных, которая содержит столбец с маскированием.</span><span class="sxs-lookup"><span data-stu-id="28fce-166">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="28fce-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28fce-167">-Confirm</span></span>
<span data-ttu-id="28fce-168">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="28fce-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28fce-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28fce-169">-WhatIf</span></span>
<span data-ttu-id="28fce-170">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="28fce-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28fce-171">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="28fce-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28fce-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28fce-172">-DefaultProfile</span></span>
<span data-ttu-id="28fce-173">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28fce-173">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28fce-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28fce-174">CommonParameters</span></span>
<span data-ttu-id="28fce-175">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28fce-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28fce-176">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28fce-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28fce-177">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28fce-177">INPUTS</span></span>

###  
<span data-ttu-id="28fce-178">Ничего</span><span class="sxs-lookup"><span data-stu-id="28fce-178">None</span></span>

## <span data-ttu-id="28fce-179">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28fce-179">OUTPUTS</span></span>

### <span data-ttu-id="28fce-180">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="28fce-180">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="28fce-181">Пуск</span><span class="sxs-lookup"><span data-stu-id="28fce-181">NOTES</span></span>

## <span data-ttu-id="28fce-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28fce-182">RELATED LINKS</span></span>

[<span data-ttu-id="28fce-183">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="28fce-183">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="28fce-184">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="28fce-184">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="28fce-185">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="28fce-185">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="28fce-186">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="28fce-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


