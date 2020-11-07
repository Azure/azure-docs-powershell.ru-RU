---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 964e99912e4f21d48e89b725da1aa44ac32ea186
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910152"
---
# <span data-ttu-id="8d9bc-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8d9bc-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="8d9bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d9bc-102">SYNOPSIS</span></span>
<span data-ttu-id="8d9bc-103">Добавление SSL-сертификата в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="8d9bc-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="8d9bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d9bc-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d9bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d9bc-105">DESCRIPTION</span></span>
<span data-ttu-id="8d9bc-106">Командлет **Add-AzApplicationGatewaySslCertificate** добавляет сертификат SSL в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="8d9bc-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="8d9bc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d9bc-107">EXAMPLES</span></span>

### <span data-ttu-id="8d9bc-108">Пример 1: Добавление SSL-сертификата в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="8d9bc-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="8d9bc-109">Эта команда получает шлюз приложения с именем ApplicationGateway01 и добавляет в него сертификат SSL с именем Cert01.</span><span class="sxs-lookup"><span data-stu-id="8d9bc-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="8d9bc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d9bc-110">PARAMETERS</span></span>

### <span data-ttu-id="8d9bc-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d9bc-111">-ApplicationGateway</span></span>
<span data-ttu-id="8d9bc-112">Указывает имя шлюза приложений, с которым этот командлет добавляет сертификат SSL.</span><span class="sxs-lookup"><span data-stu-id="8d9bc-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="8d9bc-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="8d9bc-113">-CertificateFile</span></span>
<span data-ttu-id="8d9bc-114">Задает PFX-файл SSL-сертификата, который добавляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8d9bc-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="8d9bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d9bc-115">-DefaultProfile</span></span>
<span data-ttu-id="8d9bc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d9bc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d9bc-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8d9bc-117">-Name</span></span>
<span data-ttu-id="8d9bc-118">Указывает имя SSL-сертификата, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8d9bc-118">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="8d9bc-119">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="8d9bc-119">-Password</span></span>
<span data-ttu-id="8d9bc-120">Указывает пароль SSL-сертификата, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8d9bc-120">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="8d9bc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d9bc-121">CommonParameters</span></span>
<span data-ttu-id="8d9bc-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d9bc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d9bc-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d9bc-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d9bc-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d9bc-124">INPUTS</span></span>

### <span data-ttu-id="8d9bc-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8d9bc-125">System.String</span></span>

## <span data-ttu-id="8d9bc-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d9bc-126">OUTPUTS</span></span>

### <span data-ttu-id="8d9bc-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d9bc-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8d9bc-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d9bc-128">NOTES</span></span>

## <span data-ttu-id="8d9bc-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d9bc-129">RELATED LINKS</span></span>

[<span data-ttu-id="8d9bc-130">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8d9bc-130">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8d9bc-131">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8d9bc-131">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8d9bc-132">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8d9bc-132">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8d9bc-133">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8d9bc-133">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


