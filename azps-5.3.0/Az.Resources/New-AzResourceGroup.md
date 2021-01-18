---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: 9c4bdfe189c16f3e2f6f90d3197149bdc57c78c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505209"
---
# <span data-ttu-id="356fb-101">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="356fb-101">New-AzResourceGroup</span></span>

## <span data-ttu-id="356fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="356fb-102">SYNOPSIS</span></span>
<span data-ttu-id="356fb-103">Создает группу ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="356fb-103">Creates an Azure resource group.</span></span>

## <span data-ttu-id="356fb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="356fb-104">SYNTAX</span></span>

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="356fb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="356fb-105">DESCRIPTION</span></span>
<span data-ttu-id="356fb-106">Для **этого создается** группа ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="356fb-106">The **New-AzResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="356fb-107">Вы можете создать группу ресурсов, используя только имя и расположение, а затем использовать New-AzResource для создания ресурсов для добавления в группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="356fb-107">You can create a resource group by using just a name and location, and then use the New-AzResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="356fb-108">Чтобы добавить развертывание в существующую группу ресурсов, воспользуйтесь New-AzResourceGroupDeployment управления.</span><span class="sxs-lookup"><span data-stu-id="356fb-108">To add a deployment to an existing resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="356fb-109">Чтобы добавить ресурс в существующую группу ресурсов, воспользуйтесь **cmdlet New-AzResource.**</span><span class="sxs-lookup"><span data-stu-id="356fb-109">To add a resource to an existing resource group, use the **New-AzResource** cmdlet.</span></span> <span data-ttu-id="356fb-110">Ресурс Azure — это объект Azure, управляемый пользователем, например сервер базы данных, база данных или веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="356fb-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="356fb-111">Группа ресурсов Azure — это набор ресурсов Azure, развертываемых в качестве единицы.</span><span class="sxs-lookup"><span data-stu-id="356fb-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="356fb-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="356fb-112">EXAMPLES</span></span>

