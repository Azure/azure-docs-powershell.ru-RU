---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: 588402480cbd626a747208705ec59fd10c572075
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904417"
---
# <span data-ttu-id="ff8e9-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ff8e9-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="ff8e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff8e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ff8e9-103">Обновляет состояние подключения к частной конечной точке в службе частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="ff8e9-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="ff8e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff8e9-104">SYNTAX</span></span>

```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff8e9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff8e9-105">DESCRIPTION</span></span>
<span data-ttu-id="ff8e9-106">Командлет **Set-AzPrivateEndpointConnection** обновляет состояние подключения к частной конечной точке в службе частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="ff8e9-106">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="ff8e9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff8e9-107">EXAMPLES</span></span>

### <span data-ttu-id="ff8e9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ff8e9-108">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="ff8e9-109">В этом примере обновляется состояние подключения закрытой конечной точки для утверждения.</span><span class="sxs-lookup"><span data-stu-id="ff8e9-109">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="ff8e9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff8e9-110">PARAMETERS</span></span>

### <span data-ttu-id="ff8e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff8e9-111">-DefaultProfile</span></span>
<span data-ttu-id="ff8e9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff8e9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff8e9-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="ff8e9-113">-Description</span></span>
<span data-ttu-id="ff8e9-114">Причина действия.</span><span class="sxs-lookup"><span data-stu-id="ff8e9-114">The reason of action.</span></span>

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

### <span data-ttu-id="ff8e9-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ff8e9-115">-Name</span></span>
<span data-ttu-id="ff8e9-116">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="ff8e9-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff8e9-117">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="ff8e9-117">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="ff8e9-118">Утверждение или отклонение ресурса.</span><span class="sxs-lookup"><span data-stu-id="ff8e9-118">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="ff8e9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff8e9-119">-ResourceGroupName</span></span>
<span data-ttu-id="ff8e9-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ff8e9-120">The resource group name.</span></span>

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

### <span data-ttu-id="ff8e9-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ff8e9-121">-ServiceName</span></span>
<span data-ttu-id="ff8e9-122">Имя службы частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="ff8e9-122">The private link service name.</span></span>

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

### <span data-ttu-id="ff8e9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff8e9-123">CommonParameters</span></span>
<span data-ttu-id="ff8e9-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff8e9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff8e9-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff8e9-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff8e9-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff8e9-126">INPUTS</span></span>

### <span data-ttu-id="ff8e9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ff8e9-127">System.String</span></span>

## <span data-ttu-id="ff8e9-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff8e9-128">OUTPUTS</span></span>

### <span data-ttu-id="ff8e9-129">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ff8e9-129">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="ff8e9-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff8e9-130">NOTES</span></span>

## <span data-ttu-id="ff8e9-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff8e9-131">RELATED LINKS</span></span>
