---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: e8bb89f90772006ceb567ff235746a778c840bdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990055"
---
# <span data-ttu-id="fe71c-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fe71c-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="fe71c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe71c-102">SYNOPSIS</span></span>
<span data-ttu-id="fe71c-103">Добавляет доверенный корневой сертификат к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="fe71c-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="fe71c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fe71c-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe71c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe71c-105">DESCRIPTION</span></span>
<span data-ttu-id="fe71c-106">**Cmdlet Add-AzApplicationGatewayTrustedRootCertificate** добавляет доверенный корневой сертификат к шлюзу приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="fe71c-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="fe71c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fe71c-107">EXAMPLES</span></span>

### <span data-ttu-id="fe71c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe71c-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="fe71c-109">Первая команда получает шлюз приложения и сохраняет его в $gw переменной.</span><span class="sxs-lookup"><span data-stu-id="fe71c-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="fe71c-110">Вторая команда добавляет в шлюз приложения новый доверенный корневой сертификат, который берет путь к корневому сертификату в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="fe71c-110">The second command adds a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="fe71c-111">Третья команда создает новый параметр серверной серверной почты http с использованием надежного корневого сертификата для проверки сертификата сервера серверов серверов.</span><span class="sxs-lookup"><span data-stu-id="fe71c-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="fe71c-112">Четвертая команда обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="fe71c-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="fe71c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe71c-113">PARAMETERS</span></span>

### <span data-ttu-id="fe71c-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe71c-114">-ApplicationGateway</span></span>
<span data-ttu-id="fe71c-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe71c-115">The applicationGateway</span></span>

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

### <span data-ttu-id="fe71c-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="fe71c-116">-CertificateFile</span></span>
<span data-ttu-id="fe71c-117">Путь к файлу CER сертификата</span><span class="sxs-lookup"><span data-stu-id="fe71c-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="fe71c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe71c-118">-DefaultProfile</span></span>
<span data-ttu-id="fe71c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe71c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe71c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fe71c-120">-Name</span></span>
<span data-ttu-id="fe71c-121">Имя сертификата TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="fe71c-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="fe71c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe71c-122">-Confirm</span></span>
<span data-ttu-id="fe71c-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fe71c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe71c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe71c-124">-WhatIf</span></span>
<span data-ttu-id="fe71c-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe71c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe71c-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fe71c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe71c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe71c-127">CommonParameters</span></span>
<span data-ttu-id="fe71c-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe71c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe71c-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe71c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe71c-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe71c-130">INPUTS</span></span>

### <span data-ttu-id="fe71c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe71c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fe71c-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe71c-132">OUTPUTS</span></span>

### <span data-ttu-id="fe71c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe71c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fe71c-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe71c-134">NOTES</span></span>

## <span data-ttu-id="fe71c-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe71c-135">RELATED LINKS</span></span>

[<span data-ttu-id="fe71c-136">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fe71c-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="fe71c-137">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fe71c-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="fe71c-138">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fe71c-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="fe71c-139">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fe71c-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
