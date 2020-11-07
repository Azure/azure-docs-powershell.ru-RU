---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 5936a7e3f15919e00fa052a2950fd31e69ca32fd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909950"
---
# <span data-ttu-id="3249b-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3249b-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="3249b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3249b-102">SYNOPSIS</span></span>
<span data-ttu-id="3249b-103">Возвращает IP-конфигурацию сетевого интерфейса для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3249b-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="3249b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3249b-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3249b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3249b-105">DESCRIPTION</span></span>
<span data-ttu-id="3249b-106">Командлет **Get-AzNetworkInterfaceIPConfig** получает IP-конфигурацию сетевого интерфейса из сетевого интерфейса Azure.</span><span class="sxs-lookup"><span data-stu-id="3249b-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="3249b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3249b-107">EXAMPLES</span></span>

### <span data-ttu-id="3249b-108">1: получение IP-конфигурации сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="3249b-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="3249b-109">Первая команда получает существующий сетевой интерфейс с именем mynic и сохраняет его в переменной $nic 1.</span><span class="sxs-lookup"><span data-stu-id="3249b-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="3249b-110">Вторая команда возвращает IP-конфигурацию с именем ipconfig1 для этого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3249b-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="3249b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3249b-111">PARAMETERS</span></span>

### <span data-ttu-id="3249b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3249b-112">-DefaultProfile</span></span>
<span data-ttu-id="3249b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3249b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3249b-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3249b-114">-Name</span></span>
<span data-ttu-id="3249b-115">Указывает имя сетевой IP-конфигурации, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3249b-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3249b-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3249b-116">-NetworkInterface</span></span>
<span data-ttu-id="3249b-117">Указывает объект **NetworkInterface** , который содержит IP-конфигурацию сети, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3249b-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3249b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3249b-118">CommonParameters</span></span>
<span data-ttu-id="3249b-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3249b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3249b-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3249b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3249b-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3249b-121">INPUTS</span></span>

### <span data-ttu-id="3249b-122">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3249b-122">PSNetworkInterface</span></span>
<span data-ttu-id="3249b-123">Параметр "NetworkInterface" принимает значение типа "PSNetworkInterface" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3249b-123">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="3249b-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3249b-124">OUTPUTS</span></span>

### <span data-ttu-id="3249b-125">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3249b-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="3249b-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="3249b-126">NOTES</span></span>
* <span data-ttu-id="3249b-127">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="3249b-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3249b-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3249b-128">RELATED LINKS</span></span>

[<span data-ttu-id="3249b-129">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3249b-129">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3249b-130">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3249b-130">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3249b-131">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3249b-131">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3249b-132">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3249b-132">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


