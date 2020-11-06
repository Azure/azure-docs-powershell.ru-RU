---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: a805145445f8bd17ac60497e2c7d7e89ea56a3c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568983"
---
# <span data-ttu-id="f2d21-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f2d21-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="f2d21-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2d21-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2d21-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2d21-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2d21-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2d21-104">DESCRIPTION</span></span>

## <span data-ttu-id="f2d21-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2d21-105">EXAMPLES</span></span>

## <span data-ttu-id="f2d21-106">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2d21-106">PARAMETERS</span></span>

### <span data-ttu-id="f2d21-107">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2d21-107">-DefaultProfile</span></span>
<span data-ttu-id="f2d21-108">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2d21-108">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2d21-109">-Force</span><span class="sxs-lookup"><span data-stu-id="f2d21-109">-Force</span></span>
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

### <span data-ttu-id="f2d21-110">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="f2d21-110">-KeyLength</span></span>
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

### <span data-ttu-id="f2d21-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f2d21-111">-Name</span></span>
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

### <span data-ttu-id="f2d21-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2d21-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f2d21-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2d21-113">-Confirm</span></span>
<span data-ttu-id="f2d21-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f2d21-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2d21-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2d21-115">-WhatIf</span></span>
<span data-ttu-id="f2d21-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f2d21-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2d21-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f2d21-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2d21-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2d21-118">CommonParameters</span></span>
<span data-ttu-id="f2d21-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2d21-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2d21-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2d21-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2d21-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2d21-121">INPUTS</span></span>

### <span data-ttu-id="f2d21-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="f2d21-122">None</span></span>
<span data-ttu-id="f2d21-123">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f2d21-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f2d21-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2d21-124">OUTPUTS</span></span>

### <span data-ttu-id="f2d21-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f2d21-125">System.String</span></span>

## <span data-ttu-id="f2d21-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2d21-126">NOTES</span></span>

## <span data-ttu-id="f2d21-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2d21-127">RELATED LINKS</span></span>

[<span data-ttu-id="f2d21-128">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f2d21-128">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="f2d21-129">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f2d21-129">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


