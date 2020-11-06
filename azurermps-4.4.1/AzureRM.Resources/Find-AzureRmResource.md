---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: e626a57088a9c726bfe9040f76157f0b011a6405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562208"
---
# <span data-ttu-id="b8b19-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b8b19-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="b8b19-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8b19-102">SYNOPSIS</span></span>
<span data-ttu-id="b8b19-103">Осуществляет поиск ресурсов на основе указанных параметров.</span><span class="sxs-lookup"><span data-stu-id="b8b19-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8b19-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8b19-104">SYNTAX</span></span>

### <span data-ttu-id="b8b19-105">Выводит список ресурсов на основе указанной области.</span><span class="sxs-lookup"><span data-stu-id="b8b19-105">Lists the resources based on the specified scope.</span></span> <span data-ttu-id="b8b19-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="b8b19-106">(Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b8b19-107">Выводит список ресурсов на основе указанной области на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="b8b19-107">Lists the resources based on the specified scope at the tenant level.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b8b19-108">Получение ресурсов с помощью запроса с несколькими подписками.</span><span class="sxs-lookup"><span data-stu-id="b8b19-108">Get a resources using a multi-subscription query.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b8b19-109">Выводит список ресурсов по объекту Tag, заданному в качестве хэш-кода.</span><span class="sxs-lookup"><span data-stu-id="b8b19-109">Lists resources by a tag object specified as a hashset.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b8b19-110">Выводит список ресурсов по тегу, заданному в качестве отдельных параметров имени и значения.</span><span class="sxs-lookup"><span data-stu-id="b8b19-110">Lists resources by a tag specified as a individual name and value parameters.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b8b19-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8b19-111">DESCRIPTION</span></span>
<span data-ttu-id="b8b19-112">Командлет **Find-AzureRmResource** выполняет поиск ресурсов на основе указанных параметров.</span><span class="sxs-lookup"><span data-stu-id="b8b19-112">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="b8b19-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8b19-113">EXAMPLES</span></span>

### <span data-ttu-id="b8b19-114">Пример 1: Поиск ресурсов по типам и именам групп ресурсов</span><span class="sxs-lookup"><span data-stu-id="b8b19-114">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="b8b19-115">Эта команда ищет ресурсы типа Microsoft. Web/Sites в группах ресурсов, имена которых соответствуют строковому элементу ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b8b19-115">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="b8b19-116">Пример 2: Поиск ресурсов по типу и названию ресурса</span><span class="sxs-lookup"><span data-stu-id="b8b19-116">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="b8b19-117">Эта команда осуществляет поиск ресурсов типа Microsoft. Web/Sites с именем ресурса, совпадающим с тестовым строкой.</span><span class="sxs-lookup"><span data-stu-id="b8b19-117">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="b8b19-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8b19-118">PARAMETERS</span></span>

### <span data-ttu-id="b8b19-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b8b19-119">-ApiVersion</span></span>
<span data-ttu-id="b8b19-120">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8b19-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b8b19-121">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="b8b19-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b19-122">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="b8b19-122">-ExpandProperties</span></span>
<span data-ttu-id="b8b19-123">Указывает на то, что этот командлет расширяет свойства ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8b19-123">Indicates that this cmdlet expands the properties of the resource.</span></span>

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

