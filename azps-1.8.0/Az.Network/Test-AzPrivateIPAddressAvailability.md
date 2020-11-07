---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: 3130aec4a5032fd62423aa35dec73d7acd6e14b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729926"
---
# <span data-ttu-id="00045-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="00045-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="00045-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00045-102">SYNOPSIS</span></span>
<span data-ttu-id="00045-103">Проверка доступности частного IP-адреса в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="00045-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="00045-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00045-104">SYNTAX</span></span>

### <span data-ttu-id="00045-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="00045-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00045-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="00045-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00045-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00045-107">DESCRIPTION</span></span>
<span data-ttu-id="00045-108">Командлет **Test-AzPrivateIPAddressAvailability** проверяет, доступен ли указанный частный IP-адрес в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="00045-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="00045-109">Этот командлет возвращает список доступных частных IP-адресов, если получен требуемый частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="00045-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="00045-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00045-110">EXAMPLES</span></span>

### <span data-ttu-id="00045-111">Пример 1: Проверка наличия IP-адреса в канале</span><span class="sxs-lookup"><span data-stu-id="00045-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="00045-112">Эта команда получает виртуальную сеть и использует оператор Pipeline для передачи его в **Test-AzPrivateIPAddressAvailability** , который проверяет, доступен ли указанный частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="00045-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="00045-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00045-113">PARAMETERS</span></span>

### <span data-ttu-id="00045-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00045-114">-DefaultProfile</span></span>
<span data-ttu-id="00045-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00045-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00045-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="00045-116">-IPAddress</span></span>
<span data-ttu-id="00045-117">Задает IP-адрес для проверки.</span><span class="sxs-lookup"><span data-stu-id="00045-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="00045-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00045-118">-ResourceGroupName</span></span>
<span data-ttu-id="00045-119">Указывает имя группы ресурсов для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="00045-119">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="00045-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="00045-120">-VirtualNetwork</span></span>
<span data-ttu-id="00045-121">Указывает объект **PSVirtualNetwork** .</span><span class="sxs-lookup"><span data-stu-id="00045-121">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="00045-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="00045-122">-VirtualNetworkName</span></span>
<span data-ttu-id="00045-123">Указывает имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="00045-123">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="00045-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00045-124">CommonParameters</span></span>
<span data-ttu-id="00045-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00045-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00045-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00045-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00045-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00045-127">INPUTS</span></span>

### <span data-ttu-id="00045-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="00045-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="00045-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00045-129">OUTPUTS</span></span>

### <span data-ttu-id="00045-130">Microsoft. Azure. Commands. Network. Models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="00045-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="00045-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="00045-131">NOTES</span></span>

## <span data-ttu-id="00045-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00045-132">RELATED LINKS</span></span>

[<span data-ttu-id="00045-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="00045-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


