---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: fd2ddd3b8c3c124e85c743c6e331b18816c48be3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562971"
---
# <span data-ttu-id="27e40-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="27e40-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="27e40-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27e40-102">SYNOPSIS</span></span>
<span data-ttu-id="27e40-103">Возвращает сертификат для проверки подлинности для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="27e40-103">Gets an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27e40-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27e40-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27e40-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27e40-105">DESCRIPTION</span></span>
<span data-ttu-id="27e40-106">Командлет **Get-AzureRmApplicationGatewayAuthenticationCertificate** получает сертификат проверки подлинности для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="27e40-106">The **Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="27e40-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27e40-107">EXAMPLES</span></span>

## <span data-ttu-id="27e40-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27e40-108">PARAMETERS</span></span>

### <span data-ttu-id="27e40-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="27e40-109">-ApplicationGateway</span></span>
<span data-ttu-id="27e40-110">Указывает имя шлюза приложений, для которого этот командлет получает сертификат проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="27e40-110">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="27e40-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27e40-111">-DefaultProfile</span></span>
<span data-ttu-id="27e40-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27e40-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27e40-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="27e40-113">-Name</span></span>
<span data-ttu-id="27e40-114">Указывает имя сертификата проверки подлинности, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="27e40-114">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e40-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27e40-115">CommonParameters</span></span>
<span data-ttu-id="27e40-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27e40-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27e40-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27e40-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27e40-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27e40-118">INPUTS</span></span>

### <span data-ttu-id="27e40-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="27e40-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="27e40-120">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="27e40-120">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="27e40-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27e40-121">OUTPUTS</span></span>

### <span data-ttu-id="27e40-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="27e40-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="27e40-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="27e40-123">NOTES</span></span>
* <span data-ttu-id="27e40-124">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="27e40-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="27e40-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27e40-125">RELATED LINKS</span></span>

[<span data-ttu-id="27e40-126">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="27e40-126">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="27e40-127">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="27e40-127">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="27e40-128">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="27e40-128">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="27e40-129">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="27e40-129">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


