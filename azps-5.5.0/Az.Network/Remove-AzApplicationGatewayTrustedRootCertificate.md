---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 3e8c4f6bc25ea5ff9b8efcee989937fb688fea57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218393"
---
# <span data-ttu-id="1a049-101">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1a049-101">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="1a049-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a049-102">SYNOPSIS</span></span>
<span data-ttu-id="1a049-103">Удаляет доверенный корневой сертификат из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1a049-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

## <span data-ttu-id="1a049-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1a049-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedRootCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a049-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a049-105">DESCRIPTION</span></span>
<span data-ttu-id="1a049-106">**Cmdlet Remove-AzApplicationGateWayTrustedRootCertificate** удаляет доверенный корневой сертификат из существующего шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1a049-106">The **Remove-AzApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="1a049-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1a049-107">EXAMPLES</span></span>

### <span data-ttu-id="1a049-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1a049-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="1a049-109">Первая команда получает шлюз приложения и сохраняет его в переменной $gw.</span><span class="sxs-lookup"><span data-stu-id="1a049-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="1a049-110">Вторая команда удаляет доверенный корневой сертификат myRootCA из шлюза приложения, который хранится в $gw.</span><span class="sxs-lookup"><span data-stu-id="1a049-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="1a049-111">Третья команда обновляет шлюз приложения в Azure.</span><span class="sxs-lookup"><span data-stu-id="1a049-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="1a049-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a049-112">PARAMETERS</span></span>

### <span data-ttu-id="1a049-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1a049-113">-ApplicationGateway</span></span>
<span data-ttu-id="1a049-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1a049-114">The applicationGateway</span></span>

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

### <span data-ttu-id="1a049-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a049-115">-DefaultProfile</span></span>
<span data-ttu-id="1a049-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a049-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a049-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1a049-117">-Name</span></span>
<span data-ttu-id="1a049-118">Имя сертификата TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="1a049-118">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a049-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a049-119">-Confirm</span></span>
<span data-ttu-id="1a049-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a049-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a049-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a049-121">-WhatIf</span></span>
<span data-ttu-id="1a049-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a049-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a049-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1a049-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a049-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a049-124">CommonParameters</span></span>
<span data-ttu-id="1a049-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a049-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a049-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a049-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a049-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a049-127">INPUTS</span></span>

### <span data-ttu-id="1a049-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1a049-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1a049-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1a049-129">OUTPUTS</span></span>

### <span data-ttu-id="1a049-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1a049-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1a049-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1a049-131">NOTES</span></span>

## <span data-ttu-id="1a049-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a049-132">RELATED LINKS</span></span>

[<span data-ttu-id="1a049-133">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1a049-133">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="1a049-134">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1a049-134">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="1a049-135">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1a049-135">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="1a049-136">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1a049-136">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
