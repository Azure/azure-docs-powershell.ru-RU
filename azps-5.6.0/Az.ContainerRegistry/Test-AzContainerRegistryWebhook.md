---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 837e0fa40bc07ce5c38d6dfd4b7c86efe2425be9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956328"
---
# <span data-ttu-id="c89d1-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c89d1-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="c89d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c89d1-102">SYNOPSIS</span></span>
<span data-ttu-id="c89d1-103">Вызывает событие ping webhook.</span><span class="sxs-lookup"><span data-stu-id="c89d1-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="c89d1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c89d1-104">SYNTAX</span></span>

### <span data-ttu-id="c89d1-105">ResourceIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c89d1-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c89d1-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="c89d1-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c89d1-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c89d1-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c89d1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c89d1-108">DESCRIPTION</span></span>
<span data-ttu-id="c89d1-109">Этот Test-AzContainerRegistryWebhook вызывает событие ping webhook.</span><span class="sxs-lookup"><span data-stu-id="c89d1-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="c89d1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c89d1-110">EXAMPLES</span></span>

### <span data-ttu-id="c89d1-111">Пример 1. Вызывает событие ping webhook.</span><span class="sxs-lookup"><span data-stu-id="c89d1-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="c89d1-112">Вызывает событие ping webhook.</span><span class="sxs-lookup"><span data-stu-id="c89d1-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="c89d1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c89d1-113">PARAMETERS</span></span>

### <span data-ttu-id="c89d1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c89d1-114">-DefaultProfile</span></span>
<span data-ttu-id="c89d1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c89d1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c89d1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c89d1-116">-Name</span></span>
<span data-ttu-id="c89d1-117">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="c89d1-117">Webhook Name.</span></span>

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

### <span data-ttu-id="c89d1-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="c89d1-118">-RegistryName</span></span>
<span data-ttu-id="c89d1-119">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="c89d1-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="c89d1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c89d1-120">-ResourceGroupName</span></span>
<span data-ttu-id="c89d1-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c89d1-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="c89d1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c89d1-122">-ResourceId</span></span>
<span data-ttu-id="c89d1-123">ИД ресурса Webhook реестра контейнеров</span><span class="sxs-lookup"><span data-stu-id="c89d1-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="c89d1-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="c89d1-124">-Webhook</span></span>
<span data-ttu-id="c89d1-125">Объект Container Registry.</span><span class="sxs-lookup"><span data-stu-id="c89d1-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="c89d1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c89d1-126">CommonParameters</span></span>
<span data-ttu-id="c89d1-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c89d1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c89d1-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c89d1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c89d1-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c89d1-129">INPUTS</span></span>

### <span data-ttu-id="c89d1-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c89d1-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="c89d1-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c89d1-131">System.String</span></span>

## <span data-ttu-id="c89d1-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c89d1-132">OUTPUTS</span></span>

### <span data-ttu-id="c89d1-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="c89d1-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="c89d1-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c89d1-134">NOTES</span></span>

## <span data-ttu-id="c89d1-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c89d1-135">RELATED LINKS</span></span>

[<span data-ttu-id="c89d1-136">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c89d1-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="c89d1-137">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c89d1-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="c89d1-138">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c89d1-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="c89d1-139">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c89d1-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)