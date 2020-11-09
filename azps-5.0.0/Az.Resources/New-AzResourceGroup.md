---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: 9c4bdfe189c16f3e2f6f90d3197149bdc57c78c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315671"
---
# <span data-ttu-id="94e0e-101">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94e0e-101">New-AzResourceGroup</span></span>

## <span data-ttu-id="94e0e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94e0e-102">SYNOPSIS</span></span>
<span data-ttu-id="94e0e-103">Создание группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="94e0e-103">Creates an Azure resource group.</span></span>

## <span data-ttu-id="94e0e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94e0e-104">SYNTAX</span></span>

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94e0e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94e0e-105">DESCRIPTION</span></span>
<span data-ttu-id="94e0e-106">Командлет **New-AzResourceGroup** создает группу ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="94e0e-106">The **New-AzResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="94e0e-107">Вы можете создать группу ресурсов, используя только имя и расположение, а затем с помощью командлета New-AzResource создать ресурсы, которые нужно добавить в группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94e0e-107">You can create a resource group by using just a name and location, and then use the New-AzResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="94e0e-108">Чтобы добавить развертывание в существующую группу ресурсов, используйте командлет New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="94e0e-108">To add a deployment to an existing resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="94e0e-109">Чтобы добавить ресурс в существующую группу ресурсов, используйте командлет **New-AzResource** .</span><span class="sxs-lookup"><span data-stu-id="94e0e-109">To add a resource to an existing resource group, use the **New-AzResource** cmdlet.</span></span> <span data-ttu-id="94e0e-110">Ресурс Azure — это управляемая пользователем сущность Azure, например сервер базы данных, база данных или веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="94e0e-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="94e0e-111">Группа ресурсов Azure — это коллекция ресурсов Azure, развернутых как единое целое.</span><span class="sxs-lookup"><span data-stu-id="94e0e-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="94e0e-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94e0e-112">EXAMPLES</span></span>

