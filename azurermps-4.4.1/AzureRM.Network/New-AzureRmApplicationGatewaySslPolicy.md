---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: dc6dc0c201ebb8298805064e06af5bb6c63ceda8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563887"
---
# <span data-ttu-id="67954-101">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="67954-101">New-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="67954-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67954-102">SYNOPSIS</span></span>
<span data-ttu-id="67954-103">Создает политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="67954-103">Creates an SSL policy for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67954-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67954-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67954-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67954-105">DESCRIPTION</span></span>
<span data-ttu-id="67954-106">Командлет **New-AzureRmApplicationGatewaySslPolicy** создает политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="67954-106">The **New-AzureRmApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="67954-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67954-107">EXAMPLES</span></span>

### <span data-ttu-id="67954-108">1:</span><span class="sxs-lookup"><span data-stu-id="67954-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzureRmApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="67954-109">Эта команда создает специальную политику.</span><span class="sxs-lookup"><span data-stu-id="67954-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="67954-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67954-110">PARAMETERS</span></span>

### <span data-ttu-id="67954-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="67954-111">-CipherSuite</span></span>
<span data-ttu-id="67954-112">Комплекты шифров SSL, которые должны быть включены в указанном порядке для доступа к шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="67954-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="67954-113">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="67954-113">-DisabledSslProtocols</span></span>
<span data-ttu-id="67954-114">Указывает, какие протоколы отключены.</span><span class="sxs-lookup"><span data-stu-id="67954-114">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="67954-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="67954-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67954-116">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="67954-116">TLSv1_0</span></span> 
- <span data-ttu-id="67954-117">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="67954-117">TLSv1_1</span></span> 
- <span data-ttu-id="67954-118">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="67954-118">TLSv1_2</span></span>

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

### <span data-ttu-id="67954-119">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="67954-119">-MinProtocolVersion</span></span>
<span data-ttu-id="67954-120">Минимальная версия протокола SSL, поддерживаемая на шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="67954-120">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="67954-121">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="67954-121">-PolicyName</span></span>
<span data-ttu-id="67954-122">Имя предопределенной политики SSL</span><span class="sxs-lookup"><span data-stu-id="67954-122">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="67954-123">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="67954-123">-PolicyType</span></span>
<span data-ttu-id="67954-124">Тип политики SSL</span><span class="sxs-lookup"><span data-stu-id="67954-124">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="67954-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67954-125">-Confirm</span></span>
<span data-ttu-id="67954-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="67954-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67954-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67954-127">-WhatIf</span></span>
<span data-ttu-id="67954-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="67954-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67954-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="67954-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67954-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67954-130">-DefaultProfile</span></span>
<span data-ttu-id="67954-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67954-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67954-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67954-132">CommonParameters</span></span>
<span data-ttu-id="67954-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67954-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67954-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67954-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67954-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67954-135">INPUTS</span></span>

### <span data-ttu-id="67954-136">System. String</span><span class="sxs-lookup"><span data-stu-id="67954-136">System.String</span></span>

## <span data-ttu-id="67954-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67954-137">OUTPUTS</span></span>

### <span data-ttu-id="67954-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="67954-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="67954-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="67954-139">NOTES</span></span>
* <span data-ttu-id="67954-140">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="67954-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="67954-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67954-141">RELATED LINKS</span></span>

[<span data-ttu-id="67954-142">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="67954-142">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="67954-143">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="67954-143">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


