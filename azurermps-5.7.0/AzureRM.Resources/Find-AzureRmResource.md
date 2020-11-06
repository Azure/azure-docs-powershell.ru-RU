---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/find-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: 67389829eb5edc5ea7ac21fcc891cc85787b5e9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566140"
---
# <span data-ttu-id="caf9d-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="caf9d-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="caf9d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="caf9d-102">SYNOPSIS</span></span>
<span data-ttu-id="caf9d-103">Осуществляет поиск ресурсов на основе указанных параметров.</span><span class="sxs-lookup"><span data-stu-id="caf9d-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caf9d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="caf9d-104">SYNTAX</span></span>

### <span data-ttu-id="caf9d-105">GetBySpecifiedScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="caf9d-105">GetBySpecifiedScope (Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="caf9d-106">GetBySpecifiedScopeAtTenantLevel</span><span class="sxs-lookup"><span data-stu-id="caf9d-106">GetBySpecifiedScopeAtTenantLevel</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="caf9d-107">GetByMultiSubscriptionQuery</span><span class="sxs-lookup"><span data-stu-id="caf9d-107">GetByMultiSubscriptionQuery</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="caf9d-108">GetByTagObject</span><span class="sxs-lookup"><span data-stu-id="caf9d-108">GetByTagObject</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="caf9d-109">GetByTagNameValue</span><span class="sxs-lookup"><span data-stu-id="caf9d-109">GetByTagNameValue</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="caf9d-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="caf9d-110">DESCRIPTION</span></span>
<span data-ttu-id="caf9d-111">Командлет **Find-AzureRmResource** выполняет поиск ресурсов на основе указанных параметров.</span><span class="sxs-lookup"><span data-stu-id="caf9d-111">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="caf9d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="caf9d-112">EXAMPLES</span></span>

### <span data-ttu-id="caf9d-113">Пример 1: Поиск ресурсов по типам и именам групп ресурсов</span><span class="sxs-lookup"><span data-stu-id="caf9d-113">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="caf9d-114">Эта команда ищет ресурсы типа Microsoft. Web/Sites в группах ресурсов, имена которых соответствуют строковому элементу ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="caf9d-114">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="caf9d-115">Пример 2: Поиск ресурсов по типу и названию ресурса</span><span class="sxs-lookup"><span data-stu-id="caf9d-115">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="caf9d-116">Эта команда осуществляет поиск ресурсов типа Microsoft. Web/Sites с именем ресурса, совпадающим с тестовым строкой.</span><span class="sxs-lookup"><span data-stu-id="caf9d-116">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="caf9d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="caf9d-117">PARAMETERS</span></span>

