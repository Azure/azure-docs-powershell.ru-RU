---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 2aa9792c632a7e615091a69182c87bc06b565c18
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234933"
---
# <span data-ttu-id="e7bf3-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e7bf3-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="e7bf3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="e7bf3-103">Удаление IP-конфигурации сетевого интерфейса из сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="e7bf3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7bf3-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7bf3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7bf3-105">DESCRIPTION</span></span>
<span data-ttu-id="e7bf3-106">Командлет **Remove-AzNetworkInterfaceIpConfig** удаляет IP-конфигурацию сетевого интерфейса из сетевого интерфейса Azure.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="e7bf3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7bf3-107">EXAMPLES</span></span>

### <span data-ttu-id="e7bf3-108">Пример 1: Удаление IP-конфигурации с сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="e7bf3-108">Example 1: Delete an IP configuration from a network interface</span></span>
```powershell
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic

Set-AzNetworkInterface -NetworkInterface $nic
```

<span data-ttu-id="e7bf3-109">Первая команда получает сетевой интерфейс с именем mynic и сохраняет его в переменной $nic.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="e7bf3-110">Вторая команда удаляет IP-конфигурацию с именем IPConfig-1, связанную с этим сетевым интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span> <span data-ttu-id="e7bf3-111">Третья команда задает изменения, внесенные в сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-111">The third command sets changes made to the network interface.</span></span>

## <span data-ttu-id="e7bf3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7bf3-112">PARAMETERS</span></span>

### <span data-ttu-id="e7bf3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7bf3-113">-DefaultProfile</span></span>
<span data-ttu-id="e7bf3-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7bf3-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e7bf3-115">-Name</span></span>
<span data-ttu-id="e7bf3-116">Указывает имя IP-конфигурации сетевого интерфейса, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-116">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="e7bf3-117">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e7bf3-117">-NetworkInterface</span></span>
<span data-ttu-id="e7bf3-118">Указывает объект **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="e7bf3-118">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="e7bf3-119">Этот объект включает IP-конфигурацию сетевого интерфейса, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-119">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="e7bf3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7bf3-120">CommonParameters</span></span>
<span data-ttu-id="e7bf3-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7bf3-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7bf3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7bf3-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7bf3-123">INPUTS</span></span>

### <span data-ttu-id="e7bf3-124">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e7bf3-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="e7bf3-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7bf3-125">OUTPUTS</span></span>

### <span data-ttu-id="e7bf3-126">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e7bf3-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="e7bf3-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7bf3-127">NOTES</span></span>
* <span data-ttu-id="e7bf3-128">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="e7bf3-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e7bf3-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7bf3-129">RELATED LINKS</span></span>

[<span data-ttu-id="e7bf3-130">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e7bf3-130">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e7bf3-131">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e7bf3-131">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e7bf3-132">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e7bf3-132">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e7bf3-133">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e7bf3-133">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


