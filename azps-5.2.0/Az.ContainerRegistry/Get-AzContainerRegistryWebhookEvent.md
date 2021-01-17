---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhookevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhookEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhookEvent.md
ms.openlocfilehash: 6dacce96cf01441dfef5be6d54008b4fc41822d5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414231"
---
# <span data-ttu-id="c741e-101">Get-AzContainerRegistryWebhookEvent</span><span class="sxs-lookup"><span data-stu-id="c741e-101">Get-AzContainerRegistryWebhookEvent</span></span>

## <span data-ttu-id="c741e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c741e-102">SYNOPSIS</span></span>
<span data-ttu-id="c741e-103">Возвращает события веб-приложения реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="c741e-103">Gets events of a container registry webhook.</span></span>

## <span data-ttu-id="c741e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c741e-104">SYNTAX</span></span>

### <span data-ttu-id="c741e-105">ListWebhookEventsByNameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c741e-105">ListWebhookEventsByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhookEvent [-WebhookName] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c741e-106">ListWebhookEventsByWebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c741e-106">ListWebhookEventsByWebhookObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhookEvent -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c741e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c741e-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhookEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c741e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c741e-108">DESCRIPTION</span></span>
<span data-ttu-id="c741e-109">В Get-AzContainerRegistryWebhookEvent будет перечислены все события веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="c741e-109">The Get-AzContainerRegistryWebhookEvent cmdlet lists all the events of a webhook.</span></span>

## <span data-ttu-id="c741e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c741e-110">EXAMPLES</span></span>

### <span data-ttu-id="c741e-111">Пример 1. Возвращает все события веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="c741e-111">Example 1: Gets all the events of a webhook.</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhookEvent -ResourceGroupName mattacrtest001 -RegistryName premium001 -Name webhook001

   Webhook service Uri: http://www.bing.com/

ID                                       Action   Timestamp                      Response
                                                                                 StatusCode
--                                       ------   ---------                      ----------
3c6281b6-47cd-4129-948b-4036780236f0     ping     11/17/2017 5:10:09 PM          200
70f1d41d-15fe-4251-87b6-43c32a91eae7     ping     11/17/2017 6:56:23 AM          200
5d25556b-32d0-4377-8031-d8ba7a263d6a     ping     11/17/2017 6:27:41 AM          200
c1e7d8aa-9f1b-447c-9583-2a58b7f81026     ping     11/17/2017 12:09:41 AM         200
eb4aa503-0d14-4f25-8ae5-33cce9a8fd50     ping     11/16/2017 11:35:03 PM         200
85a93d7f-3923-4ec5-bb8e-9ded5b6549c1     ping     11/17/2017 5:10:09 PM          200
9e3c8b5f-e0ee-47cf-9727-df1c8d45a497     ping     11/17/2017 6:56:23 AM          200
2d0ce294-9b59-4f5c-953a-47f2b270526f     ping     11/17/2017 6:27:41 AM          200
```

<span data-ttu-id="c741e-112">Возвращает все события веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="c741e-112">Gets all the events of a webhook.</span></span>

## <span data-ttu-id="c741e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c741e-113">PARAMETERS</span></span>

### <span data-ttu-id="c741e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c741e-114">-DefaultProfile</span></span>
<span data-ttu-id="c741e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c741e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c741e-116">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="c741e-116">-RegistryName</span></span>
<span data-ttu-id="c741e-117">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="c741e-117">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c741e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c741e-118">-ResourceGroupName</span></span>
<span data-ttu-id="c741e-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c741e-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c741e-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c741e-120">-ResourceId</span></span>
<span data-ttu-id="c741e-121">ИД ресурса Webhook реестра контейнеров</span><span class="sxs-lookup"><span data-stu-id="c741e-121">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="c741e-122">-Webhook</span><span class="sxs-lookup"><span data-stu-id="c741e-122">-Webhook</span></span>
<span data-ttu-id="c741e-123">Объект Container Registry.</span><span class="sxs-lookup"><span data-stu-id="c741e-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook
Parameter Sets: ListWebhookEventsByWebhookObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c741e-124">-WebhookName</span><span class="sxs-lookup"><span data-stu-id="c741e-124">-WebhookName</span></span>
<span data-ttu-id="c741e-125">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="c741e-125">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c741e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c741e-126">CommonParameters</span></span>
<span data-ttu-id="c741e-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c741e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c741e-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c741e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c741e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c741e-129">INPUTS</span></span>

### <span data-ttu-id="c741e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c741e-130">System.String</span></span>

## <span data-ttu-id="c741e-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c741e-131">OUTPUTS</span></span>

### <span data-ttu-id="c741e-132">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhookEvent</span><span class="sxs-lookup"><span data-stu-id="c741e-132">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhookEvent</span></span>

## <span data-ttu-id="c741e-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c741e-133">NOTES</span></span>

## <span data-ttu-id="c741e-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c741e-134">RELATED LINKS</span></span>

[<span data-ttu-id="c741e-135">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c741e-135">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="c741e-136">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c741e-136">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="c741e-137">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c741e-137">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="c741e-138">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c741e-138">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="c741e-139">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c741e-139">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

