---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 9769a5506f528eb03d5e6d5a26340b961786c363
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963992"
---
# <span data-ttu-id="38c95-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="38c95-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="38c95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38c95-102">SYNOPSIS</span></span>
<span data-ttu-id="38c95-103">Изменяет перекрестное подключение ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="38c95-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="38c95-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="38c95-104">SYNTAX</span></span>

### <span data-ttu-id="38c95-105">ModifyByCircuitReference</span><span class="sxs-lookup"><span data-stu-id="38c95-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38c95-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="38c95-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38c95-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38c95-107">DESCRIPTION</span></span>
<span data-ttu-id="38c95-108">С **его использованием** можно сохранить измененное перекрестное подключение ExpressRoute к Azure.</span><span class="sxs-lookup"><span data-stu-id="38c95-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="38c95-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="38c95-109">EXAMPLES</span></span>

### <span data-ttu-id="38c95-110">Пример 1. Изменение состояния поставщика услуг для перекрестного подключения ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="38c95-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="38c95-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38c95-111">PARAMETERS</span></span>

### <span data-ttu-id="38c95-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38c95-112">-AsJob</span></span>
<span data-ttu-id="38c95-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="38c95-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38c95-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38c95-114">-DefaultProfile</span></span>
<span data-ttu-id="38c95-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38c95-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38c95-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="38c95-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="38c95-117">Определяет объект **ExpressRouteCrossConnection,** который изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38c95-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: ModifyByCircuitReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38c95-118">-Force</span><span class="sxs-lookup"><span data-stu-id="38c95-118">-Force</span></span>
<span data-ttu-id="38c95-119">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="38c95-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="38c95-120">-Name</span><span class="sxs-lookup"><span data-stu-id="38c95-120">-Name</span></span>
<span data-ttu-id="38c95-121">Имя прямого перекрестного подключения.</span><span class="sxs-lookup"><span data-stu-id="38c95-121">The name of express route cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c95-122">-Пиринги</span><span class="sxs-lookup"><span data-stu-id="38c95-122">-Peerings</span></span>
<span data-ttu-id="38c95-123">Список пирингов для перекрестного подключения</span><span class="sxs-lookup"><span data-stu-id="38c95-123">The list of peerings for the cross connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionPeering[]
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38c95-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38c95-124">-ResourceGroupName</span></span>
<span data-ttu-id="38c95-125">The ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="38c95-125">The ExpressRouteCrossConnection</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38c95-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="38c95-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="38c95-127">Примечания поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="38c95-127">The service provider notes</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38c95-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="38c95-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="38c95-129">Состояние подготовка поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="38c95-129">The service provider provisioning state to be set</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38c95-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38c95-130">-Confirm</span></span>
<span data-ttu-id="38c95-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38c95-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38c95-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38c95-132">-WhatIf</span></span>
<span data-ttu-id="38c95-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38c95-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38c95-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="38c95-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38c95-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c95-135">CommonParameters</span></span>
<span data-ttu-id="38c95-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38c95-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38c95-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38c95-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c95-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38c95-138">INPUTS</span></span>

### <span data-ttu-id="38c95-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="38c95-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="38c95-140">Параметр "ExpressRouteCrossConnection" принимает значение типа PSExpressRouteCrossConnection из конвейера.</span><span class="sxs-lookup"><span data-stu-id="38c95-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="38c95-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="38c95-141">OUTPUTS</span></span>

### <span data-ttu-id="38c95-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="38c95-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="38c95-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="38c95-143">NOTES</span></span>

## <span data-ttu-id="38c95-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38c95-144">RELATED LINKS</span></span>

[<span data-ttu-id="38c95-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="38c95-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)
