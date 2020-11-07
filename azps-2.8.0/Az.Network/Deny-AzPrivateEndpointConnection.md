---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 4a67914fd3709ef972adac8eba6b1b2fa211fbf6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902537"
---
# <span data-ttu-id="2ac62-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2ac62-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="2ac62-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ac62-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac62-103">отклоняет подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2ac62-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="2ac62-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ac62-104">SYNTAX</span></span>

### <span data-ttu-id="2ac62-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2ac62-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ac62-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="2ac62-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ac62-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ac62-107">DESCRIPTION</span></span>
<span data-ttu-id="2ac62-108">Командлет **Deny-AzPrivateEndpointConnection** запрещает подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2ac62-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="2ac62-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ac62-109">EXAMPLES</span></span>

### <span data-ttu-id="2ac62-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2ac62-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="2ac62-111">В этом примере отклоняется подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2ac62-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="2ac62-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ac62-112">PARAMETERS</span></span>

### <span data-ttu-id="2ac62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac62-113">-DefaultProfile</span></span>
<span data-ttu-id="2ac62-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ac62-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ac62-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="2ac62-115">-Description</span></span>
<span data-ttu-id="2ac62-116">Причина действия.</span><span class="sxs-lookup"><span data-stu-id="2ac62-116">The reason of action.</span></span>

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

### <span data-ttu-id="2ac62-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2ac62-117">-Name</span></span>
<span data-ttu-id="2ac62-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="2ac62-118">The resource name.</span></span>

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

### <span data-ttu-id="2ac62-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ac62-119">-ResourceGroupName</span></span>
<span data-ttu-id="2ac62-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2ac62-120">The resource group name.</span></span>

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

### <span data-ttu-id="2ac62-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ac62-121">-ResourceId</span></span>
<span data-ttu-id="2ac62-122">Идентификатор диспетчера ресурсов Azure для подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2ac62-122">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="2ac62-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2ac62-123">-ServiceName</span></span>
<span data-ttu-id="2ac62-124">Имя службы частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="2ac62-124">The private link service name.</span></span>

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

### <span data-ttu-id="2ac62-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac62-125">CommonParameters</span></span>
<span data-ttu-id="2ac62-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ac62-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac62-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ac62-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac62-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ac62-128">INPUTS</span></span>

### <span data-ttu-id="2ac62-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2ac62-129">System.String</span></span>

## <span data-ttu-id="2ac62-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ac62-130">OUTPUTS</span></span>

### <span data-ttu-id="2ac62-131">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2ac62-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="2ac62-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ac62-132">NOTES</span></span>

## <span data-ttu-id="2ac62-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ac62-133">RELATED LINKS</span></span>

[<span data-ttu-id="2ac62-134">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2ac62-134">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="2ac62-135">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2ac62-135">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="2ac62-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2ac62-136">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)