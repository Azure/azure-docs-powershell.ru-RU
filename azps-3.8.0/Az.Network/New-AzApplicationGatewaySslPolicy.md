---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 758dddc18e029aadd1e3d548d613a07abd7fd565
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074776"
---
# <span data-ttu-id="55293-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="55293-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="55293-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55293-102">SYNOPSIS</span></span>
<span data-ttu-id="55293-103">Создает политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="55293-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="55293-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55293-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy [-DisabledSslProtocols <String[]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55293-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55293-105">DESCRIPTION</span></span>
<span data-ttu-id="55293-106">Командлет **New-AzApplicationGatewaySslPolicy** создает политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="55293-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="55293-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55293-107">EXAMPLES</span></span>

### <span data-ttu-id="55293-108">1:</span><span class="sxs-lookup"><span data-stu-id="55293-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="55293-109">Эта команда создает специальную политику.</span><span class="sxs-lookup"><span data-stu-id="55293-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="55293-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55293-110">PARAMETERS</span></span>

### <span data-ttu-id="55293-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="55293-111">-CipherSuite</span></span>
<span data-ttu-id="55293-112">Комплекты шифров SSL, которые должны быть включены в указанном порядке для доступа к шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="55293-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="55293-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55293-113">-DefaultProfile</span></span>
<span data-ttu-id="55293-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55293-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55293-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="55293-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="55293-116">Указывает, какие протоколы отключены.</span><span class="sxs-lookup"><span data-stu-id="55293-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="55293-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="55293-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="55293-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="55293-118">TLSv1_0</span></span> 
- <span data-ttu-id="55293-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="55293-119">TLSv1_1</span></span> 
- <span data-ttu-id="55293-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="55293-120">TLSv1_2</span></span>

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

### <span data-ttu-id="55293-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="55293-121">-MinProtocolVersion</span></span>
<span data-ttu-id="55293-122">Минимальная версия протокола SSL, поддерживаемая на шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="55293-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="55293-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="55293-123">-PolicyName</span></span>
<span data-ttu-id="55293-124">Имя предопределенной политики SSL</span><span class="sxs-lookup"><span data-stu-id="55293-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="55293-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="55293-125">-PolicyType</span></span>
<span data-ttu-id="55293-126">Тип политики SSL</span><span class="sxs-lookup"><span data-stu-id="55293-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="55293-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55293-127">-Confirm</span></span>
<span data-ttu-id="55293-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="55293-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55293-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55293-129">-WhatIf</span></span>
<span data-ttu-id="55293-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="55293-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55293-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="55293-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55293-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55293-132">CommonParameters</span></span>
<span data-ttu-id="55293-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55293-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55293-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55293-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55293-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55293-135">INPUTS</span></span>

### <span data-ttu-id="55293-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="55293-136">None</span></span>

## <span data-ttu-id="55293-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55293-137">OUTPUTS</span></span>

### <span data-ttu-id="55293-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="55293-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="55293-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="55293-139">NOTES</span></span>
* <span data-ttu-id="55293-140">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="55293-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="55293-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55293-141">RELATED LINKS</span></span>

[<span data-ttu-id="55293-142">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="55293-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="55293-143">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="55293-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