### <span data-ttu-id="356fb-113">Пример 1. Создание пустой группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="356fb-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="356fb-114">Эта команда создает группу ресурсов без ресурсов.</span><span class="sxs-lookup"><span data-stu-id="356fb-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="356fb-115">Для добавления ресурсов и развертывания в эту группу ресурсов можно использовать **new-AzResource** или **New-AzResourceGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="356fb-115">You can use the **New-AzResource** or **New-AzResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="356fb-116">Пример 2. Создание пустой группы ресурсов с использованием позиционной параметров</span><span class="sxs-lookup"><span data-stu-id="356fb-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzResourceGroup RG01 "South Central US"
```

<span data-ttu-id="356fb-117">Эта команда создает группу ресурсов без ресурсов.</span><span class="sxs-lookup"><span data-stu-id="356fb-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="356fb-118">Пример 3. Создание группы ресурсов с тегами</span><span class="sxs-lookup"><span data-stu-id="356fb-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="356fb-119">Эта команда создает пустую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="356fb-119">This command creates an empty resource group.</span></span> <span data-ttu-id="356fb-120">Эта команда та же, что и в примере 1, за исключением того, что она назначает теги группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="356fb-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="356fb-121">Первый тег с именем "Пусто" можно использовать для определения групп ресурсов, не имеющих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="356fb-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="356fb-122">Второй тег называется "Отдел" и имеет значение "Маркетинг".</span><span class="sxs-lookup"><span data-stu-id="356fb-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="356fb-123">С помощью такого тега можно классифицировать группы ресурсов для администрирования или бюджетизации.</span><span class="sxs-lookup"><span data-stu-id="356fb-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="356fb-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="356fb-124">PARAMETERS</span></span>

### <span data-ttu-id="356fb-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="356fb-125">-ApiVersion</span></span>
<span data-ttu-id="356fb-126">Указывает версию API, которая поддерживается поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="356fb-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="356fb-127">Вы можете указать другую версию, чем версия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="356fb-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="356fb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="356fb-128">-DefaultProfile</span></span>
<span data-ttu-id="356fb-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="356fb-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="356fb-130">-Force</span><span class="sxs-lookup"><span data-stu-id="356fb-130">-Force</span></span>
<span data-ttu-id="356fb-131">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="356fb-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="356fb-132">-Location</span><span class="sxs-lookup"><span data-stu-id="356fb-132">-Location</span></span>
<span data-ttu-id="356fb-133">Определяет расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="356fb-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="356fb-134">Укажите расположение центра обработки данных Azure, например "Западная США" или "Юго-Восточная Азия".</span><span class="sxs-lookup"><span data-stu-id="356fb-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="356fb-135">Группу ресурсов можно разместить в любом месте.</span><span class="sxs-lookup"><span data-stu-id="356fb-135">You can place a resource group in any location.</span></span> <span data-ttu-id="356fb-136">Группа ресурсов не должна быть расположена в том же расположении, что и ее подписка На Azure.</span><span class="sxs-lookup"><span data-stu-id="356fb-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="356fb-137">Чтобы определить, какое расположение поддерживает каждый тип ресурсов, используйте Get-AzResourceProvider с параметром *ProviderNamespace.*</span><span class="sxs-lookup"><span data-stu-id="356fb-137">To determine which location supports each resource type, use the Get-AzResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

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

### <span data-ttu-id="356fb-138">-Name</span><span class="sxs-lookup"><span data-stu-id="356fb-138">-Name</span></span>
<span data-ttu-id="356fb-139">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="356fb-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="356fb-140">Имя ресурса должно быть уникальным в подписке.</span><span class="sxs-lookup"><span data-stu-id="356fb-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="356fb-141">Если группа ресурсов с таким именем уже существует, перед заменой существующей группы ресурсов будет предложено подтвердить ее.</span><span class="sxs-lookup"><span data-stu-id="356fb-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

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

### <span data-ttu-id="356fb-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="356fb-142">-Pre</span></span>
<span data-ttu-id="356fb-143">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="356fb-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="356fb-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="356fb-144">-Tag</span></span>
<span data-ttu-id="356fb-145">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="356fb-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="356fb-146">Например: @{key0="value0";key1=$null;key2="value2"} Чтобы добавить или изменить тег, необходимо заменить коллекцию тегов для группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="356fb-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="356fb-147">После назначения тегов ресурсам и группам можно  использовать параметр "Тег" в Get-AzResource и Get-AzResourceGroup для поиска ресурсов и групп по имени или имени и значению.</span><span class="sxs-lookup"><span data-stu-id="356fb-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="356fb-148">С помощью тегов можно классифицировать ресурсы,например по отделам или затратам, а также для отслеживания заметок и примечаний к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="356fb-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="356fb-149">Чтобы получить предопределные теги, воспользуйтесь Get-AzTag командлетом.</span><span class="sxs-lookup"><span data-stu-id="356fb-149">To get your predefined tags, use the Get-AzTag cmdlet.</span></span>

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

### <span data-ttu-id="356fb-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="356fb-150">-Confirm</span></span>
<span data-ttu-id="356fb-151">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="356fb-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="356fb-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="356fb-152">-WhatIf</span></span>
<span data-ttu-id="356fb-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="356fb-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="356fb-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="356fb-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="356fb-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="356fb-155">CommonParameters</span></span>
<span data-ttu-id="356fb-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="356fb-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="356fb-157">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="356fb-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="356fb-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="356fb-158">INPUTS</span></span>

### <span data-ttu-id="356fb-159">System.String</span><span class="sxs-lookup"><span data-stu-id="356fb-159">System.String</span></span>

### <span data-ttu-id="356fb-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="356fb-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="356fb-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="356fb-161">OUTPUTS</span></span>

### <span data-ttu-id="356fb-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="356fb-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="356fb-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="356fb-163">NOTES</span></span>

## <span data-ttu-id="356fb-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="356fb-164">RELATED LINKS</span></span>

[<span data-ttu-id="356fb-165">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="356fb-165">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="356fb-166">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="356fb-166">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="356fb-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="356fb-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="356fb-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="356fb-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="356fb-169">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="356fb-169">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="356fb-170">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="356fb-170">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)
