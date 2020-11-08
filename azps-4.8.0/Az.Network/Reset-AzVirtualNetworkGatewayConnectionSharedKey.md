---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 496e5aca71d1a947b97c8fd27cab348cee9ba49b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235991"
---
# <span data-ttu-id="73f66-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="73f66-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="73f66-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73f66-102">SYNOPSIS</span></span>
<span data-ttu-id="73f66-103">Сброс общего ключа подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="73f66-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="73f66-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73f66-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73f66-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73f66-105">DESCRIPTION</span></span>
<span data-ttu-id="73f66-106">Сброс общего ключа подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="73f66-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="73f66-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73f66-107">EXAMPLES</span></span>

### <span data-ttu-id="73f66-108">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="73f66-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="73f66-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73f66-109">PARAMETERS</span></span>

### <span data-ttu-id="73f66-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f66-110">-DefaultProfile</span></span>
<span data-ttu-id="73f66-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73f66-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73f66-112">-Force</span><span class="sxs-lookup"><span data-stu-id="73f66-112">-Force</span></span>
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

### <span data-ttu-id="73f66-113">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="73f66-113">-KeyLength</span></span>
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

### <span data-ttu-id="73f66-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="73f66-114">-Name</span></span>
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

### <span data-ttu-id="73f66-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73f66-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="73f66-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73f66-116">-Confirm</span></span>
<span data-ttu-id="73f66-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="73f66-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73f66-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73f66-118">-WhatIf</span></span>
<span data-ttu-id="73f66-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="73f66-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73f66-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="73f66-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73f66-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f66-121">CommonParameters</span></span>
<span data-ttu-id="73f66-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73f66-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f66-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73f66-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f66-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73f66-124">INPUTS</span></span>

### <span data-ttu-id="73f66-125">System. String</span><span class="sxs-lookup"><span data-stu-id="73f66-125">System.String</span></span>

### <span data-ttu-id="73f66-126">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="73f66-126">System.UInt32</span></span>

## <span data-ttu-id="73f66-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73f66-127">OUTPUTS</span></span>

### <span data-ttu-id="73f66-128">System. String</span><span class="sxs-lookup"><span data-stu-id="73f66-128">System.String</span></span>

## <span data-ttu-id="73f66-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="73f66-129">NOTES</span></span>

## <span data-ttu-id="73f66-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73f66-130">RELATED LINKS</span></span>

[<span data-ttu-id="73f66-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="73f66-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="73f66-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="73f66-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