### <span data-ttu-id="caf9d-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="caf9d-118">-ApiVersion</span></span>
<span data-ttu-id="caf9d-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="caf9d-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="caf9d-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="caf9d-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf9d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caf9d-121">-DefaultProfile</span></span>
<span data-ttu-id="caf9d-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="caf9d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="caf9d-123">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="caf9d-123">-ExpandProperties</span></span>
<span data-ttu-id="caf9d-124">Указывает на то, что этот командлет расширяет свойства ресурса.</span><span class="sxs-lookup"><span data-stu-id="caf9d-124">Indicates that this cmdlet expands the properties of the resource.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf9d-125">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="caf9d-125">-ExtensionResourceType</span></span>
<span data-ttu-id="caf9d-126">Указывает тип ресурсов расширения для ресурсов, которые выполняет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="caf9d-126">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="caf9d-127">Например:</span><span class="sxs-lookup"><span data-stu-id="caf9d-127">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf9d-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="caf9d-128">-InformationAction</span></span>
<span data-ttu-id="caf9d-129">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="caf9d-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="caf9d-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="caf9d-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="caf9d-131">Продолжал</span><span class="sxs-lookup"><span data-stu-id="caf9d-131">Continue</span></span>
- <span data-ttu-id="caf9d-132">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="caf9d-132">Ignore</span></span>
- <span data-ttu-id="caf9d-133">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="caf9d-133">Inquire</span></span>
- <span data-ttu-id="caf9d-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="caf9d-134">SilentlyContinue</span></span>
- <span data-ttu-id="caf9d-135">Остановить</span><span class="sxs-lookup"><span data-stu-id="caf9d-135">Stop</span></span>
- <span data-ttu-id="caf9d-136">Рвать</span><span class="sxs-lookup"><span data-stu-id="caf9d-136">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf9d-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="caf9d-137">-InformationVariable</span></span>
<span data-ttu-id="caf9d-138">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="caf9d-138">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf9d-139">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="caf9d-139">-ODataQuery</span></span>
<span data-ttu-id="caf9d-140">Задает фильтр стиля Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="caf9d-140">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="caf9d-141">Этот командлет добавляет это значение в запрос в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="caf9d-141">This cmdlet appends this value to the request in addition to any other filters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf9d-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="caf9d-142">-Pre</span></span>
<span data-ttu-id="caf9d-143">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="caf9d-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf9d-144">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="caf9d-144">-ResourceGroupNameContains</span></span>
<span data-ttu-id="caf9d-145">Указывает частичное имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="caf9d-145">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="caf9d-146">Этот командлет соответствует группам ресурсов, для которых это значение является подстрокой.</span><span class="sxs-lookup"><span data-stu-id="caf9d-146">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="caf9d-147">Командлет выполнит поиск ресурсов в этих группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="caf9d-147">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf9d-148">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="caf9d-148">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="caf9d-149">Имя группы ресурсов для полного соответствия.</span><span class="sxs-lookup"><span data-stu-id="caf9d-149">The resource group name for a full match.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf9d-150">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="caf9d-150">-ResourceNameContains</span></span>
<span data-ttu-id="caf9d-151">Указывает частичное имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="caf9d-151">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="caf9d-152">Командлет ищет ресурсы, содержащие это значение, в виде подстроки.</span><span class="sxs-lookup"><span data-stu-id="caf9d-152">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf9d-153">-ResourceNameEquals</span><span class="sxs-lookup"><span data-stu-id="caf9d-153">-ResourceNameEquals</span></span>
<span data-ttu-id="caf9d-154">Имя ресурса для полного соответствия.</span><span class="sxs-lookup"><span data-stu-id="caf9d-154">The resource name for a full match.</span></span> <span data-ttu-id="caf9d-155">Например, если имя ресурса — testResource, вы можете указать testResource.</span><span class="sxs-lookup"><span data-stu-id="caf9d-155">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf9d-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="caf9d-156">-ResourceType</span></span>
<span data-ttu-id="caf9d-157">Указывает тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="caf9d-157">Specifies the type of a resource.</span></span>
<span data-ttu-id="caf9d-158">Например, для базы данных тип ресурса выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="caf9d-158">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="caf9d-159">Этот командлет осуществляет поиск ресурсов указанного типа.</span><span class="sxs-lookup"><span data-stu-id="caf9d-159">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf9d-160">-Тег</span><span class="sxs-lookup"><span data-stu-id="caf9d-160">-Tag</span></span>
<span data-ttu-id="caf9d-161">Фильтр тегов для запроса OData.</span><span class="sxs-lookup"><span data-stu-id="caf9d-161">The tag filter for the OData query.</span></span> <span data-ttu-id="caf9d-162">Ожидаемый формат: @ {tagName = $null} или @ {tagName = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="caf9d-162">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: Hashtable
Parameter Sets: GetByTagObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf9d-163">-TagName</span><span class="sxs-lookup"><span data-stu-id="caf9d-163">-TagName</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf9d-164">-TagValue</span><span class="sxs-lookup"><span data-stu-id="caf9d-164">-TagValue</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf9d-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="caf9d-165">-TenantLevel</span></span>
<span data-ttu-id="caf9d-166">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="caf9d-166">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf9d-167">-Top</span><span class="sxs-lookup"><span data-stu-id="caf9d-167">-Top</span></span>
<span data-ttu-id="caf9d-168">Указывает количество извлекаемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="caf9d-168">Specifies the number of resources to retrieve.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf9d-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caf9d-169">CommonParameters</span></span>
<span data-ttu-id="caf9d-170">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="caf9d-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caf9d-171">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caf9d-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caf9d-172">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="caf9d-172">INPUTS</span></span>

### <span data-ttu-id="caf9d-173">Ничего</span><span class="sxs-lookup"><span data-stu-id="caf9d-173">None</span></span>
<span data-ttu-id="caf9d-174">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="caf9d-174">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="caf9d-175">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="caf9d-175">OUTPUTS</span></span>

### <span data-ttu-id="caf9d-176">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="caf9d-176">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="caf9d-177">Пуск</span><span class="sxs-lookup"><span data-stu-id="caf9d-177">NOTES</span></span>

## <span data-ttu-id="caf9d-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="caf9d-178">RELATED LINKS</span></span>

[<span data-ttu-id="caf9d-179">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="caf9d-179">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="caf9d-180">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="caf9d-180">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="caf9d-181">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="caf9d-181">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="caf9d-182">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="caf9d-182">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="caf9d-183">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="caf9d-183">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
