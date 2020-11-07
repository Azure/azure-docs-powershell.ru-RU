---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: a1a6fd8a6c638cf9b7b5b516d12fc7c24ce0cd4f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909717"
---
# <span data-ttu-id="e860b-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e860b-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="e860b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e860b-102">SYNOPSIS</span></span>
<span data-ttu-id="e860b-103">Создает политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="e860b-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="e860b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e860b-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e860b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e860b-105">DESCRIPTION</span></span>
<span data-ttu-id="e860b-106">Командлет **New-AzApplicationGatewaySslPolicy** создает политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="e860b-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="e860b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e860b-107">EXAMPLES</span></span>

### <span data-ttu-id="e860b-108">1:</span><span class="sxs-lookup"><span data-stu-id="e860b-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="e860b-109">Эта команда создает специальную политику.</span><span class="sxs-lookup"><span data-stu-id="e860b-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="e860b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e860b-110">PARAMETERS</span></span>

### <span data-ttu-id="e860b-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="e860b-111">-CipherSuite</span></span>
<span data-ttu-id="e860b-112">Комплекты шифров SSL, которые должны быть включены в указанном порядке для доступа к шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="e860b-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="e860b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e860b-113">-DefaultProfile</span></span>
<span data-ttu-id="e860b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e860b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e860b-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="e860b-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="e860b-116">Указывает, какие протоколы отключены.</span><span class="sxs-lookup"><span data-stu-id="e860b-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="e860b-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e860b-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e860b-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="e860b-118">TLSv1_0</span></span> 
- <span data-ttu-id="e860b-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="e860b-119">TLSv1_1</span></span> 
- <span data-ttu-id="e860b-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="e860b-120">TLSv1_2</span></span>

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

### <span data-ttu-id="e860b-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="e860b-121">-MinProtocolVersion</span></span>
<span data-ttu-id="e860b-122">Минимальная версия протокола SSL, поддерживаемая на шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="e860b-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e860b-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="e860b-123">-PolicyName</span></span>
<span data-ttu-id="e860b-124">Имя предопределенной политики SSL</span><span class="sxs-lookup"><span data-stu-id="e860b-124">Name of Ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e860b-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="e860b-125">-PolicyType</span></span>
<span data-ttu-id="e860b-126">Тип политики SSL</span><span class="sxs-lookup"><span data-stu-id="e860b-126">Type of Ssl Policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e860b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e860b-127">-Confirm</span></span>
<span data-ttu-id="e860b-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e860b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e860b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e860b-129">-WhatIf</span></span>
<span data-ttu-id="e860b-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e860b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e860b-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e860b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e860b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e860b-132">CommonParameters</span></span>
<span data-ttu-id="e860b-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e860b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e860b-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e860b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e860b-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e860b-135">INPUTS</span></span>

### <span data-ttu-id="e860b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e860b-136">System.String</span></span>

## <span data-ttu-id="e860b-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e860b-137">OUTPUTS</span></span>

### <span data-ttu-id="e860b-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e860b-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="e860b-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="e860b-139">NOTES</span></span>
* <span data-ttu-id="e860b-140">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="e860b-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e860b-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e860b-141">RELATED LINKS</span></span>

[<span data-ttu-id="e860b-142">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e860b-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="e860b-143">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e860b-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


