---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5c3976ddeeaa856f956ecb785a9d35e62ba322fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249976"
---
# <span data-ttu-id="bd2e1-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bd2e1-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="bd2e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd2e1-102">SYNOPSIS</span></span>
<span data-ttu-id="bd2e1-103">Получает доверенный корневой сертификат с определенным именем из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="bd2e1-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="bd2e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd2e1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd2e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd2e1-105">DESCRIPTION</span></span>
<span data-ttu-id="bd2e1-106">Командлет **Get-AzApplicationGatewayTrustedRootCertificate** получает доверенный корневой сертификат с определенным именем из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="bd2e1-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="bd2e1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd2e1-107">EXAMPLES</span></span>

### <span data-ttu-id="bd2e1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bd2e1-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="bd2e1-109">Первая команда получает шлюз приложения и сохраняет его в $gw переменной.</span><span class="sxs-lookup"><span data-stu-id="bd2e1-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="bd2e1-110">Вторая команда получает доверенный корневой сертификат с указанным именем из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="bd2e1-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="bd2e1-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd2e1-111">PARAMETERS</span></span>

### <span data-ttu-id="bd2e1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bd2e1-112">-ApplicationGateway</span></span>
<span data-ttu-id="bd2e1-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bd2e1-113">The applicationGateway</span></span>

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

### <span data-ttu-id="bd2e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd2e1-114">-DefaultProfile</span></span>
<span data-ttu-id="bd2e1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd2e1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd2e1-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bd2e1-116">-Name</span></span>
<span data-ttu-id="bd2e1-117">Имя сертификата TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="bd2e1-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="bd2e1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd2e1-118">CommonParameters</span></span>
<span data-ttu-id="bd2e1-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd2e1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd2e1-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd2e1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd2e1-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd2e1-121">INPUTS</span></span>

### <span data-ttu-id="bd2e1-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bd2e1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bd2e1-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd2e1-123">OUTPUTS</span></span>

### <span data-ttu-id="bd2e1-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bd2e1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="bd2e1-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd2e1-125">NOTES</span></span>

## <span data-ttu-id="bd2e1-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd2e1-126">RELATED LINKS</span></span>

[<span data-ttu-id="bd2e1-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bd2e1-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="bd2e1-128">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bd2e1-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="bd2e1-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bd2e1-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="bd2e1-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bd2e1-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
