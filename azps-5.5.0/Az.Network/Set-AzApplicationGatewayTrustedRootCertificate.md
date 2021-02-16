---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 746bbc2ec606bff74a49130e356bd531a3f63f8c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213444"
---
# <span data-ttu-id="e408a-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e408a-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="e408a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e408a-102">SYNOPSIS</span></span>
<span data-ttu-id="e408a-103">Обновляет доверенный корневой сертификат шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e408a-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="e408a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e408a-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e408a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e408a-105">DESCRIPTION</span></span>
<span data-ttu-id="e408a-106">**Cmdlet Set-AzApplicationGatewayTrustedRootCertificate** изменяет существующий доверенный корневой сертификат шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e408a-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="e408a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e408a-107">EXAMPLES</span></span>

### <span data-ttu-id="e408a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e408a-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="e408a-109">В примерах выше показано, как обновить существующий доверенный корневой сертификат при его обновлении.</span><span class="sxs-lookup"><span data-stu-id="e408a-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="e408a-110">Первая команда получает шлюз приложения и сохраняет его в переменной $gw.</span><span class="sxs-lookup"><span data-stu-id="e408a-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="e408a-111">Вторая команда изменяет существующий доверенный корневой сертификат на новый корневой сертификат.</span><span class="sxs-lookup"><span data-stu-id="e408a-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="e408a-112">Третья команда обновляет шлюз приложения в Azure.</span><span class="sxs-lookup"><span data-stu-id="e408a-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="e408a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e408a-113">PARAMETERS</span></span>

### <span data-ttu-id="e408a-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e408a-114">-ApplicationGateway</span></span>
<span data-ttu-id="e408a-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e408a-115">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e408a-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e408a-116">-CertificateFile</span></span>
<span data-ttu-id="e408a-117">Путь к файлу CER сертификата</span><span class="sxs-lookup"><span data-stu-id="e408a-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="e408a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e408a-118">-DefaultProfile</span></span>
<span data-ttu-id="e408a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e408a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e408a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e408a-120">-Name</span></span>
<span data-ttu-id="e408a-121">Имя сертификата TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="e408a-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="e408a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e408a-122">-Confirm</span></span>
<span data-ttu-id="e408a-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e408a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e408a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e408a-124">-WhatIf</span></span>
<span data-ttu-id="e408a-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e408a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e408a-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e408a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e408a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e408a-127">CommonParameters</span></span>
<span data-ttu-id="e408a-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e408a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e408a-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e408a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e408a-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e408a-130">INPUTS</span></span>

### <span data-ttu-id="e408a-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e408a-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e408a-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e408a-132">OUTPUTS</span></span>

### <span data-ttu-id="e408a-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e408a-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e408a-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e408a-134">NOTES</span></span>

## <span data-ttu-id="e408a-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e408a-135">RELATED LINKS</span></span>

[<span data-ttu-id="e408a-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e408a-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="e408a-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e408a-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="e408a-138">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e408a-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="e408a-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e408a-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
