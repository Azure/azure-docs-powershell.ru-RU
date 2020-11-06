---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: c45a829414fd1009f97c99844705e9affab0ef30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558395"
---
# <span data-ttu-id="0019f-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0019f-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="0019f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0019f-102">SYNOPSIS</span></span>
<span data-ttu-id="0019f-103">Задает состояние цели SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="0019f-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0019f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0019f-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0019f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0019f-105">DESCRIPTION</span></span>
<span data-ttu-id="0019f-106">Командлет **Set-AzureRmApplicationGatewaySslCertificate** задает состояние цели SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="0019f-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="0019f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0019f-107">EXAMPLES</span></span>

### <span data-ttu-id="0019f-108">Пример 1: Установка состояния цели сертификата SSL</span><span class="sxs-lookup"><span data-stu-id="0019f-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="0019f-109">Эта команда задает состояние цели для сертификата SSL на шлюзе приложений с именем ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="0019f-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="0019f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0019f-110">PARAMETERS</span></span>

### <span data-ttu-id="0019f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0019f-111">-ApplicationGateway</span></span>
<span data-ttu-id="0019f-112">Указывает шлюз приложений, с которым связан SSL-сертификат.</span><span class="sxs-lookup"><span data-stu-id="0019f-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="0019f-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="0019f-113">-CertificateFile</span></span>
<span data-ttu-id="0019f-114">Указывает путь SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="0019f-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="0019f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0019f-115">-DefaultProfile</span></span>
<span data-ttu-id="0019f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0019f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0019f-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0019f-117">-Name</span></span>
<span data-ttu-id="0019f-118">Задает имя SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="0019f-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="0019f-119">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="0019f-119">-Password</span></span>
<span data-ttu-id="0019f-120">Указывает пароль SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="0019f-120">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="0019f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0019f-121">CommonParameters</span></span>
<span data-ttu-id="0019f-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0019f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0019f-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0019f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0019f-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0019f-124">INPUTS</span></span>

### <span data-ttu-id="0019f-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0019f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="0019f-126">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0019f-126">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="0019f-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0019f-127">OUTPUTS</span></span>

### <span data-ttu-id="0019f-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0019f-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0019f-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="0019f-129">NOTES</span></span>

## <span data-ttu-id="0019f-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0019f-130">RELATED LINKS</span></span>

[<span data-ttu-id="0019f-131">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0019f-131">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0019f-132">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0019f-132">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0019f-133">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0019f-133">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0019f-134">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0019f-134">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


