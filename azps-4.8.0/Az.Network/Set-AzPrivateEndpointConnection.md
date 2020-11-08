---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078823"
---
# <span data-ttu-id="45163-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="45163-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="45163-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45163-102">SYNOPSIS</span></span>
<span data-ttu-id="45163-103">Обновляет состояние подключения к частной конечной точке в службе частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="45163-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="45163-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45163-104">SYNTAX</span></span>

### <span data-ttu-id="45163-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45163-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45163-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="45163-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45163-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45163-107">DESCRIPTION</span></span>
<span data-ttu-id="45163-108">Командлет **Set-AzPrivateEndpointConnection** обновляет состояние подключения к частной конечной точке в службе частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="45163-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="45163-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45163-109">EXAMPLES</span></span>

### <span data-ttu-id="45163-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="45163-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="45163-111">В этом примере обновляется состояние подключения закрытой конечной точки для утверждения.</span><span class="sxs-lookup"><span data-stu-id="45163-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="45163-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45163-112">PARAMETERS</span></span>

### <span data-ttu-id="45163-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45163-113">-DefaultProfile</span></span>
<span data-ttu-id="45163-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45163-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45163-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="45163-115">-Description</span></span>
<span data-ttu-id="45163-116">Причина действия.</span><span class="sxs-lookup"><span data-stu-id="45163-116">The reason of action.</span></span>

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

### <span data-ttu-id="45163-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="45163-117">-Name</span></span>
<span data-ttu-id="45163-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="45163-118">The resource name.</span></span>

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

### <span data-ttu-id="45163-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="45163-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="45163-120">Тип ресурса «частная ссылка».</span><span class="sxs-lookup"><span data-stu-id="45163-120">The private link resource type.</span></span>

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

### <span data-ttu-id="45163-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="45163-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="45163-122">Утверждение или отклонение ресурса.</span><span class="sxs-lookup"><span data-stu-id="45163-122">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="45163-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45163-123">-ResourceGroupName</span></span>
<span data-ttu-id="45163-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45163-124">The resource group name.</span></span>

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

### <span data-ttu-id="45163-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45163-125">-ResourceId</span></span>
<span data-ttu-id="45163-126">Идентификатор диспетчера ресурсов Azure для подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="45163-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="45163-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="45163-127">-ServiceName</span></span>
<span data-ttu-id="45163-128">Имя службы частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="45163-128">The private link service name.</span></span>

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

### <span data-ttu-id="45163-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45163-129">CommonParameters</span></span>
<span data-ttu-id="45163-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45163-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45163-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45163-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45163-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45163-132">INPUTS</span></span>

### <span data-ttu-id="45163-133">System. String</span><span class="sxs-lookup"><span data-stu-id="45163-133">System.String</span></span>

## <span data-ttu-id="45163-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45163-134">OUTPUTS</span></span>

### <span data-ttu-id="45163-135">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="45163-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="45163-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="45163-136">NOTES</span></span>

## <span data-ttu-id="45163-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45163-137">RELATED LINKS</span></span>

[<span data-ttu-id="45163-138">Утвердить — AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="45163-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="45163-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="45163-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="45163-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="45163-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="45163-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="45163-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)