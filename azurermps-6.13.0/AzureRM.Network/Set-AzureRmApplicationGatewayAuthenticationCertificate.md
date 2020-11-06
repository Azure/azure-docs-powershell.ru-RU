---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: d8f2fcb875503b6d6a8063007926690ef682bdc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568441"
---
# <span data-ttu-id="b7a5c-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b7a5c-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b7a5c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7a5c-102">SYNOPSIS</span></span>
<span data-ttu-id="b7a5c-103">Обновляет сертификат проверки подлинности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b7a5c-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7a5c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7a5c-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7a5c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7a5c-105">DESCRIPTION</span></span>
<span data-ttu-id="b7a5c-106">Командлет **Set-AzureRmApplicationGatewayAuthenticationCertificate** обновляет сертификат проверки подлинности для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a5c-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b7a5c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7a5c-107">EXAMPLES</span></span>

## <span data-ttu-id="b7a5c-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7a5c-108">PARAMETERS</span></span>

### <span data-ttu-id="b7a5c-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7a5c-109">-ApplicationGateway</span></span>
<span data-ttu-id="b7a5c-110">Указывает имя шлюза приложений, для которого этот командлет обновляет сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b7a5c-110">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a5c-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b7a5c-111">-CertificateFile</span></span>
<span data-ttu-id="b7a5c-112">Задает путь к файлу сертификата проверки подлинности, с помощью которого этот командлет обновляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="b7a5c-112">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a5c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7a5c-113">-DefaultProfile</span></span>
<span data-ttu-id="b7a5c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a5c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7a5c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b7a5c-115">-Name</span></span>
<span data-ttu-id="b7a5c-116">Указывает имя сертификата проверки подлинности, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="b7a5c-116">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a5c-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7a5c-117">-Confirm</span></span>
<span data-ttu-id="b7a5c-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b7a5c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7a5c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7a5c-119">-WhatIf</span></span>
<span data-ttu-id="b7a5c-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b7a5c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7a5c-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b7a5c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7a5c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7a5c-122">CommonParameters</span></span>
<span data-ttu-id="b7a5c-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7a5c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7a5c-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7a5c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7a5c-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7a5c-125">INPUTS</span></span>

### <span data-ttu-id="b7a5c-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7a5c-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="b7a5c-127">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b7a5c-127">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="b7a5c-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7a5c-128">OUTPUTS</span></span>

### <span data-ttu-id="b7a5c-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7a5c-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b7a5c-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7a5c-130">NOTES</span></span>
* <span data-ttu-id="b7a5c-131">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="b7a5c-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b7a5c-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7a5c-132">RELATED LINKS</span></span>

[<span data-ttu-id="b7a5c-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b7a5c-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b7a5c-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b7a5c-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b7a5c-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b7a5c-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b7a5c-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b7a5c-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)


