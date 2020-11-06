---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: fc4457e23f50dea3d70a3af2115a93e460dc6a1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567724"
---
# <span data-ttu-id="9eb50-101">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9eb50-101">Add-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="9eb50-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9eb50-102">SYNOPSIS</span></span>
<span data-ttu-id="9eb50-103">Добавление SSL-сертификата в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="9eb50-103">Adds an SSL certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9eb50-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9eb50-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9eb50-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9eb50-105">DESCRIPTION</span></span>
<span data-ttu-id="9eb50-106">Командлет **Add-AzureRmApplicationGatewaySslCertificate** добавляет сертификат SSL в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="9eb50-106">The **Add-AzureRmApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="9eb50-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9eb50-107">EXAMPLES</span></span>

### <span data-ttu-id="9eb50-108">Пример 1: Добавление SSL-сертификата в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="9eb50-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="9eb50-109">Эта команда получает шлюз приложения с именем ApplicationGateway01 и добавляет в него сертификат SSL с именем Cert01.</span><span class="sxs-lookup"><span data-stu-id="9eb50-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="9eb50-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9eb50-110">PARAMETERS</span></span>

### <span data-ttu-id="9eb50-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9eb50-111">-ApplicationGateway</span></span>
<span data-ttu-id="9eb50-112">Указывает имя шлюза приложений, с которым этот командлет добавляет сертификат SSL.</span><span class="sxs-lookup"><span data-stu-id="9eb50-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="9eb50-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9eb50-113">-CertificateFile</span></span>
<span data-ttu-id="9eb50-114">Задает PFX-файл SSL-сертификата, который добавляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9eb50-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9eb50-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eb50-115">-DefaultProfile</span></span>
<span data-ttu-id="9eb50-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9eb50-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9eb50-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9eb50-117">-Name</span></span>
<span data-ttu-id="9eb50-118">Указывает имя SSL-сертификата, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9eb50-118">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9eb50-119">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="9eb50-119">-Password</span></span>
<span data-ttu-id="9eb50-120">Указывает пароль SSL-сертификата, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9eb50-120">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb50-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eb50-121">CommonParameters</span></span>
<span data-ttu-id="9eb50-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9eb50-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eb50-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9eb50-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eb50-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9eb50-124">INPUTS</span></span>

### <span data-ttu-id="9eb50-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9eb50-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="9eb50-126">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9eb50-126">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="9eb50-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9eb50-127">OUTPUTS</span></span>

### <span data-ttu-id="9eb50-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9eb50-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9eb50-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="9eb50-129">NOTES</span></span>

## <span data-ttu-id="9eb50-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9eb50-130">RELATED LINKS</span></span>

[<span data-ttu-id="9eb50-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9eb50-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9eb50-132">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9eb50-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9eb50-133">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9eb50-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9eb50-134">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9eb50-134">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


