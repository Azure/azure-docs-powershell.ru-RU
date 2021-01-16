---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 482c289922d6b8a905bee901a34568050a52c2c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421780"
---
# <span data-ttu-id="a4113-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a4113-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="a4113-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4113-102">SYNOPSIS</span></span>
<span data-ttu-id="a4113-103">Создание надежного корневого сертификата для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="a4113-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="a4113-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a4113-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4113-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4113-105">DESCRIPTION</span></span>
<span data-ttu-id="a4113-106">Для шлюза приложения Azure создается доверенный корневой сертификат **New-AzApplicationGatewayTrustedRootCertificate.**</span><span class="sxs-lookup"><span data-stu-id="a4113-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="a4113-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a4113-107">EXAMPLES</span></span>

### <span data-ttu-id="a4113-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a4113-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="a4113-109">Эта команда создает доверенный корневой сертификат list "trc1" и сохраняет результат в переменной с $trc.</span><span class="sxs-lookup"><span data-stu-id="a4113-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="a4113-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4113-110">PARAMETERS</span></span>

### <span data-ttu-id="a4113-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="a4113-111">-CertificateFile</span></span>
<span data-ttu-id="a4113-112">Путь к сертификату CER-файла</span><span class="sxs-lookup"><span data-stu-id="a4113-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="a4113-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4113-113">-DefaultProfile</span></span>
<span data-ttu-id="a4113-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4113-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4113-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a4113-115">-Name</span></span>
<span data-ttu-id="a4113-116">Имя сертификата TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="a4113-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="a4113-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4113-117">-Confirm</span></span>
<span data-ttu-id="a4113-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4113-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4113-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4113-119">-WhatIf</span></span>
<span data-ttu-id="a4113-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4113-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4113-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a4113-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4113-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4113-122">CommonParameters</span></span>
<span data-ttu-id="a4113-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4113-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4113-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4113-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4113-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4113-125">INPUTS</span></span>

### <span data-ttu-id="a4113-126">Нет</span><span class="sxs-lookup"><span data-stu-id="a4113-126">None</span></span>

## <span data-ttu-id="a4113-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a4113-127">OUTPUTS</span></span>

### <span data-ttu-id="a4113-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a4113-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="a4113-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a4113-129">NOTES</span></span>

## <span data-ttu-id="a4113-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4113-130">RELATED LINKS</span></span>

[<span data-ttu-id="a4113-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a4113-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="a4113-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a4113-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="a4113-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a4113-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="a4113-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a4113-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
