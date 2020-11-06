---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 581f3c24c8c195b1cafc4962d1c6319418cc07f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562620"
---
# <span data-ttu-id="02eb3-101">Remove-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="02eb3-101">Remove-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="02eb3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="02eb3-103">Удаление псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="02eb3-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02eb3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02eb3-104">SYNTAX</span></span>

### <span data-ttu-id="02eb3-105">GeoDRPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="02eb3-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02eb3-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="02eb3-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02eb3-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02eb3-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02eb3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02eb3-108">DESCRIPTION</span></span>
<span data-ttu-id="02eb3-109">Командлет **Remove-AzureRmServiceBusGeoDRConfiguration** удаляет псевдоним (конфигурацию аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="02eb3-109">The **Remove-AzureRmServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="02eb3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02eb3-110">EXAMPLES</span></span>

### <span data-ttu-id="02eb3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="02eb3-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="02eb3-112">Удаление псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="02eb3-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="02eb3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02eb3-113">PARAMETERS</span></span>

### <span data-ttu-id="02eb3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02eb3-114">-AsJob</span></span>
<span data-ttu-id="02eb3-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="02eb3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02eb3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02eb3-116">-DefaultProfile</span></span>
<span data-ttu-id="02eb3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02eb3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02eb3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02eb3-118">-InputObject</span></span>
<span data-ttu-id="02eb3-119">Объект конфигурации служебной шины GeoDR</span><span class="sxs-lookup"><span data-stu-id="02eb3-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="02eb3-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="02eb3-120">-Name</span></span>
<span data-ttu-id="02eb3-121">Имя псевдонима (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="02eb3-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="02eb3-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="02eb3-122">-Namespace</span></span>
<span data-ttu-id="02eb3-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="02eb3-123">Namespace Name</span></span>

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

### <span data-ttu-id="02eb3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02eb3-124">-PassThru</span></span>
<span data-ttu-id="02eb3-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="02eb3-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="02eb3-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="02eb3-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="02eb3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02eb3-127">-ResourceGroupName</span></span>
<span data-ttu-id="02eb3-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="02eb3-128">Resource Group Name</span></span>

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

### <span data-ttu-id="02eb3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02eb3-129">-ResourceId</span></span>
<span data-ttu-id="02eb3-130">Идентификатор ресурса GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="02eb3-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="02eb3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02eb3-131">-Confirm</span></span>
<span data-ttu-id="02eb3-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="02eb3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02eb3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02eb3-133">-WhatIf</span></span>
<span data-ttu-id="02eb3-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="02eb3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02eb3-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="02eb3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02eb3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02eb3-136">CommonParameters</span></span>
<span data-ttu-id="02eb3-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02eb3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02eb3-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02eb3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02eb3-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02eb3-139">INPUTS</span></span>

### <span data-ttu-id="02eb3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="02eb3-140">System.String</span></span>

### <span data-ttu-id="02eb3-141">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="02eb3-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="02eb3-142">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="02eb3-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="02eb3-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02eb3-143">OUTPUTS</span></span>

### <span data-ttu-id="02eb3-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="02eb3-144">System.Boolean</span></span>

## <span data-ttu-id="02eb3-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="02eb3-145">NOTES</span></span>

## <span data-ttu-id="02eb3-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02eb3-146">RELATED LINKS</span></span>
