---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: c226f11eecc7cf046234378be7f0417da301cf40
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391831"
---
# <span data-ttu-id="cef99-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="cef99-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="cef99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cef99-102">SYNOPSIS</span></span>
<span data-ttu-id="cef99-103">Удаляет псевдоним (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="cef99-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="cef99-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cef99-104">SYNTAX</span></span>

### <span data-ttu-id="cef99-105">GeoDRPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cef99-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef99-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cef99-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef99-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cef99-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cef99-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cef99-108">DESCRIPTION</span></span>
<span data-ttu-id="cef99-109">При **настройке Remove-AzServiceBusGeoDRConfiguration** удаляется псевдоним (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="cef99-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="cef99-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cef99-110">EXAMPLES</span></span>

### <span data-ttu-id="cef99-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cef99-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="cef99-112">Удаляет псевдоним (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="cef99-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="cef99-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cef99-113">PARAMETERS</span></span>

### <span data-ttu-id="cef99-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cef99-114">-AsJob</span></span>
<span data-ttu-id="cef99-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cef99-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cef99-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef99-116">-DefaultProfile</span></span>
<span data-ttu-id="cef99-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cef99-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cef99-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cef99-118">-InputObject</span></span>
<span data-ttu-id="cef99-119">Service Bus GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="cef99-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="cef99-120">-Name</span><span class="sxs-lookup"><span data-stu-id="cef99-120">-Name</span></span>
<span data-ttu-id="cef99-121">Имя псевдонима (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="cef99-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="cef99-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cef99-122">-Namespace</span></span>
<span data-ttu-id="cef99-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="cef99-123">Namespace Name</span></span>

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

### <span data-ttu-id="cef99-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cef99-124">-PassThru</span></span>
<span data-ttu-id="cef99-125">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="cef99-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cef99-126">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cef99-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cef99-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cef99-127">-ResourceGroupName</span></span>
<span data-ttu-id="cef99-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cef99-128">Resource Group Name</span></span>

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

### <span data-ttu-id="cef99-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cef99-129">-ResourceId</span></span>
<span data-ttu-id="cef99-130">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="cef99-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="cef99-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cef99-131">-Confirm</span></span>
<span data-ttu-id="cef99-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cef99-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cef99-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cef99-133">-WhatIf</span></span>
<span data-ttu-id="cef99-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cef99-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cef99-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cef99-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cef99-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef99-136">CommonParameters</span></span>
<span data-ttu-id="cef99-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cef99-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef99-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cef99-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef99-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cef99-139">INPUTS</span></span>

### <span data-ttu-id="cef99-140">System.String</span><span class="sxs-lookup"><span data-stu-id="cef99-140">System.String</span></span>

### <span data-ttu-id="cef99-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="cef99-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="cef99-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cef99-142">OUTPUTS</span></span>

### <span data-ttu-id="cef99-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cef99-143">System.Boolean</span></span>

## <span data-ttu-id="cef99-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cef99-144">NOTES</span></span>

## <span data-ttu-id="cef99-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cef99-145">RELATED LINKS</span></span>
