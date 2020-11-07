---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 6652da4491bc503ecc2d0c8ee016416cefbff172
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910172"
---
# <span data-ttu-id="6c012-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="6c012-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="6c012-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6c012-102">SYNOPSIS</span></span>
<span data-ttu-id="6c012-103">Добавляет сертификат проверки подлинности в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="6c012-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="6c012-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6c012-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c012-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c012-105">DESCRIPTION</span></span>
<span data-ttu-id="6c012-106">Командлет **Add-AzApplicationGatewayAuthenticationCertificate** добавляет сертификат проверки подлинности в шлюз приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="6c012-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="6c012-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6c012-107">EXAMPLES</span></span>

### <span data-ttu-id="6c012-108">1:</span><span class="sxs-lookup"><span data-stu-id="6c012-108">1:</span></span>
```

```

## <span data-ttu-id="6c012-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6c012-109">PARAMETERS</span></span>

### <span data-ttu-id="6c012-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c012-110">-ApplicationGateway</span></span>
<span data-ttu-id="6c012-111">Указывает имя шлюза приложений, для которого этот командлет добавляет сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="6c012-111">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="6c012-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="6c012-112">-CertificateFile</span></span>
<span data-ttu-id="6c012-113">Указывает путь к сертификату проверки подлинности, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6c012-113">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="6c012-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c012-114">-DefaultProfile</span></span>
<span data-ttu-id="6c012-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c012-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c012-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6c012-116">-Name</span></span>
<span data-ttu-id="6c012-117">Указывает имя сертификата, который добавляется этим командлетом в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="6c012-117">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="6c012-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c012-118">-Confirm</span></span>
<span data-ttu-id="6c012-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6c012-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c012-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c012-120">-WhatIf</span></span>
<span data-ttu-id="6c012-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6c012-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c012-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6c012-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c012-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c012-123">CommonParameters</span></span>
<span data-ttu-id="6c012-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6c012-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c012-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c012-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c012-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6c012-126">INPUTS</span></span>

### <span data-ttu-id="6c012-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6c012-127">System.String</span></span>

## <span data-ttu-id="6c012-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c012-128">OUTPUTS</span></span>

### <span data-ttu-id="6c012-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c012-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6c012-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="6c012-130">NOTES</span></span>
* <span data-ttu-id="6c012-131">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="6c012-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="6c012-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c012-132">RELATED LINKS</span></span>

[<span data-ttu-id="6c012-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="6c012-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="6c012-134">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="6c012-134">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="6c012-135">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="6c012-135">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="6c012-136">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="6c012-136">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


