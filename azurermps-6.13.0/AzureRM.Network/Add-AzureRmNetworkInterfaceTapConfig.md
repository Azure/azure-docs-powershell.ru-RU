---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: 10d51bd2e70db0d2b1d06b907769fb6842e413cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569831"
---
# <span data-ttu-id="d56df-101">Add-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d56df-101">Add-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="d56df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d56df-102">SYNOPSIS</span></span>
<span data-ttu-id="d56df-103">Создает ресурс TapConfiguration, связанный с NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="d56df-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="d56df-104">Это будет ссылаться на существующий ресурс VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="d56df-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d56df-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d56df-105">SYNTAX</span></span>

### <span data-ttu-id="d56df-106">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d56df-106">SetByResource (Default)</span></span>
```
Add-AzureRmNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d56df-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d56df-107">SetByResourceId</span></span>
```
Add-AzureRmNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d56df-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d56df-108">DESCRIPTION</span></span>
<span data-ttu-id="d56df-109">Командлет **Add-AzureRmNetworkInterfaceTapConfig** создает ресурс TapConfiguration, связанный с NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="d56df-109">The **Add-AzureRmNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="d56df-110">Это будет ссылаться на существующий ресурс VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="d56df-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="d56df-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d56df-111">EXAMPLES</span></span>

### <span data-ttu-id="d56df-112">Пример 1: Добавление TapConfiguration в заданный NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d56df-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzureRmNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="d56df-113">Добавьте TapConfiguration в sourceNic.</span><span class="sxs-lookup"><span data-stu-id="d56df-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="d56df-114">Трафик из VM sourceNic будет зеркально отображен на целевую виртуальную машину, на которую ссылается vVirtualNetworkTap ресурс.</span><span class="sxs-lookup"><span data-stu-id="d56df-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="d56df-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d56df-115">PARAMETERS</span></span>

### <span data-ttu-id="d56df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d56df-116">-DefaultProfile</span></span>
<span data-ttu-id="d56df-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d56df-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d56df-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d56df-118">-Name</span></span>
<span data-ttu-id="d56df-119">Имя конфигурации TAP.</span><span class="sxs-lookup"><span data-stu-id="d56df-119">Name of the tap configuration.</span></span>

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

### <span data-ttu-id="d56df-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d56df-120">-NetworkInterface</span></span>
<span data-ttu-id="d56df-121">Ссылка на ресурс сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d56df-121">The reference of the network interface resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d56df-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d56df-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="d56df-123">Ссылка на ресурс касания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d56df-123">The reference of the virtual network tap resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d56df-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="d56df-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="d56df-125">Ссылка на ресурс касания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d56df-125">The reference of the virtual network tap resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d56df-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d56df-126">-Confirm</span></span>
<span data-ttu-id="d56df-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d56df-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56df-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d56df-128">-WhatIf</span></span>
<span data-ttu-id="d56df-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d56df-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d56df-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d56df-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56df-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d56df-131">CommonParameters</span></span>
<span data-ttu-id="d56df-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d56df-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d56df-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d56df-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d56df-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d56df-134">INPUTS</span></span>

### <span data-ttu-id="d56df-135">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d56df-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="d56df-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d56df-136">System.String</span></span>

### <span data-ttu-id="d56df-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d56df-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="d56df-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d56df-138">OUTPUTS</span></span>

### <span data-ttu-id="d56df-139">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d56df-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="d56df-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="d56df-140">NOTES</span></span>

## <span data-ttu-id="d56df-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d56df-141">RELATED LINKS</span></span>
