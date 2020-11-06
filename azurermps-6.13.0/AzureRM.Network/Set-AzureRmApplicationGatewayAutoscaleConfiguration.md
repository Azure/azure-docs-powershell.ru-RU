---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 2d7fa9dd9030f1e5878293276a248c2f6718efe5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566443"
---
# <span data-ttu-id="a695e-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a695e-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="a695e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a695e-102">SYNOPSIS</span></span>
<span data-ttu-id="a695e-103">Обновляет конфигурацию автоматического масштабирования для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="a695e-103">Updates Autoscale Configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a695e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a695e-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 -MinCapacity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a695e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a695e-105">DESCRIPTION</span></span>
<span data-ttu-id="a695e-106">Командлет **Set-AzureRmApplicationGatewayAutoscaleConfiguration** изменяет существующую конфигурацию автомасштабирования для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="a695e-106">The **Set-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="a695e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a695e-107">EXAMPLES</span></span>

### <span data-ttu-id="a695e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a695e-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="a695e-109">Первая команда получает шлюз приложения и сохраняет его в $gw переменной.</span><span class="sxs-lookup"><span data-stu-id="a695e-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="a695e-110">Вторая команда обновляет конфигурацию автомасштабирования из шлюза applicationg.</span><span class="sxs-lookup"><span data-stu-id="a695e-110">The second command updates the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="a695e-111">Третья команда обновляет шлюз приложения в Azure.</span><span class="sxs-lookup"><span data-stu-id="a695e-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="a695e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a695e-112">PARAMETERS</span></span>

### <span data-ttu-id="a695e-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a695e-113">-ApplicationGateway</span></span>
<span data-ttu-id="a695e-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a695e-114">The applicationGateway</span></span>

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

### <span data-ttu-id="a695e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a695e-115">-DefaultProfile</span></span>
<span data-ttu-id="a695e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a695e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a695e-117">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="a695e-117">-MinCapacity</span></span>
<span data-ttu-id="a695e-118">Минимальная capcity для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="a695e-118">Minimum capcity for application gateway.</span></span>

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

### <span data-ttu-id="a695e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a695e-119">-Confirm</span></span>
<span data-ttu-id="a695e-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a695e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a695e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a695e-121">-WhatIf</span></span>
<span data-ttu-id="a695e-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a695e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a695e-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a695e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a695e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a695e-124">CommonParameters</span></span>
<span data-ttu-id="a695e-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a695e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a695e-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a695e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a695e-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a695e-127">INPUTS</span></span>

### <span data-ttu-id="a695e-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a695e-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a695e-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a695e-129">OUTPUTS</span></span>

### <span data-ttu-id="a695e-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a695e-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a695e-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="a695e-131">NOTES</span></span>

## <span data-ttu-id="a695e-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a695e-132">RELATED LINKS</span></span>
