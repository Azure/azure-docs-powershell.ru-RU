---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 7b82cf189d912d000c143b20cca76c4f2683b7d1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914030"
---
# <span data-ttu-id="266c1-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="266c1-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="266c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="266c1-102">SYNOPSIS</span></span>
<span data-ttu-id="266c1-103">Удаляет пул серверных адресов из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="266c1-103">Removes a back-end address pool from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="266c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="266c1-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="266c1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="266c1-105">DESCRIPTION</span></span>
<span data-ttu-id="266c1-106">Командлет **Remove-AzureRmApplicationGatewayBackendAddressPool** удаляет пул серверных адресов из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="266c1-106">The **Remove-AzureRmApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="266c1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="266c1-107">EXAMPLES</span></span>

### <span data-ttu-id="266c1-108">Пример 1: Удаление пула конечных адресов из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="266c1-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="266c1-109">Первая команда получает шлюз приложения с именем ApplicationGateway01, принадлежащий группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="266c1-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>

<span data-ttu-id="266c1-110">Вторая команда удаляет пул серверных адресов с именем BackEndPool02 из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="266c1-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="266c1-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="266c1-111">PARAMETERS</span></span>

### <span data-ttu-id="266c1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="266c1-112">-ApplicationGateway</span></span>
<span data-ttu-id="266c1-113">Указывает шлюз приложений, из которого этот командлет удаляет пул из заднего серверного адреса.</span><span class="sxs-lookup"><span data-stu-id="266c1-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="266c1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="266c1-114">-DefaultProfile</span></span>
<span data-ttu-id="266c1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="266c1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="266c1-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="266c1-116">-Name</span></span>
<span data-ttu-id="266c1-117">Указывает имя пула серверных адресов, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="266c1-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="266c1-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="266c1-118">-Confirm</span></span>
<span data-ttu-id="266c1-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="266c1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="266c1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="266c1-120">-WhatIf</span></span>
<span data-ttu-id="266c1-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="266c1-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="266c1-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="266c1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="266c1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="266c1-123">CommonParameters</span></span>
<span data-ttu-id="266c1-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="266c1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="266c1-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="266c1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="266c1-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="266c1-126">INPUTS</span></span>

### <span data-ttu-id="266c1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="266c1-127">System.String</span></span>

## <span data-ttu-id="266c1-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="266c1-128">OUTPUTS</span></span>

### <span data-ttu-id="266c1-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="266c1-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="266c1-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="266c1-130">NOTES</span></span>

## <span data-ttu-id="266c1-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="266c1-131">RELATED LINKS</span></span>

[<span data-ttu-id="266c1-132">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="266c1-132">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="266c1-133">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="266c1-133">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="266c1-134">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="266c1-134">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="266c1-135">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="266c1-135">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


