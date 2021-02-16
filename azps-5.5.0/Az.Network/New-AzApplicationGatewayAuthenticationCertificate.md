---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: c43fe72f8f3669b7e6e123a7f1d606771b161084
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236921"
---
# <span data-ttu-id="b07e7-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b07e7-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b07e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b07e7-102">SYNOPSIS</span></span>
<span data-ttu-id="b07e7-103">Создает сертификат проверки подлинности для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b07e7-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="b07e7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b07e7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b07e7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b07e7-105">DESCRIPTION</span></span>
<span data-ttu-id="b07e7-106">**Новый-AzApplicationGatewayAuthenticationCertificate** создает сертификат проверки подлинности для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="b07e7-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b07e7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b07e7-107">EXAMPLES</span></span>

### <span data-ttu-id="b07e7-108">Пример 1. Создание сертификата проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="b07e7-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="b07e7-109">Первая команда создает сертификат проверки подлинности с именем cert01.</span><span class="sxs-lookup"><span data-stu-id="b07e7-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="b07e7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b07e7-110">PARAMETERS</span></span>

### <span data-ttu-id="b07e7-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b07e7-111">-CertificateFile</span></span>
<span data-ttu-id="b07e7-112">Путь к сертификату проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b07e7-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="b07e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b07e7-113">-DefaultProfile</span></span>
<span data-ttu-id="b07e7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b07e7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b07e7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b07e7-115">-Name</span></span>
<span data-ttu-id="b07e7-116">Указывает имя сертификата проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b07e7-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="b07e7-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b07e7-117">-Confirm</span></span>
<span data-ttu-id="b07e7-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b07e7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b07e7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b07e7-119">-WhatIf</span></span>
<span data-ttu-id="b07e7-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b07e7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b07e7-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b07e7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b07e7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b07e7-122">CommonParameters</span></span>
<span data-ttu-id="b07e7-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b07e7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b07e7-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b07e7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b07e7-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b07e7-125">INPUTS</span></span>

### <span data-ttu-id="b07e7-126">Нет</span><span class="sxs-lookup"><span data-stu-id="b07e7-126">None</span></span>

## <span data-ttu-id="b07e7-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b07e7-127">OUTPUTS</span></span>

### <span data-ttu-id="b07e7-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b07e7-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b07e7-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b07e7-129">NOTES</span></span>
* <span data-ttu-id="b07e7-130">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="b07e7-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b07e7-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b07e7-131">RELATED LINKS</span></span>

[<span data-ttu-id="b07e7-132">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b07e7-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b07e7-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b07e7-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b07e7-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b07e7-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b07e7-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b07e7-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