### <span data-ttu-id="b8b19-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="b8b19-124">-ExtensionResourceType</span></span>
<span data-ttu-id="b8b19-125">Указывает тип ресурсов расширения для ресурсов, которые выполняет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b8b19-125">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="b8b19-126">Например:</span><span class="sxs-lookup"><span data-stu-id="b8b19-126">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b19-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b8b19-127">-InformationAction</span></span>
<span data-ttu-id="b8b19-128">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="b8b19-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b8b19-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b8b19-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8b19-130">Продолжал</span><span class="sxs-lookup"><span data-stu-id="b8b19-130">Continue</span></span>
- <span data-ttu-id="b8b19-131">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="b8b19-131">Ignore</span></span>
- <span data-ttu-id="b8b19-132">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="b8b19-132">Inquire</span></span>
- <span data-ttu-id="b8b19-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b8b19-133">SilentlyContinue</span></span>
- <span data-ttu-id="b8b19-134">Остановить</span><span class="sxs-lookup"><span data-stu-id="b8b19-134">Stop</span></span>
- <span data-ttu-id="b8b19-135">Рвать</span><span class="sxs-lookup"><span data-stu-id="b8b19-135">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b19-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b8b19-136">-InformationVariable</span></span>
<span data-ttu-id="b8b19-137">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="b8b19-137">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b19-138">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="b8b19-138">-ODataQuery</span></span>
<span data-ttu-id="b8b19-139">Задает фильтр стиля Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="b8b19-139">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="b8b19-140">Этот командлет добавляет это значение в запрос в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="b8b19-140">This cmdlet appends this value to the request in addition to any other filters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b19-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="b8b19-141">-Pre</span></span>
<span data-ttu-id="b8b19-142">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="b8b19-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b8b19-143">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="b8b19-143">-ResourceGroupNameContains</span></span>
<span data-ttu-id="b8b19-144">Указывает частичное имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8b19-144">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="b8b19-145">Этот командлет соответствует группам ресурсов, для которых это значение является подстрокой.</span><span class="sxs-lookup"><span data-stu-id="b8b19-145">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="b8b19-146">Командлет выполнит поиск ресурсов в этих группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8b19-146">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b19-147">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="b8b19-147">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="b8b19-148">Имя группы ресурсов для полного соответствия.</span><span class="sxs-lookup"><span data-stu-id="b8b19-148">The resource group name for a full match.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b19-149">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="b8b19-149">-ResourceNameContains</span></span>
<span data-ttu-id="b8b19-150">Указывает частичное имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8b19-150">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="b8b19-151">Командлет ищет ресурсы, содержащие это значение, в виде подстроки.</span><span class="sxs-lookup"><span data-stu-id="b8b19-151">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b19-152">-ResourceNameEquals</span><span class="sxs-lookup"><span data-stu-id="b8b19-152">-ResourceNameEquals</span></span>
<span data-ttu-id="b8b19-153">Имя ресурса для полного соответствия.</span><span class="sxs-lookup"><span data-stu-id="b8b19-153">The resource name for a full match.</span></span> <span data-ttu-id="b8b19-154">Например, если имя ресурса — testResource, вы можете указать testResource.</span><span class="sxs-lookup"><span data-stu-id="b8b19-154">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b19-155">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b8b19-155">-ResourceType</span></span>
<span data-ttu-id="b8b19-156">Указывает тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8b19-156">Specifies the type of a resource.</span></span>
<span data-ttu-id="b8b19-157">Например, для базы данных тип ресурса выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b8b19-157">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="b8b19-158">Этот командлет осуществляет поиск ресурсов указанного типа.</span><span class="sxs-lookup"><span data-stu-id="b8b19-158">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b19-159">-Тег</span><span class="sxs-lookup"><span data-stu-id="b8b19-159">-Tag</span></span>
<span data-ttu-id="b8b19-160">Фильтр тегов для запроса OData.</span><span class="sxs-lookup"><span data-stu-id="b8b19-160">The tag filter for the OData query.</span></span> <span data-ttu-id="b8b19-161">Ожидаемый формат: @ {tagName = $null} или @ {tagName = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="b8b19-161">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Lists resources by a tag object specified as a hashset.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b19-162">-TagName</span><span class="sxs-lookup"><span data-stu-id="b8b19-162">-TagName</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b19-163">-TagValue</span><span class="sxs-lookup"><span data-stu-id="b8b19-163">-TagValue</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b19-164">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="b8b19-164">-TenantLevel</span></span>
<span data-ttu-id="b8b19-165">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="b8b19-165">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b19-166">-Top</span><span class="sxs-lookup"><span data-stu-id="b8b19-166">-Top</span></span>
<span data-ttu-id="b8b19-167">Указывает количество извлекаемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8b19-167">Specifies the number of resources to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b19-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8b19-168">-DefaultProfile</span></span>
<span data-ttu-id="b8b19-169">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8b19-169">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8b19-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8b19-170">CommonParameters</span></span>
<span data-ttu-id="b8b19-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8b19-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8b19-172">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8b19-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8b19-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8b19-173">INPUTS</span></span>

## <span data-ttu-id="b8b19-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8b19-174">OUTPUTS</span></span>

### <span data-ttu-id="b8b19-175">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b8b19-175">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b8b19-176">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8b19-176">NOTES</span></span>

## <span data-ttu-id="b8b19-177">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8b19-177">RELATED LINKS</span></span>

[<span data-ttu-id="b8b19-178">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b8b19-178">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="b8b19-179">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b8b19-179">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="b8b19-180">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b8b19-180">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="b8b19-181">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b8b19-181">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="b8b19-182">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b8b19-182">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
