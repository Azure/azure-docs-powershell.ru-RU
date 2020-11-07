---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 1a1d484d3b8d23633393c0f300f84091b06c1d0e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730756"
---
# <span data-ttu-id="c8691-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c8691-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="c8691-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8691-102">SYNOPSIS</span></span>
<span data-ttu-id="c8691-103">Добавляет сертификат проверки подлинности в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="c8691-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="c8691-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8691-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8691-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8691-105">DESCRIPTION</span></span>
<span data-ttu-id="c8691-106">Командлет **Add-AzApplicationGatewayAuthenticationCertificate** добавляет сертификат проверки подлинности в шлюз приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="c8691-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="c8691-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8691-107">EXAMPLES</span></span>

### <span data-ttu-id="c8691-108">Пример 1: Добавление сертификата проверки подлинности в шлюз приложений</span><span class="sxs-lookup"><span data-stu-id="c8691-108">Example 1: Add authentication certificate to an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="c8691-109">Первая команда получает шлюз приложения с именем appGwName и сохраняет его в $appgw переменной.</span><span class="sxs-lookup"><span data-stu-id="c8691-109">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="c8691-110">Вторая команда добавляет сертификат проверки подлинности с именем cert01 в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="c8691-110">The second command adds authentication certificate named cert01 to the application gateway.</span></span>
<span data-ttu-id="c8691-111">Третья команда обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="c8691-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="c8691-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8691-112">PARAMETERS</span></span>

### <span data-ttu-id="c8691-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8691-113">-ApplicationGateway</span></span>
<span data-ttu-id="c8691-114">Указывает имя шлюза приложений, для которого этот командлет добавляет сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="c8691-114">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="c8691-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="c8691-115">-CertificateFile</span></span>
<span data-ttu-id="c8691-116">Указывает путь к сертификату проверки подлинности, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c8691-116">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="c8691-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8691-117">-DefaultProfile</span></span>
<span data-ttu-id="c8691-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8691-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8691-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c8691-119">-Name</span></span>
<span data-ttu-id="c8691-120">Указывает имя сертификата, который добавляется этим командлетом в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="c8691-120">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="c8691-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8691-121">-Confirm</span></span>
<span data-ttu-id="c8691-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c8691-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8691-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8691-123">-WhatIf</span></span>
<span data-ttu-id="c8691-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c8691-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8691-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c8691-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8691-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8691-126">CommonParameters</span></span>
<span data-ttu-id="c8691-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8691-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8691-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8691-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8691-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8691-129">INPUTS</span></span>

### <span data-ttu-id="c8691-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8691-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c8691-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8691-131">OUTPUTS</span></span>

### <span data-ttu-id="c8691-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8691-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c8691-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8691-133">NOTES</span></span>
* <span data-ttu-id="c8691-134">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="c8691-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c8691-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8691-135">RELATED LINKS</span></span>

[<span data-ttu-id="c8691-136">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c8691-136">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c8691-137">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c8691-137">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c8691-138">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c8691-138">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c8691-139">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c8691-139">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


