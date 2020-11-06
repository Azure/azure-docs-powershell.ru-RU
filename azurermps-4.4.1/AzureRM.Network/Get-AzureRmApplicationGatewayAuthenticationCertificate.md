---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 846cdf57e78ca1d3bacb7673d23fd16d460e4400
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559708"
---
# <span data-ttu-id="786e7-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="786e7-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="786e7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="786e7-102">SYNOPSIS</span></span>
<span data-ttu-id="786e7-103">Возвращает сертификат для проверки подлинности для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="786e7-103">Gets an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="786e7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="786e7-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="786e7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="786e7-105">DESCRIPTION</span></span>
<span data-ttu-id="786e7-106">Командлет **Get-AzureRmApplicationGatewayAuthenticationCertificate** получает сертификат проверки подлинности для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="786e7-106">The **Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="786e7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="786e7-107">EXAMPLES</span></span>

## <span data-ttu-id="786e7-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="786e7-108">PARAMETERS</span></span>

### <span data-ttu-id="786e7-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="786e7-109">-ApplicationGateway</span></span>
<span data-ttu-id="786e7-110">Указывает имя шлюза приложений, для которого этот командлет получает сертификат проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="786e7-110">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="786e7-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="786e7-111">-Name</span></span>
<span data-ttu-id="786e7-112">Указывает имя сертификата проверки подлинности, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="786e7-112">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="786e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="786e7-113">-DefaultProfile</span></span>
<span data-ttu-id="786e7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="786e7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="786e7-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="786e7-115">CommonParameters</span></span>
<span data-ttu-id="786e7-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="786e7-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="786e7-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="786e7-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="786e7-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="786e7-118">INPUTS</span></span>

### <span data-ttu-id="786e7-119">System. String</span><span class="sxs-lookup"><span data-stu-id="786e7-119">System.String</span></span>

## <span data-ttu-id="786e7-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="786e7-120">OUTPUTS</span></span>

### <span data-ttu-id="786e7-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="786e7-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="786e7-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="786e7-122">NOTES</span></span>
* <span data-ttu-id="786e7-123">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="786e7-123">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="786e7-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="786e7-124">RELATED LINKS</span></span>

[<span data-ttu-id="786e7-125">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="786e7-125">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="786e7-126">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="786e7-126">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="786e7-127">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="786e7-127">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="786e7-128">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="786e7-128">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


