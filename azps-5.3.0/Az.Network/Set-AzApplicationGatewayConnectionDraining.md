---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: e2cecb2061b605c5380597c51cb72860596690cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506836"
---
# <span data-ttu-id="6697d-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="6697d-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="6697d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6697d-102">SYNOPSIS</span></span>
<span data-ttu-id="6697d-103">Изменяет конфигурацию разрядки подключения для конечного объекта параметров HTTP.</span><span class="sxs-lookup"><span data-stu-id="6697d-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="6697d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6697d-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6697d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6697d-105">DESCRIPTION</span></span>
<span data-ttu-id="6697d-106">**Cmdlet Set-AzApplicationGatewayWebApplicationFirewallConfiguration** изменяет конфигурацию разрядки подключения для объекта параметров HTTP.</span><span class="sxs-lookup"><span data-stu-id="6697d-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="6697d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6697d-107">EXAMPLES</span></span>

### <span data-ttu-id="6697d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6697d-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="6697d-109">Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="6697d-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6697d-110">Вторая команда получает back-end HTTP-параметры с именем Settings01 для $AppGw и сохраняет их в $Settings переменной.</span><span class="sxs-lookup"><span data-stu-id="6697d-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="6697d-111">Последняя команда изменяет конфигурацию разрядки подключения для объекта back-end HTTP settings, который хранится в $Settings, установив параметры Enabled to False и DrainTimeoutInSec на 3600.</span><span class="sxs-lookup"><span data-stu-id="6697d-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="6697d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6697d-112">PARAMETERS</span></span>

### <span data-ttu-id="6697d-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6697d-113">-BackendHttpSettings</span></span>
<span data-ttu-id="6697d-114">Параметры backend http</span><span class="sxs-lookup"><span data-stu-id="6697d-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6697d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6697d-115">-DefaultProfile</span></span>
<span data-ttu-id="6697d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6697d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6697d-117">-DrainTimeoutInsec</span><span class="sxs-lookup"><span data-stu-id="6697d-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="6697d-118">Разрядка соединения за считанные секунды активна.</span><span class="sxs-lookup"><span data-stu-id="6697d-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="6697d-119">Допустимыми являются значения от 1 секунды до 3600 секунд.</span><span class="sxs-lookup"><span data-stu-id="6697d-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6697d-120">-Enabled</span><span class="sxs-lookup"><span data-stu-id="6697d-120">-Enabled</span></span>
<span data-ttu-id="6697d-121">Включена ли разрядка подключения.</span><span class="sxs-lookup"><span data-stu-id="6697d-121">Whether connection draining is enabled or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6697d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6697d-122">CommonParameters</span></span>
<span data-ttu-id="6697d-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6697d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6697d-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6697d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6697d-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6697d-125">INPUTS</span></span>

### <span data-ttu-id="6697d-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6697d-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="6697d-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6697d-127">OUTPUTS</span></span>

### <span data-ttu-id="6697d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6697d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="6697d-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6697d-129">NOTES</span></span>

## <span data-ttu-id="6697d-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6697d-130">RELATED LINKS</span></span>

[<span data-ttu-id="6697d-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6697d-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="6697d-132">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="6697d-132">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="6697d-133">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="6697d-133">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="6697d-134">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="6697d-134">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="6697d-135">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="6697d-135">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

