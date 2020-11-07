---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bf11b2b3010a7f7683d670c3c5e95d4248b83cd6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909581"
---
# <span data-ttu-id="56510-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="56510-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="56510-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56510-102">SYNOPSIS</span></span>
<span data-ttu-id="56510-103">Удаляет сертификат проверки подлинности из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="56510-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="56510-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56510-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56510-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56510-105">DESCRIPTION</span></span>
<span data-ttu-id="56510-106">Командлет **Remove-AzApplicationGatewayAuthenticationCertificate** Удаляет сертификат для проверки подлинности из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="56510-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="56510-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56510-107">EXAMPLES</span></span>

### <span data-ttu-id="56510-108">1:</span><span class="sxs-lookup"><span data-stu-id="56510-108">1:</span></span>
```

```

## <span data-ttu-id="56510-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56510-109">PARAMETERS</span></span>

### <span data-ttu-id="56510-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="56510-110">-ApplicationGateway</span></span>
<span data-ttu-id="56510-111">Указывает имя шлюза приложений, из которого этот командлет удаляет сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="56510-111">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="56510-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56510-112">-DefaultProfile</span></span>
<span data-ttu-id="56510-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56510-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56510-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="56510-114">-Name</span></span>
<span data-ttu-id="56510-115">Указывает имя сертификата для проверки подлинности, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="56510-115">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="56510-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56510-116">-Confirm</span></span>
<span data-ttu-id="56510-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="56510-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56510-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56510-118">-WhatIf</span></span>
<span data-ttu-id="56510-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="56510-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56510-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="56510-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56510-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56510-121">CommonParameters</span></span>
<span data-ttu-id="56510-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56510-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56510-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56510-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56510-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56510-124">INPUTS</span></span>

### <span data-ttu-id="56510-125">System. String</span><span class="sxs-lookup"><span data-stu-id="56510-125">System.String</span></span>

## <span data-ttu-id="56510-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56510-126">OUTPUTS</span></span>

### <span data-ttu-id="56510-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="56510-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="56510-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="56510-128">NOTES</span></span>
* <span data-ttu-id="56510-129">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="56510-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="56510-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56510-130">RELATED LINKS</span></span>

[<span data-ttu-id="56510-131">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="56510-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="56510-132">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="56510-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="56510-133">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="56510-133">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="56510-134">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="56510-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


