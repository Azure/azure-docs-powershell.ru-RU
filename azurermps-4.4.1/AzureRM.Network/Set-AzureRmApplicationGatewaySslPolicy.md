---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 984556937e57d710b9f62d80f20f7f30955865ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562440"
---
# <span data-ttu-id="9b0fb-101">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="9b0fb-101">Set-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="9b0fb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b0fb-102">SYNOPSIS</span></span>
<span data-ttu-id="9b0fb-103">Изменяет политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="9b0fb-103">Modifies the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b0fb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b0fb-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b0fb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b0fb-105">DESCRIPTION</span></span>
<span data-ttu-id="9b0fb-106">Командлет **Set-AzureRmApplicationGatewaySslPolicy** изменяет политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="9b0fb-106">The **Set-AzureRmApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="9b0fb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b0fb-107">EXAMPLES</span></span>

### <span data-ttu-id="9b0fb-108">1:</span><span class="sxs-lookup"><span data-stu-id="9b0fb-108">1:</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="9b0fb-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9b0fb-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="9b0fb-110">Эта вторая команда изменяет политику SSL на тип предопределенной политики и имя политики AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="9b0fb-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="9b0fb-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b0fb-111">PARAMETERS</span></span>

### <span data-ttu-id="9b0fb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b0fb-112">-ApplicationGateway</span></span>
<span data-ttu-id="9b0fb-113">Определяет шлюз приложения политики SSL, измененной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9b0fb-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9b0fb-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="9b0fb-114">-CipherSuite</span></span>
<span data-ttu-id="9b0fb-115">Комплекты шифров SSL, которые должны быть включены в указанном порядке для доступа к шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="9b0fb-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="9b0fb-116">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="9b0fb-116">-DisabledSslProtocols</span></span>
<span data-ttu-id="9b0fb-117">Указывает, какие протоколы отключены.</span><span class="sxs-lookup"><span data-stu-id="9b0fb-117">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="9b0fb-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9b0fb-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9b0fb-119">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="9b0fb-119">TLSv1_0</span></span> 
- <span data-ttu-id="9b0fb-120">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="9b0fb-120">TLSv1_1</span></span> 
- <span data-ttu-id="9b0fb-121">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="9b0fb-121">TLSv1_2</span></span>

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

### <span data-ttu-id="9b0fb-122">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="9b0fb-122">-MinProtocolVersion</span></span>
<span data-ttu-id="9b0fb-123">Минимальная версия протокола SSL, поддерживаемая на шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="9b0fb-123">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="9b0fb-124">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="9b0fb-124">-PolicyName</span></span>
<span data-ttu-id="9b0fb-125">Имя предопределенной политики SSL</span><span class="sxs-lookup"><span data-stu-id="9b0fb-125">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="9b0fb-126">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="9b0fb-126">-PolicyType</span></span>
<span data-ttu-id="9b0fb-127">Тип политики SSL</span><span class="sxs-lookup"><span data-stu-id="9b0fb-127">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="9b0fb-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b0fb-128">-Confirm</span></span>
<span data-ttu-id="9b0fb-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9b0fb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b0fb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b0fb-130">-WhatIf</span></span>
<span data-ttu-id="9b0fb-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9b0fb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b0fb-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9b0fb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b0fb-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b0fb-133">-DefaultProfile</span></span>
<span data-ttu-id="9b0fb-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b0fb-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b0fb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b0fb-135">CommonParameters</span></span>
<span data-ttu-id="9b0fb-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b0fb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b0fb-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b0fb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b0fb-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b0fb-138">INPUTS</span></span>

### <span data-ttu-id="9b0fb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9b0fb-139">System.String</span></span>

## <span data-ttu-id="9b0fb-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b0fb-140">OUTPUTS</span></span>

### <span data-ttu-id="9b0fb-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b0fb-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9b0fb-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b0fb-142">NOTES</span></span>
* <span data-ttu-id="9b0fb-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="9b0fb-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9b0fb-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b0fb-144">RELATED LINKS</span></span>

[<span data-ttu-id="9b0fb-145">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="9b0fb-145">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="9b0fb-146">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="9b0fb-146">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)


