---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 05a395ce1244130f5f11eb4e0593a1855dc8fb76
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416303"
---
# <span data-ttu-id="f900c-101">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="f900c-101">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="f900c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f900c-102">SYNOPSIS</span></span>
<span data-ttu-id="f900c-103">Вызывает отбой GEO DR и повторно настроит псевдоним, чтобы он указать на дополнительное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="f900c-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="f900c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f900c-104">SYNTAX</span></span>

### <span data-ttu-id="f900c-105">GeoDRPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f900c-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f900c-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f900c-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f900c-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f900c-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f900c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f900c-108">DESCRIPTION</span></span>
<span data-ttu-id="f900c-109">Cmdlet **Set-AzServiceBusGeoDRConfigurationFailOver** вызывает отбой GEO DR и повторно настроен псевдоним, чтобы он ссылался на дополнительное пространство имен</span><span class="sxs-lookup"><span data-stu-id="f900c-109">The **Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="f900c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f900c-110">EXAMPLES</span></span>

### <span data-ttu-id="f900c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f900c-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="f900c-112">Вызывает отрезок failover над псевдонимом SampleDRConfigName, перенаправляет его на дополнительное пространство имен "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="f900c-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="f900c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f900c-113">PARAMETERS</span></span>

### <span data-ttu-id="f900c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f900c-114">-DefaultProfile</span></span>
<span data-ttu-id="f900c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f900c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f900c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f900c-116">-InputObject</span></span>
<span data-ttu-id="f900c-117">Service Bus GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="f900c-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="f900c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f900c-118">-Name</span></span>
<span data-ttu-id="f900c-119">Имя конфигурации DR — псевдоним</span><span class="sxs-lookup"><span data-stu-id="f900c-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="f900c-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f900c-120">-Namespace</span></span>
<span data-ttu-id="f900c-121">Namespace Name ( Дополнительное пространство имен)</span><span class="sxs-lookup"><span data-stu-id="f900c-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="f900c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f900c-122">-PassThru</span></span>
<span data-ttu-id="f900c-123">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f900c-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f900c-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f900c-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f900c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f900c-125">-ResourceGroupName</span></span>
<span data-ttu-id="f900c-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f900c-126">Resource Group Name</span></span>

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

### <span data-ttu-id="f900c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f900c-127">-ResourceId</span></span>
<span data-ttu-id="f900c-128">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="f900c-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="f900c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f900c-129">-Confirm</span></span>
<span data-ttu-id="f900c-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f900c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f900c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f900c-131">-WhatIf</span></span>
<span data-ttu-id="f900c-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f900c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f900c-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f900c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f900c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f900c-134">CommonParameters</span></span>
<span data-ttu-id="f900c-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f900c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f900c-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f900c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f900c-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f900c-137">INPUTS</span></span>

### <span data-ttu-id="f900c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f900c-138">System.String</span></span>

### <span data-ttu-id="f900c-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f900c-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="f900c-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f900c-140">OUTPUTS</span></span>

### <span data-ttu-id="f900c-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f900c-141">System.Boolean</span></span>

## <span data-ttu-id="f900c-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f900c-142">NOTES</span></span>

## <span data-ttu-id="f900c-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f900c-143">RELATED LINKS</span></span>
