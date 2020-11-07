---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 00ad021e86617d08f0ca30f660cac28110348885
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913610"
---
# <span data-ttu-id="13875-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="13875-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="13875-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13875-102">SYNOPSIS</span></span>
<span data-ttu-id="13875-103">Удаляет сертификат проверки подлинности из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="13875-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13875-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13875-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13875-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13875-105">DESCRIPTION</span></span>
<span data-ttu-id="13875-106">Командлет **Remove-AzureRmApplicationGatewayAuthenticationCertificate** Удаляет сертификат для проверки подлинности из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="13875-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="13875-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13875-107">EXAMPLES</span></span>

### <span data-ttu-id="13875-108">1:</span><span class="sxs-lookup"><span data-stu-id="13875-108">1:</span></span>
```

```

## <span data-ttu-id="13875-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13875-109">PARAMETERS</span></span>

### <span data-ttu-id="13875-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13875-110">-ApplicationGateway</span></span>
<span data-ttu-id="13875-111">Указывает имя шлюза приложений, из которого этот командлет удаляет сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="13875-111">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="13875-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13875-112">-DefaultProfile</span></span>
<span data-ttu-id="13875-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13875-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13875-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13875-114">-Name</span></span>
<span data-ttu-id="13875-115">Указывает имя сертификата для проверки подлинности, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="13875-115">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="13875-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13875-116">-Confirm</span></span>
<span data-ttu-id="13875-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="13875-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13875-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13875-118">-WhatIf</span></span>
<span data-ttu-id="13875-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="13875-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13875-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="13875-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13875-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13875-121">CommonParameters</span></span>
<span data-ttu-id="13875-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13875-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13875-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13875-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13875-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13875-124">INPUTS</span></span>

### <span data-ttu-id="13875-125">System. String</span><span class="sxs-lookup"><span data-stu-id="13875-125">System.String</span></span>

## <span data-ttu-id="13875-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13875-126">OUTPUTS</span></span>

### <span data-ttu-id="13875-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13875-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="13875-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="13875-128">NOTES</span></span>
* <span data-ttu-id="13875-129">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="13875-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="13875-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13875-130">RELATED LINKS</span></span>

[<span data-ttu-id="13875-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="13875-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="13875-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="13875-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="13875-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="13875-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="13875-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="13875-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


