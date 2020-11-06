---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 01e4e6b990a35b8573a9ea1d2f2803f6d6fabc1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567089"
---
# <span data-ttu-id="376a6-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="376a6-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="376a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="376a6-102">SYNOPSIS</span></span>
<span data-ttu-id="376a6-103">Возвращает ресурсы.</span><span class="sxs-lookup"><span data-stu-id="376a6-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="376a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="376a6-104">SYNTAX</span></span>

### <span data-ttu-id="376a6-105">Установленный список параметров для всех ресурсов.</span><span class="sxs-lookup"><span data-stu-id="376a6-105">The list all resources parameter set.</span></span> <span data-ttu-id="376a6-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="376a6-106">(Default)</span></span>
```
Get-AzureRmResource [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="376a6-107">Получить один ресурс по его идентификатору.</span><span class="sxs-lookup"><span data-stu-id="376a6-107">Get a single resource by its Id.</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="376a6-108">Получить один ресурс на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="376a6-108">Get a single resource at the tenant level.</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="376a6-109">Выводит список ресурсов на основе указанной области на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="376a6-109">Lists the resources based on the specified scope at the tenant level.</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-Top <Int32>] [-ODataQuery <String>]
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="376a6-110">Получение ресурсов по имени и группе</span><span class="sxs-lookup"><span data-stu-id="376a6-110">Get resource by name and group</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="376a6-111">Получение ресурса по имени и типу.</span><span class="sxs-lookup"><span data-stu-id="376a6-111">Get a resource by name and type.</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="376a6-112">Получение ресурсов по имени, группе и типу</span><span class="sxs-lookup"><span data-stu-id="376a6-112">Get resource by name, group and type</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-ODataQuery <String>] -ResourceGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="376a6-113">Получение коллекции ресурсов</span><span class="sxs-lookup"><span data-stu-id="376a6-113">Get resource collection</span></span>
```
Get-AzureRmResource [-ResourceType <String>] [-ExtensionResourceType <String>] [-ExpandProperties]
 [-IsCollection] [-ODataQuery <String>] [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="376a6-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="376a6-114">DESCRIPTION</span></span>
<span data-ttu-id="376a6-115">Командлет **Get-AzureRmResource** получает ресурсы Azure.</span><span class="sxs-lookup"><span data-stu-id="376a6-115">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="376a6-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="376a6-116">EXAMPLES</span></span>

### <span data-ttu-id="376a6-117">Пример 1: получение ресурса</span><span class="sxs-lookup"><span data-stu-id="376a6-117">Example 1: Get a resource</span></span>
```
PS C:\>Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoWebsite"
```

<span data-ttu-id="376a6-118">Эта команда возвращает ресурс типа Microsoft. Web/Sites с именем ContosoWebsite в разделе ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="376a6-118">This command gets a resource of the type microsoft.web/sites, named ContosoWebsite under ResourceGroup11.</span></span>

## <span data-ttu-id="376a6-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="376a6-119">PARAMETERS</span></span>

### <span data-ttu-id="376a6-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="376a6-120">-ApiVersion</span></span>
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

### <span data-ttu-id="376a6-121">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="376a6-121">-ExpandProperties</span></span>
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

### <span data-ttu-id="376a6-122">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="376a6-122">-ExtensionResourceName</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="376a6-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="376a6-123">-ExtensionResourceType</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="376a6-124">-IsCollection</span><span class="sxs-lookup"><span data-stu-id="376a6-124">-IsCollection</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="376a6-125">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="376a6-125">-ODataQuery</span></span>
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

### <span data-ttu-id="376a6-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="376a6-126">-Pre</span></span>
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

### <span data-ttu-id="376a6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="376a6-127">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: Get resource by name and group
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="376a6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="376a6-128">-ResourceId</span></span>
<span data-ttu-id="376a6-129">Указывает полный идентификатор ресурса, включая подписку, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="376a6-129">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span> 

<span data-ttu-id="376a6-130">`/subscriptions/`Идентификатор подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="376a6-130">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

<span data-ttu-id="376a6-131">Этот командлет получает ресурс с таким ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="376a6-131">This cmdlet gets the resource that has this ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a single resource by its Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="376a6-132">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="376a6-132">-ResourceName</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="376a6-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="376a6-133">-ResourceType</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resource by name and type.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="376a6-134">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="376a6-134">-TenantLevel</span></span>
<span data-ttu-id="376a6-135">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="376a6-135">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="376a6-136">-Top</span><span class="sxs-lookup"><span data-stu-id="376a6-136">-Top</span></span>
```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="376a6-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="376a6-137">-DefaultProfile</span></span>
<span data-ttu-id="376a6-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="376a6-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="376a6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="376a6-139">CommonParameters</span></span>
<span data-ttu-id="376a6-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="376a6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="376a6-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="376a6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="376a6-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="376a6-142">INPUTS</span></span>

## <span data-ttu-id="376a6-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="376a6-143">OUTPUTS</span></span>

### <span data-ttu-id="376a6-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="376a6-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="376a6-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="376a6-145">NOTES</span></span>

## <span data-ttu-id="376a6-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="376a6-146">RELATED LINKS</span></span>

[<span data-ttu-id="376a6-147">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="376a6-147">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="376a6-148">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="376a6-148">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="376a6-149">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="376a6-149">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="376a6-150">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="376a6-150">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="376a6-151">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="376a6-151">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


