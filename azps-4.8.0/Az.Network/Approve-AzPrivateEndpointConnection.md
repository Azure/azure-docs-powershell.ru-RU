---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 8fe3058b122c88448403293ad4f109aa5d62b23f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244406"
---
# <span data-ttu-id="2e9b3-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2e9b3-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="2e9b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2e9b3-102">SYNOPSIS</span></span>
<span data-ttu-id="2e9b3-103">Утверждает подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2e9b3-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="2e9b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2e9b3-104">SYNTAX</span></span>

### <span data-ttu-id="2e9b3-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2e9b3-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e9b3-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="2e9b3-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e9b3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e9b3-107">DESCRIPTION</span></span>
<span data-ttu-id="2e9b3-108">Командлет **reодобряет-AzPrivateEndpointConnection** утверждает подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2e9b3-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="2e9b3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2e9b3-109">EXAMPLES</span></span>

### <span data-ttu-id="2e9b3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2e9b3-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="2e9b3-111">В этом примере утверждается подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2e9b3-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="2e9b3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2e9b3-112">PARAMETERS</span></span>

### <span data-ttu-id="2e9b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e9b3-113">-DefaultProfile</span></span>
<span data-ttu-id="2e9b3-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2e9b3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e9b3-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="2e9b3-115">-Description</span></span>
<span data-ttu-id="2e9b3-116">Причина действия.</span><span class="sxs-lookup"><span data-stu-id="2e9b3-116">The reason of action.</span></span>

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

### <span data-ttu-id="2e9b3-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2e9b3-117">-Name</span></span>
<span data-ttu-id="2e9b3-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="2e9b3-118">The resource name.</span></span>

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

### <span data-ttu-id="2e9b3-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="2e9b3-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="2e9b3-120">Тип ресурса «частная ссылка».</span><span class="sxs-lookup"><span data-stu-id="2e9b3-120">The private link resource type.</span></span>

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

### <span data-ttu-id="2e9b3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e9b3-121">-ResourceGroupName</span></span>
<span data-ttu-id="2e9b3-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2e9b3-122">The resource group name.</span></span>

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

### <span data-ttu-id="2e9b3-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e9b3-123">-ResourceId</span></span>
<span data-ttu-id="2e9b3-124">Идентификатор диспетчера ресурсов Azure для подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2e9b3-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="2e9b3-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2e9b3-125">-ServiceName</span></span>
<span data-ttu-id="2e9b3-126">Имя службы частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="2e9b3-126">The private link service name.</span></span>

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


### <span data-ttu-id="2e9b3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e9b3-127">CommonParameters</span></span>
<span data-ttu-id="2e9b3-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2e9b3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e9b3-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e9b3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e9b3-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2e9b3-130">INPUTS</span></span>

### <span data-ttu-id="2e9b3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2e9b3-131">System.String</span></span>

## <span data-ttu-id="2e9b3-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e9b3-132">OUTPUTS</span></span>

### <span data-ttu-id="2e9b3-133">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2e9b3-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="2e9b3-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="2e9b3-134">NOTES</span></span>

## <span data-ttu-id="2e9b3-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e9b3-135">RELATED LINKS</span></span>

[<span data-ttu-id="2e9b3-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2e9b3-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="2e9b3-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2e9b3-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="2e9b3-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2e9b3-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="2e9b3-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2e9b3-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)