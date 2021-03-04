---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 572ea4aac029068e3b7e4fbcf12f3b240129d585
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006344"
---
# <span data-ttu-id="3048f-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3048f-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="3048f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3048f-102">SYNOPSIS</span></span>
<span data-ttu-id="3048f-103">Получает конфигурацию IP-интерфейса для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3048f-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="3048f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3048f-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3048f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3048f-105">DESCRIPTION</span></span>
<span data-ttu-id="3048f-106">Командлет **Get-AzNetworkInterfaceIPConfig** получает конфигурацию IP-интерфейса сетевого интерфейса Azure.</span><span class="sxs-lookup"><span data-stu-id="3048f-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="3048f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3048f-107">EXAMPLES</span></span>

### <span data-ttu-id="3048f-108">1. Настройка IP-интерфейса</span><span class="sxs-lookup"><span data-stu-id="3048f-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="3048f-109">Первая команда получает существующий сетевой интерфейс mynic и сохраняет его в переменной $nic 1.</span><span class="sxs-lookup"><span data-stu-id="3048f-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="3048f-110">Вторая команда получает конфигурацию IP-адреса под названием ipconfig1 этого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3048f-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="3048f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3048f-111">PARAMETERS</span></span>

### <span data-ttu-id="3048f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3048f-112">-DefaultProfile</span></span>
<span data-ttu-id="3048f-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3048f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3048f-114">-Name</span><span class="sxs-lookup"><span data-stu-id="3048f-114">-Name</span></span>
<span data-ttu-id="3048f-115">Указывает имя конфигурации IP-адреса сети, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3048f-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3048f-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3048f-116">-NetworkInterface</span></span>
<span data-ttu-id="3048f-117">Определяет объект **NetworkInterface,** который содержит конфигурацию IP-адреса сети, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3048f-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3048f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3048f-118">CommonParameters</span></span>
<span data-ttu-id="3048f-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3048f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3048f-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3048f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3048f-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3048f-121">INPUTS</span></span>

### <span data-ttu-id="3048f-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3048f-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="3048f-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3048f-123">OUTPUTS</span></span>

### <span data-ttu-id="3048f-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3048f-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="3048f-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3048f-125">NOTES</span></span>
* <span data-ttu-id="3048f-126">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="3048f-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3048f-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3048f-127">RELATED LINKS</span></span>

[<span data-ttu-id="3048f-128">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3048f-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3048f-129">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3048f-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3048f-130">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3048f-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3048f-131">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3048f-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


