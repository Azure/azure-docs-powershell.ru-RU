---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: f040110ea3e00e99b989c07e8757d3c3a0c4b976
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993947"
---
# <span data-ttu-id="568dc-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="568dc-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="568dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="568dc-102">SYNOPSIS</span></span>
<span data-ttu-id="568dc-103">Получает доверенный корневой сертификат с определенным именем из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="568dc-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="568dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="568dc-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="568dc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="568dc-105">DESCRIPTION</span></span>
<span data-ttu-id="568dc-106">**Cmdlet Get-AzApplicationGatewayTrustedRootCertificate** получает доверенный корневой сертификат с определенным именем из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="568dc-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="568dc-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="568dc-107">EXAMPLES</span></span>

### <span data-ttu-id="568dc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="568dc-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="568dc-109">Первая команда получает шлюз приложения и сохраняет его в $gw переменной.</span><span class="sxs-lookup"><span data-stu-id="568dc-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="568dc-110">Вторая команда получает доверенный корневой сертификат с указанным именем из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="568dc-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="568dc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="568dc-111">PARAMETERS</span></span>

### <span data-ttu-id="568dc-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="568dc-112">-ApplicationGateway</span></span>
<span data-ttu-id="568dc-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="568dc-113">The applicationGateway</span></span>

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

### <span data-ttu-id="568dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="568dc-114">-DefaultProfile</span></span>
<span data-ttu-id="568dc-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="568dc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="568dc-116">-Name</span><span class="sxs-lookup"><span data-stu-id="568dc-116">-Name</span></span>
<span data-ttu-id="568dc-117">Имя сертификата TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="568dc-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="568dc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="568dc-118">CommonParameters</span></span>
<span data-ttu-id="568dc-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="568dc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="568dc-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="568dc-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="568dc-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="568dc-121">INPUTS</span></span>

### <span data-ttu-id="568dc-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="568dc-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="568dc-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="568dc-123">OUTPUTS</span></span>

### <span data-ttu-id="568dc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="568dc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="568dc-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="568dc-125">NOTES</span></span>

## <span data-ttu-id="568dc-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="568dc-126">RELATED LINKS</span></span>

[<span data-ttu-id="568dc-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="568dc-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="568dc-128">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="568dc-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="568dc-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="568dc-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="568dc-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="568dc-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
