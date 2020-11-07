---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 175082a90a1a494eb4508bc83d71584326c9eb97
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901805"
---
# <span data-ttu-id="f68c4-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f68c4-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="f68c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f68c4-102">SYNOPSIS</span></span>
<span data-ttu-id="f68c4-103">Изменение перекрестного соединения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f68c4-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="f68c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f68c4-104">SYNTAX</span></span>

### <span data-ttu-id="f68c4-105">ModifyByCircuitReference</span><span class="sxs-lookup"><span data-stu-id="f68c4-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f68c4-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="f68c4-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f68c4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f68c4-107">DESCRIPTION</span></span>
<span data-ttu-id="f68c4-108">Командлет **Set-AzExpressRouteCrossConnection** сохраняет измененное перекрестное соединение ExpressRoute в Azure.</span><span class="sxs-lookup"><span data-stu-id="f68c4-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="f68c4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f68c4-109">EXAMPLES</span></span>

### <span data-ttu-id="f68c4-110">Пример 1: изменение состояния подготовки для перекрестного соединения ExpressRoute поставщиком услуг</span><span class="sxs-lookup"><span data-stu-id="f68c4-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="f68c4-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f68c4-111">PARAMETERS</span></span>

### <span data-ttu-id="f68c4-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f68c4-112">-AsJob</span></span>
<span data-ttu-id="f68c4-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f68c4-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f68c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f68c4-114">-DefaultProfile</span></span>
<span data-ttu-id="f68c4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f68c4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f68c4-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f68c4-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="f68c4-117">Указывает объект **ExpressRouteCrossConnection** , который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f68c4-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f68c4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f68c4-118">-Force</span></span>
<span data-ttu-id="f68c4-119">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="f68c4-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f68c4-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f68c4-120">-Name</span></span>
<span data-ttu-id="f68c4-121">Имя перекрестного соединения по экспресс же маршруту.</span><span class="sxs-lookup"><span data-stu-id="f68c4-121">The name of express route cross connection.</span></span>

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

### <span data-ttu-id="f68c4-122">-Peers</span><span class="sxs-lookup"><span data-stu-id="f68c4-122">-Peerings</span></span>
<span data-ttu-id="f68c4-123">Список одноранговых элементов для перекрестного соединения</span><span class="sxs-lookup"><span data-stu-id="f68c4-123">The list of peerings for the cross connection</span></span>

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

### <span data-ttu-id="f68c4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f68c4-124">-ResourceGroupName</span></span>
<span data-ttu-id="f68c4-125">ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f68c4-125">The ExpressRouteCrossConnection</span></span>

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

### <span data-ttu-id="f68c4-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="f68c4-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="f68c4-127">Заметки поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="f68c4-127">The service provider notes</span></span>

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

### <span data-ttu-id="f68c4-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="f68c4-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="f68c4-129">Заданное состояние подготовки поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="f68c4-129">The service provider provisioning state to be set</span></span>

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

### <span data-ttu-id="f68c4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f68c4-130">-Confirm</span></span>
<span data-ttu-id="f68c4-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f68c4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f68c4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f68c4-132">-WhatIf</span></span>
<span data-ttu-id="f68c4-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f68c4-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f68c4-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f68c4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f68c4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f68c4-135">CommonParameters</span></span>
<span data-ttu-id="f68c4-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f68c4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f68c4-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f68c4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f68c4-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f68c4-138">INPUTS</span></span>

### <span data-ttu-id="f68c4-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f68c4-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="f68c4-140">Параметр "ExpressRouteCrossConnection" принимает значение типа "PSExpressRouteCrossConnection" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f68c4-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="f68c4-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f68c4-141">OUTPUTS</span></span>

### <span data-ttu-id="f68c4-142">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f68c4-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="f68c4-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="f68c4-143">NOTES</span></span>

## <span data-ttu-id="f68c4-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f68c4-144">RELATED LINKS</span></span>

[<span data-ttu-id="f68c4-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f68c4-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)
