---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 4064728aeffb53fe9f6065d295455738b6a0f046
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912065"
---
# <span data-ttu-id="578df-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="578df-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="578df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="578df-102">SYNOPSIS</span></span>
<span data-ttu-id="578df-103">Удаление веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="578df-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="578df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="578df-104">SYNTAX</span></span>

### <span data-ttu-id="578df-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="578df-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="578df-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="578df-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="578df-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="578df-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="578df-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="578df-108">DESCRIPTION</span></span>
<span data-ttu-id="578df-109">Командлет Remove-AzContainerRegistryWebhook удаляет веб-перехватчик реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="578df-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="578df-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="578df-110">EXAMPLES</span></span>

### <span data-ttu-id="578df-111">Пример 1: удаление веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="578df-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="578df-112">Удаление веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="578df-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="578df-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="578df-113">PARAMETERS</span></span>

### <span data-ttu-id="578df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="578df-114">-DefaultProfile</span></span>
<span data-ttu-id="578df-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="578df-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="578df-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="578df-116">-Name</span></span>
<span data-ttu-id="578df-117">Имя веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="578df-117">Webhook Name.</span></span>

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

### <span data-ttu-id="578df-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="578df-118">-PassThru</span></span>
<span data-ttu-id="578df-119">Указывает на то, что этот командлет возвращает значение true, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="578df-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="578df-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="578df-120">-RegistryName</span></span>
<span data-ttu-id="578df-121">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="578df-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="578df-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="578df-122">-ResourceGroupName</span></span>
<span data-ttu-id="578df-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="578df-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="578df-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="578df-124">-ResourceId</span></span>
<span data-ttu-id="578df-125">Идентификатор ресурса веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="578df-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="578df-126">-Перехватчик</span><span class="sxs-lookup"><span data-stu-id="578df-126">-Webhook</span></span>
<span data-ttu-id="578df-127">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="578df-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="578df-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="578df-128">-Confirm</span></span>
<span data-ttu-id="578df-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="578df-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="578df-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="578df-130">-WhatIf</span></span>
<span data-ttu-id="578df-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="578df-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="578df-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="578df-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="578df-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="578df-133">CommonParameters</span></span>
<span data-ttu-id="578df-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="578df-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="578df-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="578df-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="578df-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="578df-136">INPUTS</span></span>

### <span data-ttu-id="578df-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="578df-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="578df-138">System. String</span><span class="sxs-lookup"><span data-stu-id="578df-138">System.String</span></span>

## <span data-ttu-id="578df-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="578df-139">OUTPUTS</span></span>

### <span data-ttu-id="578df-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="578df-140">System.Boolean</span></span>

## <span data-ttu-id="578df-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="578df-141">NOTES</span></span>

## <span data-ttu-id="578df-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="578df-142">RELATED LINKS</span></span>

[<span data-ttu-id="578df-143">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="578df-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="578df-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="578df-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="578df-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="578df-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="578df-146">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="578df-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)