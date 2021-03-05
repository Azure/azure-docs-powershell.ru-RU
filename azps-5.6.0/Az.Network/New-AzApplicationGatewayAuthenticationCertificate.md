---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: c4c2c2041c6bf21aa6bf8b13055d0dac5ffbc64a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010419"
---
# <span data-ttu-id="adec4-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="adec4-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="adec4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adec4-102">SYNOPSIS</span></span>
<span data-ttu-id="adec4-103">Создает сертификат проверки подлинности для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="adec4-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="adec4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="adec4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adec4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="adec4-105">DESCRIPTION</span></span>
<span data-ttu-id="adec4-106">**Новый-AzApplicationGatewayAuthenticationCertificate** создает сертификат проверки подлинности для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="adec4-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="adec4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="adec4-107">EXAMPLES</span></span>

### <span data-ttu-id="adec4-108">Пример 1. Создание сертификата проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="adec4-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="adec4-109">Первая команда создает сертификат проверки подлинности с именем cert01.</span><span class="sxs-lookup"><span data-stu-id="adec4-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="adec4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adec4-110">PARAMETERS</span></span>

### <span data-ttu-id="adec4-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="adec4-111">-CertificateFile</span></span>
<span data-ttu-id="adec4-112">Путь к сертификату проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="adec4-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="adec4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adec4-113">-DefaultProfile</span></span>
<span data-ttu-id="adec4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="adec4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adec4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="adec4-115">-Name</span></span>
<span data-ttu-id="adec4-116">Указывает имя сертификата проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="adec4-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="adec4-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="adec4-117">-Confirm</span></span>
<span data-ttu-id="adec4-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adec4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adec4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adec4-119">-WhatIf</span></span>
<span data-ttu-id="adec4-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adec4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adec4-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="adec4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adec4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adec4-122">CommonParameters</span></span>
<span data-ttu-id="adec4-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adec4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adec4-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adec4-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adec4-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="adec4-125">INPUTS</span></span>

### <span data-ttu-id="adec4-126">Нет</span><span class="sxs-lookup"><span data-stu-id="adec4-126">None</span></span>

## <span data-ttu-id="adec4-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="adec4-127">OUTPUTS</span></span>

### <span data-ttu-id="adec4-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="adec4-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="adec4-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="adec4-129">NOTES</span></span>
* <span data-ttu-id="adec4-130">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="adec4-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="adec4-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="adec4-131">RELATED LINKS</span></span>

[<span data-ttu-id="adec4-132">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="adec4-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="adec4-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="adec4-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="adec4-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="adec4-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="adec4-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="adec4-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


