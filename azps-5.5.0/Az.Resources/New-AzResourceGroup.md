---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: 9c4bdfe189c16f3e2f6f90d3197149bdc57c78c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226796"
---
# <span data-ttu-id="064a4-101">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="064a4-101">New-AzResourceGroup</span></span>

## <span data-ttu-id="064a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="064a4-102">SYNOPSIS</span></span>
<span data-ttu-id="064a4-103">Создает группу ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="064a4-103">Creates an Azure resource group.</span></span>

## <span data-ttu-id="064a4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="064a4-104">SYNTAX</span></span>

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="064a4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="064a4-105">DESCRIPTION</span></span>
<span data-ttu-id="064a4-106">Для **этого создается** группа ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="064a4-106">The **New-AzResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="064a4-107">Вы можете создать группу ресурсов, используя только имя и расположение, а затем использовать New-AzResource для создания ресурсов для добавления в группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="064a4-107">You can create a resource group by using just a name and location, and then use the New-AzResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="064a4-108">Чтобы добавить развертывание в существующую группу ресурсов, воспользуйтесь New-AzResourceGroupDeployment управления.</span><span class="sxs-lookup"><span data-stu-id="064a4-108">To add a deployment to an existing resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="064a4-109">Чтобы добавить ресурс в существующую группу ресурсов, воспользуйтесь **cmdlet New-AzResource.**</span><span class="sxs-lookup"><span data-stu-id="064a4-109">To add a resource to an existing resource group, use the **New-AzResource** cmdlet.</span></span> <span data-ttu-id="064a4-110">Ресурс Azure — это объект Azure, управляемый пользователем, например сервер базы данных, база данных или веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="064a4-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="064a4-111">Группа ресурсов Azure — это набор ресурсов Azure, развертывается как единица.</span><span class="sxs-lookup"><span data-stu-id="064a4-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="064a4-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="064a4-112">EXAMPLES</span></span>

