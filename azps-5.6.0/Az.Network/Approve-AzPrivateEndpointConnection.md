---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 3768bc8769d81056dc8f2de4f42f9f1783f89728
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979640"
---
# <span data-ttu-id="8d892-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d892-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="8d892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d892-102">SYNOPSIS</span></span>
<span data-ttu-id="8d892-103">Утверждает подключение к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="8d892-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="8d892-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8d892-104">SYNTAX</span></span>

### <span data-ttu-id="8d892-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8d892-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d892-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="8d892-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d892-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d892-107">DESCRIPTION</span></span>
<span data-ttu-id="8d892-108">**Cmdlet Approve-AzPrivateEndpointConnection** утверждает подключение к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="8d892-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="8d892-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8d892-109">EXAMPLES</span></span>

### <span data-ttu-id="8d892-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8d892-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="8d892-111">В этом примере утверждается подключение к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="8d892-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="8d892-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d892-112">PARAMETERS</span></span>

### <span data-ttu-id="8d892-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d892-113">-DefaultProfile</span></span>
<span data-ttu-id="8d892-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d892-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d892-115">-Description</span><span class="sxs-lookup"><span data-stu-id="8d892-115">-Description</span></span>
<span data-ttu-id="8d892-116">Причина действия.</span><span class="sxs-lookup"><span data-stu-id="8d892-116">The reason of action.</span></span>

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

### <span data-ttu-id="8d892-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8d892-117">-Name</span></span>
<span data-ttu-id="8d892-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="8d892-118">The resource name.</span></span>

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

### <span data-ttu-id="8d892-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="8d892-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="8d892-120">Тип ресурса private link.</span><span class="sxs-lookup"><span data-stu-id="8d892-120">The private link resource type.</span></span>

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

### <span data-ttu-id="8d892-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d892-121">-ResourceGroupName</span></span>
<span data-ttu-id="8d892-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8d892-122">The resource group name.</span></span>

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

### <span data-ttu-id="8d892-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d892-123">-ResourceId</span></span>
<span data-ttu-id="8d892-124">ИД диспетчера ресурсов Azure для подключения к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="8d892-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="8d892-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8d892-125">-ServiceName</span></span>
<span data-ttu-id="8d892-126">Имя службы личной ссылки.</span><span class="sxs-lookup"><span data-stu-id="8d892-126">The private link service name.</span></span>

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


### <span data-ttu-id="8d892-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d892-127">CommonParameters</span></span>
<span data-ttu-id="8d892-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d892-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d892-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d892-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d892-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d892-130">INPUTS</span></span>

### <span data-ttu-id="8d892-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8d892-131">System.String</span></span>

## <span data-ttu-id="8d892-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8d892-132">OUTPUTS</span></span>

### <span data-ttu-id="8d892-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8d892-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="8d892-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8d892-134">NOTES</span></span>

## <span data-ttu-id="8d892-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d892-135">RELATED LINKS</span></span>

[<span data-ttu-id="8d892-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d892-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="8d892-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d892-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="8d892-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d892-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="8d892-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d892-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)