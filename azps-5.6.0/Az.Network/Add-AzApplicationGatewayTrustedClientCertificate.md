---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: ac4da06b2f90f9d7bb5c3cbccbde98c8c65db481
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982472"
---
# <span data-ttu-id="c73dd-101">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c73dd-101">Add-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="c73dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c73dd-102">SYNOPSIS</span></span>
<span data-ttu-id="c73dd-103">Добавляет цепочку сертификатов доверенных клиентских ЦС в шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="c73dd-103">Adds a trusted client CA certificate chain to an application gateway.</span></span>

## <span data-ttu-id="c73dd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c73dd-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c73dd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c73dd-105">DESCRIPTION</span></span>
<span data-ttu-id="c73dd-106">**Cmdlet Add-AzApplicationGatewayTrustedClientCertificate** добавляет цепочку сертификатов доверенных клиентских ЦС к шлюзу приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="c73dd-106">The **Add-AzApplicationGatewayTrustedClientCertificate** cmdlet adds a trusted client CA certificate chain to an Azure application gateway.</span></span>

## <span data-ttu-id="c73dd-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c73dd-107">EXAMPLES</span></span>

### <span data-ttu-id="c73dd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c73dd-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfileName -ApplicationGateway $gw -TrustedClientCertificates $trustedClient
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="c73dd-109">Первая команда получает шлюз приложения и сохраняет его в $gw переменной.</span><span class="sxs-lookup"><span data-stu-id="c73dd-109">The first command gets the application gateway and stores it in $gw variable.</span></span> <span data-ttu-id="c73dd-110">Вторая команда создает новую цепочку сертификатов доверенных клиентских ЦС, принимая в качестве входных данных путь к сертификату клиентского ЦС.</span><span class="sxs-lookup"><span data-stu-id="c73dd-110">The second command creates a new trusted client CA certificate chain taking path of the client CA certificate as input.</span></span> <span data-ttu-id="c73dd-111">Третья команда создает профиль SSL с использованием сертификата надежного клиента.</span><span class="sxs-lookup"><span data-stu-id="c73dd-111">The third command creates a SSL profile using trusted client certificate.</span></span> <span data-ttu-id="c73dd-112">Четвертая команда обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="c73dd-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="c73dd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c73dd-113">PARAMETERS</span></span>

### <span data-ttu-id="c73dd-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c73dd-114">-ApplicationGateway</span></span>
<span data-ttu-id="c73dd-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c73dd-115">The applicationGateway</span></span>

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

### <span data-ttu-id="c73dd-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="c73dd-116">-CertificateFile</span></span>
<span data-ttu-id="c73dd-117">Путь к файлу цепочки сертификатов надежного клиента ЦС</span><span class="sxs-lookup"><span data-stu-id="c73dd-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="c73dd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c73dd-118">-DefaultProfile</span></span>
<span data-ttu-id="c73dd-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c73dd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c73dd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c73dd-120">-Name</span></span>
<span data-ttu-id="c73dd-121">Имя цепочки сертификатов доверенного клиента ЦС</span><span class="sxs-lookup"><span data-stu-id="c73dd-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="c73dd-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c73dd-122">-Confirm</span></span>
<span data-ttu-id="c73dd-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c73dd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c73dd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c73dd-124">-WhatIf</span></span>
<span data-ttu-id="c73dd-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c73dd-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c73dd-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c73dd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c73dd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c73dd-127">CommonParameters</span></span>
<span data-ttu-id="c73dd-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c73dd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c73dd-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c73dd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c73dd-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c73dd-130">INPUTS</span></span>

### <span data-ttu-id="c73dd-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c73dd-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c73dd-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c73dd-132">OUTPUTS</span></span>

### <span data-ttu-id="c73dd-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c73dd-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c73dd-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c73dd-134">NOTES</span></span>

## <span data-ttu-id="c73dd-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c73dd-135">RELATED LINKS</span></span>

[<span data-ttu-id="c73dd-136">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c73dd-136">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="c73dd-137">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c73dd-137">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="c73dd-138">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c73dd-138">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="c73dd-139">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c73dd-139">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)