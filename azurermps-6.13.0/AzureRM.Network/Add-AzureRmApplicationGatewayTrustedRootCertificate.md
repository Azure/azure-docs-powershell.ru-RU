---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: e44136d5fa9b0a6b0b979005c13faf6041d98f61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567723"
---
# <span data-ttu-id="9b981-101">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9b981-101">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="9b981-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b981-102">SYNOPSIS</span></span>
<span data-ttu-id="9b981-103">Добавляет доверенный корневой сертификат в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="9b981-103">Adds a trusted root certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b981-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b981-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b981-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b981-105">DESCRIPTION</span></span>
<span data-ttu-id="9b981-106">Командлет **Add-AzureRmApplicationGatewayTrustedRootCertificate** добавляет доверенный корневой сертификат в шлюз приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="9b981-106">The **Add-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="9b981-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b981-107">EXAMPLES</span></span>

### <span data-ttu-id="9b981-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9b981-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzureRmApplicationGatewayBackendHttpSetting -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="9b981-109">Первая команда получает шлюз приложения и сохраняет его в $gw переменной.</span><span class="sxs-lookup"><span data-stu-id="9b981-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="9b981-110">Вторая команда Addes новый доверенный корневой сертификат для шлюза приложения, который принимает путь корневого сертификата в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="9b981-110">The second command addes a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="9b981-111">Третья команда создает новый параметр HTTP-базы данных с использованием доверенного корневого сертификата для проверки серверного сертификата внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="9b981-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="9b981-112">Команда fouth обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="9b981-112">The fouth command updates the Application Gateway.</span></span>

## <span data-ttu-id="9b981-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b981-113">PARAMETERS</span></span>

### <span data-ttu-id="9b981-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b981-114">-ApplicationGateway</span></span>
<span data-ttu-id="9b981-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b981-115">The applicationGateway</span></span>

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

### <span data-ttu-id="9b981-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9b981-116">-CertificateFile</span></span>
<span data-ttu-id="9b981-117">Путь к файлу CER сертификата</span><span class="sxs-lookup"><span data-stu-id="9b981-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="9b981-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b981-118">-DefaultProfile</span></span>
<span data-ttu-id="9b981-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b981-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b981-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9b981-120">-Name</span></span>
<span data-ttu-id="9b981-121">Имя сертификата TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="9b981-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="9b981-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b981-122">-Confirm</span></span>
<span data-ttu-id="9b981-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9b981-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b981-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b981-124">-WhatIf</span></span>
<span data-ttu-id="9b981-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9b981-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b981-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9b981-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b981-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b981-127">CommonParameters</span></span>
<span data-ttu-id="9b981-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b981-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b981-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b981-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b981-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b981-130">INPUTS</span></span>

### <span data-ttu-id="9b981-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b981-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9b981-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b981-132">OUTPUTS</span></span>

### <span data-ttu-id="9b981-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b981-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9b981-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b981-134">NOTES</span></span>

## <span data-ttu-id="9b981-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b981-135">RELATED LINKS</span></span>
