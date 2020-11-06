---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRoute.md
ms.openlocfilehash: 7197c90e5d5cb0c8a0e15b5e16d1a3c05aaeebf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566799"
---
# <span data-ttu-id="b0fc3-101">New-AzureRmVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="b0fc3-101">New-AzureRmVirtualHubRoute</span></span>

## <span data-ttu-id="b0fc3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b0fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="b0fc3-103">Создает объект-маршрут виртуального концентратора Azure.</span><span class="sxs-lookup"><span data-stu-id="b0fc3-103">Creates an Azure Virtual Hub Route object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0fc3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b0fc3-104">SYNTAX</span></span>

```
New-AzureRmVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0fc3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0fc3-105">DESCRIPTION</span></span>
<span data-ttu-id="b0fc3-106">Создает объект-маршрут виртуального концентратора Azure.</span><span class="sxs-lookup"><span data-stu-id="b0fc3-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="b0fc3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b0fc3-107">EXAMPLES</span></span>

### <span data-ttu-id="b0fc3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b0fc3-108">Example 1</span></span>

```powershell
PS C:\> $route1 = 

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="b0fc3-109">В приведенном выше примере создается объект-маршрут виртуального концентратора, который может быть включен в таблицу виртуальных маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="b0fc3-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="b0fc3-110">Виртуальный серверный маршрут — это объект в памяти, который можно использовать для создания объекта VirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="b0fc3-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="b0fc3-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b0fc3-111">PARAMETERS</span></span>

### <span data-ttu-id="b0fc3-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b0fc3-112">-AddressPrefix</span></span>
<span data-ttu-id="b0fc3-113">Список префиксов адресов.</span><span class="sxs-lookup"><span data-stu-id="b0fc3-113">List of Address Prefixes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fc3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0fc3-114">-DefaultProfile</span></span>
<span data-ttu-id="b0fc3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0fc3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fc3-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="b0fc3-116">-NextHopIpAddress</span></span>
<span data-ttu-id="b0fc3-117">IP-адрес следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="b0fc3-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="b0fc3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0fc3-118">CommonParameters</span></span>
<span data-ttu-id="b0fc3-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b0fc3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0fc3-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0fc3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0fc3-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b0fc3-121">INPUTS</span></span>

### <span data-ttu-id="b0fc3-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="b0fc3-122">None</span></span>

## <span data-ttu-id="b0fc3-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0fc3-123">OUTPUTS</span></span>

### <span data-ttu-id="b0fc3-124">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="b0fc3-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="b0fc3-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="b0fc3-125">NOTES</span></span>

## <span data-ttu-id="b0fc3-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0fc3-126">RELATED LINKS</span></span>
