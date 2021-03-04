---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: a39dd390e0307662c8105bf84999ae8dfc1fc7aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951720"
---
# <span data-ttu-id="bdcf2-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="bdcf2-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="bdcf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdcf2-102">SYNOPSIS</span></span>
<span data-ttu-id="bdcf2-103">Проверьте доступность личного IP-адреса в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="bdcf2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bdcf2-104">SYNTAX</span></span>

### <span data-ttu-id="bdcf2-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="bdcf2-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdcf2-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="bdcf2-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdcf2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdcf2-107">DESCRIPTION</span></span>
<span data-ttu-id="bdcf2-108">С помощью cmdlet **Test-AzPrivateIPAddressAvailability** можно проверить, доступен ли указанный частный IP-адрес в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="bdcf2-109">Этот cmdlet возвращает список доступных частных IP-адресов, если запрашивается частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="bdcf2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bdcf2-110">EXAMPLES</span></span>

### <span data-ttu-id="bdcf2-111">Пример 1. Проверка того, доступен ли IP-адрес при использовании конвейера</span><span class="sxs-lookup"><span data-stu-id="bdcf2-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="bdcf2-112">Эта команда получает виртуальную сеть и использует оператор конвейера для ее переадресации **Test-AzPrivateIPAddressAvailability,** проверяя доступность указанного закрытого IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability**, which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="bdcf2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdcf2-113">PARAMETERS</span></span>

### <span data-ttu-id="bdcf2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdcf2-114">-DefaultProfile</span></span>
<span data-ttu-id="bdcf2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdcf2-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="bdcf2-116">-IPAddress</span></span>
<span data-ttu-id="bdcf2-117">Ip-адрес, который нужно проверить.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="bdcf2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdcf2-118">-ResourceGroupName</span></span>
<span data-ttu-id="bdcf2-119">Имя группы ресурсов для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-119">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcf2-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bdcf2-120">-VirtualNetwork</span></span>
<span data-ttu-id="bdcf2-121">Указывает объект **PSVirtualNetwork.**</span><span class="sxs-lookup"><span data-stu-id="bdcf2-121">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: TestByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdcf2-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="bdcf2-122">-VirtualNetworkName</span></span>
<span data-ttu-id="bdcf2-123">Указывает имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-123">Specifies the name of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcf2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdcf2-124">CommonParameters</span></span>
<span data-ttu-id="bdcf2-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdcf2-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdcf2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdcf2-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bdcf2-127">INPUTS</span></span>

### <span data-ttu-id="bdcf2-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bdcf2-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="bdcf2-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bdcf2-129">OUTPUTS</span></span>

### <span data-ttu-id="bdcf2-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="bdcf2-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="bdcf2-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bdcf2-131">NOTES</span></span>

## <span data-ttu-id="bdcf2-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bdcf2-132">RELATED LINKS</span></span>

[<span data-ttu-id="bdcf2-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bdcf2-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


