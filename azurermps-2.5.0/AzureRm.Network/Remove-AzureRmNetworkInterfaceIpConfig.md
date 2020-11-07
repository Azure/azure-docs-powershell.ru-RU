---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterfaceipconfig
schema: 2.0.0
ms.openlocfilehash: c9ffd5b3a61dab57859f8c099950ddca0f47822c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913290"
---
# <span data-ttu-id="22774-101">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="22774-101">Remove-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="22774-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="22774-102">SYNOPSIS</span></span>
<span data-ttu-id="22774-103">Удаление IP-конфигурации сетевого интерфейса из сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="22774-103">Removes a network interface IP configuration from a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22774-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="22774-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22774-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22774-105">DESCRIPTION</span></span>
<span data-ttu-id="22774-106">Командлет **Remove-AzureRmNetworkInterfaceIpConfig** удаляет IP-конфигурацию сетевого интерфейса из сетевого интерфейса Azure.</span><span class="sxs-lookup"><span data-stu-id="22774-106">The **Remove-AzureRmNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="22774-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="22774-107">EXAMPLES</span></span>

### <span data-ttu-id="22774-108">1: Удаление IP-конфигурации с сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="22774-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzureRmNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="22774-109">Первая команда получает сетевой интерфейс с именем mynic и сохраняет его в переменной $nic.</span><span class="sxs-lookup"><span data-stu-id="22774-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="22774-110">Вторая команда удаляет IP-конфигурацию с именем IPConfig-1, связанную с этим сетевым интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="22774-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="22774-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="22774-111">PARAMETERS</span></span>

### <span data-ttu-id="22774-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22774-112">-DefaultProfile</span></span>
<span data-ttu-id="22774-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22774-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22774-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="22774-114">-Name</span></span>
<span data-ttu-id="22774-115">Указывает имя IP-конфигурации сетевого интерфейса, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="22774-115">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="22774-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="22774-116">-NetworkInterface</span></span>
<span data-ttu-id="22774-117">Указывает объект **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="22774-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="22774-118">Этот объект включает IP-конфигурацию сетевого интерфейса, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="22774-118">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="22774-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22774-119">CommonParameters</span></span>
<span data-ttu-id="22774-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="22774-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22774-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22774-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22774-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="22774-122">INPUTS</span></span>

### <span data-ttu-id="22774-123">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="22774-123">PSNetworkInterface</span></span>
<span data-ttu-id="22774-124">Параметр "NetworkInterface" принимает значение типа "PSNetworkInterface" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="22774-124">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="22774-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="22774-125">OUTPUTS</span></span>

### <span data-ttu-id="22774-126">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="22774-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="22774-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="22774-127">NOTES</span></span>
* <span data-ttu-id="22774-128">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="22774-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="22774-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22774-129">RELATED LINKS</span></span>

[<span data-ttu-id="22774-130">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="22774-130">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="22774-131">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="22774-131">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="22774-132">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="22774-132">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="22774-133">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="22774-133">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


