---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 482c289922d6b8a905bee901a34568050a52c2c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411340"
---
# <span data-ttu-id="21bf4-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="21bf4-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="21bf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="21bf4-103">Создание надежного корневого сертификата для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="21bf4-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="21bf4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="21bf4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21bf4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21bf4-105">DESCRIPTION</span></span>
<span data-ttu-id="21bf4-106">Для шлюза приложения Azure создается доверенный корневой сертификат **New-AzApplicationGatewayTrustedRootCertificate.**</span><span class="sxs-lookup"><span data-stu-id="21bf4-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="21bf4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="21bf4-107">EXAMPLES</span></span>

### <span data-ttu-id="21bf4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="21bf4-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="21bf4-109">Эта команда создает доверенный корневой сертификат list "trc1" и сохраняет результат в переменной с $trc.</span><span class="sxs-lookup"><span data-stu-id="21bf4-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="21bf4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21bf4-110">PARAMETERS</span></span>

### <span data-ttu-id="21bf4-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="21bf4-111">-CertificateFile</span></span>
<span data-ttu-id="21bf4-112">Путь к файлу CER сертификата</span><span class="sxs-lookup"><span data-stu-id="21bf4-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="21bf4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21bf4-113">-DefaultProfile</span></span>
<span data-ttu-id="21bf4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="21bf4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21bf4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="21bf4-115">-Name</span></span>
<span data-ttu-id="21bf4-116">Имя сертификата TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="21bf4-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="21bf4-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21bf4-117">-Confirm</span></span>
<span data-ttu-id="21bf4-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="21bf4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21bf4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21bf4-119">-WhatIf</span></span>
<span data-ttu-id="21bf4-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21bf4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21bf4-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="21bf4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21bf4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21bf4-122">CommonParameters</span></span>
<span data-ttu-id="21bf4-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21bf4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21bf4-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21bf4-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21bf4-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21bf4-125">INPUTS</span></span>

### <span data-ttu-id="21bf4-126">Нет</span><span class="sxs-lookup"><span data-stu-id="21bf4-126">None</span></span>

## <span data-ttu-id="21bf4-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="21bf4-127">OUTPUTS</span></span>

### <span data-ttu-id="21bf4-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="21bf4-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="21bf4-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="21bf4-129">NOTES</span></span>

## <span data-ttu-id="21bf4-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21bf4-130">RELATED LINKS</span></span>

[<span data-ttu-id="21bf4-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="21bf4-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="21bf4-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="21bf4-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="21bf4-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="21bf4-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="21bf4-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="21bf4-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
