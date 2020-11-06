---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 865b9a576219cbaf7d938094baf923c497436e07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562851"
---
# <span data-ttu-id="e4199-101">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e4199-101">Remove-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e4199-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e4199-102">SYNOPSIS</span></span>
<span data-ttu-id="e4199-103">Удаление SSL-сертификата из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="e4199-103">Removes an SSL certificate from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4199-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e4199-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4199-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4199-105">DESCRIPTION</span></span>
<span data-ttu-id="e4199-106">Командлет **Remove-AzureRmApplicationGatewaySslCertificate** УДАЛЯЕТ сертификат SSL (Secure Sockets Layer) из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="e4199-106">The **Remove-AzureRmApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="e4199-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e4199-107">EXAMPLES</span></span>

### <span data-ttu-id="e4199-108">Пример 1: Удаление SSL-сертификата из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="e4199-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="e4199-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e4199-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="e4199-110">Вторая команда удаляет SSL-сертификат с именем Cert02 из шлюза приложения, который хранится в переменной $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e4199-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="e4199-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e4199-111">PARAMETERS</span></span>

### <span data-ttu-id="e4199-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4199-112">-ApplicationGateway</span></span>
<span data-ttu-id="e4199-113">Указывает шлюз приложений, с которого этот командлет удаляет сертификат SSL.</span><span class="sxs-lookup"><span data-stu-id="e4199-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="e4199-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4199-114">-DefaultProfile</span></span>
<span data-ttu-id="e4199-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e4199-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4199-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e4199-116">-Name</span></span>
<span data-ttu-id="e4199-117">Указывает имя SSL-сертификата, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="e4199-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e4199-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4199-118">CommonParameters</span></span>
<span data-ttu-id="e4199-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e4199-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4199-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4199-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4199-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e4199-121">INPUTS</span></span>

### <span data-ttu-id="e4199-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4199-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="e4199-123">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e4199-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="e4199-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4199-124">OUTPUTS</span></span>

### <span data-ttu-id="e4199-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4199-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e4199-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="e4199-126">NOTES</span></span>

## <span data-ttu-id="e4199-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4199-127">RELATED LINKS</span></span>

[<span data-ttu-id="e4199-128">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e4199-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e4199-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e4199-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e4199-130">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e4199-130">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e4199-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e4199-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


