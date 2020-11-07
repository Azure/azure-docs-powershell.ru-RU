---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 3c70fcd0e04b566ff1cd3297525d3ed2c9ed95ba
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915045"
---
# <span data-ttu-id="f76ac-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f76ac-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="f76ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f76ac-102">SYNOPSIS</span></span>
<span data-ttu-id="f76ac-103">Обновляет сертификат проверки подлинности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="f76ac-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f76ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f76ac-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f76ac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f76ac-105">DESCRIPTION</span></span>
<span data-ttu-id="f76ac-106">Командлет **Set-AzureRmApplicationGatewayAuthenticationCertificate** обновляет сертификат проверки подлинности для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="f76ac-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="f76ac-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f76ac-107">EXAMPLES</span></span>

### <span data-ttu-id="f76ac-108">1:</span><span class="sxs-lookup"><span data-stu-id="f76ac-108">1:</span></span>
```

```

## <span data-ttu-id="f76ac-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f76ac-109">PARAMETERS</span></span>

### <span data-ttu-id="f76ac-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f76ac-110">-ApplicationGateway</span></span>
<span data-ttu-id="f76ac-111">Указывает имя шлюза приложений, для которого этот командлет обновляет сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="f76ac-111">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="f76ac-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f76ac-112">-CertificateFile</span></span>
<span data-ttu-id="f76ac-113">Задает путь к файлу сертификата проверки подлинности, с помощью которого этот командлет обновляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="f76ac-113">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="f76ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f76ac-114">-DefaultProfile</span></span>
<span data-ttu-id="f76ac-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f76ac-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f76ac-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f76ac-116">-Name</span></span>
<span data-ttu-id="f76ac-117">Указывает имя сертификата проверки подлинности, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f76ac-117">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="f76ac-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f76ac-118">-Confirm</span></span>
<span data-ttu-id="f76ac-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f76ac-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f76ac-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f76ac-120">-WhatIf</span></span>
<span data-ttu-id="f76ac-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f76ac-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f76ac-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f76ac-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f76ac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f76ac-123">CommonParameters</span></span>
<span data-ttu-id="f76ac-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f76ac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f76ac-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f76ac-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f76ac-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f76ac-126">INPUTS</span></span>

### <span data-ttu-id="f76ac-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f76ac-127">System.String</span></span>

## <span data-ttu-id="f76ac-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f76ac-128">OUTPUTS</span></span>

### <span data-ttu-id="f76ac-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f76ac-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f76ac-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="f76ac-130">NOTES</span></span>
* <span data-ttu-id="f76ac-131">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="f76ac-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f76ac-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f76ac-132">RELATED LINKS</span></span>

[<span data-ttu-id="f76ac-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f76ac-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f76ac-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f76ac-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f76ac-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f76ac-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f76ac-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f76ac-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)


