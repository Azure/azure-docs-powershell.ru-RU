---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 1522e8d9c66ccd2429ab331e1f39d26c06da5930
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978408"
---
# <span data-ttu-id="2438e-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2438e-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="2438e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2438e-102">SYNOPSIS</span></span>
<span data-ttu-id="2438e-103">не имеет подключения к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2438e-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="2438e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2438e-104">SYNTAX</span></span>

### <span data-ttu-id="2438e-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2438e-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2438e-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="2438e-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
[-PrivateLinkResourceType <string>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2438e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2438e-107">DESCRIPTION</span></span>
<span data-ttu-id="2438e-108">Проектлет **Deny-AzPrivateEndpointConnection** отрицает подключение к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2438e-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="2438e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2438e-109">EXAMPLES</span></span>

### <span data-ttu-id="2438e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2438e-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="2438e-111">В этом примере соединение закрытой конечной точки не заказано.</span><span class="sxs-lookup"><span data-stu-id="2438e-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="2438e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2438e-112">PARAMETERS</span></span>

### <span data-ttu-id="2438e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2438e-113">-DefaultProfile</span></span>
<span data-ttu-id="2438e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2438e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2438e-115">-Description</span><span class="sxs-lookup"><span data-stu-id="2438e-115">-Description</span></span>
<span data-ttu-id="2438e-116">Причина действия.</span><span class="sxs-lookup"><span data-stu-id="2438e-116">The reason of action.</span></span>

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

### <span data-ttu-id="2438e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2438e-117">-Name</span></span>
<span data-ttu-id="2438e-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="2438e-118">The resource name.</span></span>

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

### <span data-ttu-id="2438e-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="2438e-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="2438e-120">Тип ресурса private link.</span><span class="sxs-lookup"><span data-stu-id="2438e-120">The private link resource type.</span></span>

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

### <span data-ttu-id="2438e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2438e-121">-ResourceGroupName</span></span>
<span data-ttu-id="2438e-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2438e-122">The resource group name.</span></span>

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

### <span data-ttu-id="2438e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2438e-123">-ResourceId</span></span>
<span data-ttu-id="2438e-124">ИД диспетчера ресурсов Azure для подключения к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2438e-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="2438e-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2438e-125">-ServiceName</span></span>
<span data-ttu-id="2438e-126">Имя службы, к которую относится частное подключение к конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2438e-126">The name of service that private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="2438e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2438e-127">CommonParameters</span></span>
<span data-ttu-id="2438e-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2438e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2438e-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2438e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2438e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2438e-130">INPUTS</span></span>

### <span data-ttu-id="2438e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="2438e-131">System.String</span></span>

## <span data-ttu-id="2438e-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2438e-132">OUTPUTS</span></span>

### <span data-ttu-id="2438e-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2438e-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="2438e-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2438e-134">NOTES</span></span>

## <span data-ttu-id="2438e-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2438e-135">RELATED LINKS</span></span>

[<span data-ttu-id="2438e-136">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2438e-136">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="2438e-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2438e-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="2438e-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2438e-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="2438e-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2438e-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)