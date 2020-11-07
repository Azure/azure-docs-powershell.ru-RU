---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 4d664018592f05203c684a896f0a0701940301a6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914105"
---
# <span data-ttu-id="c2d2b-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c2d2b-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="c2d2b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2d2b-102">SYNOPSIS</span></span>
<span data-ttu-id="c2d2b-103">Добавляет сертификат проверки подлинности в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="c2d2b-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2d2b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2d2b-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2d2b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2d2b-105">DESCRIPTION</span></span>
<span data-ttu-id="c2d2b-106">Командлет **Add-AzureRmApplicationGatewayAuthenticationCertificate** добавляет сертификат проверки подлинности в шлюз приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="c2d2b-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="c2d2b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2d2b-107">EXAMPLES</span></span>

### <span data-ttu-id="c2d2b-108">1:</span><span class="sxs-lookup"><span data-stu-id="c2d2b-108">1:</span></span>
```

```

## <span data-ttu-id="c2d2b-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2d2b-109">PARAMETERS</span></span>

### <span data-ttu-id="c2d2b-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c2d2b-110">-ApplicationGateway</span></span>
<span data-ttu-id="c2d2b-111">Указывает имя шлюза приложений, для которого этот командлет добавляет сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="c2d2b-111">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="c2d2b-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="c2d2b-112">-CertificateFile</span></span>
<span data-ttu-id="c2d2b-113">Указывает путь к сертификату проверки подлинности, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c2d2b-113">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="c2d2b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2d2b-114">-DefaultProfile</span></span>
<span data-ttu-id="c2d2b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2d2b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2d2b-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c2d2b-116">-Name</span></span>
<span data-ttu-id="c2d2b-117">Указывает имя сертификата, который добавляется этим командлетом в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="c2d2b-117">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="c2d2b-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2d2b-118">-Confirm</span></span>
<span data-ttu-id="c2d2b-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c2d2b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2d2b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2d2b-120">-WhatIf</span></span>
<span data-ttu-id="c2d2b-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c2d2b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2d2b-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c2d2b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2d2b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2d2b-123">CommonParameters</span></span>
<span data-ttu-id="c2d2b-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2d2b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2d2b-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2d2b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2d2b-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2d2b-126">INPUTS</span></span>

### <span data-ttu-id="c2d2b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c2d2b-127">System.String</span></span>

## <span data-ttu-id="c2d2b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2d2b-128">OUTPUTS</span></span>

### <span data-ttu-id="c2d2b-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c2d2b-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c2d2b-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2d2b-130">NOTES</span></span>
* <span data-ttu-id="c2d2b-131">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="c2d2b-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c2d2b-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2d2b-132">RELATED LINKS</span></span>

[<span data-ttu-id="c2d2b-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c2d2b-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c2d2b-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c2d2b-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c2d2b-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c2d2b-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c2d2b-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c2d2b-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


