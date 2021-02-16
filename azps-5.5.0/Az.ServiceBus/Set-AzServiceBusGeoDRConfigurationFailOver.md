---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 05a395ce1244130f5f11eb4e0593a1855dc8fb76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235644"
---
# <span data-ttu-id="a5a8e-101">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="a5a8e-101">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="a5a8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5a8e-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a8e-103">Вызывает отбой GEO DR и повторно настроит псевдоним, чтобы он указать на дополнительное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="a5a8e-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="a5a8e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a5a8e-104">SYNTAX</span></span>

### <span data-ttu-id="a5a8e-105">GeoDRPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5a8e-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5a8e-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a5a8e-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5a8e-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5a8e-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5a8e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5a8e-108">DESCRIPTION</span></span>
<span data-ttu-id="a5a8e-109">Cmdlet **Set-AzServiceBusGeoDRConfigurationFailOver** вызывает отбой GEO DR и повторно настроит псевдоним так, чтобы он ссылался на дополнительное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="a5a8e-109">The **Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="a5a8e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a5a8e-110">EXAMPLES</span></span>

### <span data-ttu-id="a5a8e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a5a8e-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="a5a8e-112">Вызывает отрезок failover над псевдонимом SampleDRConfigName, перенаправляет его на дополнительное пространство имен "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="a5a8e-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="a5a8e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5a8e-113">PARAMETERS</span></span>

### <span data-ttu-id="a5a8e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a8e-114">-DefaultProfile</span></span>
<span data-ttu-id="a5a8e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a8e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5a8e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5a8e-116">-InputObject</span></span>
<span data-ttu-id="a5a8e-117">Service Bus GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="a5a8e-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="a5a8e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a5a8e-118">-Name</span></span>
<span data-ttu-id="a5a8e-119">Имя конфигурации DR — псевдоним</span><span class="sxs-lookup"><span data-stu-id="a5a8e-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="a5a8e-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a5a8e-120">-Namespace</span></span>
<span data-ttu-id="a5a8e-121">Namespace Name ( Дополнительное пространство имен)</span><span class="sxs-lookup"><span data-stu-id="a5a8e-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="a5a8e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5a8e-122">-PassThru</span></span>
<span data-ttu-id="a5a8e-123">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="a5a8e-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a5a8e-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a5a8e-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a5a8e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a8e-125">-ResourceGroupName</span></span>
<span data-ttu-id="a5a8e-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a5a8e-126">Resource Group Name</span></span>

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

### <span data-ttu-id="a5a8e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5a8e-127">-ResourceId</span></span>
<span data-ttu-id="a5a8e-128">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="a5a8e-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="a5a8e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5a8e-129">-Confirm</span></span>
<span data-ttu-id="a5a8e-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5a8e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5a8e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5a8e-131">-WhatIf</span></span>
<span data-ttu-id="a5a8e-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5a8e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5a8e-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a5a8e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5a8e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a8e-134">CommonParameters</span></span>
<span data-ttu-id="a5a8e-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a8e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a8e-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5a8e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a8e-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5a8e-137">INPUTS</span></span>

### <span data-ttu-id="a5a8e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a5a8e-138">System.String</span></span>

### <span data-ttu-id="a5a8e-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="a5a8e-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="a5a8e-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a5a8e-140">OUTPUTS</span></span>

### <span data-ttu-id="a5a8e-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5a8e-141">System.Boolean</span></span>

## <span data-ttu-id="a5a8e-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a5a8e-142">NOTES</span></span>

## <span data-ttu-id="a5a8e-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5a8e-143">RELATED LINKS</span></span>
