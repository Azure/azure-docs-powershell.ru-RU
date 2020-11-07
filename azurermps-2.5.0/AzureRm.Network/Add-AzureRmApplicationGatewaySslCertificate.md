---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: 65c178cc8cf293cf6c20e6262733031e377f61fe
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913462"
---
# <span data-ttu-id="9c18d-101">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9c18d-101">Add-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="9c18d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c18d-102">SYNOPSIS</span></span>
<span data-ttu-id="9c18d-103">Добавление SSL-сертификата в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="9c18d-103">Adds an SSL certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c18d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c18d-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c18d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c18d-105">DESCRIPTION</span></span>
<span data-ttu-id="9c18d-106">Командлет **Add-AzureRmApplicationGatewaySslCertificate** добавляет сертификат SSL в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="9c18d-106">The **Add-AzureRmApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="9c18d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c18d-107">EXAMPLES</span></span>

### <span data-ttu-id="9c18d-108">Пример 1: Добавление SSL-сертификата в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="9c18d-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="9c18d-109">Эта команда получает шлюз приложения с именем ApplicationGateway01 и добавляет в него сертификат SSL с именем Cert01.</span><span class="sxs-lookup"><span data-stu-id="9c18d-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="9c18d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c18d-110">PARAMETERS</span></span>

### <span data-ttu-id="9c18d-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c18d-111">-ApplicationGateway</span></span>
<span data-ttu-id="9c18d-112">Указывает имя шлюза приложений, с которым этот командлет добавляет сертификат SSL.</span><span class="sxs-lookup"><span data-stu-id="9c18d-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="9c18d-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9c18d-113">-CertificateFile</span></span>
<span data-ttu-id="9c18d-114">Задает PFX-файл SSL-сертификата, который добавляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9c18d-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9c18d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c18d-115">-DefaultProfile</span></span>
<span data-ttu-id="9c18d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c18d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c18d-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9c18d-117">-Name</span></span>
<span data-ttu-id="9c18d-118">Указывает имя SSL-сертификата, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9c18d-118">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9c18d-119">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="9c18d-119">-Password</span></span>
<span data-ttu-id="9c18d-120">Указывает пароль SSL-сертификата, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9c18d-120">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c18d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c18d-121">CommonParameters</span></span>
<span data-ttu-id="9c18d-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c18d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c18d-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c18d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c18d-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c18d-124">INPUTS</span></span>

### <span data-ttu-id="9c18d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9c18d-125">System.String</span></span>

## <span data-ttu-id="9c18d-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c18d-126">OUTPUTS</span></span>

### <span data-ttu-id="9c18d-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c18d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9c18d-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c18d-128">NOTES</span></span>

## <span data-ttu-id="9c18d-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c18d-129">RELATED LINKS</span></span>

[<span data-ttu-id="9c18d-130">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9c18d-130">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9c18d-131">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9c18d-131">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9c18d-132">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9c18d-132">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9c18d-133">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9c18d-133">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


