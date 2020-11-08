---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073095"
---
# <span data-ttu-id="d2153-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d2153-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="d2153-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2153-102">SYNOPSIS</span></span>
<span data-ttu-id="d2153-103">Обновляет состояние подключения к частной конечной точке в службе частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="d2153-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="d2153-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2153-104">SYNTAX</span></span>

### <span data-ttu-id="d2153-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2153-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2153-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="d2153-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2153-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2153-107">DESCRIPTION</span></span>
<span data-ttu-id="d2153-108">Командлет **Set-AzPrivateEndpointConnection** обновляет состояние подключения к частной конечной точке в службе частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="d2153-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="d2153-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2153-109">EXAMPLES</span></span>

### <span data-ttu-id="d2153-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d2153-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="d2153-111">В этом примере обновляется состояние подключения закрытой конечной точки для утверждения.</span><span class="sxs-lookup"><span data-stu-id="d2153-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="d2153-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2153-112">PARAMETERS</span></span>

### <span data-ttu-id="d2153-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2153-113">-DefaultProfile</span></span>
<span data-ttu-id="d2153-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2153-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2153-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="d2153-115">-Description</span></span>
<span data-ttu-id="d2153-116">Причина действия.</span><span class="sxs-lookup"><span data-stu-id="d2153-116">The reason of action.</span></span>

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

### <span data-ttu-id="d2153-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d2153-117">-Name</span></span>
<span data-ttu-id="d2153-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2153-118">The resource name.</span></span>

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

### <span data-ttu-id="d2153-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="d2153-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="d2153-120">Тип ресурса «частная ссылка».</span><span class="sxs-lookup"><span data-stu-id="d2153-120">The private link resource type.</span></span>

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

### <span data-ttu-id="d2153-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="d2153-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="d2153-122">Утверждение или отклонение ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2153-122">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="d2153-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2153-123">-ResourceGroupName</span></span>
<span data-ttu-id="d2153-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2153-124">The resource group name.</span></span>

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

### <span data-ttu-id="d2153-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2153-125">-ResourceId</span></span>
<span data-ttu-id="d2153-126">Идентификатор диспетчера ресурсов Azure для подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="d2153-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="d2153-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d2153-127">-ServiceName</span></span>
<span data-ttu-id="d2153-128">Имя службы частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="d2153-128">The private link service name.</span></span>

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

### <span data-ttu-id="d2153-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2153-129">CommonParameters</span></span>
<span data-ttu-id="d2153-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2153-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2153-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2153-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2153-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2153-132">INPUTS</span></span>

### <span data-ttu-id="d2153-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d2153-133">System.String</span></span>

## <span data-ttu-id="d2153-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2153-134">OUTPUTS</span></span>

### <span data-ttu-id="d2153-135">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d2153-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="d2153-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2153-136">NOTES</span></span>

## <span data-ttu-id="d2153-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2153-137">RELATED LINKS</span></span>

[<span data-ttu-id="d2153-138">Утвердить — AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d2153-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="d2153-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d2153-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="d2153-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d2153-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="d2153-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d2153-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)