---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 2161c3c4bc81721c0d99b88ab0adfc43beac8eee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563327"
---
# <span data-ttu-id="9c272-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9c272-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="9c272-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c272-102">SYNOPSIS</span></span>
<span data-ttu-id="9c272-103">Возвращает ресурсы.</span><span class="sxs-lookup"><span data-stu-id="9c272-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c272-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c272-104">SYNTAX</span></span>

### <span data-ttu-id="9c272-105">GetAllResources (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c272-105">GetAllResources (Default)</span></span>
```
Get-AzureRmResource [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c272-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9c272-106">GetByResourceId</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c272-107">GetByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="9c272-107">GetByTenantLevel</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c272-108">GetBySpecifiedScopeAtTenantLevel</span><span class="sxs-lookup"><span data-stu-id="9c272-108">GetBySpecifiedScopeAtTenantLevel</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-Top <Int32>] [-ODataQuery <String>]
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c272-109">GetByNameAndGroup</span><span class="sxs-lookup"><span data-stu-id="9c272-109">GetByNameAndGroup</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c272-110">GetByResourceNameAndType</span><span class="sxs-lookup"><span data-stu-id="9c272-110">GetByResourceNameAndType</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c272-111">GetByNameGroupAndType</span><span class="sxs-lookup"><span data-stu-id="9c272-111">GetByNameGroupAndType</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-ODataQuery <String>] -ResourceGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c272-112">GetResourceCollection</span><span class="sxs-lookup"><span data-stu-id="9c272-112">GetResourceCollection</span></span>
```
Get-AzureRmResource [-ResourceType <String>] [-ExtensionResourceType <String>] [-ExpandProperties]
 [-IsCollection] [-ODataQuery <String>] [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c272-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c272-113">DESCRIPTION</span></span>
<span data-ttu-id="9c272-114">Командлет **Get-AzureRmResource** получает ресурсы Azure.</span><span class="sxs-lookup"><span data-stu-id="9c272-114">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="9c272-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c272-115">EXAMPLES</span></span>

### <span data-ttu-id="9c272-116">Пример 1: получение всех ресурсов определенного типа</span><span class="sxs-lookup"><span data-stu-id="9c272-116">Example 1: Get all the resources of a particular type</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceType microsoft.web/sites
```

<span data-ttu-id="9c272-117">Эта команда возвращает ресурс типа Microsoft. Web/Sites в разделе ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9c272-117">This command gets a resource of the type microsoft.web/sites under ResourceGroup11.</span></span>

### <span data-ttu-id="9c272-118">Пример 2: получение ресурса по имени</span><span class="sxs-lookup"><span data-stu-id="9c272-118">Example 2: Get a resource by name</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceName ContosoWebsite
```

<span data-ttu-id="9c272-119">Эта команда получает ресурс с именем ContosoWebsite в разделе ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9c272-119">This command gets a resource  named ContosoWebsite under ResourceGroup11.</span></span>

### <span data-ttu-id="9c272-120">Пример 3: отображение всех состояний учетных записей хранения в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="9c272-120">Example 3: Show all the status of storage accounts in a Resource Group</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceType Microsoft.ClassicStorage/storageAccounts -ExpandProperties |
   Select * -Expand Properties |
   Sort Name |
   Format-Table Name,Status*
```

## <span data-ttu-id="9c272-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c272-121">PARAMETERS</span></span>

### <span data-ttu-id="9c272-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9c272-122">-ApiVersion</span></span>
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

### <span data-ttu-id="9c272-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c272-123">-DefaultProfile</span></span>
<span data-ttu-id="9c272-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9c272-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c272-125">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="9c272-125">-ExpandProperties</span></span>
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

### <span data-ttu-id="9c272-126">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="9c272-126">-ExtensionResourceName</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetByNameGroupAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c272-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="9c272-127">-ExtensionResourceType</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetByNameGroupAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c272-128">-IsCollection</span><span class="sxs-lookup"><span data-stu-id="9c272-128">-IsCollection</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c272-129">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="9c272-129">-ODataQuery</span></span>
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

### <span data-ttu-id="9c272-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="9c272-130">-Pre</span></span>
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

### <span data-ttu-id="9c272-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c272-131">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: GetByNameAndGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByNameGroupAndType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c272-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c272-132">-ResourceId</span></span>
<span data-ttu-id="9c272-133">Указывает полный идентификатор ресурса, включая подписку, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="9c272-133">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span> 

<span data-ttu-id="9c272-134">`/subscriptions/`Идентификатор подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="9c272-134">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

<span data-ttu-id="9c272-135">Этот командлет получает ресурс с таким ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="9c272-135">This cmdlet gets the resource that has this ID.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c272-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9c272-136">-ResourceName</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetByNameGroupAndType
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c272-137">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9c272-137">-ResourceType</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetByNameGroupAndType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByResourceNameAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c272-138">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="9c272-138">-TenantLevel</span></span>
<span data-ttu-id="9c272-139">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="9c272-139">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c272-140">-Top</span><span class="sxs-lookup"><span data-stu-id="9c272-140">-Top</span></span>
```yaml
Type: Int32
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c272-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c272-141">CommonParameters</span></span>
<span data-ttu-id="9c272-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c272-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c272-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c272-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c272-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c272-144">INPUTS</span></span>

### <span data-ttu-id="9c272-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="9c272-145">None</span></span>
<span data-ttu-id="9c272-146">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9c272-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9c272-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c272-147">OUTPUTS</span></span>

### <span data-ttu-id="9c272-148">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9c272-148">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9c272-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c272-149">NOTES</span></span>

## <span data-ttu-id="9c272-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c272-150">RELATED LINKS</span></span>

[<span data-ttu-id="9c272-151">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9c272-151">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="9c272-152">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9c272-152">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="9c272-153">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9c272-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="9c272-154">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9c272-154">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="9c272-155">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9c272-155">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


