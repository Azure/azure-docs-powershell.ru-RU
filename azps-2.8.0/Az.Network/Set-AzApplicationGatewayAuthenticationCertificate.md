---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 6e0194135b93898ea14998d92f8f23afd612f221
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901861"
---
# <span data-ttu-id="4dc17-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4dc17-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="4dc17-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4dc17-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc17-103">Обновляет сертификат проверки подлинности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="4dc17-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="4dc17-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4dc17-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dc17-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4dc17-105">DESCRIPTION</span></span>
<span data-ttu-id="4dc17-106">Командлет **Set-AzApplicationGatewayAuthenticationCertificate** обновляет сертификат проверки подлинности для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="4dc17-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="4dc17-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4dc17-107">EXAMPLES</span></span>

### <span data-ttu-id="4dc17-108">Пример 1: обновление сертификата для проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="4dc17-108">Example 1: Update an authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert2.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="4dc17-109">Первая команда получает шлюз приложения с именем appGwName и сохраняет результат в переменной $appgw.</span><span class="sxs-lookup"><span data-stu-id="4dc17-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="4dc17-110">Вторая команда обновляет сертификат проверки подлинности с именем cert01 на шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="4dc17-110">The second command updates the authentication certificate named cert01 in the application gateway.</span></span>
<span data-ttu-id="4dc17-111">Третья команда обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="4dc17-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="4dc17-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4dc17-112">PARAMETERS</span></span>

### <span data-ttu-id="4dc17-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4dc17-113">-ApplicationGateway</span></span>
<span data-ttu-id="4dc17-114">Указывает имя шлюза приложений, для которого этот командлет обновляет сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="4dc17-114">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="4dc17-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="4dc17-115">-CertificateFile</span></span>
<span data-ttu-id="4dc17-116">Задает путь к файлу сертификата проверки подлинности, с помощью которого этот командлет обновляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="4dc17-116">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="4dc17-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc17-117">-DefaultProfile</span></span>
<span data-ttu-id="4dc17-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4dc17-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4dc17-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4dc17-119">-Name</span></span>
<span data-ttu-id="4dc17-120">Указывает имя сертификата проверки подлинности, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="4dc17-120">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="4dc17-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4dc17-121">-Confirm</span></span>
<span data-ttu-id="4dc17-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4dc17-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dc17-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dc17-123">-WhatIf</span></span>
<span data-ttu-id="4dc17-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4dc17-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dc17-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4dc17-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dc17-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc17-126">CommonParameters</span></span>
<span data-ttu-id="4dc17-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4dc17-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc17-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dc17-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc17-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4dc17-129">INPUTS</span></span>

### <span data-ttu-id="4dc17-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4dc17-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4dc17-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4dc17-131">OUTPUTS</span></span>

### <span data-ttu-id="4dc17-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4dc17-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4dc17-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="4dc17-133">NOTES</span></span>
* <span data-ttu-id="4dc17-134">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="4dc17-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4dc17-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4dc17-135">RELATED LINKS</span></span>

[<span data-ttu-id="4dc17-136">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4dc17-136">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4dc17-137">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4dc17-137">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4dc17-138">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4dc17-138">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4dc17-139">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4dc17-139">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


