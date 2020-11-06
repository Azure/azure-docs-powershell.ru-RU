---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: eac8a985cfcb531247fcf2617fee86da92ea0112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570224"
---
# <span data-ttu-id="8c0f8-101">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8c0f8-101">Get-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="8c0f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c0f8-102">SYNOPSIS</span></span>
<span data-ttu-id="8c0f8-103">Возвращает IP-конфигурацию сетевого интерфейса для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-103">Gets a network interface IP configuration for a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c0f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c0f8-104">SYNTAX</span></span>

```
Get-AzureRmNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c0f8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c0f8-105">DESCRIPTION</span></span>
<span data-ttu-id="8c0f8-106">Командлет **Get-AzureRmNetworkInterfaceIPConfig** получает IP-конфигурацию сетевого интерфейса из сетевого интерфейса Azure.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-106">The **Get-AzureRmNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="8c0f8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c0f8-107">EXAMPLES</span></span>

### <span data-ttu-id="8c0f8-108">1: получение IP-конфигурации сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="8c0f8-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="8c0f8-109">Первая команда получает существующий сетевой интерфейс с именем mynic и сохраняет его в переменной $nic 1.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="8c0f8-110">Вторая команда возвращает IP-конфигурацию с именем ipconfig1 для этого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="8c0f8-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c0f8-111">PARAMETERS</span></span>

### <span data-ttu-id="8c0f8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c0f8-112">-DefaultProfile</span></span>
<span data-ttu-id="8c0f8-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c0f8-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8c0f8-114">-Name</span></span>
<span data-ttu-id="8c0f8-115">Указывает имя сетевой IP-конфигурации, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8c0f8-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8c0f8-116">-NetworkInterface</span></span>
<span data-ttu-id="8c0f8-117">Указывает объект **NetworkInterface** , который содержит IP-конфигурацию сети, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8c0f8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c0f8-118">CommonParameters</span></span>
<span data-ttu-id="8c0f8-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c0f8-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c0f8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c0f8-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c0f8-121">INPUTS</span></span>

### <span data-ttu-id="8c0f8-122">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8c0f8-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>
<span data-ttu-id="8c0f8-123">Параметры: NetworkInterface (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8c0f8-123">Parameters: NetworkInterface (ByValue)</span></span>

## <span data-ttu-id="8c0f8-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c0f8-124">OUTPUTS</span></span>

### <span data-ttu-id="8c0f8-125">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c0f8-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="8c0f8-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c0f8-126">NOTES</span></span>
* <span data-ttu-id="8c0f8-127">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="8c0f8-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8c0f8-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c0f8-128">RELATED LINKS</span></span>

[<span data-ttu-id="8c0f8-129">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8c0f8-129">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="8c0f8-130">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8c0f8-130">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="8c0f8-131">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8c0f8-131">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="8c0f8-132">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8c0f8-132">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


