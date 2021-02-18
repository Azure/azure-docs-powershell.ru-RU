---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 99d56b837b67fe8b816c4f27c8658932a74452e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227985"
---
# <span data-ttu-id="06bb8-101">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="06bb8-101">Get-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="06bb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06bb8-102">SYNOPSIS</span></span>
<span data-ttu-id="06bb8-103">Возвращает цепочку сертификатов доверенных клиентских ЦС с определенным именем из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="06bb8-103">Gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="06bb8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="06bb8-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedClientCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06bb8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06bb8-105">DESCRIPTION</span></span>
<span data-ttu-id="06bb8-106">Этот Get-AzApplicationGatewayTrustedClientCertificate получает цепочку сертификатов доверенных клиентских ЦС, имя которого задано шлюзом приложений.</span><span class="sxs-lookup"><span data-stu-id="06bb8-106">The Get-AzApplicationGatewayTrustedClientCertificate cmdlet gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="06bb8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="06bb8-107">EXAMPLES</span></span>

### <span data-ttu-id="06bb8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="06bb8-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClientCert = Get-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName
```

<span data-ttu-id="06bb8-109">Первая команда получает шлюз приложения и сохраняет его в $gw переменной.</span><span class="sxs-lookup"><span data-stu-id="06bb8-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span> <span data-ttu-id="06bb8-110">Вторая команда получает цепочку сертификатов доверенных клиентских ЦС с указанным именем из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="06bb8-110">The second command gets the trusted client CA certificate chain with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="06bb8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06bb8-111">PARAMETERS</span></span>

### <span data-ttu-id="06bb8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06bb8-112">-ApplicationGateway</span></span>
<span data-ttu-id="06bb8-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06bb8-113">The applicationGateway</span></span>

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

### <span data-ttu-id="06bb8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06bb8-114">-DefaultProfile</span></span>
<span data-ttu-id="06bb8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06bb8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06bb8-116">-Name</span><span class="sxs-lookup"><span data-stu-id="06bb8-116">-Name</span></span>
<span data-ttu-id="06bb8-117">Имя цепочки сертификатов доверенного клиента ЦС</span><span class="sxs-lookup"><span data-stu-id="06bb8-117">The name of the trusted client CA certificate chain</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06bb8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06bb8-118">CommonParameters</span></span>
<span data-ttu-id="06bb8-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06bb8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06bb8-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06bb8-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06bb8-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06bb8-121">INPUTS</span></span>

### <span data-ttu-id="06bb8-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06bb8-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="06bb8-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="06bb8-123">OUTPUTS</span></span>

### <span data-ttu-id="06bb8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="06bb8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="06bb8-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="06bb8-125">NOTES</span></span>

## <span data-ttu-id="06bb8-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06bb8-126">RELATED LINKS</span></span>

[<span data-ttu-id="06bb8-127">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="06bb8-127">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="06bb8-128">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="06bb8-128">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="06bb8-129">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="06bb8-129">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="06bb8-130">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="06bb8-130">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)