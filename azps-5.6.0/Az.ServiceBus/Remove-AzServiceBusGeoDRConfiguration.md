---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 3fa1dd4c3f926e0c6011d8ffec3a510340a7eab3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999720"
---
# <span data-ttu-id="beade-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="beade-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="beade-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="beade-102">SYNOPSIS</span></span>
<span data-ttu-id="beade-103">Удаление псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="beade-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="beade-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="beade-104">SYNTAX</span></span>

### <span data-ttu-id="beade-105">GeoDRPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="beade-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="beade-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="beade-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="beade-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="beade-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="beade-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="beade-108">DESCRIPTION</span></span>
<span data-ttu-id="beade-109">При **настройке Remove-AzServiceBusGeoDRConfiguration** удаляется псевдоним (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="beade-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="beade-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="beade-110">EXAMPLES</span></span>

### <span data-ttu-id="beade-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="beade-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="beade-112">Удаление псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="beade-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="beade-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="beade-113">PARAMETERS</span></span>

### <span data-ttu-id="beade-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="beade-114">-AsJob</span></span>
<span data-ttu-id="beade-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="beade-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="beade-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beade-116">-DefaultProfile</span></span>
<span data-ttu-id="beade-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="beade-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="beade-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="beade-118">-InputObject</span></span>
<span data-ttu-id="beade-119">Service Bus GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="beade-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="beade-120">-Name</span><span class="sxs-lookup"><span data-stu-id="beade-120">-Name</span></span>
<span data-ttu-id="beade-121">Имя псевдонима (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="beade-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="beade-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="beade-122">-Namespace</span></span>
<span data-ttu-id="beade-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="beade-123">Namespace Name</span></span>

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

### <span data-ttu-id="beade-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="beade-124">-PassThru</span></span>
<span data-ttu-id="beade-125">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="beade-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="beade-126">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="beade-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="beade-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beade-127">-ResourceGroupName</span></span>
<span data-ttu-id="beade-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="beade-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beade-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="beade-129">-ResourceId</span></span>
<span data-ttu-id="beade-130">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="beade-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="beade-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="beade-131">-Confirm</span></span>
<span data-ttu-id="beade-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="beade-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beade-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beade-133">-WhatIf</span></span>
<span data-ttu-id="beade-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="beade-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beade-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="beade-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beade-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beade-136">CommonParameters</span></span>
<span data-ttu-id="beade-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beade-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beade-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beade-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beade-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="beade-139">INPUTS</span></span>

### <span data-ttu-id="beade-140">System.String</span><span class="sxs-lookup"><span data-stu-id="beade-140">System.String</span></span>

### <span data-ttu-id="beade-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="beade-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="beade-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="beade-142">OUTPUTS</span></span>

### <span data-ttu-id="beade-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="beade-143">System.Boolean</span></span>

## <span data-ttu-id="beade-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="beade-144">NOTES</span></span>

## <span data-ttu-id="beade-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="beade-145">RELATED LINKS</span></span>
