---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b68f0bf3b0112587256fddc3dbb6c31605f811b7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911059"
---
# <span data-ttu-id="b33a3-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b33a3-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b33a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b33a3-102">SYNOPSIS</span></span>
<span data-ttu-id="b33a3-103">Задает состояние цели SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="b33a3-103">Sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="b33a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b33a3-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b33a3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b33a3-105">DESCRIPTION</span></span>
<span data-ttu-id="b33a3-106">Командлет **Set-AzApplicationGatewaySslCertificate** задает состояние цели SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="b33a3-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="b33a3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b33a3-107">EXAMPLES</span></span>

### <span data-ttu-id="b33a3-108">Пример 1: Установка состояния цели сертификата SSL</span><span class="sxs-lookup"><span data-stu-id="b33a3-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="b33a3-109">Эта команда задает состояние цели для сертификата SSL на шлюзе приложений с именем ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="b33a3-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="b33a3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b33a3-110">PARAMETERS</span></span>

### <span data-ttu-id="b33a3-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b33a3-111">-ApplicationGateway</span></span>
<span data-ttu-id="b33a3-112">Указывает шлюз приложений, с которым связан SSL-сертификат.</span><span class="sxs-lookup"><span data-stu-id="b33a3-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="b33a3-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b33a3-113">-CertificateFile</span></span>
<span data-ttu-id="b33a3-114">Указывает путь SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="b33a3-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="b33a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b33a3-115">-DefaultProfile</span></span>
<span data-ttu-id="b33a3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b33a3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b33a3-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b33a3-117">-Name</span></span>
<span data-ttu-id="b33a3-118">Задает имя SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="b33a3-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="b33a3-119">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="b33a3-119">-Password</span></span>
<span data-ttu-id="b33a3-120">Указывает пароль SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="b33a3-120">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="b33a3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b33a3-121">CommonParameters</span></span>
<span data-ttu-id="b33a3-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b33a3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b33a3-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b33a3-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b33a3-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b33a3-124">INPUTS</span></span>

### <span data-ttu-id="b33a3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b33a3-125">System.String</span></span>

## <span data-ttu-id="b33a3-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b33a3-126">OUTPUTS</span></span>

### <span data-ttu-id="b33a3-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b33a3-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b33a3-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b33a3-128">NOTES</span></span>

## <span data-ttu-id="b33a3-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b33a3-129">RELATED LINKS</span></span>

[<span data-ttu-id="b33a3-130">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b33a3-130">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b33a3-131">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b33a3-131">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b33a3-132">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b33a3-132">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b33a3-133">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b33a3-133">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


