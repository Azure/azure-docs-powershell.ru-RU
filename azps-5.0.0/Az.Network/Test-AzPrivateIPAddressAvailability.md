---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: af5e1591e0d5c497b0cfe854235536d7edf404c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318506"
---
# <span data-ttu-id="83fd9-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="83fd9-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="83fd9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="83fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="83fd9-103">Проверка доступности частного IP-адреса в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="83fd9-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="83fd9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="83fd9-104">SYNTAX</span></span>

### <span data-ttu-id="83fd9-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="83fd9-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83fd9-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="83fd9-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83fd9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83fd9-107">DESCRIPTION</span></span>
<span data-ttu-id="83fd9-108">Командлет **Test-AzPrivateIPAddressAvailability** проверяет, доступен ли указанный частный IP-адрес в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="83fd9-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="83fd9-109">Этот командлет возвращает список доступных частных IP-адресов, если получен требуемый частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="83fd9-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="83fd9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="83fd9-110">EXAMPLES</span></span>

### <span data-ttu-id="83fd9-111">Пример 1: Проверка наличия IP-адреса в канале</span><span class="sxs-lookup"><span data-stu-id="83fd9-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="83fd9-112">Эта команда получает виртуальную сеть и использует оператор Pipeline для передачи его в **Test-AzPrivateIPAddressAvailability** , который проверяет, доступен ли указанный частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="83fd9-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="83fd9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="83fd9-113">PARAMETERS</span></span>

### <span data-ttu-id="83fd9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83fd9-114">-DefaultProfile</span></span>
<span data-ttu-id="83fd9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="83fd9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83fd9-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="83fd9-116">-IPAddress</span></span>
<span data-ttu-id="83fd9-117">Задает IP-адрес для проверки.</span><span class="sxs-lookup"><span data-stu-id="83fd9-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="83fd9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83fd9-118">-ResourceGroupName</span></span>
<span data-ttu-id="83fd9-119">Указывает имя группы ресурсов для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="83fd9-119">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="83fd9-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="83fd9-120">-VirtualNetwork</span></span>
<span data-ttu-id="83fd9-121">Указывает объект **PSVirtualNetwork** .</span><span class="sxs-lookup"><span data-stu-id="83fd9-121">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="83fd9-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="83fd9-122">-VirtualNetworkName</span></span>
<span data-ttu-id="83fd9-123">Указывает имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="83fd9-123">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="83fd9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83fd9-124">CommonParameters</span></span>
<span data-ttu-id="83fd9-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="83fd9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83fd9-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83fd9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83fd9-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="83fd9-127">INPUTS</span></span>

### <span data-ttu-id="83fd9-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="83fd9-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="83fd9-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="83fd9-129">OUTPUTS</span></span>

### <span data-ttu-id="83fd9-130">Microsoft. Azure. Commands. Network. Models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="83fd9-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="83fd9-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="83fd9-131">NOTES</span></span>

## <span data-ttu-id="83fd9-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83fd9-132">RELATED LINKS</span></span>

[<span data-ttu-id="83fd9-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="83fd9-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


