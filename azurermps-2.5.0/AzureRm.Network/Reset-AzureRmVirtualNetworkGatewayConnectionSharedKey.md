---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
ms.openlocfilehash: 160fb1b7455a2440773978ec80741922248a8af4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915066"
---
# <span data-ttu-id="76744-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="76744-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="76744-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76744-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76744-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76744-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76744-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76744-104">DESCRIPTION</span></span>

## <span data-ttu-id="76744-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76744-105">EXAMPLES</span></span>

### <span data-ttu-id="76744-106">1:</span><span class="sxs-lookup"><span data-stu-id="76744-106">1:</span></span>
```

```

## <span data-ttu-id="76744-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76744-107">PARAMETERS</span></span>

### <span data-ttu-id="76744-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76744-108">-DefaultProfile</span></span>
<span data-ttu-id="76744-109">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76744-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76744-110">-Force</span><span class="sxs-lookup"><span data-stu-id="76744-110">-Force</span></span>
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

### <span data-ttu-id="76744-111">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="76744-111">-KeyLength</span></span>
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

### <span data-ttu-id="76744-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="76744-112">-Name</span></span>
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

### <span data-ttu-id="76744-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76744-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="76744-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76744-114">-Confirm</span></span>
<span data-ttu-id="76744-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="76744-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76744-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76744-116">-WhatIf</span></span>
<span data-ttu-id="76744-117">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="76744-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76744-118">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="76744-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76744-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76744-119">CommonParameters</span></span>
<span data-ttu-id="76744-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76744-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76744-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76744-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76744-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76744-122">INPUTS</span></span>

## <span data-ttu-id="76744-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76744-123">OUTPUTS</span></span>

### <span data-ttu-id="76744-124">System. String</span><span class="sxs-lookup"><span data-stu-id="76744-124">System.String</span></span>

## <span data-ttu-id="76744-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="76744-125">NOTES</span></span>

## <span data-ttu-id="76744-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76744-126">RELATED LINKS</span></span>

[<span data-ttu-id="76744-127">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="76744-127">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="76744-128">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="76744-128">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


