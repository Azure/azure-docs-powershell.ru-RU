---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 285e9c343ed18d4aa21c328344b7be82319f0d3b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227745"
---
# <span data-ttu-id="ff0d5-101">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ff0d5-101">New-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="ff0d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff0d5-102">SYNOPSIS</span></span>
<span data-ttu-id="ff0d5-103">Создает цепочку сертификатов доверенных клиентских ЦС для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="ff0d5-103">Creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="ff0d5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ff0d5-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedClientCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff0d5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff0d5-105">DESCRIPTION</span></span>
<span data-ttu-id="ff0d5-106">С New-AzApplicationGatewayTrustedClientCertificate создается цепочка сертификатов доверенных клиентских ЦС для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="ff0d5-106">The New-AzApplicationGatewayTrustedClientCertificate cmdlet creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="ff0d5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ff0d5-107">EXAMPLES</span></span>

### <span data-ttu-id="ff0d5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ff0d5-108">Example 1</span></span>
```powershell
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
```
<span data-ttu-id="ff0d5-109">Команда создает надежный объект цепочки сертификатов клиента, который в качестве входных данных берет путь к сертификату клиентского ЦС.</span><span class="sxs-lookup"><span data-stu-id="ff0d5-109">The command creates a new trusted client CA certificate chain object taking path of the client CA certificate as input.</span></span>

## <span data-ttu-id="ff0d5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff0d5-110">PARAMETERS</span></span>

### <span data-ttu-id="ff0d5-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="ff0d5-111">-CertificateFile</span></span>
<span data-ttu-id="ff0d5-112">Путь к файлу цепочки сертификатов надежного клиента ЦС</span><span class="sxs-lookup"><span data-stu-id="ff0d5-112">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="ff0d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff0d5-113">-DefaultProfile</span></span>
<span data-ttu-id="ff0d5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff0d5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff0d5-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ff0d5-115">-Name</span></span>
<span data-ttu-id="ff0d5-116">Имя цепочки сертификатов доверенного клиента ЦС</span><span class="sxs-lookup"><span data-stu-id="ff0d5-116">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="ff0d5-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff0d5-117">-Confirm</span></span>
<span data-ttu-id="ff0d5-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff0d5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff0d5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff0d5-119">-WhatIf</span></span>
<span data-ttu-id="ff0d5-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff0d5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff0d5-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ff0d5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff0d5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff0d5-122">CommonParameters</span></span>
<span data-ttu-id="ff0d5-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff0d5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff0d5-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff0d5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff0d5-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff0d5-125">INPUTS</span></span>

### <span data-ttu-id="ff0d5-126">Нет</span><span class="sxs-lookup"><span data-stu-id="ff0d5-126">None</span></span>

## <span data-ttu-id="ff0d5-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ff0d5-127">OUTPUTS</span></span>

### <span data-ttu-id="ff0d5-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ff0d5-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="ff0d5-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ff0d5-129">NOTES</span></span>

## <span data-ttu-id="ff0d5-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff0d5-130">RELATED LINKS</span></span>

[<span data-ttu-id="ff0d5-131">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ff0d5-131">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="ff0d5-132">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ff0d5-132">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="ff0d5-133">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ff0d5-133">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="ff0d5-134">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ff0d5-134">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)