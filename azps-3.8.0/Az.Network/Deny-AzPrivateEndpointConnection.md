---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 159b320b24ff1e9ab1b4c71e6c374931ecfeffdd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073587"
---
# <span data-ttu-id="9ac6c-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9ac6c-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="9ac6c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ac6c-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac6c-103">отклоняет подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="9ac6c-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="9ac6c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ac6c-104">SYNTAX</span></span>

### <span data-ttu-id="9ac6c-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ac6c-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ac6c-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="9ac6c-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
[-PrivateLinkResourceType <string>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ac6c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ac6c-107">DESCRIPTION</span></span>
<span data-ttu-id="9ac6c-108">Командлет **Deny-AzPrivateEndpointConnection** запрещает подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="9ac6c-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="9ac6c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ac6c-109">EXAMPLES</span></span>

### <span data-ttu-id="9ac6c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9ac6c-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="9ac6c-111">В этом примере отклоняется подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="9ac6c-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="9ac6c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ac6c-112">PARAMETERS</span></span>

### <span data-ttu-id="9ac6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac6c-113">-DefaultProfile</span></span>
<span data-ttu-id="9ac6c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ac6c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ac6c-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="9ac6c-115">-Description</span></span>
<span data-ttu-id="9ac6c-116">Причина действия.</span><span class="sxs-lookup"><span data-stu-id="9ac6c-116">The reason of action.</span></span>

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

### <span data-ttu-id="9ac6c-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9ac6c-117">-Name</span></span>
<span data-ttu-id="9ac6c-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="9ac6c-118">The resource name.</span></span>

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

### <span data-ttu-id="9ac6c-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="9ac6c-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="9ac6c-120">Тип ресурса «частная ссылка».</span><span class="sxs-lookup"><span data-stu-id="9ac6c-120">The private link resource type.</span></span>

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

### <span data-ttu-id="9ac6c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ac6c-121">-ResourceGroupName</span></span>
<span data-ttu-id="9ac6c-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ac6c-122">The resource group name.</span></span>

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

### <span data-ttu-id="9ac6c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ac6c-123">-ResourceId</span></span>
<span data-ttu-id="9ac6c-124">Идентификатор диспетчера ресурсов Azure для подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="9ac6c-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="9ac6c-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9ac6c-125">-ServiceName</span></span>
<span data-ttu-id="9ac6c-126">Имя службы, к которой принадлежит подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="9ac6c-126">The name of service that private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="9ac6c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac6c-127">CommonParameters</span></span>
<span data-ttu-id="9ac6c-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ac6c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac6c-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ac6c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac6c-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ac6c-130">INPUTS</span></span>

### <span data-ttu-id="9ac6c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9ac6c-131">System.String</span></span>

## <span data-ttu-id="9ac6c-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ac6c-132">OUTPUTS</span></span>

### <span data-ttu-id="9ac6c-133">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="9ac6c-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="9ac6c-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ac6c-134">NOTES</span></span>

## <span data-ttu-id="9ac6c-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ac6c-135">RELATED LINKS</span></span>

[<span data-ttu-id="9ac6c-136">Утвердить — AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9ac6c-136">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9ac6c-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9ac6c-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9ac6c-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9ac6c-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9ac6c-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9ac6c-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)