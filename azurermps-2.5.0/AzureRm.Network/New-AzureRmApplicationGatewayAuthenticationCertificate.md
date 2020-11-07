---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 3847c1026f8cea6f3c33db45215a7a3253e4c680
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913811"
---
# <span data-ttu-id="be98e-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="be98e-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="be98e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be98e-102">SYNOPSIS</span></span>
<span data-ttu-id="be98e-103">Создание сертификата проверки подлинности для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="be98e-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be98e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be98e-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be98e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be98e-105">DESCRIPTION</span></span>
<span data-ttu-id="be98e-106">Командлет **New-AzureRmApplicationGatewayAuthenticationCertificate** создает сертификат для проверки подлинности для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="be98e-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="be98e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be98e-107">EXAMPLES</span></span>

### <span data-ttu-id="be98e-108">1:</span><span class="sxs-lookup"><span data-stu-id="be98e-108">1:</span></span>
```

```

## <span data-ttu-id="be98e-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be98e-109">PARAMETERS</span></span>

### <span data-ttu-id="be98e-110">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="be98e-110">-CertificateFile</span></span>
<span data-ttu-id="be98e-111">Указывает путь сертификата для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="be98e-111">Specifies the path of the authentication certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be98e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be98e-112">-DefaultProfile</span></span>
<span data-ttu-id="be98e-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be98e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be98e-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="be98e-114">-Name</span></span>
<span data-ttu-id="be98e-115">Задает имя сертификата для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="be98e-115">Specifies a name for the authentication certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be98e-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be98e-116">-Confirm</span></span>
<span data-ttu-id="be98e-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="be98e-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be98e-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be98e-118">-WhatIf</span></span>
<span data-ttu-id="be98e-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="be98e-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be98e-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="be98e-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be98e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be98e-121">CommonParameters</span></span>
<span data-ttu-id="be98e-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be98e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be98e-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be98e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be98e-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be98e-124">INPUTS</span></span>

### <span data-ttu-id="be98e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="be98e-125">System.String</span></span>

## <span data-ttu-id="be98e-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be98e-126">OUTPUTS</span></span>

### <span data-ttu-id="be98e-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="be98e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="be98e-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="be98e-128">NOTES</span></span>
* <span data-ttu-id="be98e-129">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="be98e-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="be98e-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be98e-130">RELATED LINKS</span></span>

[<span data-ttu-id="be98e-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="be98e-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="be98e-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="be98e-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="be98e-133">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="be98e-133">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="be98e-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="be98e-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