### <span data-ttu-id="064a4-113">Пример 1. Создание пустой группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="064a4-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="064a4-114">Эта команда создает группу ресурсов без ресурсов.</span><span class="sxs-lookup"><span data-stu-id="064a4-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="064a4-115">Для добавления ресурсов и развертывания в эту группу ресурсов можно использовать **new-AzResource** или **New-AzResourceGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="064a4-115">You can use the **New-AzResource** or **New-AzResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="064a4-116">Пример 2. Создание пустой группы ресурсов с использованием позиционной параметров</span><span class="sxs-lookup"><span data-stu-id="064a4-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzResourceGroup RG01 "South Central US"
```

<span data-ttu-id="064a4-117">Эта команда создает группу ресурсов без ресурсов.</span><span class="sxs-lookup"><span data-stu-id="064a4-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="064a4-118">Пример 3. Создание группы ресурсов с тегами</span><span class="sxs-lookup"><span data-stu-id="064a4-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="064a4-119">Эта команда создает пустую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="064a4-119">This command creates an empty resource group.</span></span> <span data-ttu-id="064a4-120">Эта команда та же, что и в примере 1, за исключением того, что она назначает теги группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="064a4-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="064a4-121">Первый тег с именем "Пусто" можно использовать для определения групп ресурсов, не имеющих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="064a4-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="064a4-122">Второй тег называется "Отдел" и имеет значение "Маркетинг".</span><span class="sxs-lookup"><span data-stu-id="064a4-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="064a4-123">С помощью такого тега можно классифицировать группы ресурсов для администрирования или бюджетизации.</span><span class="sxs-lookup"><span data-stu-id="064a4-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="064a4-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="064a4-124">PARAMETERS</span></span>

### <span data-ttu-id="064a4-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="064a4-125">-ApiVersion</span></span>
<span data-ttu-id="064a4-126">Указывает версию API, которая поддерживается поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="064a4-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="064a4-127">Можно указать другую версию, чем версия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="064a4-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="064a4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="064a4-128">-DefaultProfile</span></span>
<span data-ttu-id="064a4-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="064a4-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="064a4-130">-Force</span><span class="sxs-lookup"><span data-stu-id="064a4-130">-Force</span></span>
<span data-ttu-id="064a4-131">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="064a4-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="064a4-132">-Location</span><span class="sxs-lookup"><span data-stu-id="064a4-132">-Location</span></span>
<span data-ttu-id="064a4-133">Определяет расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="064a4-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="064a4-134">Укажите расположение центра обработки данных Azure, например "Западная США" или "Юго-Восточная Азия".</span><span class="sxs-lookup"><span data-stu-id="064a4-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="064a4-135">Группу ресурсов можно разместить в любом месте.</span><span class="sxs-lookup"><span data-stu-id="064a4-135">You can place a resource group in any location.</span></span> <span data-ttu-id="064a4-136">Группа ресурсов не должна быть расположена в том же расположении, что и ее подписка На Azure, или в том же расположении, что и ее ресурсы.</span><span class="sxs-lookup"><span data-stu-id="064a4-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="064a4-137">Чтобы определить, какое расположение поддерживает каждый тип ресурсов, используйте Get-AzResourceProvider с параметром *ProviderNamespace.*</span><span class="sxs-lookup"><span data-stu-id="064a4-137">To determine which location supports each resource type, use the Get-AzResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

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

### <span data-ttu-id="064a4-138">-Name</span><span class="sxs-lookup"><span data-stu-id="064a4-138">-Name</span></span>
<span data-ttu-id="064a4-139">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="064a4-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="064a4-140">Имя ресурса должно быть уникальным в подписке.</span><span class="sxs-lookup"><span data-stu-id="064a4-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="064a4-141">Если группа ресурсов с таким именем уже существует, перед заменой существующей группы ресурсов будет предложено подтвердить ее.</span><span class="sxs-lookup"><span data-stu-id="064a4-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="064a4-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="064a4-142">-Pre</span></span>
<span data-ttu-id="064a4-143">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="064a4-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="064a4-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="064a4-144">-Tag</span></span>
<span data-ttu-id="064a4-145">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="064a4-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="064a4-146">Например: @{key0="value0";key1=$null;key2="value2"} Чтобы добавить или изменить тег, необходимо заменить коллекцию тегов для группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="064a4-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="064a4-147">После назначения тегов ресурсам и группам можно  использовать параметр "Тег" Get-AzResource и Get-AzResourceGroup для поиска ресурсов и групп по имени или имени и значению.</span><span class="sxs-lookup"><span data-stu-id="064a4-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="064a4-148">С помощью тегов можно классифицировать ресурсы,например по отделам или затратам, а также для отслеживания заметок и примечаний к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="064a4-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="064a4-149">Чтобы получить предопределные теги, воспользуйтесь Get-AzTag командлетом.</span><span class="sxs-lookup"><span data-stu-id="064a4-149">To get your predefined tags, use the Get-AzTag cmdlet.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="064a4-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="064a4-150">-Confirm</span></span>
<span data-ttu-id="064a4-151">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="064a4-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="064a4-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="064a4-152">-WhatIf</span></span>
<span data-ttu-id="064a4-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="064a4-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="064a4-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="064a4-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="064a4-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="064a4-155">CommonParameters</span></span>
<span data-ttu-id="064a4-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="064a4-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="064a4-157">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="064a4-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="064a4-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="064a4-158">INPUTS</span></span>

### <span data-ttu-id="064a4-159">System.String</span><span class="sxs-lookup"><span data-stu-id="064a4-159">System.String</span></span>

### <span data-ttu-id="064a4-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="064a4-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="064a4-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="064a4-161">OUTPUTS</span></span>

### <span data-ttu-id="064a4-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="064a4-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="064a4-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="064a4-163">NOTES</span></span>

## <span data-ttu-id="064a4-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="064a4-164">RELATED LINKS</span></span>

[<span data-ttu-id="064a4-165">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="064a4-165">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="064a4-166">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="064a4-166">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="064a4-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="064a4-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="064a4-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="064a4-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="064a4-169">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="064a4-169">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="064a4-170">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="064a4-170">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)
