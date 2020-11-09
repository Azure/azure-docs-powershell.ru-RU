---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8152cf778cabed1c4a8a346ac86b708266058fc6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246212"
---
# <span data-ttu-id="289fd-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="289fd-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="289fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="289fd-102">SYNOPSIS</span></span>
<span data-ttu-id="289fd-103">Возвращает IP-конфигурацию сетевого интерфейса для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="289fd-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="289fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="289fd-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="289fd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="289fd-105">DESCRIPTION</span></span>
<span data-ttu-id="289fd-106">Командлет **Get-AzNetworkInterfaceIPConfig** получает IP-конфигурацию сетевого интерфейса из сетевого интерфейса Azure.</span><span class="sxs-lookup"><span data-stu-id="289fd-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="289fd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="289fd-107">EXAMPLES</span></span>

### <span data-ttu-id="289fd-108">1: получение IP-конфигурации сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="289fd-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="289fd-109">Первая команда получает существующий сетевой интерфейс с именем mynic и сохраняет его в переменной $nic 1.</span><span class="sxs-lookup"><span data-stu-id="289fd-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="289fd-110">Вторая команда возвращает IP-конфигурацию с именем ipconfig1 для этого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="289fd-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="289fd-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="289fd-111">PARAMETERS</span></span>

### <span data-ttu-id="289fd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="289fd-112">-DefaultProfile</span></span>
<span data-ttu-id="289fd-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="289fd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="289fd-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="289fd-114">-Name</span></span>
<span data-ttu-id="289fd-115">Указывает имя сетевой IP-конфигурации, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="289fd-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="289fd-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="289fd-116">-NetworkInterface</span></span>
<span data-ttu-id="289fd-117">Указывает объект **NetworkInterface** , который содержит IP-конфигурацию сети, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="289fd-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="289fd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="289fd-118">CommonParameters</span></span>
<span data-ttu-id="289fd-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="289fd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="289fd-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="289fd-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="289fd-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="289fd-121">INPUTS</span></span>

### <span data-ttu-id="289fd-122">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="289fd-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="289fd-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="289fd-123">OUTPUTS</span></span>

### <span data-ttu-id="289fd-124">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="289fd-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="289fd-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="289fd-125">NOTES</span></span>
* <span data-ttu-id="289fd-126">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="289fd-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="289fd-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="289fd-127">RELATED LINKS</span></span>

[<span data-ttu-id="289fd-128">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="289fd-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="289fd-129">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="289fd-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="289fd-130">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="289fd-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="289fd-131">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="289fd-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)

