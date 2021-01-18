---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: 9c7c002861832da3e871b49f03753608ba48268d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505269"
---
# <span data-ttu-id="cca7d-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cca7d-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="cca7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cca7d-102">SYNOPSIS</span></span>
<span data-ttu-id="cca7d-103">Возвращает группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cca7d-103">Gets resource groups.</span></span>

## <span data-ttu-id="cca7d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cca7d-104">SYNTAX</span></span>

### <span data-ttu-id="cca7d-105">GetByResourceGroupName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cca7d-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cca7d-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="cca7d-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cca7d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cca7d-107">DESCRIPTION</span></span>
<span data-ttu-id="cca7d-108">С **использованием cmdlet Get-AzResourceGroup** группы ресурсов Azure будут в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="cca7d-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="cca7d-109">Вы можете получить все группы ресурсов или указать группу ресурсов по имени или другим свойствам.</span><span class="sxs-lookup"><span data-stu-id="cca7d-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="cca7d-110">По умолчанию этот cmdlet получает все группы ресурсов в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="cca7d-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="cca7d-111">Дополнительные сведения о ресурсах Azure и группах ресурсов Azure см. в New-AzResourceGroup>.</span><span class="sxs-lookup"><span data-stu-id="cca7d-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="cca7d-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cca7d-112">EXAMPLES</span></span>

### <span data-ttu-id="cca7d-113">Пример 1. Получить группу ресурсов по имени</span><span class="sxs-lookup"><span data-stu-id="cca7d-113">Example 1: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="cca7d-114">Эта команда получает группу ресурсов Azure в вашей подписке с именем EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="cca7d-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="cca7d-115">Пример 2. Получить все теги группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cca7d-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="cca7d-116">Эта команда получает группу ресурсов с именем ContosoRG и отображает связанные с ней теги.</span><span class="sxs-lookup"><span data-stu-id="cca7d-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="cca7d-117">Пример 3. Получить группы ресурсов на основе тега</span><span class="sxs-lookup"><span data-stu-id="cca7d-117">Example 3: Get resource groups based on tag</span></span>
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### <span data-ttu-id="cca7d-118">Пример 4. Показывать группы ресурсов по расположению</span><span class="sxs-lookup"><span data-stu-id="cca7d-118">Example 4: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="cca7d-119">Пример 5. Показ имен всех групп ресурсов в определенном расположении</span><span class="sxs-lookup"><span data-stu-id="cca7d-119">Example 5: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="cca7d-120">Пример 6. Показывать группы ресурсов, имена которых начинаются с WebServer</span><span class="sxs-lookup"><span data-stu-id="cca7d-120">Example 6: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## <span data-ttu-id="cca7d-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cca7d-121">PARAMETERS</span></span>

### <span data-ttu-id="cca7d-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cca7d-122">-ApiVersion</span></span>
<span data-ttu-id="cca7d-123">Указывает версию API, которая поддерживается поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cca7d-123">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="cca7d-124">Вы можете указать другую версию, чем версия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cca7d-124">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="cca7d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca7d-125">-DefaultProfile</span></span>
<span data-ttu-id="cca7d-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cca7d-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cca7d-127">-Id</span><span class="sxs-lookup"><span data-stu-id="cca7d-127">-Id</span></span>
<span data-ttu-id="cca7d-128">Определяет ИД группы ресурсов, которая будет получать.</span><span class="sxs-lookup"><span data-stu-id="cca7d-128">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="cca7d-129">Поддиавные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="cca7d-129">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cca7d-130">-Location</span><span class="sxs-lookup"><span data-stu-id="cca7d-130">-Location</span></span>
<span data-ttu-id="cca7d-131">Определяет расположение группы ресурсов, которая будет получаться.</span><span class="sxs-lookup"><span data-stu-id="cca7d-131">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cca7d-132">-Name</span><span class="sxs-lookup"><span data-stu-id="cca7d-132">-Name</span></span>
<span data-ttu-id="cca7d-133">Имя группы ресурсов, которая будет получаться.</span><span class="sxs-lookup"><span data-stu-id="cca7d-133">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="cca7d-134">Этот параметр поддерживает поддиавные знаки в начале или в конце строки.</span><span class="sxs-lookup"><span data-stu-id="cca7d-134">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="cca7d-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="cca7d-135">-Pre</span></span>
<span data-ttu-id="cca7d-136">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="cca7d-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cca7d-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="cca7d-137">-Tag</span></span>
<span data-ttu-id="cca7d-138">Тег может в несколько раз отфильтровать группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cca7d-138">The tag hashtable to filter resource groups by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cca7d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca7d-139">CommonParameters</span></span>
<span data-ttu-id="cca7d-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cca7d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca7d-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cca7d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca7d-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cca7d-142">INPUTS</span></span>

### <span data-ttu-id="cca7d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="cca7d-143">System.String</span></span>

### <span data-ttu-id="cca7d-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="cca7d-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cca7d-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cca7d-145">OUTPUTS</span></span>

### <span data-ttu-id="cca7d-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cca7d-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="cca7d-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cca7d-147">NOTES</span></span>

## <span data-ttu-id="cca7d-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cca7d-148">RELATED LINKS</span></span>

[<span data-ttu-id="cca7d-149">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cca7d-149">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="cca7d-150">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cca7d-150">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="cca7d-151">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cca7d-151">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)

