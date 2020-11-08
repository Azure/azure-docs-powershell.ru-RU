---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 482c289922d6b8a905bee901a34568050a52c2c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244377"
---
# <span data-ttu-id="3dac6-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3dac6-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="3dac6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3dac6-102">SYNOPSIS</span></span>
<span data-ttu-id="3dac6-103">Создает доверенный корневой сертификат для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3dac6-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="3dac6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3dac6-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dac6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3dac6-105">DESCRIPTION</span></span>
<span data-ttu-id="3dac6-106">Командлет **New-AzApplicationGatewayTrustedRootCertificate** создает доверенный корневой сертификат для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="3dac6-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="3dac6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3dac6-107">EXAMPLES</span></span>

### <span data-ttu-id="3dac6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3dac6-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="3dac6-109">Эта команда создает доверенный корневой сертификат с именем List "trc1" и сохраняет результат в переменной с именем $trc.</span><span class="sxs-lookup"><span data-stu-id="3dac6-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="3dac6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3dac6-110">PARAMETERS</span></span>

### <span data-ttu-id="3dac6-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="3dac6-111">-CertificateFile</span></span>
<span data-ttu-id="3dac6-112">Путь к файлу CER сертификата</span><span class="sxs-lookup"><span data-stu-id="3dac6-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="3dac6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dac6-113">-DefaultProfile</span></span>
<span data-ttu-id="3dac6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3dac6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dac6-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3dac6-115">-Name</span></span>
<span data-ttu-id="3dac6-116">Имя сертификата TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="3dac6-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="3dac6-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3dac6-117">-Confirm</span></span>
<span data-ttu-id="3dac6-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3dac6-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dac6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dac6-119">-WhatIf</span></span>
<span data-ttu-id="3dac6-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3dac6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dac6-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3dac6-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dac6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dac6-122">CommonParameters</span></span>
<span data-ttu-id="3dac6-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3dac6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dac6-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dac6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dac6-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3dac6-125">INPUTS</span></span>

### <span data-ttu-id="3dac6-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="3dac6-126">None</span></span>

## <span data-ttu-id="3dac6-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3dac6-127">OUTPUTS</span></span>

### <span data-ttu-id="3dac6-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3dac6-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="3dac6-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="3dac6-129">NOTES</span></span>

## <span data-ttu-id="3dac6-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3dac6-130">RELATED LINKS</span></span>

[<span data-ttu-id="3dac6-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3dac6-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="3dac6-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3dac6-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="3dac6-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3dac6-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="3dac6-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3dac6-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
