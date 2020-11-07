---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 9b47fb1954b13e28268f6b7aad66fa8190e20584
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902545"
---
# <span data-ttu-id="b4058-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b4058-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="b4058-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4058-102">SYNOPSIS</span></span>
<span data-ttu-id="b4058-103">Утверждает подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="b4058-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="b4058-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4058-104">SYNTAX</span></span>

### <span data-ttu-id="b4058-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b4058-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4058-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="b4058-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4058-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4058-107">DESCRIPTION</span></span>
<span data-ttu-id="b4058-108">Командлет **reодобряет-AzPrivateEndpointConnection** утверждает подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="b4058-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="b4058-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4058-109">EXAMPLES</span></span>

### <span data-ttu-id="b4058-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b4058-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="b4058-111">В этом примере утверждается подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="b4058-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="b4058-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4058-112">PARAMETERS</span></span>

### <span data-ttu-id="b4058-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4058-113">-DefaultProfile</span></span>
<span data-ttu-id="b4058-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4058-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4058-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="b4058-115">-Description</span></span>
<span data-ttu-id="b4058-116">Причина действия.</span><span class="sxs-lookup"><span data-stu-id="b4058-116">The reason of action.</span></span>

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

### <span data-ttu-id="b4058-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b4058-117">-Name</span></span>
<span data-ttu-id="b4058-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="b4058-118">The resource name.</span></span>

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

### <span data-ttu-id="b4058-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4058-119">-ResourceGroupName</span></span>
<span data-ttu-id="b4058-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4058-120">The resource group name.</span></span>

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

### <span data-ttu-id="b4058-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4058-121">-ResourceId</span></span>
<span data-ttu-id="b4058-122">Идентификатор диспетчера ресурсов Azure для подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="b4058-122">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="b4058-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b4058-123">-ServiceName</span></span>
<span data-ttu-id="b4058-124">Имя службы частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="b4058-124">The private link service name.</span></span>

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

### <span data-ttu-id="b4058-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4058-125">CommonParameters</span></span>
<span data-ttu-id="b4058-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4058-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4058-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4058-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4058-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4058-128">INPUTS</span></span>

### <span data-ttu-id="b4058-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b4058-129">System.String</span></span>

## <span data-ttu-id="b4058-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4058-130">OUTPUTS</span></span>

### <span data-ttu-id="b4058-131">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b4058-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="b4058-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4058-132">NOTES</span></span>

## <span data-ttu-id="b4058-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4058-133">RELATED LINKS</span></span>

[<span data-ttu-id="b4058-134">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b4058-134">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="b4058-135">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b4058-135">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="b4058-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b4058-136">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)