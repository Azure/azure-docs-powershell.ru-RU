---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: a12f22260ce8ee5412cd17ddfa420a7d23f82008
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563999"
---
# <span data-ttu-id="fd086-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="fd086-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="fd086-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd086-102">SYNOPSIS</span></span>
<span data-ttu-id="fd086-103">Эта операция отключает восстановление после аварии и останавливает репликацию изменений из основного в дополнительные пространства имен.</span><span class="sxs-lookup"><span data-stu-id="fd086-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd086-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd086-104">SYNTAX</span></span>

### <span data-ttu-id="fd086-105">GeoDRPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fd086-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd086-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fd086-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd086-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd086-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd086-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd086-108">DESCRIPTION</span></span>
<span data-ttu-id="fd086-109">Командлет **Set-AzureRmServiceBusGeoDRConfigurationBreakPair** отключает аварийное восстановление и останавливает репликацию изменений из основного в дополнительные пространства имен.</span><span class="sxs-lookup"><span data-stu-id="fd086-109">The **Set-AzureRmServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="fd086-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd086-110">EXAMPLES</span></span>

### <span data-ttu-id="fd086-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fd086-111">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="fd086-112">Эта операция отключает восстановление после аварии и останавливает репликацию изменений из основного в дополнительные пространства имен.</span><span class="sxs-lookup"><span data-stu-id="fd086-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="fd086-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd086-113">PARAMETERS</span></span>

### <span data-ttu-id="fd086-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd086-114">-DefaultProfile</span></span>
<span data-ttu-id="fd086-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd086-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd086-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd086-116">-InputObject</span></span>
<span data-ttu-id="fd086-117">Объект конфигурации служебной шины GeoDR</span><span class="sxs-lookup"><span data-stu-id="fd086-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="fd086-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fd086-118">-Name</span></span>
<span data-ttu-id="fd086-119">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="fd086-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="fd086-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fd086-120">-Namespace</span></span>
<span data-ttu-id="fd086-121">Имя пространства имен — основное пространство имен</span><span class="sxs-lookup"><span data-stu-id="fd086-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="fd086-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd086-122">-PassThru</span></span>
<span data-ttu-id="fd086-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="fd086-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fd086-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="fd086-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fd086-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd086-125">-ResourceGroupName</span></span>
<span data-ttu-id="fd086-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="fd086-126">Resource Group Name</span></span>

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

### <span data-ttu-id="fd086-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd086-127">-ResourceId</span></span>
<span data-ttu-id="fd086-128">Идентификатор ресурса GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd086-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="fd086-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd086-129">-Confirm</span></span>
<span data-ttu-id="fd086-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fd086-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd086-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd086-131">-WhatIf</span></span>
<span data-ttu-id="fd086-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fd086-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd086-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fd086-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd086-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd086-134">CommonParameters</span></span>
<span data-ttu-id="fd086-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd086-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd086-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd086-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd086-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd086-137">INPUTS</span></span>

### <span data-ttu-id="fd086-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fd086-138">System.String</span></span>

### <span data-ttu-id="fd086-139">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="fd086-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="fd086-140">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fd086-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fd086-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd086-141">OUTPUTS</span></span>

### <span data-ttu-id="fd086-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd086-142">System.Boolean</span></span>

## <span data-ttu-id="fd086-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd086-143">NOTES</span></span>

## <span data-ttu-id="fd086-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd086-144">RELATED LINKS</span></span>
