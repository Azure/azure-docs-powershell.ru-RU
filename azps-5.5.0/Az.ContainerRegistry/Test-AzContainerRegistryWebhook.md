---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 1245c92e13af691b0b439d6745a35a917bdf4d89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243941"
---
# <span data-ttu-id="838d7-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="838d7-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="838d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="838d7-102">SYNOPSIS</span></span>
<span data-ttu-id="838d7-103">Вызывает событие ping webhook.</span><span class="sxs-lookup"><span data-stu-id="838d7-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="838d7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="838d7-104">SYNTAX</span></span>

### <span data-ttu-id="838d7-105">ResourceIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="838d7-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="838d7-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="838d7-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="838d7-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="838d7-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="838d7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="838d7-108">DESCRIPTION</span></span>
<span data-ttu-id="838d7-109">Этот Test-AzContainerRegistryWebhook вызывает событие ping webhook.</span><span class="sxs-lookup"><span data-stu-id="838d7-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="838d7-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="838d7-110">EXAMPLES</span></span>

### <span data-ttu-id="838d7-111">Пример 1. Вызывает событие ping webhook.</span><span class="sxs-lookup"><span data-stu-id="838d7-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="838d7-112">Вызывает событие ping webhook.</span><span class="sxs-lookup"><span data-stu-id="838d7-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="838d7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="838d7-113">PARAMETERS</span></span>

### <span data-ttu-id="838d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="838d7-114">-DefaultProfile</span></span>
<span data-ttu-id="838d7-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="838d7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="838d7-116">-Name</span><span class="sxs-lookup"><span data-stu-id="838d7-116">-Name</span></span>
<span data-ttu-id="838d7-117">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="838d7-117">Webhook Name.</span></span>

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

### <span data-ttu-id="838d7-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="838d7-118">-RegistryName</span></span>
<span data-ttu-id="838d7-119">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="838d7-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="838d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="838d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="838d7-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="838d7-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="838d7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="838d7-122">-ResourceId</span></span>
<span data-ttu-id="838d7-123">ИД ресурса Webhook реестра контейнеров</span><span class="sxs-lookup"><span data-stu-id="838d7-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="838d7-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="838d7-124">-Webhook</span></span>
<span data-ttu-id="838d7-125">Объект Container Registry.</span><span class="sxs-lookup"><span data-stu-id="838d7-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="838d7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="838d7-126">CommonParameters</span></span>
<span data-ttu-id="838d7-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="838d7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="838d7-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="838d7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="838d7-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="838d7-129">INPUTS</span></span>

### <span data-ttu-id="838d7-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="838d7-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="838d7-131">System.String</span><span class="sxs-lookup"><span data-stu-id="838d7-131">System.String</span></span>

## <span data-ttu-id="838d7-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="838d7-132">OUTPUTS</span></span>

### <span data-ttu-id="838d7-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="838d7-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="838d7-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="838d7-134">NOTES</span></span>

## <span data-ttu-id="838d7-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="838d7-135">RELATED LINKS</span></span>

[<span data-ttu-id="838d7-136">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="838d7-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="838d7-137">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="838d7-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="838d7-138">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="838d7-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="838d7-139">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="838d7-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)