---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 5af778b84981b5b15acaa688bd8ad1702e5ab7e3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390927"
---
# <span data-ttu-id="8200b-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8200b-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="8200b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8200b-102">SYNOPSIS</span></span>
<span data-ttu-id="8200b-103">Обновляет сертификат проверки подлинности для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="8200b-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="8200b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8200b-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8200b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8200b-105">DESCRIPTION</span></span>
<span data-ttu-id="8200b-106">**Cmdlet Set-AzApplicationGatewayAuthenticationCertificate** обновляет сертификат проверки подлинности для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="8200b-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="8200b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8200b-107">EXAMPLES</span></span>

### <span data-ttu-id="8200b-108">Пример 1. Обновление сертификата проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="8200b-108">Example 1: Update an authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert2.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="8200b-109">Первая команда получает шлюз приложения appGwName и сохраняет результат в переменной $appgw.</span><span class="sxs-lookup"><span data-stu-id="8200b-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="8200b-110">Вторая команда обновляет сертификат проверки подлинности с именем cert01 в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="8200b-110">The second command updates the authentication certificate named cert01 in the application gateway.</span></span>
<span data-ttu-id="8200b-111">Третья команда обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="8200b-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="8200b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8200b-112">PARAMETERS</span></span>

### <span data-ttu-id="8200b-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8200b-113">-ApplicationGateway</span></span>
<span data-ttu-id="8200b-114">Указывает имя шлюза приложения, для которого этот cmdlet обновляет сертификат проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="8200b-114">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="8200b-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="8200b-115">-CertificateFile</span></span>
<span data-ttu-id="8200b-116">Путь к файлу сертификата проверки подлинности, с помощью которого этот cmdlet обновляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="8200b-116">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="8200b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8200b-117">-DefaultProfile</span></span>
<span data-ttu-id="8200b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8200b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8200b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8200b-119">-Name</span></span>
<span data-ttu-id="8200b-120">Указывает имя сертификата проверки подлинности, который обновляется этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8200b-120">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="8200b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8200b-121">-Confirm</span></span>
<span data-ttu-id="8200b-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8200b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8200b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8200b-123">-WhatIf</span></span>
<span data-ttu-id="8200b-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8200b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8200b-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8200b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8200b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8200b-126">CommonParameters</span></span>
<span data-ttu-id="8200b-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8200b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8200b-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8200b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8200b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8200b-129">INPUTS</span></span>

### <span data-ttu-id="8200b-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8200b-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8200b-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8200b-131">OUTPUTS</span></span>

### <span data-ttu-id="8200b-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8200b-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8200b-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8200b-133">NOTES</span></span>
* <span data-ttu-id="8200b-134">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="8200b-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8200b-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8200b-135">RELATED LINKS</span></span>

[<span data-ttu-id="8200b-136">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8200b-136">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8200b-137">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8200b-137">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8200b-138">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8200b-138">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8200b-139">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8200b-139">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

