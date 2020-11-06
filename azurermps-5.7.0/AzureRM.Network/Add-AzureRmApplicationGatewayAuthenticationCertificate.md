---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 317fd5bf8306416ad4cbef3d1fb64d56d556ed1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564828"
---
# <span data-ttu-id="247c3-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="247c3-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="247c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="247c3-102">SYNOPSIS</span></span>
<span data-ttu-id="247c3-103">Добавляет сертификат проверки подлинности в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="247c3-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="247c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="247c3-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="247c3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="247c3-105">DESCRIPTION</span></span>
<span data-ttu-id="247c3-106">Командлет **Add-AzureRmApplicationGatewayAuthenticationCertificate** добавляет сертификат проверки подлинности в шлюз приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="247c3-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="247c3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="247c3-107">EXAMPLES</span></span>

## <span data-ttu-id="247c3-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="247c3-108">PARAMETERS</span></span>

### <span data-ttu-id="247c3-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="247c3-109">-ApplicationGateway</span></span>
<span data-ttu-id="247c3-110">Указывает имя шлюза приложений, для которого этот командлет добавляет сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="247c3-110">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="247c3-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="247c3-111">-CertificateFile</span></span>
<span data-ttu-id="247c3-112">Указывает путь к сертификату проверки подлинности, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="247c3-112">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="247c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="247c3-113">-DefaultProfile</span></span>
<span data-ttu-id="247c3-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="247c3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="247c3-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="247c3-115">-Name</span></span>
<span data-ttu-id="247c3-116">Указывает имя сертификата, который добавляется этим командлетом в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="247c3-116">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="247c3-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="247c3-117">-Confirm</span></span>
<span data-ttu-id="247c3-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="247c3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="247c3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="247c3-119">-WhatIf</span></span>
<span data-ttu-id="247c3-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="247c3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="247c3-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="247c3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="247c3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="247c3-122">CommonParameters</span></span>
<span data-ttu-id="247c3-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="247c3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="247c3-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="247c3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="247c3-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="247c3-125">INPUTS</span></span>

### <span data-ttu-id="247c3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="247c3-126">System.String</span></span>

## <span data-ttu-id="247c3-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="247c3-127">OUTPUTS</span></span>

### <span data-ttu-id="247c3-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="247c3-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="247c3-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="247c3-129">NOTES</span></span>
* <span data-ttu-id="247c3-130">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="247c3-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="247c3-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="247c3-131">RELATED LINKS</span></span>

[<span data-ttu-id="247c3-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="247c3-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="247c3-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="247c3-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="247c3-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="247c3-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="247c3-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="247c3-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


