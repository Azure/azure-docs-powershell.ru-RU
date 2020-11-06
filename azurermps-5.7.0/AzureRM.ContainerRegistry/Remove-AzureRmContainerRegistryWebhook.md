---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 058c923528227e05a4c8b8078f4495c56edfe20c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559132"
---
# <span data-ttu-id="9f6ff-101">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9f6ff-101">Remove-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="9f6ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f6ff-102">SYNOPSIS</span></span>
<span data-ttu-id="9f6ff-103">Удаление веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="9f6ff-103">Removes a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f6ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f6ff-104">SYNTAX</span></span>

### <span data-ttu-id="9f6ff-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f6ff-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f6ff-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f6ff-106">WebhookObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f6ff-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f6ff-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f6ff-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f6ff-108">DESCRIPTION</span></span>
<span data-ttu-id="9f6ff-109">Командлет Remove-AzureRmContainerRegistryWebhook удаляет веб-перехватчик реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="9f6ff-109">The Remove-AzureRmContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="9f6ff-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f6ff-110">EXAMPLES</span></span>

### <span data-ttu-id="9f6ff-111">Пример 1: удаление веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="9f6ff-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="9f6ff-112">Удаление веб-перехватчика реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="9f6ff-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="9f6ff-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f6ff-113">PARAMETERS</span></span>

### <span data-ttu-id="9f6ff-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f6ff-114">-Confirm</span></span>
<span data-ttu-id="9f6ff-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9f6ff-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f6ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f6ff-116">-DefaultProfile</span></span>
<span data-ttu-id="9f6ff-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f6ff-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f6ff-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9f6ff-118">-Name</span></span>
<span data-ttu-id="9f6ff-119">Имя веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="9f6ff-119">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f6ff-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="9f6ff-120">-RegistryName</span></span>
<span data-ttu-id="9f6ff-121">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="9f6ff-121">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f6ff-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f6ff-122">-ResourceGroupName</span></span>
<span data-ttu-id="9f6ff-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f6ff-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f6ff-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f6ff-124">-ResourceId</span></span>
<span data-ttu-id="9f6ff-125">Идентификатор ресурса веб-перехватчика реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="9f6ff-125">The container registry Webhook resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f6ff-126">-Перехватчик</span><span class="sxs-lookup"><span data-stu-id="9f6ff-126">-Webhook</span></span>
<span data-ttu-id="9f6ff-127">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="9f6ff-127">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f6ff-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f6ff-128">-WhatIf</span></span>
<span data-ttu-id="9f6ff-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9f6ff-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f6ff-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9f6ff-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f6ff-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f6ff-131">-PassThru</span></span>
<span data-ttu-id="9f6ff-132">Указывает на то, что этот командлет возвращает значение true, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="9f6ff-132">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="9f6ff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f6ff-133">CommonParameters</span></span>
<span data-ttu-id="9f6ff-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f6ff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f6ff-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f6ff-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f6ff-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f6ff-136">INPUTS</span></span>

### <span data-ttu-id="9f6ff-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9f6ff-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="9f6ff-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9f6ff-138">System.String</span></span>

## <span data-ttu-id="9f6ff-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f6ff-139">OUTPUTS</span></span>

### <span data-ttu-id="9f6ff-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="9f6ff-140">System.Object</span></span>

## <span data-ttu-id="9f6ff-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f6ff-141">NOTES</span></span>

## <span data-ttu-id="9f6ff-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f6ff-142">RELATED LINKS</span></span>

[<span data-ttu-id="9f6ff-143">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9f6ff-143">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="9f6ff-144">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9f6ff-144">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="9f6ff-145">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9f6ff-145">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="9f6ff-146">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9f6ff-146">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
