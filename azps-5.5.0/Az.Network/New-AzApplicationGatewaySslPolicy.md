---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: cf2f2ef91fa217b1710eeb100f4e3e6c2ce6fb9d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221148"
---
# <span data-ttu-id="d3da5-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="d3da5-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="d3da5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3da5-102">SYNOPSIS</span></span>
<span data-ttu-id="d3da5-103">Создает SSL-политику для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="d3da5-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="d3da5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d3da5-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy [-DisabledSslProtocols <String[]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3da5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3da5-105">DESCRIPTION</span></span>
<span data-ttu-id="d3da5-106">**Cmdlet New-AzApplicationGatewaySslPolicy** создает политику SSL для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="d3da5-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="d3da5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d3da5-107">EXAMPLES</span></span>

### <span data-ttu-id="d3da5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d3da5-108">Example 1</span></span>
```powershell
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="d3da5-109">Эта команда создает настраиваемую политику.</span><span class="sxs-lookup"><span data-stu-id="d3da5-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="d3da5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3da5-110">PARAMETERS</span></span>

### <span data-ttu-id="d3da5-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="d3da5-111">-CipherSuite</span></span>
<span data-ttu-id="d3da5-112">Наборы шифров SSL, которые нужно включить в указанном порядке для шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="d3da5-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3da5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3da5-113">-DefaultProfile</span></span>
<span data-ttu-id="d3da5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3da5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3da5-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="d3da5-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="d3da5-116">Определяет, какие протоколы отключены.</span><span class="sxs-lookup"><span data-stu-id="d3da5-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="d3da5-117">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="d3da5-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d3da5-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="d3da5-118">TLSv1_0</span></span> 
- <span data-ttu-id="d3da5-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="d3da5-119">TLSv1_1</span></span> 
- <span data-ttu-id="d3da5-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="d3da5-120">TLSv1_2</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3da5-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="d3da5-121">-MinProtocolVersion</span></span>
<span data-ttu-id="d3da5-122">Минимальная версия SSL-протокола, поддерживаемая шлюзом приложения</span><span class="sxs-lookup"><span data-stu-id="d3da5-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3da5-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="d3da5-123">-PolicyName</span></span>
<span data-ttu-id="d3da5-124">Имя предопределяемой политики SSL</span><span class="sxs-lookup"><span data-stu-id="d3da5-124">Name of Ssl predefined policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3da5-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="d3da5-125">-PolicyType</span></span>
<span data-ttu-id="d3da5-126">Тип SSL-политики</span><span class="sxs-lookup"><span data-stu-id="d3da5-126">Type of Ssl Policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3da5-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3da5-127">-Confirm</span></span>
<span data-ttu-id="d3da5-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3da5-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3da5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3da5-129">-WhatIf</span></span>
<span data-ttu-id="d3da5-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3da5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3da5-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d3da5-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3da5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3da5-132">CommonParameters</span></span>
<span data-ttu-id="d3da5-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3da5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3da5-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3da5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3da5-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3da5-135">INPUTS</span></span>

### <span data-ttu-id="d3da5-136">Нет</span><span class="sxs-lookup"><span data-stu-id="d3da5-136">None</span></span>

## <span data-ttu-id="d3da5-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3da5-137">OUTPUTS</span></span>

### <span data-ttu-id="d3da5-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="d3da5-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="d3da5-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d3da5-139">NOTES</span></span>
* <span data-ttu-id="d3da5-140">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="d3da5-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d3da5-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3da5-141">RELATED LINKS</span></span>

[<span data-ttu-id="d3da5-142">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="d3da5-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="d3da5-143">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="d3da5-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


