---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: c4c23b877ae42703ade4b163c8c09d9156725e77
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729173"
---
# <span data-ttu-id="07a85-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="07a85-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="07a85-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07a85-102">SYNOPSIS</span></span>
<span data-ttu-id="07a85-103">Удаление псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="07a85-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="07a85-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07a85-104">SYNTAX</span></span>

### <span data-ttu-id="07a85-105">GeoDRPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07a85-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07a85-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="07a85-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07a85-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07a85-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07a85-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07a85-108">DESCRIPTION</span></span>
<span data-ttu-id="07a85-109">Командлет **Remove-AzServiceBusGeoDRConfiguration** удаляет псевдоним (конфигурацию аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="07a85-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="07a85-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07a85-110">EXAMPLES</span></span>

### <span data-ttu-id="07a85-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="07a85-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="07a85-112">Удаление псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="07a85-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="07a85-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07a85-113">PARAMETERS</span></span>

### <span data-ttu-id="07a85-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07a85-114">-AsJob</span></span>
<span data-ttu-id="07a85-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="07a85-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07a85-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07a85-116">-DefaultProfile</span></span>
<span data-ttu-id="07a85-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07a85-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07a85-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07a85-118">-InputObject</span></span>
<span data-ttu-id="07a85-119">Объект конфигурации служебной шины GeoDR</span><span class="sxs-lookup"><span data-stu-id="07a85-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="07a85-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="07a85-120">-Name</span></span>
<span data-ttu-id="07a85-121">Имя псевдонима (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="07a85-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="07a85-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="07a85-122">-Namespace</span></span>
<span data-ttu-id="07a85-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="07a85-123">Namespace Name</span></span>

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

### <span data-ttu-id="07a85-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07a85-124">-PassThru</span></span>
<span data-ttu-id="07a85-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="07a85-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="07a85-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="07a85-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="07a85-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07a85-127">-ResourceGroupName</span></span>
<span data-ttu-id="07a85-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="07a85-128">Resource Group Name</span></span>

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

### <span data-ttu-id="07a85-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07a85-129">-ResourceId</span></span>
<span data-ttu-id="07a85-130">Идентификатор ресурса GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="07a85-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="07a85-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07a85-131">-Confirm</span></span>
<span data-ttu-id="07a85-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="07a85-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07a85-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07a85-133">-WhatIf</span></span>
<span data-ttu-id="07a85-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="07a85-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07a85-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="07a85-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07a85-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a85-136">CommonParameters</span></span>
<span data-ttu-id="07a85-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07a85-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a85-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07a85-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a85-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07a85-139">INPUTS</span></span>

### <span data-ttu-id="07a85-140">System. String</span><span class="sxs-lookup"><span data-stu-id="07a85-140">System.String</span></span>

### <span data-ttu-id="07a85-141">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="07a85-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="07a85-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07a85-142">OUTPUTS</span></span>

### <span data-ttu-id="07a85-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="07a85-143">System.Boolean</span></span>

## <span data-ttu-id="07a85-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="07a85-144">NOTES</span></span>

## <span data-ttu-id="07a85-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07a85-145">RELATED LINKS</span></span>
