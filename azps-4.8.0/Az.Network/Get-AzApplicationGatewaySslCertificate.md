---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 3e7010309c6aed367e3771971a8b1c2841548fe0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236962"
---
# <span data-ttu-id="935c0-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="935c0-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="935c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="935c0-102">SYNOPSIS</span></span>
<span data-ttu-id="935c0-103">Получает SSL-сертификат для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="935c0-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="935c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="935c0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="935c0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="935c0-105">DESCRIPTION</span></span>
<span data-ttu-id="935c0-106">Командлет **Get-AzApplicationGatewaySslCertificate** получает сертификат SSL для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="935c0-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="935c0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="935c0-107">EXAMPLES</span></span>

### <span data-ttu-id="935c0-108">Пример 1: получение определенного SSL-сертификата</span><span class="sxs-lookup"><span data-stu-id="935c0-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="935c0-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="935c0-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="935c0-110">Вторая команда получает сертификат SSL с именем Cert01 из шлюза приложения, который хранится в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="935c0-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="935c0-111">Эта команда хранит сертификат в переменной с именем $Cert.</span><span class="sxs-lookup"><span data-stu-id="935c0-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="935c0-112">Пример 2: получение списка SSL-сертификатов</span><span class="sxs-lookup"><span data-stu-id="935c0-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="935c0-113">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="935c0-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="935c0-114">Вторая команда возвращает список SSL-сертификатов из шлюза приложения, который хранится в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="935c0-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="935c0-115">Затем команда сохраняет результаты в переменной с именем $Certs.</span><span class="sxs-lookup"><span data-stu-id="935c0-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="935c0-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="935c0-116">PARAMETERS</span></span>

### <span data-ttu-id="935c0-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="935c0-117">-ApplicationGateway</span></span>
<span data-ttu-id="935c0-118">Указывает объект шлюза приложения, который содержит сертификат SSL.</span><span class="sxs-lookup"><span data-stu-id="935c0-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="935c0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="935c0-119">-DefaultProfile</span></span>
<span data-ttu-id="935c0-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="935c0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="935c0-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="935c0-121">-Name</span></span>
<span data-ttu-id="935c0-122">Указывает имя пула сертификатов SSL, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="935c0-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="935c0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="935c0-123">CommonParameters</span></span>
<span data-ttu-id="935c0-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="935c0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="935c0-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="935c0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="935c0-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="935c0-126">INPUTS</span></span>

### <span data-ttu-id="935c0-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="935c0-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="935c0-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="935c0-128">OUTPUTS</span></span>

### <span data-ttu-id="935c0-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="935c0-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="935c0-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="935c0-130">NOTES</span></span>

## <span data-ttu-id="935c0-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="935c0-131">RELATED LINKS</span></span>

[<span data-ttu-id="935c0-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="935c0-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="935c0-133">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="935c0-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="935c0-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="935c0-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="935c0-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="935c0-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)

