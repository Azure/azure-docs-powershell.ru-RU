---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
ms.openlocfilehash: fabe9019ff1a793bf5c7b5b0608f63ea4d9881f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561539"
---
# <span data-ttu-id="e8394-101">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e8394-101">New-AzureRmResourceGroup</span></span>

## <span data-ttu-id="e8394-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8394-102">SYNOPSIS</span></span>
<span data-ttu-id="e8394-103">Создание группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="e8394-103">Creates an Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8394-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8394-104">SYNTAX</span></span>

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8394-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8394-105">DESCRIPTION</span></span>
<span data-ttu-id="e8394-106">Командлет **New-AzureRmResourceGroup** создает группу ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="e8394-106">The **New-AzureRmResourceGroup** cmdlet creates an Azure resource group.</span></span>

<span data-ttu-id="e8394-107">Вы можете создать группу ресурсов, используя только имя и расположение, а затем с помощью командлета New-AzureRmResource создать ресурсы, которые нужно добавить в группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8394-107">You can create a resource group by using just a name and location, and then use the New-AzureRmResource cmdlet to create resources to add to the resource group.</span></span>

<span data-ttu-id="e8394-108">Чтобы добавить развертывание в существующую группу ресурсов, используйте командлет New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="e8394-108">To add a deployment to an existing resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="e8394-109">Чтобы добавить ресурс в существующую группу ресурсов, используйте командлет **New-AzureRmResource** .</span><span class="sxs-lookup"><span data-stu-id="e8394-109">To add a resource to an existing resource group, use the **New-AzureRmResource** cmdlet.</span></span> <span data-ttu-id="e8394-110">Ресурс Azure — это управляемая пользователем сущность Azure, например сервер базы данных, база данных или веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="e8394-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="e8394-111">Группа ресурсов Azure — это коллекция ресурсов Azure, развернутых как единое целое.</span><span class="sxs-lookup"><span data-stu-id="e8394-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="e8394-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8394-112">EXAMPLES</span></span>

