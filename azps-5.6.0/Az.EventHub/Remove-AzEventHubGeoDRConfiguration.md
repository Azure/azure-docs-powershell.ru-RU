---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 2de5501c63ebbdd8842acb6cbfa40ec51893cbf4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992701"
---
# <span data-ttu-id="14da4-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="14da4-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="14da4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14da4-102">SYNOPSIS</span></span>
<span data-ttu-id="14da4-103">Удаляет псевдоним (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="14da4-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="14da4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="14da4-104">SYNTAX</span></span>

### <span data-ttu-id="14da4-105">GeoDRParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="14da4-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14da4-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="14da4-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14da4-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14da4-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14da4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14da4-108">DESCRIPTION</span></span>
<span data-ttu-id="14da4-109">При **настройке Remove-AzEventHubGeoDRConfiguration** удаляется псевдоним (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="14da4-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="14da4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="14da4-110">EXAMPLES</span></span>

### <span data-ttu-id="14da4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="14da4-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="14da4-112">Удаление псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="14da4-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="14da4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14da4-113">PARAMETERS</span></span>

### <span data-ttu-id="14da4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14da4-114">-AsJob</span></span>
<span data-ttu-id="14da4-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="14da4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14da4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14da4-116">-DefaultProfile</span></span>
<span data-ttu-id="14da4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14da4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14da4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14da4-118">-InputObject</span></span>
<span data-ttu-id="14da4-119">Объект конфигурации Eventhub GeoDR</span><span class="sxs-lookup"><span data-stu-id="14da4-119">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="14da4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="14da4-120">-Name</span></span>
<span data-ttu-id="14da4-121">Псевдоним (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="14da4-121">Alias (GeoDR)</span></span>

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

### <span data-ttu-id="14da4-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="14da4-122">-Namespace</span></span>
<span data-ttu-id="14da4-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="14da4-123">Namespace Name</span></span>

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

### <span data-ttu-id="14da4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14da4-124">-PassThru</span></span>
<span data-ttu-id="14da4-125">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="14da4-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="14da4-126">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="14da4-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="14da4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14da4-127">-ResourceGroupName</span></span>
<span data-ttu-id="14da4-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="14da4-128">Resource Group Name</span></span>

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

### <span data-ttu-id="14da4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14da4-129">-ResourceId</span></span>
<span data-ttu-id="14da4-130">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="14da4-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="14da4-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14da4-131">-Confirm</span></span>
<span data-ttu-id="14da4-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14da4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14da4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14da4-133">-WhatIf</span></span>
<span data-ttu-id="14da4-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14da4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14da4-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="14da4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14da4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14da4-136">CommonParameters</span></span>
<span data-ttu-id="14da4-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14da4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14da4-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14da4-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14da4-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14da4-139">INPUTS</span></span>

### <span data-ttu-id="14da4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="14da4-140">System.String</span></span>

### <span data-ttu-id="14da4-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="14da4-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="14da4-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="14da4-142">OUTPUTS</span></span>

### <span data-ttu-id="14da4-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="14da4-143">System.Boolean</span></span>

## <span data-ttu-id="14da4-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="14da4-144">NOTES</span></span>

## <span data-ttu-id="14da4-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14da4-145">RELATED LINKS</span></span>
