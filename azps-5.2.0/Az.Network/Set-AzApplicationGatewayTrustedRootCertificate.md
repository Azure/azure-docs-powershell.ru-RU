---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 746bbc2ec606bff74a49130e356bd531a3f63f8c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405159"
---
# <span data-ttu-id="39178-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="39178-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="39178-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39178-102">SYNOPSIS</span></span>
<span data-ttu-id="39178-103">Обновляет доверенный корневой сертификат шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="39178-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="39178-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="39178-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39178-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39178-105">DESCRIPTION</span></span>
<span data-ttu-id="39178-106">**Cmdlet Set-AzApplicationGatewayTrustedRootCertificate** изменяет существующий доверенный корневой сертификат шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="39178-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="39178-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="39178-107">EXAMPLES</span></span>

### <span data-ttu-id="39178-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="39178-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="39178-109">В примерах выше показано, как обновить существующий доверенный корневой сертификат при его обновлении.</span><span class="sxs-lookup"><span data-stu-id="39178-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="39178-110">Первая команда получает шлюз приложения и сохраняет его в переменной $gw.</span><span class="sxs-lookup"><span data-stu-id="39178-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="39178-111">Вторая команда изменяет существующий доверенный корневой сертификат на новый корневой сертификат.</span><span class="sxs-lookup"><span data-stu-id="39178-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="39178-112">Третья команда обновляет шлюз приложения в Azure.</span><span class="sxs-lookup"><span data-stu-id="39178-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="39178-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39178-113">PARAMETERS</span></span>

### <span data-ttu-id="39178-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39178-114">-ApplicationGateway</span></span>
<span data-ttu-id="39178-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39178-115">The applicationGateway</span></span>

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

### <span data-ttu-id="39178-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="39178-116">-CertificateFile</span></span>
<span data-ttu-id="39178-117">Путь к файлу CER сертификата</span><span class="sxs-lookup"><span data-stu-id="39178-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="39178-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39178-118">-DefaultProfile</span></span>
<span data-ttu-id="39178-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39178-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39178-120">-Name</span><span class="sxs-lookup"><span data-stu-id="39178-120">-Name</span></span>
<span data-ttu-id="39178-121">Имя сертификата TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="39178-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="39178-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39178-122">-Confirm</span></span>
<span data-ttu-id="39178-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39178-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39178-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39178-124">-WhatIf</span></span>
<span data-ttu-id="39178-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39178-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39178-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="39178-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39178-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39178-127">CommonParameters</span></span>
<span data-ttu-id="39178-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39178-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39178-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39178-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39178-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39178-130">INPUTS</span></span>

### <span data-ttu-id="39178-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39178-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="39178-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="39178-132">OUTPUTS</span></span>

### <span data-ttu-id="39178-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39178-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="39178-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="39178-134">NOTES</span></span>

## <span data-ttu-id="39178-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39178-135">RELATED LINKS</span></span>

[<span data-ttu-id="39178-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="39178-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="39178-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="39178-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="39178-138">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="39178-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="39178-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="39178-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
