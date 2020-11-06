---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 1ca390eb8c99ad991f5a15c6a3959d366ae5f983
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560871"
---
# <span data-ttu-id="7f05e-101">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f05e-101">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="7f05e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7f05e-102">SYNOPSIS</span></span>
<span data-ttu-id="7f05e-103">Удаляет конфигурацию автомасштабирования из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="7f05e-103">Removes Autoscale Configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f05e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7f05e-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f05e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f05e-105">DESCRIPTION</span></span>
<span data-ttu-id="7f05e-106">Командлет **Remove-AzureRmApplicationGatewayAutoscaleConfiguration** удаляет конфигурацию автомасштабирования из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="7f05e-106">The **Remove-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="7f05e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7f05e-107">EXAMPLES</span></span>

### <span data-ttu-id="7f05e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7f05e-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="7f05e-109">Первая команда получает шлюз приложения и сохраняет его в $gw переменной.</span><span class="sxs-lookup"><span data-stu-id="7f05e-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="7f05e-110">Вторая команда удаляет конфигурацию автомасштабирования из шлюза applicationg.</span><span class="sxs-lookup"><span data-stu-id="7f05e-110">The second command removes the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="7f05e-111">Третья команда обновляет шлюз приложения в Azure.</span><span class="sxs-lookup"><span data-stu-id="7f05e-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="7f05e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7f05e-112">PARAMETERS</span></span>

### <span data-ttu-id="7f05e-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f05e-113">-ApplicationGateway</span></span>
<span data-ttu-id="7f05e-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f05e-114">The applicationGateway</span></span>

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

### <span data-ttu-id="7f05e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f05e-115">-DefaultProfile</span></span>
<span data-ttu-id="7f05e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f05e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f05e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7f05e-117">-Force</span></span>
<span data-ttu-id="7f05e-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="7f05e-118">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f05e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f05e-119">-Confirm</span></span>
<span data-ttu-id="7f05e-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7f05e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f05e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f05e-121">-WhatIf</span></span>
<span data-ttu-id="7f05e-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7f05e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f05e-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7f05e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f05e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f05e-124">CommonParameters</span></span>
<span data-ttu-id="7f05e-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7f05e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f05e-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f05e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f05e-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7f05e-127">INPUTS</span></span>

### <span data-ttu-id="7f05e-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f05e-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7f05e-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f05e-129">OUTPUTS</span></span>

### <span data-ttu-id="7f05e-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f05e-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7f05e-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="7f05e-131">NOTES</span></span>

## <span data-ttu-id="7f05e-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f05e-132">RELATED LINKS</span></span>
