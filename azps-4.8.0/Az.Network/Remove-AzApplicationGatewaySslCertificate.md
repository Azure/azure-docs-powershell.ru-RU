---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b03d35b511bafefe0ba062eb15a9c1eee8961585
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236025"
---
# <span data-ttu-id="1e497-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1e497-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="1e497-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e497-102">SYNOPSIS</span></span>
<span data-ttu-id="1e497-103">Удаление SSL-сертификата из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="1e497-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="1e497-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e497-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e497-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e497-105">DESCRIPTION</span></span>
<span data-ttu-id="1e497-106">Командлет **Remove-AzApplicationGatewaySslCertificate** УДАЛЯЕТ сертификат SSL (Secure Sockets Layer) из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="1e497-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="1e497-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e497-107">EXAMPLES</span></span>

### <span data-ttu-id="1e497-108">Пример 1: Удаление SSL-сертификата из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="1e497-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="1e497-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="1e497-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="1e497-110">Вторая команда удаляет SSL-сертификат с именем Cert02 из шлюза приложения, который хранится в переменной $AppGW.</span><span class="sxs-lookup"><span data-stu-id="1e497-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="1e497-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e497-111">PARAMETERS</span></span>

### <span data-ttu-id="1e497-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e497-112">-ApplicationGateway</span></span>
<span data-ttu-id="1e497-113">Указывает шлюз приложений, с которого этот командлет удаляет сертификат SSL.</span><span class="sxs-lookup"><span data-stu-id="1e497-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="1e497-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e497-114">-DefaultProfile</span></span>
<span data-ttu-id="1e497-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e497-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e497-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1e497-116">-Name</span></span>
<span data-ttu-id="1e497-117">Указывает имя SSL-сертификата, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="1e497-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1e497-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e497-118">CommonParameters</span></span>
<span data-ttu-id="1e497-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e497-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e497-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e497-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e497-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e497-121">INPUTS</span></span>

### <span data-ttu-id="1e497-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e497-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1e497-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e497-123">OUTPUTS</span></span>

### <span data-ttu-id="1e497-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e497-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1e497-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e497-125">NOTES</span></span>

## <span data-ttu-id="1e497-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e497-126">RELATED LINKS</span></span>

[<span data-ttu-id="1e497-127">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1e497-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="1e497-128">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1e497-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="1e497-129">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1e497-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="1e497-130">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1e497-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)

