---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 3e8c4f6bc25ea5ff9b8efcee989937fb688fea57
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244795"
---
# <span data-ttu-id="0f020-101">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0f020-101">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="0f020-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f020-102">SYNOPSIS</span></span>
<span data-ttu-id="0f020-103">Удаляет доверенный корневой сертификат из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0f020-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

## <span data-ttu-id="0f020-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f020-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedRootCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f020-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f020-105">DESCRIPTION</span></span>
<span data-ttu-id="0f020-106">Командлет **Remove-AzApplicationGatewayTrustedRootCertificate** Удаляет доверенный корневой сертификат из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0f020-106">The **Remove-AzApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="0f020-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f020-107">EXAMPLES</span></span>

### <span data-ttu-id="0f020-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0f020-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="0f020-109">Первая команда получает шлюз приложения и сохраняет его в переменной $gw.</span><span class="sxs-lookup"><span data-stu-id="0f020-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="0f020-110">Вторая команда удаляет доверенный корневой сертификат с именем myRootCA из шлюза приложений, хранящегося в $gw.</span><span class="sxs-lookup"><span data-stu-id="0f020-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="0f020-111">Третья команда обновляет шлюз приложения в Azure.</span><span class="sxs-lookup"><span data-stu-id="0f020-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="0f020-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f020-112">PARAMETERS</span></span>

### <span data-ttu-id="0f020-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0f020-113">-ApplicationGateway</span></span>
<span data-ttu-id="0f020-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0f020-114">The applicationGateway</span></span>

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

### <span data-ttu-id="0f020-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f020-115">-DefaultProfile</span></span>
<span data-ttu-id="0f020-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f020-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f020-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f020-117">-Name</span></span>
<span data-ttu-id="0f020-118">Имя сертификата TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="0f020-118">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="0f020-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f020-119">-Confirm</span></span>
<span data-ttu-id="0f020-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0f020-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f020-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f020-121">-WhatIf</span></span>
<span data-ttu-id="0f020-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0f020-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f020-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0f020-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f020-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f020-124">CommonParameters</span></span>
<span data-ttu-id="0f020-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f020-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f020-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f020-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f020-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f020-127">INPUTS</span></span>

### <span data-ttu-id="0f020-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0f020-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0f020-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f020-129">OUTPUTS</span></span>

### <span data-ttu-id="0f020-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0f020-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0f020-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f020-131">NOTES</span></span>

## <span data-ttu-id="0f020-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f020-132">RELATED LINKS</span></span>

[<span data-ttu-id="0f020-133">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0f020-133">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="0f020-134">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0f020-134">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="0f020-135">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0f020-135">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="0f020-136">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0f020-136">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)