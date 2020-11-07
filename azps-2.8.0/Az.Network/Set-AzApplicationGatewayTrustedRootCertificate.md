---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: e94ca1bbed8e37643b301e5a5cb2ca3acc78d264
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901818"
---
# <span data-ttu-id="f6c2c-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f6c2c-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="f6c2c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6c2c-102">SYNOPSIS</span></span>
<span data-ttu-id="f6c2c-103">Обновляет доверенный корневой сертификат шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="f6c2c-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="f6c2c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6c2c-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6c2c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6c2c-105">DESCRIPTION</span></span>
<span data-ttu-id="f6c2c-106">Командлет **Set-AzApplicationGatewayTrustedRootCertificate** изменяет существующий доверенный корневой сертификат шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="f6c2c-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="f6c2c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6c2c-107">EXAMPLES</span></span>

### <span data-ttu-id="f6c2c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f6c2c-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="f6c2c-109">В приведенных выше примерах сценариев показано, как обновить существующий доверенный корневой сертификат при развертывании корневого сертификата.</span><span class="sxs-lookup"><span data-stu-id="f6c2c-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="f6c2c-110">Первая команда получает шлюз приложения и сохраняет его в переменной $gw.</span><span class="sxs-lookup"><span data-stu-id="f6c2c-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="f6c2c-111">Вторая команда изменяет существующий доверенный корневой сертификат с новым корневым сертификатом.</span><span class="sxs-lookup"><span data-stu-id="f6c2c-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="f6c2c-112">Третья команда обновляет шлюз приложения в Azure.</span><span class="sxs-lookup"><span data-stu-id="f6c2c-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="f6c2c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6c2c-113">PARAMETERS</span></span>

### <span data-ttu-id="f6c2c-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6c2c-114">-ApplicationGateway</span></span>
<span data-ttu-id="f6c2c-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6c2c-115">The applicationGateway</span></span>

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

### <span data-ttu-id="f6c2c-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f6c2c-116">-CertificateFile</span></span>
<span data-ttu-id="f6c2c-117">Путь к файлу CER сертификата</span><span class="sxs-lookup"><span data-stu-id="f6c2c-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="f6c2c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6c2c-118">-DefaultProfile</span></span>
<span data-ttu-id="f6c2c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6c2c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6c2c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f6c2c-120">-Name</span></span>
<span data-ttu-id="f6c2c-121">Имя сертификата TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="f6c2c-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="f6c2c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6c2c-122">-Confirm</span></span>
<span data-ttu-id="f6c2c-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f6c2c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6c2c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6c2c-124">-WhatIf</span></span>
<span data-ttu-id="f6c2c-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f6c2c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6c2c-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f6c2c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6c2c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6c2c-127">CommonParameters</span></span>
<span data-ttu-id="f6c2c-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6c2c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6c2c-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6c2c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6c2c-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6c2c-130">INPUTS</span></span>

### <span data-ttu-id="f6c2c-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6c2c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f6c2c-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6c2c-132">OUTPUTS</span></span>

### <span data-ttu-id="f6c2c-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6c2c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f6c2c-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6c2c-134">NOTES</span></span>

## <span data-ttu-id="f6c2c-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6c2c-135">RELATED LINKS</span></span>

[<span data-ttu-id="f6c2c-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f6c2c-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f6c2c-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f6c2c-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f6c2c-138">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f6c2c-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f6c2c-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f6c2c-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
