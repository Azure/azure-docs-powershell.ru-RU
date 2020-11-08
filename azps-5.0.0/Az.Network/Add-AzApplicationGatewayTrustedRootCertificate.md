---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: f5e8624beeb8053cbf054526cddc24c7da6cdf3f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247052"
---
# <span data-ttu-id="68eee-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="68eee-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="68eee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="68eee-102">SYNOPSIS</span></span>
<span data-ttu-id="68eee-103">Добавляет доверенный корневой сертификат в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="68eee-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="68eee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="68eee-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68eee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68eee-105">DESCRIPTION</span></span>
<span data-ttu-id="68eee-106">Командлет **Add-AzApplicationGatewayTrustedRootCertificate** добавляет доверенный корневой сертификат в шлюз приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="68eee-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="68eee-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="68eee-107">EXAMPLES</span></span>

### <span data-ttu-id="68eee-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="68eee-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="68eee-109">Первая команда получает шлюз приложения и сохраняет его в $gw переменной.</span><span class="sxs-lookup"><span data-stu-id="68eee-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="68eee-110">Вторая команда добавляет новый доверенный корневой сертификат в шлюз приложения, который принимает путь корневого сертификата в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="68eee-110">The second command adds a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="68eee-111">Третья команда создает новый параметр HTTP-базы данных с использованием доверенного корневого сертификата для проверки серверного сертификата внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="68eee-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="68eee-112">Четвертая команда обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="68eee-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="68eee-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="68eee-113">PARAMETERS</span></span>

### <span data-ttu-id="68eee-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68eee-114">-ApplicationGateway</span></span>
<span data-ttu-id="68eee-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68eee-115">The applicationGateway</span></span>

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

### <span data-ttu-id="68eee-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="68eee-116">-CertificateFile</span></span>
<span data-ttu-id="68eee-117">Путь к файлу CER сертификата</span><span class="sxs-lookup"><span data-stu-id="68eee-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="68eee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68eee-118">-DefaultProfile</span></span>
<span data-ttu-id="68eee-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68eee-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68eee-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="68eee-120">-Name</span></span>
<span data-ttu-id="68eee-121">Имя сертификата TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="68eee-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="68eee-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68eee-122">-Confirm</span></span>
<span data-ttu-id="68eee-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="68eee-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68eee-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68eee-124">-WhatIf</span></span>
<span data-ttu-id="68eee-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="68eee-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68eee-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="68eee-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68eee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68eee-127">CommonParameters</span></span>
<span data-ttu-id="68eee-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="68eee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68eee-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68eee-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68eee-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="68eee-130">INPUTS</span></span>

### <span data-ttu-id="68eee-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68eee-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="68eee-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="68eee-132">OUTPUTS</span></span>

### <span data-ttu-id="68eee-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68eee-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="68eee-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="68eee-134">NOTES</span></span>

## <span data-ttu-id="68eee-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68eee-135">RELATED LINKS</span></span>

[<span data-ttu-id="68eee-136">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="68eee-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="68eee-137">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="68eee-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="68eee-138">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="68eee-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="68eee-139">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="68eee-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
