---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 23b337779da46169be29e3dd6fef55fc70f4f035
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911087"
---
# <span data-ttu-id="2fc9d-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2fc9d-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="2fc9d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2fc9d-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc9d-103">Обновляет сертификат проверки подлинности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2fc9d-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="2fc9d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2fc9d-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2fc9d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fc9d-105">DESCRIPTION</span></span>
<span data-ttu-id="2fc9d-106">Командлет **Set-AzApplicationGatewayAuthenticationCertificate** обновляет сертификат проверки подлинности для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="2fc9d-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="2fc9d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2fc9d-107">EXAMPLES</span></span>

### <span data-ttu-id="2fc9d-108">1:</span><span class="sxs-lookup"><span data-stu-id="2fc9d-108">1:</span></span>
```

```

## <span data-ttu-id="2fc9d-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2fc9d-109">PARAMETERS</span></span>

### <span data-ttu-id="2fc9d-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fc9d-110">-ApplicationGateway</span></span>
<span data-ttu-id="2fc9d-111">Указывает имя шлюза приложений, для которого этот командлет обновляет сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2fc9d-111">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="2fc9d-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="2fc9d-112">-CertificateFile</span></span>
<span data-ttu-id="2fc9d-113">Задает путь к файлу сертификата проверки подлинности, с помощью которого этот командлет обновляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="2fc9d-113">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="2fc9d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc9d-114">-DefaultProfile</span></span>
<span data-ttu-id="2fc9d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2fc9d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fc9d-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2fc9d-116">-Name</span></span>
<span data-ttu-id="2fc9d-117">Указывает имя сертификата проверки подлинности, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="2fc9d-117">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="2fc9d-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fc9d-118">-Confirm</span></span>
<span data-ttu-id="2fc9d-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2fc9d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fc9d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fc9d-120">-WhatIf</span></span>
<span data-ttu-id="2fc9d-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2fc9d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fc9d-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2fc9d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fc9d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc9d-123">CommonParameters</span></span>
<span data-ttu-id="2fc9d-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2fc9d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc9d-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fc9d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc9d-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2fc9d-126">INPUTS</span></span>

### <span data-ttu-id="2fc9d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2fc9d-127">System.String</span></span>

## <span data-ttu-id="2fc9d-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fc9d-128">OUTPUTS</span></span>

### <span data-ttu-id="2fc9d-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fc9d-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2fc9d-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="2fc9d-130">NOTES</span></span>
* <span data-ttu-id="2fc9d-131">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="2fc9d-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2fc9d-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2fc9d-132">RELATED LINKS</span></span>

[<span data-ttu-id="2fc9d-133">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2fc9d-133">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2fc9d-134">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2fc9d-134">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2fc9d-135">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2fc9d-135">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2fc9d-136">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2fc9d-136">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


