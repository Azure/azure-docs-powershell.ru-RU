---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 7e1c5c301b13f37086f4b6fc96e7254230684d10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902798"
---
# <span data-ttu-id="4f318-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4f318-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="4f318-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4f318-102">SYNOPSIS</span></span>
<span data-ttu-id="4f318-103">Создание сертификата проверки подлинности для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="4f318-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="4f318-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4f318-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f318-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f318-105">DESCRIPTION</span></span>
<span data-ttu-id="4f318-106">Командлет **New-AzApplicationGatewayAuthenticationCertificate** создает сертификат для проверки подлинности для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="4f318-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="4f318-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4f318-107">EXAMPLES</span></span>

### <span data-ttu-id="4f318-108">Пример 1: создание сертификата для проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="4f318-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="4f318-109">Первая команда создает сертификат для проверки подлинности с именем cert01.</span><span class="sxs-lookup"><span data-stu-id="4f318-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="4f318-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4f318-110">PARAMETERS</span></span>

### <span data-ttu-id="4f318-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="4f318-111">-CertificateFile</span></span>
<span data-ttu-id="4f318-112">Указывает путь сертификата для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="4f318-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="4f318-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f318-113">-DefaultProfile</span></span>
<span data-ttu-id="4f318-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4f318-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f318-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4f318-115">-Name</span></span>
<span data-ttu-id="4f318-116">Задает имя сертификата для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="4f318-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="4f318-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f318-117">-Confirm</span></span>
<span data-ttu-id="4f318-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4f318-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f318-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f318-119">-WhatIf</span></span>
<span data-ttu-id="4f318-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4f318-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f318-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4f318-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f318-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f318-122">CommonParameters</span></span>
<span data-ttu-id="4f318-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4f318-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f318-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f318-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f318-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4f318-125">INPUTS</span></span>

### <span data-ttu-id="4f318-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="4f318-126">None</span></span>

## <span data-ttu-id="4f318-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f318-127">OUTPUTS</span></span>

### <span data-ttu-id="4f318-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4f318-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="4f318-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="4f318-129">NOTES</span></span>
* <span data-ttu-id="4f318-130">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="4f318-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4f318-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f318-131">RELATED LINKS</span></span>

[<span data-ttu-id="4f318-132">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4f318-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4f318-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4f318-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4f318-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4f318-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4f318-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4f318-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


