---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 4064728aeffb53fe9f6065d295455738b6a0f046
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326804"
---
# <span data-ttu-id="9d269-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9d269-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="9d269-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d269-102">SYNOPSIS</span></span>
<span data-ttu-id="9d269-103">Удаляет веб-сайт реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="9d269-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="9d269-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9d269-104">SYNTAX</span></span>

### <span data-ttu-id="9d269-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9d269-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d269-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d269-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d269-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d269-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d269-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d269-108">DESCRIPTION</span></span>
<span data-ttu-id="9d269-109">Новый Remove-AzContainerRegistryWebhook удаляет веб-сайт реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="9d269-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="9d269-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9d269-110">EXAMPLES</span></span>

### <span data-ttu-id="9d269-111">Пример 1. Удаление веб-приложения реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="9d269-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="9d269-112">Удаляет веб-сайт реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="9d269-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="9d269-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d269-113">PARAMETERS</span></span>

### <span data-ttu-id="9d269-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d269-114">-DefaultProfile</span></span>
<span data-ttu-id="9d269-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d269-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d269-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9d269-116">-Name</span></span>
<span data-ttu-id="9d269-117">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="9d269-117">Webhook Name.</span></span>

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

### <span data-ttu-id="9d269-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d269-118">-PassThru</span></span>
<span data-ttu-id="9d269-119">Указывает на то, что этот cmdlet возвращает истина, если удаление было успешно.</span><span class="sxs-lookup"><span data-stu-id="9d269-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="9d269-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="9d269-120">-RegistryName</span></span>
<span data-ttu-id="9d269-121">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="9d269-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="9d269-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d269-122">-ResourceGroupName</span></span>
<span data-ttu-id="9d269-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9d269-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="9d269-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d269-124">-ResourceId</span></span>
<span data-ttu-id="9d269-125">ИД ресурса Webhook реестра контейнеров</span><span class="sxs-lookup"><span data-stu-id="9d269-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="9d269-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="9d269-126">-Webhook</span></span>
<span data-ttu-id="9d269-127">Объект Container Registry.</span><span class="sxs-lookup"><span data-stu-id="9d269-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="9d269-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d269-128">-Confirm</span></span>
<span data-ttu-id="9d269-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9d269-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d269-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d269-130">-WhatIf</span></span>
<span data-ttu-id="9d269-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d269-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d269-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9d269-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d269-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d269-133">CommonParameters</span></span>
<span data-ttu-id="9d269-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d269-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d269-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d269-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d269-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d269-136">INPUTS</span></span>

### <span data-ttu-id="9d269-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9d269-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="9d269-138">System.String</span><span class="sxs-lookup"><span data-stu-id="9d269-138">System.String</span></span>

## <span data-ttu-id="9d269-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9d269-139">OUTPUTS</span></span>

### <span data-ttu-id="9d269-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9d269-140">System.Boolean</span></span>

## <span data-ttu-id="9d269-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9d269-141">NOTES</span></span>

## <span data-ttu-id="9d269-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d269-142">RELATED LINKS</span></span>

[<span data-ttu-id="9d269-143">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9d269-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="9d269-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9d269-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="9d269-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9d269-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="9d269-146">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9d269-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)