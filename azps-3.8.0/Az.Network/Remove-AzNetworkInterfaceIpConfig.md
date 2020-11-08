---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 784374b620af09b00f460ff5c50d0a08baa46233
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074019"
---
# <span data-ttu-id="a815d-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a815d-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="a815d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a815d-102">SYNOPSIS</span></span>
<span data-ttu-id="a815d-103">Удаление IP-конфигурации сетевого интерфейса из сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a815d-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="a815d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a815d-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a815d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a815d-105">DESCRIPTION</span></span>
<span data-ttu-id="a815d-106">Командлет **Remove-AzNetworkInterfaceIpConfig** удаляет IP-конфигурацию сетевого интерфейса из сетевого интерфейса Azure.</span><span class="sxs-lookup"><span data-stu-id="a815d-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="a815d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a815d-107">EXAMPLES</span></span>

### <span data-ttu-id="a815d-108">1: Удаление IP-конфигурации с сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="a815d-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="a815d-109">Первая команда получает сетевой интерфейс с именем mynic и сохраняет его в переменной $nic.</span><span class="sxs-lookup"><span data-stu-id="a815d-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="a815d-110">Вторая команда удаляет IP-конфигурацию с именем IPConfig-1, связанную с этим сетевым интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="a815d-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="a815d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a815d-111">PARAMETERS</span></span>

### <span data-ttu-id="a815d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a815d-112">-DefaultProfile</span></span>
<span data-ttu-id="a815d-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a815d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a815d-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a815d-114">-Name</span></span>
<span data-ttu-id="a815d-115">Указывает имя IP-конфигурации сетевого интерфейса, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a815d-115">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="a815d-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a815d-116">-NetworkInterface</span></span>
<span data-ttu-id="a815d-117">Указывает объект **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="a815d-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="a815d-118">Этот объект включает IP-конфигурацию сетевого интерфейса, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a815d-118">This object contains the network interface IP configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a815d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a815d-119">CommonParameters</span></span>
<span data-ttu-id="a815d-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a815d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a815d-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a815d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a815d-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a815d-122">INPUTS</span></span>

### <span data-ttu-id="a815d-123">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a815d-123">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="a815d-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a815d-124">OUTPUTS</span></span>

### <span data-ttu-id="a815d-125">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a815d-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="a815d-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="a815d-126">NOTES</span></span>
* <span data-ttu-id="a815d-127">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="a815d-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a815d-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a815d-128">RELATED LINKS</span></span>

[<span data-ttu-id="a815d-129">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a815d-129">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="a815d-130">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a815d-130">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="a815d-131">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a815d-131">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="a815d-132">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a815d-132">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


