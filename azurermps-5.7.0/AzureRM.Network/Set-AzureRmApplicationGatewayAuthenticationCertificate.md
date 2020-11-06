---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: ebeff6e8c8542d487305ec7570a30c26689e6885
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570244"
---
# <span data-ttu-id="f8711-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f8711-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="f8711-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8711-102">SYNOPSIS</span></span>
<span data-ttu-id="f8711-103">Обновляет сертификат проверки подлинности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="f8711-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8711-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8711-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8711-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8711-105">DESCRIPTION</span></span>
<span data-ttu-id="f8711-106">Командлет **Set-AzureRmApplicationGatewayAuthenticationCertificate** обновляет сертификат проверки подлинности для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="f8711-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="f8711-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8711-107">EXAMPLES</span></span>

## <span data-ttu-id="f8711-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8711-108">PARAMETERS</span></span>

### <span data-ttu-id="f8711-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f8711-109">-ApplicationGateway</span></span>
<span data-ttu-id="f8711-110">Указывает имя шлюза приложений, для которого этот командлет обновляет сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="f8711-110">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="f8711-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f8711-111">-CertificateFile</span></span>
<span data-ttu-id="f8711-112">Задает путь к файлу сертификата проверки подлинности, с помощью которого этот командлет обновляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="f8711-112">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="f8711-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8711-113">-DefaultProfile</span></span>
<span data-ttu-id="f8711-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8711-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8711-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f8711-115">-Name</span></span>
<span data-ttu-id="f8711-116">Указывает имя сертификата проверки подлинности, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f8711-116">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="f8711-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8711-117">-Confirm</span></span>
<span data-ttu-id="f8711-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f8711-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8711-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8711-119">-WhatIf</span></span>
<span data-ttu-id="f8711-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f8711-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8711-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f8711-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8711-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8711-122">CommonParameters</span></span>
<span data-ttu-id="f8711-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8711-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8711-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8711-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8711-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8711-125">INPUTS</span></span>

### <span data-ttu-id="f8711-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f8711-126">System.String</span></span>

## <span data-ttu-id="f8711-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8711-127">OUTPUTS</span></span>

### <span data-ttu-id="f8711-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f8711-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f8711-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8711-129">NOTES</span></span>
* <span data-ttu-id="f8711-130">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="f8711-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f8711-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8711-131">RELATED LINKS</span></span>

[<span data-ttu-id="f8711-132">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f8711-132">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f8711-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f8711-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f8711-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f8711-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f8711-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f8711-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)


