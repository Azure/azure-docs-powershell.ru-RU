---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400572"
---
# <span data-ttu-id="4dddd-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4dddd-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="4dddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dddd-102">SYNOPSIS</span></span>
<span data-ttu-id="4dddd-103">Обновляет состояние подключения частной конечной точки в службе частных ссылок.</span><span class="sxs-lookup"><span data-stu-id="4dddd-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="4dddd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4dddd-104">SYNTAX</span></span>

### <span data-ttu-id="4dddd-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4dddd-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4dddd-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="4dddd-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dddd-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4dddd-107">DESCRIPTION</span></span>
<span data-ttu-id="4dddd-108">**Cmdlet Set-AzPrivateEndpointConnection** обновляет состояние подключения частной конечной точки в частной службе связывания.</span><span class="sxs-lookup"><span data-stu-id="4dddd-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="4dddd-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4dddd-109">EXAMPLES</span></span>

### <span data-ttu-id="4dddd-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4dddd-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="4dddd-111">В этом примере состояние подключения частной конечной точки обновляется на "Утверждено".</span><span class="sxs-lookup"><span data-stu-id="4dddd-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="4dddd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4dddd-112">PARAMETERS</span></span>

### <span data-ttu-id="4dddd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dddd-113">-DefaultProfile</span></span>
<span data-ttu-id="4dddd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4dddd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dddd-115">-Description</span><span class="sxs-lookup"><span data-stu-id="4dddd-115">-Description</span></span>
<span data-ttu-id="4dddd-116">Причина действия.</span><span class="sxs-lookup"><span data-stu-id="4dddd-116">The reason of action.</span></span>

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

### <span data-ttu-id="4dddd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4dddd-117">-Name</span></span>
<span data-ttu-id="4dddd-118">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="4dddd-118">The resource name.</span></span>

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

### <span data-ttu-id="4dddd-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="4dddd-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="4dddd-120">Тип ресурса private link.</span><span class="sxs-lookup"><span data-stu-id="4dddd-120">The private link resource type.</span></span>

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

### <span data-ttu-id="4dddd-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="4dddd-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="4dddd-122">Утвержден или отклонен ресурс.</span><span class="sxs-lookup"><span data-stu-id="4dddd-122">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="4dddd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dddd-123">-ResourceGroupName</span></span>
<span data-ttu-id="4dddd-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4dddd-124">The resource group name.</span></span>

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

### <span data-ttu-id="4dddd-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4dddd-125">-ResourceId</span></span>
<span data-ttu-id="4dddd-126">ИД диспетчера ресурсов Azure для подключения к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="4dddd-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="4dddd-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4dddd-127">-ServiceName</span></span>
<span data-ttu-id="4dddd-128">Имя службы личной ссылки.</span><span class="sxs-lookup"><span data-stu-id="4dddd-128">The private link service name.</span></span>

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

### <span data-ttu-id="4dddd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dddd-129">CommonParameters</span></span>
<span data-ttu-id="4dddd-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dddd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dddd-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4dddd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dddd-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4dddd-132">INPUTS</span></span>

### <span data-ttu-id="4dddd-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4dddd-133">System.String</span></span>

## <span data-ttu-id="4dddd-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4dddd-134">OUTPUTS</span></span>

### <span data-ttu-id="4dddd-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4dddd-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="4dddd-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4dddd-136">NOTES</span></span>

## <span data-ttu-id="4dddd-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4dddd-137">RELATED LINKS</span></span>

[<span data-ttu-id="4dddd-138">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4dddd-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="4dddd-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4dddd-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="4dddd-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4dddd-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="4dddd-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4dddd-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)