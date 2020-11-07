---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 3519fd616be92e2404ef7b4d51241b675240470c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911093"
---
# <span data-ttu-id="3b6f7-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="3b6f7-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="3b6f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b6f7-102">SYNOPSIS</span></span>

## <span data-ttu-id="3b6f7-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b6f7-103">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b6f7-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b6f7-104">DESCRIPTION</span></span>

## <span data-ttu-id="3b6f7-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b6f7-105">EXAMPLES</span></span>

### <span data-ttu-id="3b6f7-106">1:</span><span class="sxs-lookup"><span data-stu-id="3b6f7-106">1:</span></span>
```

```

## <span data-ttu-id="3b6f7-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b6f7-107">PARAMETERS</span></span>

### <span data-ttu-id="3b6f7-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b6f7-108">-DefaultProfile</span></span>
<span data-ttu-id="3b6f7-109">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b6f7-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b6f7-110">-Force</span><span class="sxs-lookup"><span data-stu-id="3b6f7-110">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b6f7-111">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="3b6f7-111">-KeyLength</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b6f7-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3b6f7-112">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b6f7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b6f7-113">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b6f7-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b6f7-114">-Confirm</span></span>
<span data-ttu-id="3b6f7-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3b6f7-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b6f7-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b6f7-116">-WhatIf</span></span>
<span data-ttu-id="3b6f7-117">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3b6f7-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b6f7-118">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3b6f7-118">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b6f7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b6f7-119">CommonParameters</span></span>
<span data-ttu-id="3b6f7-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b6f7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b6f7-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b6f7-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b6f7-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b6f7-122">INPUTS</span></span>

## <span data-ttu-id="3b6f7-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b6f7-123">OUTPUTS</span></span>

### <span data-ttu-id="3b6f7-124">System. String</span><span class="sxs-lookup"><span data-stu-id="3b6f7-124">System.String</span></span>

## <span data-ttu-id="3b6f7-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b6f7-125">NOTES</span></span>

## <span data-ttu-id="3b6f7-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b6f7-126">RELATED LINKS</span></span>

[<span data-ttu-id="3b6f7-127">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="3b6f7-127">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="3b6f7-128">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="3b6f7-128">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)


