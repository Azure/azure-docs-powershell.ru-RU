---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: cec5a6aa0b61889e7923ebce67d1247f99d215e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734266"
---
# <span data-ttu-id="7da64-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7da64-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="7da64-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7da64-102">SYNOPSIS</span></span>
<span data-ttu-id="7da64-103">Задает состояние цели SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="7da64-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7da64-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7da64-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7da64-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7da64-105">DESCRIPTION</span></span>
<span data-ttu-id="7da64-106">Командлет **Set-AzureRmApplicationGatewaySslCertificate** задает состояние цели SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="7da64-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="7da64-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7da64-107">EXAMPLES</span></span>

### <span data-ttu-id="7da64-108">Пример 1: Установка состояния цели сертификата SSL</span><span class="sxs-lookup"><span data-stu-id="7da64-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password "Password01"
```

<span data-ttu-id="7da64-109">Эта команда задает состояние цели для сертификата SSL на шлюзе приложений с именем ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="7da64-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="7da64-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7da64-110">PARAMETERS</span></span>

### <span data-ttu-id="7da64-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7da64-111">-ApplicationGateway</span></span>
<span data-ttu-id="7da64-112">Указывает шлюз приложений, с которым связан SSL-сертификат.</span><span class="sxs-lookup"><span data-stu-id="7da64-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="7da64-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="7da64-113">-CertificateFile</span></span>
<span data-ttu-id="7da64-114">Указывает путь SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="7da64-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="7da64-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7da64-115">-Name</span></span>
<span data-ttu-id="7da64-116">Задает имя SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="7da64-116">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="7da64-117">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="7da64-117">-Password</span></span>
<span data-ttu-id="7da64-118">Указывает пароль SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="7da64-118">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="7da64-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da64-119">-DefaultProfile</span></span>
<span data-ttu-id="7da64-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7da64-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7da64-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da64-121">CommonParameters</span></span>
<span data-ttu-id="7da64-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7da64-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da64-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7da64-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da64-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7da64-124">INPUTS</span></span>

### <span data-ttu-id="7da64-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7da64-125">System.String</span></span>

## <span data-ttu-id="7da64-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7da64-126">OUTPUTS</span></span>

### <span data-ttu-id="7da64-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7da64-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7da64-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="7da64-128">NOTES</span></span>

## <span data-ttu-id="7da64-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7da64-129">RELATED LINKS</span></span>

[<span data-ttu-id="7da64-130">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7da64-130">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="7da64-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7da64-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="7da64-132">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7da64-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="7da64-133">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7da64-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


