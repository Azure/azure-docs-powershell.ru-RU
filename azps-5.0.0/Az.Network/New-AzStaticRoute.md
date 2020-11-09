---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: e4d9b8cd09aa1bf1528de1cd2179a76e7907e82b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317024"
---
# <span data-ttu-id="e7f89-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="e7f89-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="e7f89-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7f89-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f89-103">Создает объект StaticRoute, который затем можно добавить в объект RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e7f89-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="e7f89-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7f89-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7f89-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7f89-105">DESCRIPTION</span></span>
<span data-ttu-id="e7f89-106">Создает объект StaticRoute.</span><span class="sxs-lookup"><span data-stu-id="e7f89-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="e7f89-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7f89-107">EXAMPLES</span></span>

### <span data-ttu-id="e7f89-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e7f89-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="e7f89-109">Вышеприведенная команда создаст объект StaticRoute, который затем можно будет добавить в объект RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e7f89-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="e7f89-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7f89-110">PARAMETERS</span></span>

### <span data-ttu-id="e7f89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f89-111">-DefaultProfile</span></span>
<span data-ttu-id="e7f89-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7f89-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f89-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e7f89-113">-AddressPrefix</span></span>
<span data-ttu-id="e7f89-114">Список префиксов адресов.</span><span class="sxs-lookup"><span data-stu-id="e7f89-114">List of address prefixes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f89-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e7f89-115">-Name</span></span>
<span data-ttu-id="e7f89-116">Имя маршрута.</span><span class="sxs-lookup"><span data-stu-id="e7f89-116">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f89-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="e7f89-117">-NextHopIpAddress</span></span>
<span data-ttu-id="e7f89-118">IP-адрес следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="e7f89-118">The next hop ip address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f89-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f89-119">CommonParameters</span></span>
<span data-ttu-id="e7f89-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7f89-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f89-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7f89-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f89-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7f89-122">INPUTS</span></span>

### <span data-ttu-id="e7f89-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e7f89-123">System.String</span></span>

## <span data-ttu-id="e7f89-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7f89-124">OUTPUTS</span></span>

### <span data-ttu-id="e7f89-125">Microsoft. Azure. Commands. Network. Models. PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="e7f89-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="e7f89-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7f89-126">NOTES</span></span>

## <span data-ttu-id="e7f89-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7f89-127">RELATED LINKS</span></span>

[<span data-ttu-id="e7f89-128">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7f89-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