### <span data-ttu-id="94e0e-113">Пример 1: создание пустой группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="94e0e-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="94e0e-114">Эта команда создает группу ресурсов, в которой нет ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94e0e-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="94e0e-115">Вы можете использовать командлеты **New-AzResource** или **New-AzResourceGroupDeployment** для добавления ресурсов и развертываний в эту группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94e0e-115">You can use the **New-AzResource** or **New-AzResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="94e0e-116">Пример 2: создание пустой группы ресурсов с помощью позиционных параметров</span><span class="sxs-lookup"><span data-stu-id="94e0e-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzResourceGroup RG01 "South Central US"
```

<span data-ttu-id="94e0e-117">Эта команда создает группу ресурсов, в которой нет ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94e0e-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="94e0e-118">Пример 3: создание группы ресурсов с помощью тегов</span><span class="sxs-lookup"><span data-stu-id="94e0e-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="94e0e-119">Эта команда создает пустую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94e0e-119">This command creates an empty resource group.</span></span> <span data-ttu-id="94e0e-120">Эта команда аналогична команде в примере 1, за исключением того, что она назначает теги для группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94e0e-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="94e0e-121">Первый тег, именуемый Empty, можно использовать для идентификации групп ресурсов, не имеющих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94e0e-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="94e0e-122">Второй тег называется "Отдел" и имеет значение "маркетинг".</span><span class="sxs-lookup"><span data-stu-id="94e0e-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="94e0e-123">Вы можете использовать тег, например этот, для классификации групп ресурсов для администрирования и бюджетирования.</span><span class="sxs-lookup"><span data-stu-id="94e0e-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="94e0e-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94e0e-124">PARAMETERS</span></span>

### <span data-ttu-id="94e0e-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="94e0e-125">-ApiVersion</span></span>
<span data-ttu-id="94e0e-126">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94e0e-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="94e0e-127">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="94e0e-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="94e0e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e0e-128">-DefaultProfile</span></span>
<span data-ttu-id="94e0e-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="94e0e-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94e0e-130">-Force</span><span class="sxs-lookup"><span data-stu-id="94e0e-130">-Force</span></span>
<span data-ttu-id="94e0e-131">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="94e0e-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="94e0e-132">-Location</span><span class="sxs-lookup"><span data-stu-id="94e0e-132">-Location</span></span>
<span data-ttu-id="94e0e-133">Указывает расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94e0e-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="94e0e-134">Укажите расположение центра обработки данных Azure, например Западная часть США или Юго-Восток Азии.</span><span class="sxs-lookup"><span data-stu-id="94e0e-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="94e0e-135">Группу ресурсов можно поместить в любое место.</span><span class="sxs-lookup"><span data-stu-id="94e0e-135">You can place a resource group in any location.</span></span> <span data-ttu-id="94e0e-136">Группа ресурсов может не находиться в той же папке, в которой находится подписка на Azure, или в том же местоположении, что и его ресурсы.</span><span class="sxs-lookup"><span data-stu-id="94e0e-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="94e0e-137">Чтобы определить, в каком месте поддерживается каждый тип ресурсов, используйте командлет Get-AzResourceProvider с параметром *ProviderNamespace* .</span><span class="sxs-lookup"><span data-stu-id="94e0e-137">To determine which location supports each resource type, use the Get-AzResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

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

### <span data-ttu-id="94e0e-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="94e0e-138">-Name</span></span>
<span data-ttu-id="94e0e-139">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94e0e-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="94e0e-140">Имя ресурса должно быть уникальным в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="94e0e-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="94e0e-141">Если группа ресурсов с таким именем уже существует, она запрашивает подтверждение перед тем, как заменить существующую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94e0e-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

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

### <span data-ttu-id="94e0e-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="94e0e-142">-Pre</span></span>
<span data-ttu-id="94e0e-143">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="94e0e-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="94e0e-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="94e0e-144">-Tag</span></span>
<span data-ttu-id="94e0e-145">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="94e0e-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="94e0e-146">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"} чтобы добавить или изменить тег, необходимо заменить коллекцию тегов для группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94e0e-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="94e0e-147">Определив теги для ресурсов и групп, вы можете использовать параметр *Tag* Get-AzResource и Get-AzResourceGroup для поиска ресурсов и групп по имени тега или по имени и значению.</span><span class="sxs-lookup"><span data-stu-id="94e0e-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="94e0e-148">Теги можно использовать для классификации ресурсов, таких как отдел или центр затрат, а также для отслеживания заметок и примечаний к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="94e0e-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="94e0e-149">Чтобы получить предопределенные теги, используйте командлет Get-AzTag.</span><span class="sxs-lookup"><span data-stu-id="94e0e-149">To get your predefined tags, use the Get-AzTag cmdlet.</span></span>

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

### <span data-ttu-id="94e0e-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94e0e-150">-Confirm</span></span>
<span data-ttu-id="94e0e-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="94e0e-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94e0e-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94e0e-152">-WhatIf</span></span>
<span data-ttu-id="94e0e-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="94e0e-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94e0e-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="94e0e-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94e0e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e0e-155">CommonParameters</span></span>
<span data-ttu-id="94e0e-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94e0e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e0e-157">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94e0e-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e0e-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94e0e-158">INPUTS</span></span>

### <span data-ttu-id="94e0e-159">System. String</span><span class="sxs-lookup"><span data-stu-id="94e0e-159">System.String</span></span>

### <span data-ttu-id="94e0e-160">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="94e0e-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="94e0e-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94e0e-161">OUTPUTS</span></span>

### <span data-ttu-id="94e0e-162">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94e0e-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="94e0e-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="94e0e-163">NOTES</span></span>

## <span data-ttu-id="94e0e-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94e0e-164">RELATED LINKS</span></span>

[<span data-ttu-id="94e0e-165">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="94e0e-165">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="94e0e-166">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94e0e-166">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="94e0e-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="94e0e-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="94e0e-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="94e0e-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="94e0e-169">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94e0e-169">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="94e0e-170">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94e0e-170">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)
