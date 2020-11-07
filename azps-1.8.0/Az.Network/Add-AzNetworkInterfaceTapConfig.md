---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: c5c2481244de752a76eb1a1863d1fcc49d93ddb2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730700"
---
# <span data-ttu-id="972f1-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="972f1-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="972f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="972f1-102">SYNOPSIS</span></span>
<span data-ttu-id="972f1-103">Создает ресурс TapConfiguration, связанный с NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="972f1-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="972f1-104">Это будет ссылаться на существующий ресурс VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="972f1-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="972f1-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="972f1-105">SYNTAX</span></span>

### <span data-ttu-id="972f1-106">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="972f1-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="972f1-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="972f1-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="972f1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="972f1-108">DESCRIPTION</span></span>
<span data-ttu-id="972f1-109">Командлет **Add-AzNetworkInterfaceTapConfig** создает ресурс TapConfiguration, связанный с NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="972f1-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="972f1-110">Это будет ссылаться на существующий ресурс VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="972f1-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="972f1-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="972f1-111">EXAMPLES</span></span>

### <span data-ttu-id="972f1-112">Пример 1: Добавление TapConfiguration в заданный NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="972f1-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="972f1-113">Добавьте TapConfiguration в sourceNic.</span><span class="sxs-lookup"><span data-stu-id="972f1-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="972f1-114">Трафик из VM sourceNic будет зеркально отображен на целевую виртуальную машину, на которую ссылается vVirtualNetworkTap ресурс.</span><span class="sxs-lookup"><span data-stu-id="972f1-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="972f1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="972f1-115">PARAMETERS</span></span>

### <span data-ttu-id="972f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="972f1-116">-DefaultProfile</span></span>
<span data-ttu-id="972f1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="972f1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="972f1-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="972f1-118">-Name</span></span>
<span data-ttu-id="972f1-119">Имя конфигурации TAP.</span><span class="sxs-lookup"><span data-stu-id="972f1-119">Name of the tap configuration.</span></span>

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

### <span data-ttu-id="972f1-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="972f1-120">-NetworkInterface</span></span>
<span data-ttu-id="972f1-121">Ссылка на ресурс сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="972f1-121">The reference of the network interface resource.</span></span>

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

### <span data-ttu-id="972f1-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="972f1-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="972f1-123">Ссылка на ресурс касания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="972f1-123">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="972f1-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="972f1-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="972f1-125">Ссылка на ресурс касания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="972f1-125">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="972f1-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="972f1-126">-Confirm</span></span>
<span data-ttu-id="972f1-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="972f1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="972f1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="972f1-128">-WhatIf</span></span>
<span data-ttu-id="972f1-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="972f1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="972f1-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="972f1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="972f1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="972f1-131">CommonParameters</span></span>
<span data-ttu-id="972f1-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="972f1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="972f1-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="972f1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="972f1-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="972f1-134">INPUTS</span></span>

### <span data-ttu-id="972f1-135">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="972f1-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="972f1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="972f1-136">System.String</span></span>

### <span data-ttu-id="972f1-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="972f1-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="972f1-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="972f1-138">OUTPUTS</span></span>

### <span data-ttu-id="972f1-139">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="972f1-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="972f1-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="972f1-140">NOTES</span></span>

## <span data-ttu-id="972f1-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="972f1-141">RELATED LINKS</span></span>

[<span data-ttu-id="972f1-142">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="972f1-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="972f1-143">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="972f1-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="972f1-144">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="972f1-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
