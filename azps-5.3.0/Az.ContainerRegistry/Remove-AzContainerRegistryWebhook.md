---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 4064728aeffb53fe9f6065d295455738b6a0f046
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519385"
---
# <span data-ttu-id="edaca-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="edaca-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="edaca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edaca-102">SYNOPSIS</span></span>
<span data-ttu-id="edaca-103">Удаляет веб-сайт контейнера реестра.</span><span class="sxs-lookup"><span data-stu-id="edaca-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="edaca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="edaca-104">SYNTAX</span></span>

### <span data-ttu-id="edaca-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="edaca-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edaca-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="edaca-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edaca-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="edaca-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edaca-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="edaca-108">DESCRIPTION</span></span>
<span data-ttu-id="edaca-109">Новый Remove-AzContainerRegistryWebhook удаляет веб-сайт реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="edaca-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="edaca-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="edaca-110">EXAMPLES</span></span>

### <span data-ttu-id="edaca-111">Пример 1. Удаление веб-приложения реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="edaca-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="edaca-112">Удаляет веб-сайт контейнера реестра.</span><span class="sxs-lookup"><span data-stu-id="edaca-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="edaca-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edaca-113">PARAMETERS</span></span>

### <span data-ttu-id="edaca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edaca-114">-DefaultProfile</span></span>
<span data-ttu-id="edaca-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="edaca-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edaca-116">-Name</span><span class="sxs-lookup"><span data-stu-id="edaca-116">-Name</span></span>
<span data-ttu-id="edaca-117">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="edaca-117">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edaca-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edaca-118">-PassThru</span></span>
<span data-ttu-id="edaca-119">Указывает на то, что этот cmdlet возвращает истина, если удаление было успешно.</span><span class="sxs-lookup"><span data-stu-id="edaca-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="edaca-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="edaca-120">-RegistryName</span></span>
<span data-ttu-id="edaca-121">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="edaca-121">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edaca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edaca-122">-ResourceGroupName</span></span>
<span data-ttu-id="edaca-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="edaca-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edaca-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edaca-124">-ResourceId</span></span>
<span data-ttu-id="edaca-125">ИД ресурса Webhook реестра контейнеров</span><span class="sxs-lookup"><span data-stu-id="edaca-125">The container registry Webhook resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edaca-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="edaca-126">-Webhook</span></span>
<span data-ttu-id="edaca-127">Объект Container Registry.</span><span class="sxs-lookup"><span data-stu-id="edaca-127">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edaca-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edaca-128">-Confirm</span></span>
<span data-ttu-id="edaca-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="edaca-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edaca-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edaca-130">-WhatIf</span></span>
<span data-ttu-id="edaca-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edaca-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edaca-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="edaca-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edaca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edaca-133">CommonParameters</span></span>
<span data-ttu-id="edaca-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edaca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edaca-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="edaca-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edaca-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="edaca-136">INPUTS</span></span>

### <span data-ttu-id="edaca-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="edaca-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="edaca-138">System.String</span><span class="sxs-lookup"><span data-stu-id="edaca-138">System.String</span></span>

## <span data-ttu-id="edaca-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="edaca-139">OUTPUTS</span></span>

### <span data-ttu-id="edaca-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="edaca-140">System.Boolean</span></span>

## <span data-ttu-id="edaca-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="edaca-141">NOTES</span></span>

## <span data-ttu-id="edaca-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="edaca-142">RELATED LINKS</span></span>

[<span data-ttu-id="edaca-143">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="edaca-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="edaca-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="edaca-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="edaca-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="edaca-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="edaca-146">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="edaca-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)