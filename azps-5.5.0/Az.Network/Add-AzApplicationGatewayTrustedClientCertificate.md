---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: e3a92085c15116527e1b6c14d5403f68748f4f90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214020"
---
# <span data-ttu-id="4810d-101">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4810d-101">Add-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="4810d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4810d-102">SYNOPSIS</span></span>
<span data-ttu-id="4810d-103">Добавляет цепочку сертификатов доверенных клиентских ЦС в шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="4810d-103">Adds a trusted client CA certificate chain to an application gateway.</span></span>

## <span data-ttu-id="4810d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4810d-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4810d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4810d-105">DESCRIPTION</span></span>
<span data-ttu-id="4810d-106">**Cmdlet Add-AzApplicationGatewayTrustedClientCertificate** добавляет цепочку сертификатов доверенных клиентских ЦС к шлюзу приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="4810d-106">The **Add-AzApplicationGatewayTrustedClientCertificate** cmdlet adds a trusted client CA certificate chain to an Azure application gateway.</span></span>

## <span data-ttu-id="4810d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4810d-107">EXAMPLES</span></span>

### <span data-ttu-id="4810d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4810d-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfileName -ApplicationGateway $gw -TrustedClientCertificates $trustedClient
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="4810d-109">Первая команда получает шлюз приложения и сохраняет его в $gw переменной.</span><span class="sxs-lookup"><span data-stu-id="4810d-109">The first command gets the application gateway and stores it in $gw variable.</span></span> <span data-ttu-id="4810d-110">Вторая команда создает новую цепочку сертификатов доверенных клиентских ЦС, принимая в качестве входных данных путь к сертификату клиентского ЦС.</span><span class="sxs-lookup"><span data-stu-id="4810d-110">The second command creates a new trusted client CA certificate chain taking path of the client CA certificate as input.</span></span> <span data-ttu-id="4810d-111">Третья команда создает профиль SSL с использованием сертификата надежного клиента.</span><span class="sxs-lookup"><span data-stu-id="4810d-111">The third command creates a SSL profile using trusted client certificate.</span></span> <span data-ttu-id="4810d-112">Четвертая команда обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="4810d-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="4810d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4810d-113">PARAMETERS</span></span>

### <span data-ttu-id="4810d-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4810d-114">-ApplicationGateway</span></span>
<span data-ttu-id="4810d-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4810d-115">The applicationGateway</span></span>

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

### <span data-ttu-id="4810d-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="4810d-116">-CertificateFile</span></span>
<span data-ttu-id="4810d-117">Путь к файлу цепочки сертификатов доверенных клиентов ЦС</span><span class="sxs-lookup"><span data-stu-id="4810d-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="4810d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4810d-118">-DefaultProfile</span></span>
<span data-ttu-id="4810d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4810d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4810d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4810d-120">-Name</span></span>
<span data-ttu-id="4810d-121">Имя цепочки сертификатов доверенного клиента ЦС</span><span class="sxs-lookup"><span data-stu-id="4810d-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="4810d-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4810d-122">-Confirm</span></span>
<span data-ttu-id="4810d-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4810d-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4810d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4810d-124">-WhatIf</span></span>
<span data-ttu-id="4810d-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4810d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4810d-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4810d-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4810d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4810d-127">CommonParameters</span></span>
<span data-ttu-id="4810d-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4810d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4810d-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4810d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4810d-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4810d-130">INPUTS</span></span>

### <span data-ttu-id="4810d-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4810d-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4810d-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4810d-132">OUTPUTS</span></span>

### <span data-ttu-id="4810d-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4810d-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4810d-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4810d-134">NOTES</span></span>

## <span data-ttu-id="4810d-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4810d-135">RELATED LINKS</span></span>

[<span data-ttu-id="4810d-136">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4810d-136">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="4810d-137">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4810d-137">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="4810d-138">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4810d-138">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="4810d-139">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4810d-139">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)