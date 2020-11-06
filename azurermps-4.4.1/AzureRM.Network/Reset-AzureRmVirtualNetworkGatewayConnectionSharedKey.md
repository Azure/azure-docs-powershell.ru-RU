---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 65540c331074b5c140bafe9e87d625dfaec2f252
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570351"
---
# <span data-ttu-id="ebabe-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ebabe-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="ebabe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebabe-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebabe-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebabe-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ebabe-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebabe-104">DESCRIPTION</span></span>

## <span data-ttu-id="ebabe-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebabe-105">EXAMPLES</span></span>

## <span data-ttu-id="ebabe-106">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebabe-106">PARAMETERS</span></span>

### <span data-ttu-id="ebabe-107">-Force</span><span class="sxs-lookup"><span data-stu-id="ebabe-107">-Force</span></span>
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

### <span data-ttu-id="ebabe-108">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="ebabe-108">-KeyLength</span></span>
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

### <span data-ttu-id="ebabe-109">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ebabe-109">-Name</span></span>
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

### <span data-ttu-id="ebabe-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebabe-110">-ResourceGroupName</span></span>
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

### <span data-ttu-id="ebabe-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebabe-111">-Confirm</span></span>
<span data-ttu-id="ebabe-112">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ebabe-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebabe-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebabe-113">-WhatIf</span></span>
<span data-ttu-id="ebabe-114">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ebabe-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebabe-115">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ebabe-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebabe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebabe-116">-DefaultProfile</span></span>
<span data-ttu-id="ebabe-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebabe-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebabe-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebabe-118">CommonParameters</span></span>
<span data-ttu-id="ebabe-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebabe-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebabe-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebabe-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebabe-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebabe-121">INPUTS</span></span>

## <span data-ttu-id="ebabe-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebabe-122">OUTPUTS</span></span>

### <span data-ttu-id="ebabe-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ebabe-123">System.String</span></span>

## <span data-ttu-id="ebabe-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebabe-124">NOTES</span></span>

## <span data-ttu-id="ebabe-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebabe-125">RELATED LINKS</span></span>

[<span data-ttu-id="ebabe-126">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ebabe-126">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="ebabe-127">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ebabe-127">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


