---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f45899b1c2d397245461a10a6e2648f92dc9da40
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217580"
---
# <span data-ttu-id="56b2f-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="56b2f-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="56b2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="56b2f-103">Эта операция отключает аварийное восстановление и останавливает репликацию изменений из основного в дополнительное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="56b2f-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="56b2f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="56b2f-104">SYNTAX</span></span>

### <span data-ttu-id="56b2f-105">GeoDRPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="56b2f-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56b2f-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="56b2f-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56b2f-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56b2f-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56b2f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56b2f-108">DESCRIPTION</span></span>
<span data-ttu-id="56b2f-109">Cmdlet **Set-AzServiceBusGeoDRConfigurationBreakPair** отключает аварийное восстановление и останавливает репликацию изменений из основного в дополнительное пространство имен</span><span class="sxs-lookup"><span data-stu-id="56b2f-109">The **Set-AzServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="56b2f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="56b2f-110">EXAMPLES</span></span>

### <span data-ttu-id="56b2f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="56b2f-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="56b2f-112">Эта операция отключает аварийное восстановление и останавливает репликацию изменений из основного в дополнительное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="56b2f-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="56b2f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56b2f-113">PARAMETERS</span></span>

### <span data-ttu-id="56b2f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56b2f-114">-DefaultProfile</span></span>
<span data-ttu-id="56b2f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56b2f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56b2f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56b2f-116">-InputObject</span></span>
<span data-ttu-id="56b2f-117">Service Bus GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="56b2f-117">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56b2f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="56b2f-118">-Name</span></span>
<span data-ttu-id="56b2f-119">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="56b2f-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56b2f-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="56b2f-120">-Namespace</span></span>
<span data-ttu-id="56b2f-121">Namespace Name — Primary Namespace</span><span class="sxs-lookup"><span data-stu-id="56b2f-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56b2f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56b2f-122">-PassThru</span></span>
<span data-ttu-id="56b2f-123">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="56b2f-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="56b2f-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="56b2f-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="56b2f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56b2f-125">-ResourceGroupName</span></span>
<span data-ttu-id="56b2f-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="56b2f-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56b2f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56b2f-127">-ResourceId</span></span>
<span data-ttu-id="56b2f-128">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="56b2f-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56b2f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56b2f-129">-Confirm</span></span>
<span data-ttu-id="56b2f-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="56b2f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56b2f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56b2f-131">-WhatIf</span></span>
<span data-ttu-id="56b2f-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56b2f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56b2f-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="56b2f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56b2f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56b2f-134">CommonParameters</span></span>
<span data-ttu-id="56b2f-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56b2f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56b2f-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56b2f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56b2f-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56b2f-137">INPUTS</span></span>

### <span data-ttu-id="56b2f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="56b2f-138">System.String</span></span>

### <span data-ttu-id="56b2f-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="56b2f-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="56b2f-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56b2f-140">OUTPUTS</span></span>

### <span data-ttu-id="56b2f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="56b2f-141">System.Boolean</span></span>

## <span data-ttu-id="56b2f-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="56b2f-142">NOTES</span></span>

## <span data-ttu-id="56b2f-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56b2f-143">RELATED LINKS</span></span>
