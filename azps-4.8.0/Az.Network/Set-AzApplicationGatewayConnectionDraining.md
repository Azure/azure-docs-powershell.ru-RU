---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: e2cecb2061b605c5380597c51cb72860596690cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244329"
---
# <span data-ttu-id="c16fb-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c16fb-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="c16fb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c16fb-102">SYNOPSIS</span></span>
<span data-ttu-id="c16fb-103">Изменяет конфигурацию сток подключений для серверного объекта параметров HTTP.</span><span class="sxs-lookup"><span data-stu-id="c16fb-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="c16fb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c16fb-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c16fb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c16fb-105">DESCRIPTION</span></span>
<span data-ttu-id="c16fb-106">Командлет **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** изменяет конфигурацию сток подключений для серверного объекта параметров HTTP.</span><span class="sxs-lookup"><span data-stu-id="c16fb-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="c16fb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c16fb-107">EXAMPLES</span></span>

### <span data-ttu-id="c16fb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c16fb-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="c16fb-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c16fb-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c16fb-110">Вторая команда получает серверные параметры HTTP с именем Settings01 для $AppGw и сохраняет параметры в переменной $Settings.</span><span class="sxs-lookup"><span data-stu-id="c16fb-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="c16fb-111">Последняя команда изменяет конфигурацию сток подключений для серверного объекта параметров HTTP, сохраненного в $Settings, установив для параметра Enabled значение false и DrainTimeoutInSec на 3600.</span><span class="sxs-lookup"><span data-stu-id="c16fb-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="c16fb-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c16fb-112">PARAMETERS</span></span>

### <span data-ttu-id="c16fb-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c16fb-113">-BackendHttpSettings</span></span>
<span data-ttu-id="c16fb-114">Параметры внутренних HTTP-данных</span><span class="sxs-lookup"><span data-stu-id="c16fb-114">The backend http settings</span></span>

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

### <span data-ttu-id="c16fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c16fb-115">-DefaultProfile</span></span>
<span data-ttu-id="c16fb-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c16fb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c16fb-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="c16fb-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="c16fb-118">Число секунд, в течение которого сток подключений является активным.</span><span class="sxs-lookup"><span data-stu-id="c16fb-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="c16fb-119">Допустимые значения: от 1 секунды до 3600 секунд.</span><span class="sxs-lookup"><span data-stu-id="c16fb-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="c16fb-120">-Включено</span><span class="sxs-lookup"><span data-stu-id="c16fb-120">-Enabled</span></span>
<span data-ttu-id="c16fb-121">Включена ли сток подключений.</span><span class="sxs-lookup"><span data-stu-id="c16fb-121">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="c16fb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c16fb-122">CommonParameters</span></span>
<span data-ttu-id="c16fb-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c16fb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c16fb-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c16fb-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c16fb-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c16fb-125">INPUTS</span></span>

### <span data-ttu-id="c16fb-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c16fb-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c16fb-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c16fb-127">OUTPUTS</span></span>

### <span data-ttu-id="c16fb-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c16fb-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c16fb-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="c16fb-129">NOTES</span></span>

## <span data-ttu-id="c16fb-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c16fb-130">RELATED LINKS</span></span>

[<span data-ttu-id="c16fb-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c16fb-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="c16fb-132">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c16fb-132">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="c16fb-133">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c16fb-133">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="c16fb-134">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c16fb-134">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="c16fb-135">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c16fb-135">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

