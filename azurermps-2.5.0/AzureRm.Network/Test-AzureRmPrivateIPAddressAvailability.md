---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermprivateipaddressavailability
schema: 2.0.0
ms.openlocfilehash: 73924c1d1308a4cf457033e27e49ad7f9e19392e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913556"
---
# <span data-ttu-id="04a25-101">Test-AzureRmPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="04a25-101">Test-AzureRmPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="04a25-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="04a25-102">SYNOPSIS</span></span>
<span data-ttu-id="04a25-103">Проверка доступности частного IP-адреса в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="04a25-103">Test availability of a private IP address in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04a25-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="04a25-104">SYNTAX</span></span>

### <span data-ttu-id="04a25-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="04a25-105">TestByResource</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04a25-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="04a25-106">TestByResourceId</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04a25-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04a25-107">DESCRIPTION</span></span>
<span data-ttu-id="04a25-108">Командлет **Test-AzureRmPrivateIPAddressAvailability** проверяет, доступен ли указанный частный IP-адрес в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="04a25-108">The **Test-AzureRmPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="04a25-109">Этот командлет возвращает список доступных частных IP-адресов, если получен требуемый частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="04a25-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="04a25-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="04a25-110">EXAMPLES</span></span>

### <span data-ttu-id="04a25-111">Пример 1: Проверка наличия IP-адреса в канале</span><span class="sxs-lookup"><span data-stu-id="04a25-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzureRmVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzureRmPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="04a25-112">Эта команда получает виртуальную сеть и использует оператор Pipeline для передачи его в **Test-AzureRmPrivateIPAddressAvailability** , который проверяет, доступен ли указанный частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="04a25-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzureRmPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="04a25-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="04a25-113">PARAMETERS</span></span>

### <span data-ttu-id="04a25-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04a25-114">-DefaultProfile</span></span>
<span data-ttu-id="04a25-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="04a25-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a25-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="04a25-116">-IPAddress</span></span>
<span data-ttu-id="04a25-117">Задает IP-адрес для проверки.</span><span class="sxs-lookup"><span data-stu-id="04a25-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="04a25-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04a25-118">-ResourceGroupName</span></span>
<span data-ttu-id="04a25-119">Указывает имя группы ресурсов для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="04a25-119">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a25-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="04a25-120">-VirtualNetwork</span></span>
<span data-ttu-id="04a25-121">Указывает объект **PSVirtualNetwork** .</span><span class="sxs-lookup"><span data-stu-id="04a25-121">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: TestByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04a25-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="04a25-122">-VirtualNetworkName</span></span>
<span data-ttu-id="04a25-123">Указывает имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="04a25-123">Specifies the name of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a25-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04a25-124">CommonParameters</span></span>
<span data-ttu-id="04a25-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="04a25-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04a25-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04a25-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04a25-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="04a25-127">INPUTS</span></span>

### <span data-ttu-id="04a25-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="04a25-128">PSVirtualNetwork</span></span>
<span data-ttu-id="04a25-129">Параметр "VirtualNetwork" принимает значение типа "PSVirtualNetwork" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="04a25-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="04a25-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="04a25-130">OUTPUTS</span></span>

### <span data-ttu-id="04a25-131">Microsoft. Azure. Commands. Network. Models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="04a25-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="04a25-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="04a25-132">NOTES</span></span>

## <span data-ttu-id="04a25-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04a25-133">RELATED LINKS</span></span>

[<span data-ttu-id="04a25-134">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="04a25-134">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)


