---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 496e5aca71d1a947b97c8fd27cab348cee9ba49b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519924"
---
# <span data-ttu-id="50881-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="50881-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="50881-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50881-102">SYNOPSIS</span></span>
<span data-ttu-id="50881-103">Сбрасывает общий ключ подключения виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="50881-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="50881-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="50881-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50881-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50881-105">DESCRIPTION</span></span>
<span data-ttu-id="50881-106">Сбрасывает общий ключ подключения виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="50881-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="50881-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="50881-107">EXAMPLES</span></span>

### <span data-ttu-id="50881-108">Пример 1.</span><span class="sxs-lookup"><span data-stu-id="50881-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="50881-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50881-109">PARAMETERS</span></span>

### <span data-ttu-id="50881-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50881-110">-DefaultProfile</span></span>
<span data-ttu-id="50881-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50881-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50881-112">-Force</span><span class="sxs-lookup"><span data-stu-id="50881-112">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50881-113">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="50881-113">-KeyLength</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50881-114">-Name</span><span class="sxs-lookup"><span data-stu-id="50881-114">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50881-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50881-115">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50881-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50881-116">-Confirm</span></span>
<span data-ttu-id="50881-117">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="50881-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50881-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50881-118">-WhatIf</span></span>
<span data-ttu-id="50881-119">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50881-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50881-120">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="50881-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50881-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50881-121">CommonParameters</span></span>
<span data-ttu-id="50881-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50881-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50881-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50881-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50881-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50881-124">INPUTS</span></span>

### <span data-ttu-id="50881-125">System.String</span><span class="sxs-lookup"><span data-stu-id="50881-125">System.String</span></span>

### <span data-ttu-id="50881-126">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="50881-126">System.UInt32</span></span>

## <span data-ttu-id="50881-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="50881-127">OUTPUTS</span></span>

### <span data-ttu-id="50881-128">System.String</span><span class="sxs-lookup"><span data-stu-id="50881-128">System.String</span></span>

## <span data-ttu-id="50881-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="50881-129">NOTES</span></span>

## <span data-ttu-id="50881-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50881-130">RELATED LINKS</span></span>

[<span data-ttu-id="50881-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="50881-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="50881-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="50881-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
