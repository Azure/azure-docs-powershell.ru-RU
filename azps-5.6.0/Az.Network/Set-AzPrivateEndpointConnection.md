---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: 7684072abbef4af8344cc07aa4bef6cab88ad3ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979480"
---
# <span data-ttu-id="acd31-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="acd31-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="acd31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acd31-102">SYNOPSIS</span></span>
<span data-ttu-id="acd31-103">Обновляет состояние подключения частной конечной точки в службе частных ссылок.</span><span class="sxs-lookup"><span data-stu-id="acd31-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="acd31-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="acd31-104">SYNTAX</span></span>

### <span data-ttu-id="acd31-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="acd31-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acd31-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="acd31-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acd31-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="acd31-107">DESCRIPTION</span></span>
<span data-ttu-id="acd31-108">**Cmdlet Set-AzPrivateEndpointConnection** обновляет состояние подключения частной конечной точки в частной службе связывания</span><span class="sxs-lookup"><span data-stu-id="acd31-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="acd31-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="acd31-109">EXAMPLES</span></span>

### <span data-ttu-id="acd31-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="acd31-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="acd31-111">В этом примере состояние подключения частной конечной точки обновляется на "Утверждено".</span><span class="sxs-lookup"><span data-stu-id="acd31-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="acd31-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acd31-112">PARAMETERS</span></span>

### <span data-ttu-id="acd31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acd31-113">-DefaultProfile</span></span>
<span data-ttu-id="acd31-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="acd31-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acd31-115">-Description</span><span class="sxs-lookup"><span data-stu-id="acd31-115">-Description</span></span>
<span data-ttu-id="acd31-116">Причина действия.</span><span class="sxs-lookup"><span data-stu-id="acd31-116">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd31-117">-Name</span><span class="sxs-lookup"><span data-stu-id="acd31-117">-Name</span></span>
<span data-ttu-id="acd31-118">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="acd31-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd31-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="acd31-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="acd31-120">Тип ресурса private link.</span><span class="sxs-lookup"><span data-stu-id="acd31-120">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd31-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="acd31-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="acd31-122">Утвержден или отклонен ресурс.</span><span class="sxs-lookup"><span data-stu-id="acd31-122">Approved or rejected the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd31-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acd31-123">-ResourceGroupName</span></span>
<span data-ttu-id="acd31-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="acd31-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd31-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acd31-125">-ResourceId</span></span>
<span data-ttu-id="acd31-126">ИД диспетчера ресурсов Azure для подключения к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="acd31-126">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd31-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="acd31-127">-ServiceName</span></span>
<span data-ttu-id="acd31-128">Имя службы личной ссылки.</span><span class="sxs-lookup"><span data-stu-id="acd31-128">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd31-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd31-129">CommonParameters</span></span>
<span data-ttu-id="acd31-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acd31-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd31-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="acd31-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd31-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="acd31-132">INPUTS</span></span>

### <span data-ttu-id="acd31-133">System.String</span><span class="sxs-lookup"><span data-stu-id="acd31-133">System.String</span></span>

## <span data-ttu-id="acd31-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="acd31-134">OUTPUTS</span></span>

### <span data-ttu-id="acd31-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="acd31-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="acd31-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="acd31-136">NOTES</span></span>

## <span data-ttu-id="acd31-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="acd31-137">RELATED LINKS</span></span>

[<span data-ttu-id="acd31-138">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="acd31-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="acd31-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="acd31-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="acd31-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="acd31-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="acd31-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="acd31-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)