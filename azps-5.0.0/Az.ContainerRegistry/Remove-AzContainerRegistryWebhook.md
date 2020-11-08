---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 4064728aeffb53fe9f6065d295455738b6a0f046
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245577"
---
# <span data-ttu-id="7c4a6-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7c4a6-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="7c4a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c4a6-102">SYNOPSIS</span></span>
<span data-ttu-id="7c4a6-103">Удаление веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="7c4a6-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="7c4a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c4a6-104">SYNTAX</span></span>

### <span data-ttu-id="7c4a6-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7c4a6-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c4a6-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c4a6-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c4a6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c4a6-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c4a6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c4a6-108">DESCRIPTION</span></span>
<span data-ttu-id="7c4a6-109">Командлет Remove-AzContainerRegistryWebhook удаляет веб-перехватчик реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="7c4a6-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="7c4a6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c4a6-110">EXAMPLES</span></span>

### <span data-ttu-id="7c4a6-111">Пример 1: удаление веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="7c4a6-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="7c4a6-112">Удаление веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="7c4a6-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="7c4a6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c4a6-113">PARAMETERS</span></span>

### <span data-ttu-id="7c4a6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c4a6-114">-DefaultProfile</span></span>
<span data-ttu-id="7c4a6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c4a6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c4a6-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7c4a6-116">-Name</span></span>
<span data-ttu-id="7c4a6-117">Имя веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="7c4a6-117">Webhook Name.</span></span>

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

### <span data-ttu-id="7c4a6-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c4a6-118">-PassThru</span></span>
<span data-ttu-id="7c4a6-119">Указывает на то, что этот командлет возвращает значение true, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="7c4a6-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="7c4a6-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="7c4a6-120">-RegistryName</span></span>
<span data-ttu-id="7c4a6-121">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="7c4a6-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="7c4a6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c4a6-122">-ResourceGroupName</span></span>
<span data-ttu-id="7c4a6-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7c4a6-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="7c4a6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c4a6-124">-ResourceId</span></span>
<span data-ttu-id="7c4a6-125">Идентификатор ресурса веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="7c4a6-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="7c4a6-126">-Перехватчик</span><span class="sxs-lookup"><span data-stu-id="7c4a6-126">-Webhook</span></span>
<span data-ttu-id="7c4a6-127">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="7c4a6-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="7c4a6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c4a6-128">-Confirm</span></span>
<span data-ttu-id="7c4a6-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7c4a6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c4a6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c4a6-130">-WhatIf</span></span>
<span data-ttu-id="7c4a6-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7c4a6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c4a6-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7c4a6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c4a6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c4a6-133">CommonParameters</span></span>
<span data-ttu-id="7c4a6-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c4a6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c4a6-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c4a6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c4a6-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c4a6-136">INPUTS</span></span>

### <span data-ttu-id="7c4a6-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7c4a6-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="7c4a6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7c4a6-138">System.String</span></span>

## <span data-ttu-id="7c4a6-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c4a6-139">OUTPUTS</span></span>

### <span data-ttu-id="7c4a6-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7c4a6-140">System.Boolean</span></span>

## <span data-ttu-id="7c4a6-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c4a6-141">NOTES</span></span>

## <span data-ttu-id="7c4a6-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c4a6-142">RELATED LINKS</span></span>

[<span data-ttu-id="7c4a6-143">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7c4a6-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7c4a6-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7c4a6-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7c4a6-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7c4a6-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7c4a6-146">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7c4a6-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)