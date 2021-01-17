---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8152cf778cabed1c4a8a346ac86b708266058fc6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422228"
---
# <span data-ttu-id="ffda3-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ffda3-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="ffda3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffda3-102">SYNOPSIS</span></span>
<span data-ttu-id="ffda3-103">Получает конфигурацию IP-интерфейса для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ffda3-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="ffda3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ffda3-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffda3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffda3-105">DESCRIPTION</span></span>
<span data-ttu-id="ffda3-106">Командлет **Get-AzNetworkInterfaceIPConfig** получает конфигурацию IP-интерфейса сетевого интерфейса Azure.</span><span class="sxs-lookup"><span data-stu-id="ffda3-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="ffda3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ffda3-107">EXAMPLES</span></span>

### <span data-ttu-id="ffda3-108">1. Настройка IP-интерфейса</span><span class="sxs-lookup"><span data-stu-id="ffda3-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="ffda3-109">Первая команда получает существующий сетевой интерфейс mynic и сохраняет его в переменной $nic 1.</span><span class="sxs-lookup"><span data-stu-id="ffda3-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="ffda3-110">Вторая команда получает конфигурацию IP-адреса под названием ipconfig1 этого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ffda3-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="ffda3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffda3-111">PARAMETERS</span></span>

### <span data-ttu-id="ffda3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffda3-112">-DefaultProfile</span></span>
<span data-ttu-id="ffda3-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ffda3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffda3-114">-Name</span><span class="sxs-lookup"><span data-stu-id="ffda3-114">-Name</span></span>
<span data-ttu-id="ffda3-115">Указывает имя конфигурации IP-адреса сети, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffda3-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ffda3-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ffda3-116">-NetworkInterface</span></span>
<span data-ttu-id="ffda3-117">Определяет объект **NetworkInterface,** который содержит конфигурацию IP-адреса сети, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffda3-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ffda3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffda3-118">CommonParameters</span></span>
<span data-ttu-id="ffda3-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffda3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffda3-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ffda3-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffda3-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ffda3-121">INPUTS</span></span>

### <span data-ttu-id="ffda3-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ffda3-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="ffda3-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ffda3-123">OUTPUTS</span></span>

### <span data-ttu-id="ffda3-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ffda3-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="ffda3-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ffda3-125">NOTES</span></span>
* <span data-ttu-id="ffda3-126">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="ffda3-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ffda3-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ffda3-127">RELATED LINKS</span></span>

[<span data-ttu-id="ffda3-128">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ffda3-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ffda3-129">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ffda3-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ffda3-130">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ffda3-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ffda3-131">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ffda3-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


