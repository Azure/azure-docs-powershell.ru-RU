---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: f19a2e9f1531f6e009561a9d45ecae07d1bb0a3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567713"
---
# <span data-ttu-id="2ec95-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ec95-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="2ec95-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ec95-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec95-103">Создает конфигурацию автомасштабирования для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2ec95-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ec95-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ec95-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ec95-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ec95-105">DESCRIPTION</span></span>
<span data-ttu-id="2ec95-106">Командлет **New-AzureRmApplicationGatewayAutoscaleConfiguration** создает конфигурацию автомасштабирования для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="2ec95-106">The **New-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="2ec95-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ec95-107">EXAMPLES</span></span>

### <span data-ttu-id="2ec95-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2ec95-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="2ec95-109">Первая команда создает конфигурацию автомасштабирования с минимальной емкостью 3.</span><span class="sxs-lookup"><span data-stu-id="2ec95-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="2ec95-110">Вторая команда создает шлюз приложений с конфигурацией автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="2ec95-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="2ec95-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ec95-111">PARAMETERS</span></span>

### <span data-ttu-id="2ec95-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec95-112">-DefaultProfile</span></span>
<span data-ttu-id="2ec95-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ec95-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ec95-114">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="2ec95-114">-MinCapacity</span></span>
<span data-ttu-id="2ec95-115">Минимальные единицы мощности, которые будут всегда доступны [и заряжена] для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2ec95-115">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="2ec95-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ec95-116">-Confirm</span></span>
<span data-ttu-id="2ec95-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2ec95-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ec95-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ec95-118">-WhatIf</span></span>
<span data-ttu-id="2ec95-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2ec95-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ec95-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2ec95-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ec95-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec95-121">CommonParameters</span></span>
<span data-ttu-id="2ec95-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ec95-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec95-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ec95-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec95-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ec95-124">INPUTS</span></span>

### <span data-ttu-id="2ec95-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="2ec95-125">None</span></span>

## <span data-ttu-id="2ec95-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ec95-126">OUTPUTS</span></span>

### <span data-ttu-id="2ec95-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ec95-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="2ec95-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ec95-128">NOTES</span></span>

## <span data-ttu-id="2ec95-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ec95-129">RELATED LINKS</span></span>
