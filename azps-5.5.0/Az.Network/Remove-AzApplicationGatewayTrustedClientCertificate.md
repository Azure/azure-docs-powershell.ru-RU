---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 40f31fc2c8cc4d0cb3a9637b39d8c3fcbd18ee42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221052"
---
# <span data-ttu-id="b68be-101">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b68be-101">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="b68be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b68be-102">SYNOPSIS</span></span>
<span data-ttu-id="b68be-103">Удаляет объект цепочки сертификатов надежного клиента из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b68be-103">Removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="b68be-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b68be-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedClientCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b68be-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b68be-105">DESCRIPTION</span></span>
<span data-ttu-id="b68be-106">**Cmdlet Remove-AzApplicationGatewayTrustedClientCertificate** удаляет объект цепочки сертификатов клиента из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b68be-106">The **Remove-AzApplicationGatewayTrustedClientCertificate** cmdlet removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="b68be-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b68be-107">EXAMPLES</span></span>

### <span data-ttu-id="b68be-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b68be-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name "TrustedClientCertificate01"
```

<span data-ttu-id="b68be-109">Первая команда получает шлюз приложения и сохраняет его в переменной $gw.</span><span class="sxs-lookup"><span data-stu-id="b68be-109">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="b68be-110">Вторая команда удаляет цепочку сертификатов доверенных клиентов CA с именем TrustedClientCertificate01 из шлюза приложения, $gw.</span><span class="sxs-lookup"><span data-stu-id="b68be-110">The second command removes the trusted client CA certificate chain named "TrustedClientCertificate01" from the application gateway stored in $gw.</span></span>

## <span data-ttu-id="b68be-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b68be-111">PARAMETERS</span></span>

### <span data-ttu-id="b68be-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b68be-112">-ApplicationGateway</span></span>
<span data-ttu-id="b68be-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b68be-113">The applicationGateway</span></span>

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

### <span data-ttu-id="b68be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b68be-114">-DefaultProfile</span></span>
<span data-ttu-id="b68be-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b68be-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b68be-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b68be-116">-Name</span></span>
<span data-ttu-id="b68be-117">Имя цепочки сертификатов доверенного клиента ЦС</span><span class="sxs-lookup"><span data-stu-id="b68be-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="b68be-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b68be-118">-Confirm</span></span>
<span data-ttu-id="b68be-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b68be-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b68be-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b68be-120">-WhatIf</span></span>
<span data-ttu-id="b68be-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b68be-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b68be-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b68be-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b68be-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b68be-123">CommonParameters</span></span>
<span data-ttu-id="b68be-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b68be-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b68be-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b68be-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b68be-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b68be-126">INPUTS</span></span>

### <span data-ttu-id="b68be-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b68be-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b68be-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b68be-128">OUTPUTS</span></span>

### <span data-ttu-id="b68be-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b68be-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b68be-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b68be-130">NOTES</span></span>

## <span data-ttu-id="b68be-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b68be-131">RELATED LINKS</span></span>

[<span data-ttu-id="b68be-132">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b68be-132">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="b68be-133">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b68be-133">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="b68be-134">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b68be-134">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="b68be-135">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b68be-135">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)