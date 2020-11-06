---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: da831810461e763acc51319ea4d6662c45a1c3ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563904"
---
# <span data-ttu-id="9cd2b-101">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9cd2b-101">Get-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="9cd2b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9cd2b-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd2b-103">Получает SSL-сертификат для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-103">Gets an SSL certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cd2b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9cd2b-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cd2b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cd2b-105">DESCRIPTION</span></span>
<span data-ttu-id="9cd2b-106">Командлет **Get-AzureRmApplicationGatewaySslCertificate** получает сертификат SSL для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-106">The **Get-AzureRmApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="9cd2b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9cd2b-107">EXAMPLES</span></span>

### <span data-ttu-id="9cd2b-108">Пример 1: получение определенного SSL-сертификата</span><span class="sxs-lookup"><span data-stu-id="9cd2b-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="9cd2b-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="9cd2b-110">Вторая команда получает сертификат SSL с именем Cert01 из шлюза приложения, который хранится в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="9cd2b-111">Эта команда хранит сертификат в переменной с именем $Cert.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="9cd2b-112">Пример 2: получение списка SSL-сертификатов</span><span class="sxs-lookup"><span data-stu-id="9cd2b-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="9cd2b-113">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="9cd2b-114">Вторая команда возвращает список SSL-сертификатов из шлюза приложения, который хранится в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="9cd2b-115">Затем команда сохраняет результаты в переменной с именем $Certs.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="9cd2b-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9cd2b-116">PARAMETERS</span></span>

### <span data-ttu-id="9cd2b-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9cd2b-117">-ApplicationGateway</span></span>
<span data-ttu-id="9cd2b-118">Указывает объект шлюза приложения, который содержит сертификат SSL.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="9cd2b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9cd2b-119">-Name</span></span>
<span data-ttu-id="9cd2b-120">Указывает имя пула сертификатов SSL, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-120">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9cd2b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cd2b-121">-DefaultProfile</span></span>
<span data-ttu-id="9cd2b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cd2b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd2b-123">CommonParameters</span></span>
<span data-ttu-id="9cd2b-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd2b-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cd2b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd2b-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9cd2b-126">INPUTS</span></span>

### <span data-ttu-id="9cd2b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9cd2b-127">System.String</span></span>

## <span data-ttu-id="9cd2b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cd2b-128">OUTPUTS</span></span>

### <span data-ttu-id="9cd2b-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9cd2b-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="9cd2b-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="9cd2b-130">NOTES</span></span>

## <span data-ttu-id="9cd2b-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9cd2b-131">RELATED LINKS</span></span>

[<span data-ttu-id="9cd2b-132">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9cd2b-132">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9cd2b-133">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9cd2b-133">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9cd2b-134">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9cd2b-134">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9cd2b-135">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9cd2b-135">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


