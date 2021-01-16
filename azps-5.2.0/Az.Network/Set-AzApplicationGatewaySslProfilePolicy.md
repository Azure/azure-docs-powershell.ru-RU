---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 344be8b71bc74f3620ca90dd60b61f9a59026ea0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393716"
---
# <span data-ttu-id="5ef14-101">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="5ef14-101">Set-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="5ef14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ef14-102">SYNOPSIS</span></span>
<span data-ttu-id="5ef14-103">Изменяет SSL-политику SSL-профиля SSL шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="5ef14-103">Modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="5ef14-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5ef14-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DisabledSslProtocols <String[]>] [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ef14-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ef14-105">DESCRIPTION</span></span>
<span data-ttu-id="5ef14-106">**Cmdlet Set-AzApplicationGatewaySslProfilePolicy** изменяет политику SSL профиля SSL шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="5ef14-106">The **Set-AzApplicationGatewaySslProfilePolicy** cmdlet modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="5ef14-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5ef14-107">EXAMPLES</span></span>

### <span data-ttu-id="5ef14-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5ef14-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $profile = Set-AzApplicationGatewaySslProfilePolicy -SslProfile $profile -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="5ef14-109">Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в $AppGw переменной.</span><span class="sxs-lookup"><span data-stu-id="5ef14-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="5ef14-110">Вторая команда получает профиль ssl под названием SslProfile01 для $AppGw и сохраняет параметры в $profile переменной.</span><span class="sxs-lookup"><span data-stu-id="5ef14-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="5ef14-111">Последняя команда изменяет политику ssl объекта профиля SSL, храняого в $profile.</span><span class="sxs-lookup"><span data-stu-id="5ef14-111">The last command modifies the ssl policy of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="5ef14-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ef14-112">PARAMETERS</span></span>

### <span data-ttu-id="5ef14-113">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="5ef14-113">-CipherSuite</span></span>
<span data-ttu-id="5ef14-114">Наборы шифров SSL, которые нужно включить в указанном порядке для шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="5ef14-114">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef14-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ef14-115">-DefaultProfile</span></span>
<span data-ttu-id="5ef14-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ef14-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef14-117">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="5ef14-117">-DisabledSslProtocols</span></span>
<span data-ttu-id="5ef14-118">Список SSL-протоколов, которые нужно отключить</span><span class="sxs-lookup"><span data-stu-id="5ef14-118">List of SSL protocols to be disabled</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef14-119">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="5ef14-119">-MinProtocolVersion</span></span>
<span data-ttu-id="5ef14-120">Минимальная версия SSL-протокола, поддерживаемая шлюзом приложения</span><span class="sxs-lookup"><span data-stu-id="5ef14-120">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef14-121">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="5ef14-121">-PolicyName</span></span>
<span data-ttu-id="5ef14-122">Имя предопределяемой политики SSL</span><span class="sxs-lookup"><span data-stu-id="5ef14-122">Name of Ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef14-123">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="5ef14-123">-PolicyType</span></span>
<span data-ttu-id="5ef14-124">Тип SSL-политики</span><span class="sxs-lookup"><span data-stu-id="5ef14-124">Type of Ssl Policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef14-125">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="5ef14-125">-SslProfile</span></span>
<span data-ttu-id="5ef14-126">SSL-профиль шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="5ef14-126">The application gateway SSL profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef14-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ef14-127">-Confirm</span></span>
<span data-ttu-id="5ef14-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ef14-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef14-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ef14-129">-WhatIf</span></span>
<span data-ttu-id="5ef14-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ef14-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ef14-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5ef14-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef14-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ef14-132">CommonParameters</span></span>
<span data-ttu-id="5ef14-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ef14-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ef14-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ef14-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ef14-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ef14-135">INPUTS</span></span>

### <span data-ttu-id="5ef14-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="5ef14-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="5ef14-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5ef14-137">OUTPUTS</span></span>

### <span data-ttu-id="5ef14-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="5ef14-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="5ef14-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5ef14-139">NOTES</span></span>

## <span data-ttu-id="5ef14-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ef14-140">RELATED LINKS</span></span>

[<span data-ttu-id="5ef14-141">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="5ef14-141">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="5ef14-142">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="5ef14-142">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="5ef14-143">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="5ef14-143">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="5ef14-144">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="5ef14-144">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)