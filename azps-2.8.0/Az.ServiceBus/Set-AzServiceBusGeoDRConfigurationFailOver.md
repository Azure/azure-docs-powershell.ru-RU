---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 4e6426b00a05568cff5b0fe1c153dcc41b36ed6d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905333"
---
# <span data-ttu-id="96285-101">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="96285-101">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="96285-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96285-102">SYNOPSIS</span></span>
<span data-ttu-id="96285-103">Вызывает отработку отказа географического восстановления и повторно конфигурирует псевдоним, чтобы он указывал на дополнительное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="96285-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="96285-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96285-104">SYNTAX</span></span>

### <span data-ttu-id="96285-105">GeoDRPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96285-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96285-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="96285-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96285-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96285-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96285-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96285-108">DESCRIPTION</span></span>
<span data-ttu-id="96285-109">Командлет **Set-AzServiceBusGeoDRConfigurationFailOver** вызывает отработку отказа в географическом процессе и повторно конфигурирует его, чтобы он указывал на дополнительное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="96285-109">The **Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="96285-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96285-110">EXAMPLES</span></span>

### <span data-ttu-id="96285-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="96285-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="96285-112">Вызывает отработку отказа для псевдонима "SampleDRConfigName", перестраивает и указывает на дополнительное пространство имен "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="96285-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="96285-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96285-113">PARAMETERS</span></span>

### <span data-ttu-id="96285-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96285-114">-DefaultProfile</span></span>
<span data-ttu-id="96285-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96285-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96285-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96285-116">-InputObject</span></span>
<span data-ttu-id="96285-117">Объект конфигурации служебной шины GeoDR</span><span class="sxs-lookup"><span data-stu-id="96285-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="96285-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="96285-118">-Name</span></span>
<span data-ttu-id="96285-119">Имя конфигурации DR — псевдоним</span><span class="sxs-lookup"><span data-stu-id="96285-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="96285-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="96285-120">-Namespace</span></span>
<span data-ttu-id="96285-121">Имя пространства имен — дополнительное пространство имен</span><span class="sxs-lookup"><span data-stu-id="96285-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="96285-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96285-122">-PassThru</span></span>
<span data-ttu-id="96285-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="96285-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="96285-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="96285-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="96285-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96285-125">-ResourceGroupName</span></span>
<span data-ttu-id="96285-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="96285-126">Resource Group Name</span></span>

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

### <span data-ttu-id="96285-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96285-127">-ResourceId</span></span>
<span data-ttu-id="96285-128">Идентификатор ресурса GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="96285-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="96285-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96285-129">-Confirm</span></span>
<span data-ttu-id="96285-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="96285-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96285-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96285-131">-WhatIf</span></span>
<span data-ttu-id="96285-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="96285-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96285-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="96285-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96285-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96285-134">CommonParameters</span></span>
<span data-ttu-id="96285-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96285-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96285-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96285-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96285-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96285-137">INPUTS</span></span>

### <span data-ttu-id="96285-138">System. String</span><span class="sxs-lookup"><span data-stu-id="96285-138">System.String</span></span>

### <span data-ttu-id="96285-139">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="96285-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="96285-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96285-140">OUTPUTS</span></span>

### <span data-ttu-id="96285-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="96285-141">System.Boolean</span></span>

## <span data-ttu-id="96285-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="96285-142">NOTES</span></span>

## <span data-ttu-id="96285-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96285-143">RELATED LINKS</span></span>
