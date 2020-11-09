---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 496e5aca71d1a947b97c8fd27cab348cee9ba49b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245954"
---
# <span data-ttu-id="f815c-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f815c-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="f815c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f815c-102">SYNOPSIS</span></span>
<span data-ttu-id="f815c-103">Сброс общего ключа подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f815c-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="f815c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f815c-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f815c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f815c-105">DESCRIPTION</span></span>
<span data-ttu-id="f815c-106">Сброс общего ключа подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f815c-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="f815c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f815c-107">EXAMPLES</span></span>

### <span data-ttu-id="f815c-108">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="f815c-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="f815c-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f815c-109">PARAMETERS</span></span>

### <span data-ttu-id="f815c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f815c-110">-DefaultProfile</span></span>
<span data-ttu-id="f815c-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f815c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f815c-112">-Force</span><span class="sxs-lookup"><span data-stu-id="f815c-112">-Force</span></span>
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

### <span data-ttu-id="f815c-113">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="f815c-113">-KeyLength</span></span>
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

### <span data-ttu-id="f815c-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f815c-114">-Name</span></span>
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

### <span data-ttu-id="f815c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f815c-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f815c-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f815c-116">-Confirm</span></span>
<span data-ttu-id="f815c-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f815c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f815c-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f815c-118">-WhatIf</span></span>
<span data-ttu-id="f815c-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f815c-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f815c-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f815c-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f815c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f815c-121">CommonParameters</span></span>
<span data-ttu-id="f815c-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f815c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f815c-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f815c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f815c-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f815c-124">INPUTS</span></span>

### <span data-ttu-id="f815c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f815c-125">System.String</span></span>

### <span data-ttu-id="f815c-126">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="f815c-126">System.UInt32</span></span>

## <span data-ttu-id="f815c-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f815c-127">OUTPUTS</span></span>

### <span data-ttu-id="f815c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f815c-128">System.String</span></span>

## <span data-ttu-id="f815c-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="f815c-129">NOTES</span></span>

## <span data-ttu-id="f815c-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f815c-130">RELATED LINKS</span></span>

[<span data-ttu-id="f815c-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f815c-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="f815c-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f815c-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)