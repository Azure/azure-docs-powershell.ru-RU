---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: e3a92085c15116527e1b6c14d5403f68748f4f90
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402220"
---
# <span data-ttu-id="96a9e-101">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="96a9e-101">Add-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="96a9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96a9e-102">SYNOPSIS</span></span>
<span data-ttu-id="96a9e-103">Добавляет цепочку сертификатов доверенных клиентских ЦС в шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="96a9e-103">Adds a trusted client CA certificate chain to an application gateway.</span></span>

## <span data-ttu-id="96a9e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="96a9e-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96a9e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96a9e-105">DESCRIPTION</span></span>
<span data-ttu-id="96a9e-106">**Cmdlet Add-AzApplicationGatewayTrustedClientCertificate** добавляет цепочку сертификатов доверенных клиентских ЦС к шлюзу приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="96a9e-106">The **Add-AzApplicationGatewayTrustedClientCertificate** cmdlet adds a trusted client CA certificate chain to an Azure application gateway.</span></span>

## <span data-ttu-id="96a9e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="96a9e-107">EXAMPLES</span></span>

### <span data-ttu-id="96a9e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="96a9e-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfileName -ApplicationGateway $gw -TrustedClientCertificates $trustedClient
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="96a9e-109">Первая команда получает шлюз приложения и сохраняет его в $gw переменной.</span><span class="sxs-lookup"><span data-stu-id="96a9e-109">The first command gets the application gateway and stores it in $gw variable.</span></span> <span data-ttu-id="96a9e-110">Вторая команда создает новую цепочку сертификатов доверенных клиентских ЦС, принимая в качестве входных данных путь к сертификату клиентского ЦС.</span><span class="sxs-lookup"><span data-stu-id="96a9e-110">The second command creates a new trusted client CA certificate chain taking path of the client CA certificate as input.</span></span> <span data-ttu-id="96a9e-111">Третья команда создает профиль SSL с использованием сертификата надежного клиента.</span><span class="sxs-lookup"><span data-stu-id="96a9e-111">The third command creates a SSL profile using trusted client certificate.</span></span> <span data-ttu-id="96a9e-112">Четвертая команда обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="96a9e-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="96a9e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96a9e-113">PARAMETERS</span></span>

### <span data-ttu-id="96a9e-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96a9e-114">-ApplicationGateway</span></span>
<span data-ttu-id="96a9e-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96a9e-115">The applicationGateway</span></span>

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

### <span data-ttu-id="96a9e-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="96a9e-116">-CertificateFile</span></span>
<span data-ttu-id="96a9e-117">Путь к файлу цепочки сертификатов надежного клиента ЦС</span><span class="sxs-lookup"><span data-stu-id="96a9e-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="96a9e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a9e-118">-DefaultProfile</span></span>
<span data-ttu-id="96a9e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96a9e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96a9e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="96a9e-120">-Name</span></span>
<span data-ttu-id="96a9e-121">Имя цепочки сертификатов доверенного клиента ЦС</span><span class="sxs-lookup"><span data-stu-id="96a9e-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="96a9e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96a9e-122">-Confirm</span></span>
<span data-ttu-id="96a9e-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96a9e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96a9e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96a9e-124">-WhatIf</span></span>
<span data-ttu-id="96a9e-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96a9e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96a9e-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="96a9e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96a9e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a9e-127">CommonParameters</span></span>
<span data-ttu-id="96a9e-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96a9e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a9e-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96a9e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a9e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96a9e-130">INPUTS</span></span>

### <span data-ttu-id="96a9e-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96a9e-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="96a9e-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="96a9e-132">OUTPUTS</span></span>

### <span data-ttu-id="96a9e-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96a9e-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="96a9e-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="96a9e-134">NOTES</span></span>

## <span data-ttu-id="96a9e-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96a9e-135">RELATED LINKS</span></span>

[<span data-ttu-id="96a9e-136">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="96a9e-136">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="96a9e-137">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="96a9e-137">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="96a9e-138">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="96a9e-138">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="96a9e-139">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="96a9e-139">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)