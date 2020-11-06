---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRoutePort.md
ms.openlocfilehash: 46f73d2a58fe5f1109de6a15a5cb39e3b568a4b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566786"
---
# <span data-ttu-id="3fc30-101">Set-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3fc30-101">Set-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="3fc30-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3fc30-102">SYNOPSIS</span></span>
<span data-ttu-id="3fc30-103">Изменяет объект ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="3fc30-103">Modifies an ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fc30-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3fc30-104">SYNTAX</span></span>

```
Set-AzureRmExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fc30-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fc30-105">DESCRIPTION</span></span>
<span data-ttu-id="3fc30-106">Командлет **Set-AzureRmExpressRoutePort** сохраняет измененный ExpressRoutePort в Azure.</span><span class="sxs-lookup"><span data-stu-id="3fc30-106">The **Set-AzureRmExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="3fc30-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3fc30-107">EXAMPLES</span></span>

### <span data-ttu-id="3fc30-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3fc30-108">Example 1</span></span>
```powershell
$erport = Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzureRmExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="3fc30-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3fc30-109">Example 2</span></span>
```powershell
$erport = Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzureRmExpressRoutePort -InputObject $erport
```

<span data-ttu-id="3fc30-110">Изменяет состояние администратора для ссылки на ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3fc30-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="3fc30-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3fc30-111">PARAMETERS</span></span>

### <span data-ttu-id="3fc30-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fc30-112">-AsJob</span></span>
<span data-ttu-id="3fc30-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3fc30-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3fc30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fc30-114">-DefaultProfile</span></span>
<span data-ttu-id="3fc30-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3fc30-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fc30-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3fc30-116">-ExpressRoutePort</span></span>
<span data-ttu-id="3fc30-117">Объект ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="3fc30-117">The ExpressRoutePort object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fc30-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fc30-118">-Confirm</span></span>
<span data-ttu-id="3fc30-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3fc30-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fc30-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fc30-120">-WhatIf</span></span>
<span data-ttu-id="3fc30-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3fc30-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fc30-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3fc30-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fc30-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fc30-123">CommonParameters</span></span>
<span data-ttu-id="3fc30-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3fc30-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fc30-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fc30-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fc30-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3fc30-126">INPUTS</span></span>

### <span data-ttu-id="3fc30-127">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3fc30-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="3fc30-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fc30-128">OUTPUTS</span></span>

### <span data-ttu-id="3fc30-129">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3fc30-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="3fc30-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="3fc30-130">NOTES</span></span>

## <span data-ttu-id="3fc30-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3fc30-131">RELATED LINKS</span></span>
