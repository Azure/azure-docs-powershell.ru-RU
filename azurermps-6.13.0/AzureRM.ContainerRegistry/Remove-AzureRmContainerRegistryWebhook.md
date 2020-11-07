---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: c1ba245f83db386e39f9fecf22f95d3681452d7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734155"
---
# <span data-ttu-id="8a766-101">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8a766-101">Remove-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="8a766-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a766-102">SYNOPSIS</span></span>
<span data-ttu-id="8a766-103">Удаление веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="8a766-103">Removes a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a766-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a766-104">SYNTAX</span></span>

### <span data-ttu-id="8a766-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8a766-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a766-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a766-106">WebhookObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a766-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a766-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a766-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a766-108">DESCRIPTION</span></span>
<span data-ttu-id="8a766-109">Командлет Remove-AzureRmContainerRegistryWebhook удаляет веб-перехватчик реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="8a766-109">The Remove-AzureRmContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="8a766-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a766-110">EXAMPLES</span></span>

### <span data-ttu-id="8a766-111">Пример 1: удаление веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="8a766-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="8a766-112">Удаление веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="8a766-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="8a766-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a766-113">PARAMETERS</span></span>

### <span data-ttu-id="8a766-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a766-114">-DefaultProfile</span></span>
<span data-ttu-id="8a766-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a766-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a766-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8a766-116">-Name</span></span>
<span data-ttu-id="8a766-117">Имя веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="8a766-117">Webhook Name.</span></span>

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

### <span data-ttu-id="8a766-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a766-118">-PassThru</span></span>
<span data-ttu-id="8a766-119">Указывает на то, что этот командлет возвращает значение true, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="8a766-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="8a766-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="8a766-120">-RegistryName</span></span>
<span data-ttu-id="8a766-121">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="8a766-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="8a766-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a766-122">-ResourceGroupName</span></span>
<span data-ttu-id="8a766-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a766-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="8a766-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a766-124">-ResourceId</span></span>
<span data-ttu-id="8a766-125">Идентификатор ресурса веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="8a766-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="8a766-126">-Перехватчик</span><span class="sxs-lookup"><span data-stu-id="8a766-126">-Webhook</span></span>
<span data-ttu-id="8a766-127">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="8a766-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="8a766-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a766-128">-Confirm</span></span>
<span data-ttu-id="8a766-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8a766-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a766-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a766-130">-WhatIf</span></span>
<span data-ttu-id="8a766-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8a766-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a766-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8a766-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a766-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a766-133">CommonParameters</span></span>
<span data-ttu-id="8a766-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a766-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a766-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a766-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a766-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a766-136">INPUTS</span></span>

### <span data-ttu-id="8a766-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8a766-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="8a766-138">Параметры: веб-перехватчик (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8a766-138">Parameters: Webhook (ByValue)</span></span>

### <span data-ttu-id="8a766-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8a766-139">System.String</span></span>

## <span data-ttu-id="8a766-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a766-140">OUTPUTS</span></span>

### <span data-ttu-id="8a766-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8a766-141">System.Boolean</span></span>

## <span data-ttu-id="8a766-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a766-142">NOTES</span></span>

## <span data-ttu-id="8a766-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a766-143">RELATED LINKS</span></span>

[<span data-ttu-id="8a766-144">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8a766-144">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="8a766-145">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8a766-145">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="8a766-146">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8a766-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="8a766-147">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8a766-147">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
