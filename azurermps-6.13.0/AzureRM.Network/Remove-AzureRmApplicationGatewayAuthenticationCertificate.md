---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 9ec4522da3c5a75a1c9e5bad977f294e0987f4fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560875"
---
# <span data-ttu-id="563a4-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="563a4-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="563a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="563a4-102">SYNOPSIS</span></span>
<span data-ttu-id="563a4-103">Удаляет сертификат проверки подлинности из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="563a4-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="563a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="563a4-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="563a4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="563a4-105">DESCRIPTION</span></span>
<span data-ttu-id="563a4-106">Командлет **Remove-AzureRmApplicationGatewayAuthenticationCertificate** Удаляет сертификат для проверки подлинности из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="563a4-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="563a4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="563a4-107">EXAMPLES</span></span>

## <span data-ttu-id="563a4-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="563a4-108">PARAMETERS</span></span>

### <span data-ttu-id="563a4-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="563a4-109">-ApplicationGateway</span></span>
<span data-ttu-id="563a4-110">Указывает имя шлюза приложений, из которого этот командлет удаляет сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="563a4-110">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="563a4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="563a4-111">-DefaultProfile</span></span>
<span data-ttu-id="563a4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="563a4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="563a4-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="563a4-113">-Name</span></span>
<span data-ttu-id="563a4-114">Указывает имя сертификата для проверки подлинности, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="563a4-114">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="563a4-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="563a4-115">-Confirm</span></span>
<span data-ttu-id="563a4-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="563a4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="563a4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="563a4-117">-WhatIf</span></span>
<span data-ttu-id="563a4-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="563a4-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="563a4-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="563a4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="563a4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="563a4-120">CommonParameters</span></span>
<span data-ttu-id="563a4-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="563a4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="563a4-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="563a4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="563a4-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="563a4-123">INPUTS</span></span>

### <span data-ttu-id="563a4-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="563a4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="563a4-125">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="563a4-125">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="563a4-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="563a4-126">OUTPUTS</span></span>

### <span data-ttu-id="563a4-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="563a4-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="563a4-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="563a4-128">NOTES</span></span>
* <span data-ttu-id="563a4-129">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="563a4-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="563a4-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="563a4-130">RELATED LINKS</span></span>

[<span data-ttu-id="563a4-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="563a4-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="563a4-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="563a4-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="563a4-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="563a4-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="563a4-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="563a4-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


