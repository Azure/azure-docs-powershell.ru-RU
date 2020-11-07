---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 85f6373cad3c6c42bbefa0aba9aac14d3699b6a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732614"
---
# <span data-ttu-id="c2ef2-101">Remove-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2ef2-101">Remove-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="c2ef2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2ef2-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ef2-103">Удаление псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="c2ef2-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2ef2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2ef2-104">SYNTAX</span></span>

### <span data-ttu-id="c2ef2-105">GeoDRParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2ef2-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2ef2-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c2ef2-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2ef2-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2ef2-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2ef2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2ef2-108">DESCRIPTION</span></span>
<span data-ttu-id="c2ef2-109">Командлет **Remove-AzureRmEventHubGeoDRConfiguration** удаляет псевдоним (конфигурацию аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="c2ef2-109">The **Remove-AzureRmEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="c2ef2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2ef2-110">EXAMPLES</span></span>

### <span data-ttu-id="c2ef2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c2ef2-111">Example 1</span></span>
```
PS C:\>Remove-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="c2ef2-112">Удаление псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="c2ef2-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="c2ef2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2ef2-113">PARAMETERS</span></span>

### <span data-ttu-id="c2ef2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2ef2-114">-AsJob</span></span>
<span data-ttu-id="c2ef2-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c2ef2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2ef2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ef2-116">-DefaultProfile</span></span>
<span data-ttu-id="c2ef2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2ef2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2ef2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2ef2-118">-InputObject</span></span>
<span data-ttu-id="c2ef2-119">Объект конфигурации GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="c2ef2-119">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2ef2-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c2ef2-120">-Name</span></span>
<span data-ttu-id="c2ef2-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="c2ef2-121">Alias (GeoDR)</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2ef2-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c2ef2-122">-Namespace</span></span>
<span data-ttu-id="c2ef2-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="c2ef2-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2ef2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2ef2-124">-PassThru</span></span>
<span data-ttu-id="c2ef2-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="c2ef2-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c2ef2-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c2ef2-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c2ef2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2ef2-127">-ResourceGroupName</span></span>
<span data-ttu-id="c2ef2-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c2ef2-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2ef2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2ef2-129">-ResourceId</span></span>
<span data-ttu-id="c2ef2-130">Идентификатор ресурса GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2ef2-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="c2ef2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2ef2-131">-Confirm</span></span>
<span data-ttu-id="c2ef2-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c2ef2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2ef2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2ef2-133">-WhatIf</span></span>
<span data-ttu-id="c2ef2-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c2ef2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2ef2-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c2ef2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2ef2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ef2-136">CommonParameters</span></span>
<span data-ttu-id="c2ef2-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2ef2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ef2-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2ef2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ef2-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2ef2-139">INPUTS</span></span>

### <span data-ttu-id="c2ef2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c2ef2-140">System.String</span></span>

### <span data-ttu-id="c2ef2-141">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c2ef2-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>
<span data-ttu-id="c2ef2-142">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c2ef2-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c2ef2-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2ef2-143">OUTPUTS</span></span>

### <span data-ttu-id="c2ef2-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2ef2-144">System.Boolean</span></span>

## <span data-ttu-id="c2ef2-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2ef2-145">NOTES</span></span>

## <span data-ttu-id="c2ef2-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2ef2-146">RELATED LINKS</span></span>
