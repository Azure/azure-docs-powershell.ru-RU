---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceConnection.md
ms.openlocfilehash: 74f531e48ca873d3853aba3312d6bb10edccdfaa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073261"
---
# <span data-ttu-id="63963-101">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="63963-101">New-AzPrivateLinkServiceConnection</span></span>

## <span data-ttu-id="63963-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63963-102">SYNOPSIS</span></span>
<span data-ttu-id="63963-103">Создание конфигурации подключения к службе частной связи.</span><span class="sxs-lookup"><span data-stu-id="63963-103">Creates a private link service connection configuration.</span></span>

## <span data-ttu-id="63963-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63963-104">SYNTAX</span></span>

### <span data-ttu-id="63963-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="63963-105">SetByResource (Default)</span></span>
```
New-AzPrivateLinkServiceConnection -Name <String> -PrivateLinkService <PSPrivateLinkService>
 [-GroupId <String[]>] [-RequestMessage <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="63963-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="63963-106">SetByResourceId</span></span>
```
New-AzPrivateLinkServiceConnection -Name <String> -PrivateLinkServiceId <String> [-GroupId <String[]>]
 [-RequestMessage <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63963-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63963-107">DESCRIPTION</span></span>
<span data-ttu-id="63963-108">Командлет **New-AzPrivateLinkServiceConnection** создает конфигурацию подключения к службе частной связи.</span><span class="sxs-lookup"><span data-stu-id="63963-108">**The New-AzPrivateLinkServiceConnection** cmdlet creates a private link service connection configuration.</span></span>

## <span data-ttu-id="63963-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63963-109">EXAMPLES</span></span>

### <span data-ttu-id="63963-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="63963-110">Example 1</span></span>
```
New-AzPrivateLinkServiceConnection -Name MyPLSConnection -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
```

<span data-ttu-id="63963-111">В этом примере для создания закрытой конечной точки используется объект подключения службы Private Link в памяти.</span><span class="sxs-lookup"><span data-stu-id="63963-111">This example create a private link service connection object in memory for using in creating private endpoint.</span></span>

## <span data-ttu-id="63963-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63963-112">PARAMETERS</span></span>

### <span data-ttu-id="63963-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63963-113">-DefaultProfile</span></span>
<span data-ttu-id="63963-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63963-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63963-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="63963-115">-GroupId</span></span>
<span data-ttu-id="63963-116">Список идентификаторов групп.</span><span class="sxs-lookup"><span data-stu-id="63963-116">The list of group id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63963-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63963-117">-Name</span></span>
<span data-ttu-id="63963-118">Имя службы частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="63963-118">The name of private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63963-119">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="63963-119">-PrivateLinkService</span></span>
<span data-ttu-id="63963-120">Служба частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="63963-120">The private link service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63963-121">-PrivateLinkServiceId</span><span class="sxs-lookup"><span data-stu-id="63963-121">-PrivateLinkServiceId</span></span>
<span data-ttu-id="63963-122">Идентификатор службы частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="63963-122">The id of private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63963-123">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="63963-123">-RequestMessage</span></span>
<span data-ttu-id="63963-124">Сообщение запроса.</span><span class="sxs-lookup"><span data-stu-id="63963-124">The request message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63963-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63963-125">CommonParameters</span></span>
<span data-ttu-id="63963-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63963-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63963-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63963-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63963-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63963-128">INPUTS</span></span>

### <span data-ttu-id="63963-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="63963-129">None</span></span>

## <span data-ttu-id="63963-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63963-130">OUTPUTS</span></span>

### <span data-ttu-id="63963-131">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="63963-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection</span></span>

## <span data-ttu-id="63963-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="63963-132">NOTES</span></span>

## <span data-ttu-id="63963-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63963-133">RELATED LINKS</span></span>

[<span data-ttu-id="63963-134">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="63963-134">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)