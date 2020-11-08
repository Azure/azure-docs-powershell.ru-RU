---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 06b8f7bdaea4ebf11ff901fbe53be94f74c9bba7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245946"
---
# <span data-ttu-id="95b64-101">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="95b64-101">Set-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="95b64-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95b64-102">SYNOPSIS</span></span>
<span data-ttu-id="95b64-103">Изменяет политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="95b64-103">Modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="95b64-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95b64-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-DisabledSslProtocols <String[]>]
 [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95b64-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95b64-105">DESCRIPTION</span></span>
<span data-ttu-id="95b64-106">Командлет **Set-AzApplicationGatewaySslPolicy** изменяет политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="95b64-106">The **Set-AzApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="95b64-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95b64-107">EXAMPLES</span></span>

### <span data-ttu-id="95b64-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="95b64-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="95b64-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="95b64-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="95b64-110">Эта вторая команда изменяет политику SSL на тип предопределенной политики и имя политики AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="95b64-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="95b64-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95b64-111">PARAMETERS</span></span>

### <span data-ttu-id="95b64-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95b64-112">-ApplicationGateway</span></span>
<span data-ttu-id="95b64-113">Определяет шлюз приложения политики SSL, измененной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="95b64-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="95b64-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="95b64-114">-CipherSuite</span></span>
<span data-ttu-id="95b64-115">Комплекты шифров SSL, которые должны быть включены в указанном порядке для доступа к шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="95b64-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95b64-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95b64-116">-DefaultProfile</span></span>
<span data-ttu-id="95b64-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95b64-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95b64-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="95b64-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="95b64-119">Указывает, какие протоколы отключены.</span><span class="sxs-lookup"><span data-stu-id="95b64-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="95b64-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="95b64-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95b64-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="95b64-121">TLSv1_0</span></span> 
- <span data-ttu-id="95b64-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="95b64-122">TLSv1_1</span></span> 
- <span data-ttu-id="95b64-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="95b64-123">TLSv1_2</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95b64-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="95b64-124">-MinProtocolVersion</span></span>
<span data-ttu-id="95b64-125">Минимальная версия протокола SSL, поддерживаемая на шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="95b64-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="95b64-126">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="95b64-126">-PolicyName</span></span>
<span data-ttu-id="95b64-127">Имя предопределенной политики SSL</span><span class="sxs-lookup"><span data-stu-id="95b64-127">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="95b64-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="95b64-128">-PolicyType</span></span>
<span data-ttu-id="95b64-129">Тип политики SSL</span><span class="sxs-lookup"><span data-stu-id="95b64-129">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="95b64-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95b64-130">-Confirm</span></span>
<span data-ttu-id="95b64-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="95b64-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95b64-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95b64-132">-WhatIf</span></span>
<span data-ttu-id="95b64-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="95b64-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95b64-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="95b64-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95b64-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95b64-135">CommonParameters</span></span>
<span data-ttu-id="95b64-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95b64-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95b64-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95b64-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95b64-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95b64-138">INPUTS</span></span>

### <span data-ttu-id="95b64-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95b64-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="95b64-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95b64-140">OUTPUTS</span></span>

### <span data-ttu-id="95b64-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95b64-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="95b64-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="95b64-142">NOTES</span></span>
* <span data-ttu-id="95b64-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="95b64-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="95b64-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95b64-144">RELATED LINKS</span></span>

[<span data-ttu-id="95b64-145">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="95b64-145">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="95b64-146">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="95b64-146">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)


