---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 5f52b68e538072e6ff6aecde99f59337b532130c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220956"
---
# <span data-ttu-id="b90c6-101">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b90c6-101">Set-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="b90c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b90c6-102">SYNOPSIS</span></span>
<span data-ttu-id="b90c6-103">Изменяет цепочку сертификатов доверенных клиентских ЦС шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b90c6-103">Modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="b90c6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b90c6-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b90c6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b90c6-105">DESCRIPTION</span></span>
<span data-ttu-id="b90c6-106">The **Set-AzApplicationGatewayTrustedClientCertificate cmdificate** the trusted client CA certificate chain of an application gateway.</span><span class="sxs-lookup"><span data-stu-id="b90c6-106">The **Set-AzApplicationGatewayTrustedClientCertificate** cmdlet modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="b90c6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b90c6-107">EXAMPLES</span></span>

### <span data-ttu-id="b90c6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b90c6-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\clientCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="b90c6-109">В примерах выше показано, как обновить существующий объект цепочки сертификатов доверенных клиентов.</span><span class="sxs-lookup"><span data-stu-id="b90c6-109">Above example scenarios shows how to update an existing trusted client CA certificate chain object.</span></span> <span data-ttu-id="b90c6-110">Первая команда получает шлюз приложения и сохраняет его в переменной $gw.</span><span class="sxs-lookup"><span data-stu-id="b90c6-110">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="b90c6-111">Вторая команда изменяет существующий объект цепочки сертификатов доверенного клиента с помощью нового файла цепочки сертификатов ЦС.</span><span class="sxs-lookup"><span data-stu-id="b90c6-111">The second command modifies the existing trusted client CA certificate chain object with a new CA certificate chain file.</span></span> <span data-ttu-id="b90c6-112">Третья команда обновляет шлюз приложения в Azure.</span><span class="sxs-lookup"><span data-stu-id="b90c6-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="b90c6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b90c6-113">PARAMETERS</span></span>

### <span data-ttu-id="b90c6-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b90c6-114">-ApplicationGateway</span></span>
<span data-ttu-id="b90c6-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b90c6-115">The applicationGateway</span></span>

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

### <span data-ttu-id="b90c6-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b90c6-116">-CertificateFile</span></span>
<span data-ttu-id="b90c6-117">Путь к файлу цепочки сертификатов доверенных клиентов ЦС</span><span class="sxs-lookup"><span data-stu-id="b90c6-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="b90c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b90c6-118">-DefaultProfile</span></span>
<span data-ttu-id="b90c6-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b90c6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b90c6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b90c6-120">-Name</span></span>
<span data-ttu-id="b90c6-121">Имя цепочки сертификатов доверенного клиента ЦС</span><span class="sxs-lookup"><span data-stu-id="b90c6-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="b90c6-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b90c6-122">-Confirm</span></span>
<span data-ttu-id="b90c6-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b90c6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b90c6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b90c6-124">-WhatIf</span></span>
<span data-ttu-id="b90c6-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b90c6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b90c6-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b90c6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b90c6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b90c6-127">CommonParameters</span></span>
<span data-ttu-id="b90c6-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b90c6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b90c6-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b90c6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b90c6-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b90c6-130">INPUTS</span></span>

### <span data-ttu-id="b90c6-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b90c6-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b90c6-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b90c6-132">OUTPUTS</span></span>

### <span data-ttu-id="b90c6-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b90c6-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b90c6-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b90c6-134">NOTES</span></span>

## <span data-ttu-id="b90c6-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b90c6-135">RELATED LINKS</span></span>

[<span data-ttu-id="b90c6-136">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b90c6-136">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="b90c6-137">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b90c6-137">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="b90c6-138">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b90c6-138">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="b90c6-139">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b90c6-139">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)