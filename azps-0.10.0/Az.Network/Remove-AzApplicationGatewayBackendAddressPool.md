---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: a9346f3ff990007ed1033032d111e5851a2ac534
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909577"
---
# <span data-ttu-id="ecba5-101">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ecba5-101">Remove-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="ecba5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ecba5-102">SYNOPSIS</span></span>
<span data-ttu-id="ecba5-103">Удаляет пул серверных адресов из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="ecba5-103">Removes a back-end address pool from an application gateway.</span></span>

## <span data-ttu-id="ecba5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ecba5-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecba5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecba5-105">DESCRIPTION</span></span>
<span data-ttu-id="ecba5-106">Командлет **Remove-AzApplicationGatewayBackendAddressPool** удаляет пул серверных адресов из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="ecba5-106">The **Remove-AzApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="ecba5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ecba5-107">EXAMPLES</span></span>

### <span data-ttu-id="ecba5-108">Пример 1: Удаление пула конечных адресов из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="ecba5-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="ecba5-109">Первая команда получает шлюз приложения с именем ApplicationGateway01, принадлежащий группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ecba5-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>

<span data-ttu-id="ecba5-110">Вторая команда удаляет пул серверных адресов с именем BackEndPool02 из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="ecba5-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="ecba5-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ecba5-111">PARAMETERS</span></span>

### <span data-ttu-id="ecba5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ecba5-112">-ApplicationGateway</span></span>
<span data-ttu-id="ecba5-113">Указывает шлюз приложений, из которого этот командлет удаляет пул из заднего серверного адреса.</span><span class="sxs-lookup"><span data-stu-id="ecba5-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecba5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecba5-114">-DefaultProfile</span></span>
<span data-ttu-id="ecba5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ecba5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecba5-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ecba5-116">-Name</span></span>
<span data-ttu-id="ecba5-117">Указывает имя пула серверных адресов, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ecba5-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecba5-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecba5-118">-Confirm</span></span>
<span data-ttu-id="ecba5-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ecba5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecba5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecba5-120">-WhatIf</span></span>
<span data-ttu-id="ecba5-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ecba5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecba5-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ecba5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecba5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecba5-123">CommonParameters</span></span>
<span data-ttu-id="ecba5-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ecba5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecba5-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecba5-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecba5-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ecba5-126">INPUTS</span></span>

### <span data-ttu-id="ecba5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ecba5-127">System.String</span></span>

## <span data-ttu-id="ecba5-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecba5-128">OUTPUTS</span></span>

### <span data-ttu-id="ecba5-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ecba5-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="ecba5-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="ecba5-130">NOTES</span></span>

## <span data-ttu-id="ecba5-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ecba5-131">RELATED LINKS</span></span>

[<span data-ttu-id="ecba5-132">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ecba5-132">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ecba5-133">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ecba5-133">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ecba5-134">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ecba5-134">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ecba5-135">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ecba5-135">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


