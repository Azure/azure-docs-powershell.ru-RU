---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bdc2821c8499c5a95acd180c9bbfa28568cc5034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562895"
---
# <span data-ttu-id="778a6-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="778a6-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="778a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="778a6-102">SYNOPSIS</span></span>
<span data-ttu-id="778a6-103">Создание сертификата проверки подлинности для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="778a6-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="778a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="778a6-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="778a6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="778a6-105">DESCRIPTION</span></span>
<span data-ttu-id="778a6-106">Командлет **New-AzureRmApplicationGatewayAuthenticationCertificate** создает сертификат для проверки подлинности для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="778a6-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="778a6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="778a6-107">EXAMPLES</span></span>

## <span data-ttu-id="778a6-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="778a6-108">PARAMETERS</span></span>

### <span data-ttu-id="778a6-109">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="778a6-109">-CertificateFile</span></span>
<span data-ttu-id="778a6-110">Указывает путь сертификата для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="778a6-110">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="778a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="778a6-111">-DefaultProfile</span></span>
<span data-ttu-id="778a6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="778a6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="778a6-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="778a6-113">-Name</span></span>
<span data-ttu-id="778a6-114">Задает имя сертификата для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="778a6-114">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="778a6-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="778a6-115">-Confirm</span></span>
<span data-ttu-id="778a6-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="778a6-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="778a6-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="778a6-117">-WhatIf</span></span>
<span data-ttu-id="778a6-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="778a6-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="778a6-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="778a6-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="778a6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="778a6-120">CommonParameters</span></span>
<span data-ttu-id="778a6-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="778a6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="778a6-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="778a6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="778a6-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="778a6-123">INPUTS</span></span>

### <span data-ttu-id="778a6-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="778a6-124">None</span></span>

## <span data-ttu-id="778a6-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="778a6-125">OUTPUTS</span></span>

### <span data-ttu-id="778a6-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="778a6-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="778a6-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="778a6-127">NOTES</span></span>
* <span data-ttu-id="778a6-128">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="778a6-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="778a6-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="778a6-129">RELATED LINKS</span></span>

[<span data-ttu-id="778a6-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="778a6-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="778a6-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="778a6-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="778a6-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="778a6-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="778a6-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="778a6-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


