---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: 2a31aa9db3264dd24c6d77bdad7b10d6ecad10b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066281"
---
# <span data-ttu-id="cf0ad-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="cf0ad-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="cf0ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf0ad-102">SYNOPSIS</span></span>
<span data-ttu-id="cf0ad-103">Создание нового IpconfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="cf0ad-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="cf0ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf0ad-104">SYNTAX</span></span>

### <span data-ttu-id="cf0ad-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf0ad-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="cf0ad-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf0ad-106">DESCRIPTION</span></span>
<span data-ttu-id="cf0ad-107">**New-AzIpConfigurationBgpPeeringAddressObject** создает объект IpConfigurationBgpPeeringAddressObject, который представляет свойство BgpPeeringAddresses в шлюзе виртуальной сети bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="cf0ad-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="cf0ad-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf0ad-108">EXAMPLES</span></span>

### <span data-ttu-id="cf0ad-109">1: создание AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="cf0ad-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="cf0ad-110">В приведенном выше примере будет создано IpConfigurationBgpPeeringAddressObject. Этот новый объект будет gw1ipconfBgp1.</span><span class="sxs-lookup"><span data-stu-id="cf0ad-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="cf0ad-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf0ad-111">PARAMETERS</span></span>

### <span data-ttu-id="cf0ad-112">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf0ad-112">-Confirm</span></span>
<span data-ttu-id="cf0ad-113">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cf0ad-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf0ad-114">-CustomAddress</span><span class="sxs-lookup"><span data-stu-id="cf0ad-114">-CustomAddress</span></span>
<span data-ttu-id="cf0ad-115">Список CustomAddress шлюза виртуальной сети для BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="cf0ad-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf0ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf0ad-116">-DefaultProfile</span></span>
<span data-ttu-id="cf0ad-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf0ad-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf0ad-118">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="cf0ad-118">-IpConfigurationId</span></span>
<span data-ttu-id="cf0ad-119">Шлюз виртуальной сети IpConfigurationId для BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="cf0ad-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="cf0ad-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf0ad-120">-WhatIf</span></span>
<span data-ttu-id="cf0ad-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cf0ad-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf0ad-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cf0ad-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf0ad-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf0ad-123">CommonParameters</span></span>
<span data-ttu-id="cf0ad-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf0ad-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf0ad-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf0ad-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf0ad-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf0ad-126">INPUTS</span></span>

### <span data-ttu-id="cf0ad-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="cf0ad-127">None</span></span>

## <span data-ttu-id="cf0ad-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf0ad-128">OUTPUTS</span></span>

### <span data-ttu-id="cf0ad-129">Microsoft. Azure. Commands. Network. Models. PSIpConfigurationBgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="cf0ad-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="cf0ad-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf0ad-130">NOTES</span></span>

## <span data-ttu-id="cf0ad-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf0ad-131">RELATED LINKS</span></span>
