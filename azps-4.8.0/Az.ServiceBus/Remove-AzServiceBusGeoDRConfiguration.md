---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: c226f11eecc7cf046234378be7f0417da301cf40
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236626"
---
# <span data-ttu-id="b6d42-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6d42-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="b6d42-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6d42-102">SYNOPSIS</span></span>
<span data-ttu-id="b6d42-103">Удаление псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="b6d42-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="b6d42-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6d42-104">SYNTAX</span></span>

### <span data-ttu-id="b6d42-105">GeoDRPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b6d42-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6d42-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b6d42-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6d42-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6d42-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6d42-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6d42-108">DESCRIPTION</span></span>
<span data-ttu-id="b6d42-109">Командлет **Remove-AzServiceBusGeoDRConfiguration** удаляет псевдоним (конфигурацию аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="b6d42-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="b6d42-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6d42-110">EXAMPLES</span></span>

### <span data-ttu-id="b6d42-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b6d42-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="b6d42-112">Удаление псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="b6d42-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="b6d42-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6d42-113">PARAMETERS</span></span>

### <span data-ttu-id="b6d42-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6d42-114">-AsJob</span></span>
<span data-ttu-id="b6d42-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b6d42-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6d42-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6d42-116">-DefaultProfile</span></span>
<span data-ttu-id="b6d42-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6d42-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6d42-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6d42-118">-InputObject</span></span>
<span data-ttu-id="b6d42-119">Объект конфигурации служебной шины GeoDR</span><span class="sxs-lookup"><span data-stu-id="b6d42-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="b6d42-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b6d42-120">-Name</span></span>
<span data-ttu-id="b6d42-121">Имя псевдонима (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="b6d42-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="b6d42-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b6d42-122">-Namespace</span></span>
<span data-ttu-id="b6d42-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="b6d42-123">Namespace Name</span></span>

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

### <span data-ttu-id="b6d42-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6d42-124">-PassThru</span></span>
<span data-ttu-id="b6d42-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="b6d42-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b6d42-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b6d42-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b6d42-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6d42-127">-ResourceGroupName</span></span>
<span data-ttu-id="b6d42-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b6d42-128">Resource Group Name</span></span>

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

### <span data-ttu-id="b6d42-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6d42-129">-ResourceId</span></span>
<span data-ttu-id="b6d42-130">Идентификатор ресурса GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6d42-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="b6d42-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6d42-131">-Confirm</span></span>
<span data-ttu-id="b6d42-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b6d42-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6d42-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6d42-133">-WhatIf</span></span>
<span data-ttu-id="b6d42-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b6d42-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6d42-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b6d42-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6d42-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6d42-136">CommonParameters</span></span>
<span data-ttu-id="b6d42-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6d42-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6d42-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6d42-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6d42-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6d42-139">INPUTS</span></span>

### <span data-ttu-id="b6d42-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b6d42-140">System.String</span></span>

### <span data-ttu-id="b6d42-141">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="b6d42-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="b6d42-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6d42-142">OUTPUTS</span></span>

### <span data-ttu-id="b6d42-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6d42-143">System.Boolean</span></span>

## <span data-ttu-id="b6d42-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6d42-144">NOTES</span></span>

## <span data-ttu-id="b6d42-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6d42-145">RELATED LINKS</span></span>
