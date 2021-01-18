---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517930"
---
# <span data-ttu-id="8e874-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8e874-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="8e874-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e874-102">SYNOPSIS</span></span>
<span data-ttu-id="8e874-103">Обновляет состояние подключения частной конечной точки в службе частных ссылок.</span><span class="sxs-lookup"><span data-stu-id="8e874-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="8e874-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8e874-104">SYNTAX</span></span>

### <span data-ttu-id="8e874-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e874-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e874-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="8e874-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e874-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e874-107">DESCRIPTION</span></span>
<span data-ttu-id="8e874-108">**Cmdlet Set-AzPrivateEndpointConnection** обновляет состояние подключения частной конечной точки в частной службе связывания.</span><span class="sxs-lookup"><span data-stu-id="8e874-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="8e874-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8e874-109">EXAMPLES</span></span>

### <span data-ttu-id="8e874-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8e874-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="8e874-111">В этом примере состояние подключения частной конечной точки обновляется на "Утверждено".</span><span class="sxs-lookup"><span data-stu-id="8e874-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="8e874-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e874-112">PARAMETERS</span></span>

### <span data-ttu-id="8e874-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e874-113">-DefaultProfile</span></span>
<span data-ttu-id="8e874-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e874-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e874-115">-Description</span><span class="sxs-lookup"><span data-stu-id="8e874-115">-Description</span></span>
<span data-ttu-id="8e874-116">Причина действия.</span><span class="sxs-lookup"><span data-stu-id="8e874-116">The reason of action.</span></span>

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

### <span data-ttu-id="8e874-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8e874-117">-Name</span></span>
<span data-ttu-id="8e874-118">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="8e874-118">The resource name.</span></span>

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

### <span data-ttu-id="8e874-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="8e874-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="8e874-120">Тип ресурса private link.</span><span class="sxs-lookup"><span data-stu-id="8e874-120">The private link resource type.</span></span>

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

### <span data-ttu-id="8e874-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="8e874-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="8e874-122">Утвержден или отклонен ресурс.</span><span class="sxs-lookup"><span data-stu-id="8e874-122">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="8e874-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e874-123">-ResourceGroupName</span></span>
<span data-ttu-id="8e874-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e874-124">The resource group name.</span></span>

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

### <span data-ttu-id="8e874-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e874-125">-ResourceId</span></span>
<span data-ttu-id="8e874-126">ИД диспетчера ресурсов Azure для подключения к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="8e874-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="8e874-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8e874-127">-ServiceName</span></span>
<span data-ttu-id="8e874-128">Имя службы личной ссылки.</span><span class="sxs-lookup"><span data-stu-id="8e874-128">The private link service name.</span></span>

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

### <span data-ttu-id="8e874-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e874-129">CommonParameters</span></span>
<span data-ttu-id="8e874-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e874-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e874-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e874-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e874-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e874-132">INPUTS</span></span>

### <span data-ttu-id="8e874-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8e874-133">System.String</span></span>

## <span data-ttu-id="8e874-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8e874-134">OUTPUTS</span></span>

### <span data-ttu-id="8e874-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8e874-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="8e874-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8e874-136">NOTES</span></span>

## <span data-ttu-id="8e874-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e874-137">RELATED LINKS</span></span>

[<span data-ttu-id="8e874-138">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8e874-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="8e874-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8e874-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="8e874-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8e874-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="8e874-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8e874-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)