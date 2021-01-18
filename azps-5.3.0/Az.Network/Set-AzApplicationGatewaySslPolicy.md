---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 06b8f7bdaea4ebf11ff901fbe53be94f74c9bba7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518021"
---
# <span data-ttu-id="dde36-101">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="dde36-101">Set-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="dde36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dde36-102">SYNOPSIS</span></span>
<span data-ttu-id="dde36-103">Изменяет политику SSL шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="dde36-103">Modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="dde36-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dde36-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-DisabledSslProtocols <String[]>]
 [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dde36-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dde36-105">DESCRIPTION</span></span>
<span data-ttu-id="dde36-106">**Cmdlet Set-AzApplicationGatewaySslPolicy** изменяет политику SSL шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="dde36-106">The **Set-AzApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="dde36-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dde36-107">EXAMPLES</span></span>

### <span data-ttu-id="dde36-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dde36-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="dde36-109">Первая команда получает шлюз приложения ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="dde36-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="dde36-110">Эта вторая команда изменяет политику ssl на тип "Предопределена" и имя политики AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="dde36-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="dde36-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dde36-111">PARAMETERS</span></span>

### <span data-ttu-id="dde36-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dde36-112">-ApplicationGateway</span></span>
<span data-ttu-id="dde36-113">Указывает шлюз приложения для политики SSL, которая изменяется этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dde36-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="dde36-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="dde36-114">-CipherSuite</span></span>
<span data-ttu-id="dde36-115">Наборы шифров SSL, которые нужно включить в указанном порядке для шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="dde36-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="dde36-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dde36-116">-DefaultProfile</span></span>
<span data-ttu-id="dde36-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dde36-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dde36-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="dde36-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="dde36-119">Определяет, какие протоколы отключены.</span><span class="sxs-lookup"><span data-stu-id="dde36-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="dde36-120">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="dde36-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dde36-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="dde36-121">TLSv1_0</span></span> 
- <span data-ttu-id="dde36-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="dde36-122">TLSv1_1</span></span> 
- <span data-ttu-id="dde36-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="dde36-123">TLSv1_2</span></span>

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

### <span data-ttu-id="dde36-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="dde36-124">-MinProtocolVersion</span></span>
<span data-ttu-id="dde36-125">Минимальная версия SSL-протокола, поддерживаемая шлюзом приложения</span><span class="sxs-lookup"><span data-stu-id="dde36-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="dde36-126">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="dde36-126">-PolicyName</span></span>
<span data-ttu-id="dde36-127">Имя предопределяемой политики SSL</span><span class="sxs-lookup"><span data-stu-id="dde36-127">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="dde36-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="dde36-128">-PolicyType</span></span>
<span data-ttu-id="dde36-129">Тип SSL-политики</span><span class="sxs-lookup"><span data-stu-id="dde36-129">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="dde36-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dde36-130">-Confirm</span></span>
<span data-ttu-id="dde36-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dde36-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dde36-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dde36-132">-WhatIf</span></span>
<span data-ttu-id="dde36-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dde36-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dde36-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dde36-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dde36-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde36-135">CommonParameters</span></span>
<span data-ttu-id="dde36-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dde36-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde36-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dde36-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde36-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dde36-138">INPUTS</span></span>

### <span data-ttu-id="dde36-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dde36-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dde36-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dde36-140">OUTPUTS</span></span>

### <span data-ttu-id="dde36-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dde36-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dde36-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dde36-142">NOTES</span></span>
* <span data-ttu-id="dde36-143">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="dde36-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="dde36-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dde36-144">RELATED LINKS</span></span>

[<span data-ttu-id="dde36-145">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="dde36-145">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="dde36-146">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="dde36-146">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)