### <span data-ttu-id="e8394-113">Пример 1: создание пустой группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e8394-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="e8394-114">Эта команда создает группу ресурсов, в которой нет ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8394-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="e8394-115">Вы можете использовать командлеты **New-AzureRmResource** или **New-AzureRmResourceGroupDeployment** для добавления ресурсов и развертываний в эту группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8394-115">You can use the **New-AzureRmResource** or **New-AzureRmResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="e8394-116">Пример 2: создание пустой группы ресурсов с помощью позиционных параметров</span><span class="sxs-lookup"><span data-stu-id="e8394-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzureRmResourceGroup RG01 "South Central US"
```

<span data-ttu-id="e8394-117">Эта команда создает группу ресурсов, в которой нет ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8394-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="e8394-118">Пример 3: создание группы ресурсов с помощью тегов</span><span class="sxs-lookup"><span data-stu-id="e8394-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="e8394-119">Эта команда создает пустую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8394-119">This command creates an empty resource group.</span></span> <span data-ttu-id="e8394-120">Эта команда аналогична команде в примере 1, за исключением того, что она назначает теги для группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8394-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="e8394-121">Первый тег, именуемый Empty, можно использовать для идентификации групп ресурсов, не имеющих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8394-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="e8394-122">Второй тег называется "Отдел" и имеет значение "маркетинг".</span><span class="sxs-lookup"><span data-stu-id="e8394-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="e8394-123">Вы можете использовать тег, например этот, для классификации групп ресурсов для администрирования и бюджетирования.</span><span class="sxs-lookup"><span data-stu-id="e8394-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="e8394-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8394-124">PARAMETERS</span></span>

### <span data-ttu-id="e8394-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e8394-125">-ApiVersion</span></span>
<span data-ttu-id="e8394-126">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8394-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e8394-127">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e8394-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e8394-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8394-128">-DefaultProfile</span></span>
<span data-ttu-id="e8394-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e8394-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8394-130">-Force</span><span class="sxs-lookup"><span data-stu-id="e8394-130">-Force</span></span>
<span data-ttu-id="e8394-131">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e8394-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e8394-132">-Location</span><span class="sxs-lookup"><span data-stu-id="e8394-132">-Location</span></span>
<span data-ttu-id="e8394-133">Указывает расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8394-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="e8394-134">Укажите расположение центра обработки данных Azure, например Западная часть США или Юго-Восток Азии.</span><span class="sxs-lookup"><span data-stu-id="e8394-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="e8394-135">Группу ресурсов можно поместить в любое место.</span><span class="sxs-lookup"><span data-stu-id="e8394-135">You can place a resource group in any location.</span></span> <span data-ttu-id="e8394-136">Группа ресурсов может не находиться в той же папке, в которой находится подписка на Azure, или в том же местоположении, что и его ресурсы.</span><span class="sxs-lookup"><span data-stu-id="e8394-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>

<span data-ttu-id="e8394-137">Чтобы определить, в каком месте поддерживается каждый тип ресурсов, используйте командлет Get-AzureRmResourceProvider с параметром *ProviderNamespace* .</span><span class="sxs-lookup"><span data-stu-id="e8394-137">To determine which location supports each resource type, use the Get-AzureRmResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8394-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e8394-138">-Name</span></span>
<span data-ttu-id="e8394-139">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8394-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="e8394-140">Имя ресурса должно быть уникальным в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="e8394-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="e8394-141">Если группа ресурсов с таким именем уже существует, она запрашивает подтверждение перед тем, как заменить существующую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8394-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8394-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="e8394-142">-Pre</span></span>
<span data-ttu-id="e8394-143">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="e8394-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e8394-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="e8394-144">-Tag</span></span>
<span data-ttu-id="e8394-145">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="e8394-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e8394-146">Например:</span><span class="sxs-lookup"><span data-stu-id="e8394-146">For example:</span></span>

<span data-ttu-id="e8394-147">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="e8394-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="e8394-148">Чтобы добавить или изменить тег, необходимо заменить коллекцию тегов для группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8394-148">To add or change a tag, you must replace the collection of tags for the resource group.</span></span>

<span data-ttu-id="e8394-149">Определив теги для ресурсов и групп, вы можете использовать параметр *Tag* Get-AzureRmResource и Get-AzureRmResourceGroup для поиска ресурсов и групп по имени тега или по имени и значению.</span><span class="sxs-lookup"><span data-stu-id="e8394-149">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="e8394-150">Теги можно использовать для классификации ресурсов, таких как отдел или центр затрат, а также для отслеживания заметок и примечаний к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="e8394-150">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>

<span data-ttu-id="e8394-151">Чтобы получить предопределенные теги, используйте командлет Get-AzureRMTag.</span><span class="sxs-lookup"><span data-stu-id="e8394-151">To get your predefined tags, use the Get-AzureRMTag cmdlet.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8394-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8394-152">-Confirm</span></span>
<span data-ttu-id="e8394-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e8394-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8394-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8394-154">-WhatIf</span></span>
<span data-ttu-id="e8394-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e8394-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8394-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e8394-156">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8394-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8394-157">CommonParameters</span></span>
<span data-ttu-id="e8394-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8394-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8394-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8394-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8394-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8394-160">INPUTS</span></span>

### <span data-ttu-id="e8394-161">Ничего</span><span class="sxs-lookup"><span data-stu-id="e8394-161">None</span></span>

## <span data-ttu-id="e8394-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8394-162">OUTPUTS</span></span>

### <span data-ttu-id="e8394-163">Microsoft. Azure. Commands. ResourceManagement. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e8394-163">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroup</span></span>

## <span data-ttu-id="e8394-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8394-164">NOTES</span></span>

## <span data-ttu-id="e8394-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8394-165">RELATED LINKS</span></span>

[<span data-ttu-id="e8394-166">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e8394-166">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="e8394-167">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e8394-167">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="e8394-168">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e8394-168">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="e8394-169">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e8394-169">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e8394-170">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e8394-170">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="e8394-171">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e8394-171">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)
