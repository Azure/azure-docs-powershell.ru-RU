---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2da755a4ac3044c6499faee82a74e2c9ec7d9f6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982451"
---
# <span data-ttu-id="f09aa-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f09aa-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="f09aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f09aa-102">SYNOPSIS</span></span>
<span data-ttu-id="f09aa-103">Создание ресурса TapConfiguration, связанного с NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="f09aa-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="f09aa-104">Это будет ссылка на существующий ресурс VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="f09aa-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="f09aa-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f09aa-105">SYNTAX</span></span>

### <span data-ttu-id="f09aa-106">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f09aa-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f09aa-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f09aa-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f09aa-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f09aa-108">DESCRIPTION</span></span>
<span data-ttu-id="f09aa-109">Командлет **Add-AzNetworkInterfaceTapConfig** создает ресурс TapConfiguration, связанный с NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="f09aa-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="f09aa-110">Это будет ссылка на существующий ресурс VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="f09aa-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="f09aa-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f09aa-111">EXAMPLES</span></span>

### <span data-ttu-id="f09aa-112">Пример 1. Добавление tapConfiguration в заданный NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f09aa-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="f09aa-113">Добавьте tapConfiguration в sourceNic.</span><span class="sxs-lookup"><span data-stu-id="f09aa-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="f09aa-114">Трафик от sourceNic VM будет зеркально отражен в конечной VM, на который ссылается ресурс vVirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="f09aa-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="f09aa-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f09aa-115">PARAMETERS</span></span>

### <span data-ttu-id="f09aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f09aa-116">-DefaultProfile</span></span>
<span data-ttu-id="f09aa-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f09aa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f09aa-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f09aa-118">-Name</span></span>
<span data-ttu-id="f09aa-119">Имя конфигурации темы.</span><span class="sxs-lookup"><span data-stu-id="f09aa-119">Name of the tap configuration.</span></span>

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

### <span data-ttu-id="f09aa-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f09aa-120">-NetworkInterface</span></span>
<span data-ttu-id="f09aa-121">Ссылка на ресурс интерфейса сети.</span><span class="sxs-lookup"><span data-stu-id="f09aa-121">The reference of the network interface resource.</span></span>

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

### <span data-ttu-id="f09aa-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f09aa-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="f09aa-123">Ссылка на ресурс виртуального сетевого коснитесь.</span><span class="sxs-lookup"><span data-stu-id="f09aa-123">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="f09aa-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="f09aa-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="f09aa-125">Ссылка на ресурс виртуального сетевого коснитесь.</span><span class="sxs-lookup"><span data-stu-id="f09aa-125">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="f09aa-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f09aa-126">-Confirm</span></span>
<span data-ttu-id="f09aa-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f09aa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f09aa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f09aa-128">-WhatIf</span></span>
<span data-ttu-id="f09aa-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f09aa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f09aa-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f09aa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f09aa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f09aa-131">CommonParameters</span></span>
<span data-ttu-id="f09aa-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f09aa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f09aa-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f09aa-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f09aa-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f09aa-134">INPUTS</span></span>

### <span data-ttu-id="f09aa-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f09aa-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="f09aa-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f09aa-136">System.String</span></span>

### <span data-ttu-id="f09aa-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f09aa-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="f09aa-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f09aa-138">OUTPUTS</span></span>

### <span data-ttu-id="f09aa-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f09aa-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="f09aa-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f09aa-140">NOTES</span></span>

## <span data-ttu-id="f09aa-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f09aa-141">RELATED LINKS</span></span>

[<span data-ttu-id="f09aa-142">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f09aa-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="f09aa-143">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f09aa-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="f09aa-144">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f09aa-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
