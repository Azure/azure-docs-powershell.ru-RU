---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 8f3685fddf4796cd0ad500c261f157e8ac5b95f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909794"
---
# <span data-ttu-id="982d5-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="982d5-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="982d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="982d5-102">SYNOPSIS</span></span>
<span data-ttu-id="982d5-103">Создание сертификата проверки подлинности для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="982d5-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="982d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="982d5-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="982d5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="982d5-105">DESCRIPTION</span></span>
<span data-ttu-id="982d5-106">Командлет **New-AzApplicationGatewayAuthenticationCertificate** создает сертификат для проверки подлинности для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="982d5-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="982d5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="982d5-107">EXAMPLES</span></span>

### <span data-ttu-id="982d5-108">1:</span><span class="sxs-lookup"><span data-stu-id="982d5-108">1:</span></span>
```

```

## <span data-ttu-id="982d5-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="982d5-109">PARAMETERS</span></span>

### <span data-ttu-id="982d5-110">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="982d5-110">-CertificateFile</span></span>
<span data-ttu-id="982d5-111">Указывает путь сертификата для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="982d5-111">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="982d5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="982d5-112">-DefaultProfile</span></span>
<span data-ttu-id="982d5-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="982d5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="982d5-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="982d5-114">-Name</span></span>
<span data-ttu-id="982d5-115">Задает имя сертификата для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="982d5-115">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="982d5-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="982d5-116">-Confirm</span></span>
<span data-ttu-id="982d5-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="982d5-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="982d5-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="982d5-118">-WhatIf</span></span>
<span data-ttu-id="982d5-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="982d5-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="982d5-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="982d5-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="982d5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="982d5-121">CommonParameters</span></span>
<span data-ttu-id="982d5-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="982d5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="982d5-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="982d5-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="982d5-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="982d5-124">INPUTS</span></span>

### <span data-ttu-id="982d5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="982d5-125">System.String</span></span>

## <span data-ttu-id="982d5-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="982d5-126">OUTPUTS</span></span>

### <span data-ttu-id="982d5-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="982d5-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="982d5-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="982d5-128">NOTES</span></span>
* <span data-ttu-id="982d5-129">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="982d5-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="982d5-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="982d5-130">RELATED LINKS</span></span>

[<span data-ttu-id="982d5-131">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="982d5-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="982d5-132">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="982d5-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="982d5-133">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="982d5-133">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="982d5-134">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="982d5-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


