---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: c482f3e4e7882f32db3415a36aab0a0313c0085a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556615"
---
# <span data-ttu-id="9ddf7-101">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="9ddf7-101">Set-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="9ddf7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ddf7-102">SYNOPSIS</span></span>
<span data-ttu-id="9ddf7-103">Изменяет политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="9ddf7-103">Modifies the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ddf7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ddf7-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ddf7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ddf7-105">DESCRIPTION</span></span>
<span data-ttu-id="9ddf7-106">Командлет **Set-AzureRmApplicationGatewaySslPolicy** изменяет политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="9ddf7-106">The **Set-AzureRmApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="9ddf7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ddf7-107">EXAMPLES</span></span>

### <span data-ttu-id="9ddf7-108">1:</span><span class="sxs-lookup"><span data-stu-id="9ddf7-108">1:</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="9ddf7-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9ddf7-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9ddf7-110">Эта вторая команда изменяет политику SSL на тип предопределенной политики и имя политики AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="9ddf7-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="9ddf7-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ddf7-111">PARAMETERS</span></span>

### <span data-ttu-id="9ddf7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ddf7-112">-ApplicationGateway</span></span>
<span data-ttu-id="9ddf7-113">Определяет шлюз приложения политики SSL, измененной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9ddf7-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ddf7-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="9ddf7-114">-CipherSuite</span></span>
<span data-ttu-id="9ddf7-115">Комплекты шифров SSL, которые должны быть включены в указанном порядке для доступа к шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="9ddf7-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddf7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ddf7-116">-DefaultProfile</span></span>
<span data-ttu-id="9ddf7-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ddf7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ddf7-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="9ddf7-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="9ddf7-119">Указывает, какие протоколы отключены.</span><span class="sxs-lookup"><span data-stu-id="9ddf7-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="9ddf7-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9ddf7-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9ddf7-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="9ddf7-121">TLSv1_0</span></span> 
- <span data-ttu-id="9ddf7-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="9ddf7-122">TLSv1_1</span></span> 
- <span data-ttu-id="9ddf7-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="9ddf7-123">TLSv1_2</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddf7-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="9ddf7-124">-MinProtocolVersion</span></span>
<span data-ttu-id="9ddf7-125">Минимальная версия протокола SSL, поддерживаемая на шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="9ddf7-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddf7-126">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="9ddf7-126">-PolicyName</span></span>
<span data-ttu-id="9ddf7-127">Имя предопределенной политики SSL</span><span class="sxs-lookup"><span data-stu-id="9ddf7-127">Name of Ssl predefined policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddf7-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="9ddf7-128">-PolicyType</span></span>
<span data-ttu-id="9ddf7-129">Тип политики SSL</span><span class="sxs-lookup"><span data-stu-id="9ddf7-129">Type of Ssl Policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddf7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ddf7-130">-Confirm</span></span>
<span data-ttu-id="9ddf7-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9ddf7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ddf7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ddf7-132">-WhatIf</span></span>
<span data-ttu-id="9ddf7-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9ddf7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ddf7-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9ddf7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ddf7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ddf7-135">CommonParameters</span></span>
<span data-ttu-id="9ddf7-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ddf7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ddf7-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ddf7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ddf7-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ddf7-138">INPUTS</span></span>

### <span data-ttu-id="9ddf7-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ddf7-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="9ddf7-140">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9ddf7-140">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="9ddf7-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ddf7-141">OUTPUTS</span></span>

### <span data-ttu-id="9ddf7-142">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ddf7-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9ddf7-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ddf7-143">NOTES</span></span>
* <span data-ttu-id="9ddf7-144">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="9ddf7-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9ddf7-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ddf7-145">RELATED LINKS</span></span>

[<span data-ttu-id="9ddf7-146">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="9ddf7-146">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="9ddf7-147">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="9ddf7-147">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)


