---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: c43fe72f8f3669b7e6e123a7f1d606771b161084
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411388"
---
# <span data-ttu-id="24204-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="24204-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="24204-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24204-102">SYNOPSIS</span></span>
<span data-ttu-id="24204-103">Создает сертификат проверки подлинности для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="24204-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="24204-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="24204-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24204-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24204-105">DESCRIPTION</span></span>
<span data-ttu-id="24204-106">**Новый-AzApplicationGatewayAuthenticationCertificate** создает сертификат проверки подлинности для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="24204-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="24204-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="24204-107">EXAMPLES</span></span>

### <span data-ttu-id="24204-108">Пример 1. Создание сертификата проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="24204-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="24204-109">Первая команда создает сертификат проверки подлинности с именем cert01.</span><span class="sxs-lookup"><span data-stu-id="24204-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="24204-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24204-110">PARAMETERS</span></span>

### <span data-ttu-id="24204-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="24204-111">-CertificateFile</span></span>
<span data-ttu-id="24204-112">Путь к сертификату проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="24204-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="24204-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24204-113">-DefaultProfile</span></span>
<span data-ttu-id="24204-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="24204-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24204-115">-Name</span><span class="sxs-lookup"><span data-stu-id="24204-115">-Name</span></span>
<span data-ttu-id="24204-116">Указывает имя сертификата проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="24204-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="24204-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24204-117">-Confirm</span></span>
<span data-ttu-id="24204-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24204-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24204-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24204-119">-WhatIf</span></span>
<span data-ttu-id="24204-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24204-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24204-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="24204-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24204-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24204-122">CommonParameters</span></span>
<span data-ttu-id="24204-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24204-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24204-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24204-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24204-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24204-125">INPUTS</span></span>

### <span data-ttu-id="24204-126">Нет</span><span class="sxs-lookup"><span data-stu-id="24204-126">None</span></span>

## <span data-ttu-id="24204-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="24204-127">OUTPUTS</span></span>

### <span data-ttu-id="24204-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="24204-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="24204-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="24204-129">NOTES</span></span>
* <span data-ttu-id="24204-130">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="24204-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="24204-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24204-131">RELATED LINKS</span></span>

[<span data-ttu-id="24204-132">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="24204-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="24204-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="24204-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="24204-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="24204-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="24204-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="24204-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


