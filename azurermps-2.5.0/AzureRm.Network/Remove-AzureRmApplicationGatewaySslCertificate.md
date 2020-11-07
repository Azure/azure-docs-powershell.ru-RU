---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: eeab1f5699af5de737bc1e0390c35d387acfdd98
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913597"
---
# <span data-ttu-id="16659-101">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="16659-101">Remove-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="16659-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16659-102">SYNOPSIS</span></span>
<span data-ttu-id="16659-103">Удаление SSL-сертификата из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="16659-103">Removes an SSL certificate from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16659-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16659-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16659-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16659-105">DESCRIPTION</span></span>
<span data-ttu-id="16659-106">Командлет **Remove-AzureRmApplicationGatewaySslCertificate** УДАЛЯЕТ сертификат SSL (Secure Sockets Layer) из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="16659-106">The **Remove-AzureRmApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="16659-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16659-107">EXAMPLES</span></span>

### <span data-ttu-id="16659-108">Пример 1: Удаление SSL-сертификата из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="16659-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="16659-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="16659-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>

<span data-ttu-id="16659-110">Вторая команда удаляет SSL-сертификат с именем Cert02 из шлюза приложения, который хранится в переменной $AppGW.</span><span class="sxs-lookup"><span data-stu-id="16659-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="16659-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16659-111">PARAMETERS</span></span>

### <span data-ttu-id="16659-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16659-112">-ApplicationGateway</span></span>
<span data-ttu-id="16659-113">Указывает шлюз приложений, с которого этот командлет удаляет сертификат SSL.</span><span class="sxs-lookup"><span data-stu-id="16659-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="16659-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16659-114">-DefaultProfile</span></span>
<span data-ttu-id="16659-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16659-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16659-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="16659-116">-Name</span></span>
<span data-ttu-id="16659-117">Указывает имя SSL-сертификата, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="16659-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="16659-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16659-118">CommonParameters</span></span>
<span data-ttu-id="16659-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16659-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16659-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16659-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16659-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16659-121">INPUTS</span></span>

### <span data-ttu-id="16659-122">System. String</span><span class="sxs-lookup"><span data-stu-id="16659-122">System.String</span></span>

## <span data-ttu-id="16659-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16659-123">OUTPUTS</span></span>

### <span data-ttu-id="16659-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16659-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="16659-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="16659-125">NOTES</span></span>

## <span data-ttu-id="16659-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16659-126">RELATED LINKS</span></span>

[<span data-ttu-id="16659-127">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="16659-127">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="16659-128">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="16659-128">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="16659-129">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="16659-129">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="16659-130">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="16659-130">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


