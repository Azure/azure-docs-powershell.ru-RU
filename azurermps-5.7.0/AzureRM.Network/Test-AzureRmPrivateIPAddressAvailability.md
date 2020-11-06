---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
ms.openlocfilehash: 769f8a5f8f95e5a97af8a495e0edbaba6b75a5d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564727"
---
# <span data-ttu-id="b2793-101">Test-AzureRmPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="b2793-101">Test-AzureRmPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="b2793-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2793-102">SYNOPSIS</span></span>
<span data-ttu-id="b2793-103">Проверка доступности частного IP-адреса в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b2793-103">Test availability of a private IP address in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2793-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2793-104">SYNTAX</span></span>

### <span data-ttu-id="b2793-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="b2793-105">TestByResource</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2793-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="b2793-106">TestByResourceId</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2793-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2793-107">DESCRIPTION</span></span>
<span data-ttu-id="b2793-108">Командлет **Test-AzureRmPrivateIPAddressAvailability** проверяет, доступен ли указанный частный IP-адрес в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b2793-108">The **Test-AzureRmPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="b2793-109">Этот командлет возвращает список доступных частных IP-адресов, если получен требуемый частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="b2793-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="b2793-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2793-110">EXAMPLES</span></span>

### <span data-ttu-id="b2793-111">Пример 1: Проверка наличия IP-адреса в канале</span><span class="sxs-lookup"><span data-stu-id="b2793-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzureRmVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzureRmPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="b2793-112">Эта команда получает виртуальную сеть и использует оператор Pipeline для передачи его в **Test-AzureRmPrivateIPAddressAvailability** , который проверяет, доступен ли указанный частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="b2793-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzureRmPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="b2793-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2793-113">PARAMETERS</span></span>

### <span data-ttu-id="b2793-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2793-114">-DefaultProfile</span></span>
<span data-ttu-id="b2793-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2793-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2793-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="b2793-116">-IPAddress</span></span>
<span data-ttu-id="b2793-117">Задает IP-адрес для проверки.</span><span class="sxs-lookup"><span data-stu-id="b2793-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="b2793-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2793-118">-ResourceGroupName</span></span>
<span data-ttu-id="b2793-119">Указывает имя группы ресурсов для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b2793-119">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="b2793-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b2793-120">-VirtualNetwork</span></span>
<span data-ttu-id="b2793-121">Указывает объект **PSVirtualNetwork** .</span><span class="sxs-lookup"><span data-stu-id="b2793-121">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="b2793-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b2793-122">-VirtualNetworkName</span></span>
<span data-ttu-id="b2793-123">Указывает имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b2793-123">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="b2793-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2793-124">CommonParameters</span></span>
<span data-ttu-id="b2793-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2793-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2793-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2793-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2793-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2793-127">INPUTS</span></span>

### <span data-ttu-id="b2793-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b2793-128">PSVirtualNetwork</span></span>
<span data-ttu-id="b2793-129">Параметр "VirtualNetwork" принимает значение типа "PSVirtualNetwork" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b2793-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="b2793-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2793-130">OUTPUTS</span></span>

### <span data-ttu-id="b2793-131">Microsoft. Azure. Commands. Network. Models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="b2793-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="b2793-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2793-132">NOTES</span></span>

## <span data-ttu-id="b2793-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2793-133">RELATED LINKS</span></span>

[<span data-ttu-id="b2793-134">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b2793-134">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)


