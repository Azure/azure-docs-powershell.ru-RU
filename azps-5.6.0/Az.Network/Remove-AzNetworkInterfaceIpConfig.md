---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: abeeabcc3930a2f18822dbf3d9986e17fbc01c88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993642"
---
# <span data-ttu-id="dd217-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd217-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="dd217-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd217-102">SYNOPSIS</span></span>
<span data-ttu-id="dd217-103">Удаляет конфигурацию IP-интерфейса сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="dd217-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="dd217-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dd217-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd217-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd217-105">DESCRIPTION</span></span>
<span data-ttu-id="dd217-106">Командлет **Remove-AzNetworkInterfaceIpConfig** удаляет конфигурацию IP-интерфейса сетевого интерфейса из интерфейса Azure.</span><span class="sxs-lookup"><span data-stu-id="dd217-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="dd217-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dd217-107">EXAMPLES</span></span>

### <span data-ttu-id="dd217-108">Пример 1. Удаление конфигурации IP-адреса из интерфейса сети</span><span class="sxs-lookup"><span data-stu-id="dd217-108">Example 1: Delete an IP configuration from a network interface</span></span>
```powershell
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic

Set-AzNetworkInterface -NetworkInterface $nic
```

<span data-ttu-id="dd217-109">Первая команда получает сетевой интерфейс mynic и сохраняет его в переменной $nic.</span><span class="sxs-lookup"><span data-stu-id="dd217-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="dd217-110">Вторая команда удаляет конфигурацию IPConfig-1, связанную с этим сетевым интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="dd217-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span> <span data-ttu-id="dd217-111">Третья команда задает изменения в сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="dd217-111">The third command sets changes made to the network interface.</span></span>

## <span data-ttu-id="dd217-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd217-112">PARAMETERS</span></span>

### <span data-ttu-id="dd217-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd217-113">-DefaultProfile</span></span>
<span data-ttu-id="dd217-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd217-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd217-115">-Name</span><span class="sxs-lookup"><span data-stu-id="dd217-115">-Name</span></span>
<span data-ttu-id="dd217-116">Имя IP-конфигурации сетевого интерфейса, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="dd217-116">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="dd217-117">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd217-117">-NetworkInterface</span></span>
<span data-ttu-id="dd217-118">Определяет объект **NetworkInterface.**</span><span class="sxs-lookup"><span data-stu-id="dd217-118">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="dd217-119">Этот объект содержит IP-конфигурацию сетевого интерфейса, которая необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="dd217-119">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="dd217-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd217-120">CommonParameters</span></span>
<span data-ttu-id="dd217-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd217-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd217-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd217-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd217-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd217-123">INPUTS</span></span>

### <span data-ttu-id="dd217-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd217-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="dd217-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dd217-125">OUTPUTS</span></span>

### <span data-ttu-id="dd217-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd217-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="dd217-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dd217-127">NOTES</span></span>
* <span data-ttu-id="dd217-128">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="dd217-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="dd217-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd217-129">RELATED LINKS</span></span>

[<span data-ttu-id="dd217-130">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd217-130">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="dd217-131">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd217-131">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="dd217-132">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd217-132">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="dd217-133">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd217-133">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


