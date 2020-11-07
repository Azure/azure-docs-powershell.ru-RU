---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: b7b1cc38402e69b5783f76ec35445aae7b6944dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720935"
---
# <span data-ttu-id="0957c-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="0957c-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="0957c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0957c-102">SYNOPSIS</span></span>
<span data-ttu-id="0957c-103">Удаление псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="0957c-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="0957c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0957c-104">SYNTAX</span></span>

### <span data-ttu-id="0957c-105">GeoDRParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0957c-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0957c-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0957c-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0957c-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0957c-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0957c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0957c-108">DESCRIPTION</span></span>
<span data-ttu-id="0957c-109">Командлет **Remove-AzEventHubGeoDRConfiguration** удаляет псевдоним (конфигурацию аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="0957c-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="0957c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0957c-110">EXAMPLES</span></span>

### <span data-ttu-id="0957c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0957c-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="0957c-112">Удаление псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="0957c-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="0957c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0957c-113">PARAMETERS</span></span>

### <span data-ttu-id="0957c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0957c-114">-AsJob</span></span>
<span data-ttu-id="0957c-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0957c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0957c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0957c-116">-DefaultProfile</span></span>
<span data-ttu-id="0957c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0957c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0957c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0957c-118">-InputObject</span></span>
<span data-ttu-id="0957c-119">Объект конфигурации GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="0957c-119">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="0957c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0957c-120">-Name</span></span>
<span data-ttu-id="0957c-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="0957c-121">Alias (GeoDR)</span></span>

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

### <span data-ttu-id="0957c-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0957c-122">-Namespace</span></span>
<span data-ttu-id="0957c-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="0957c-123">Namespace Name</span></span>

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

### <span data-ttu-id="0957c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0957c-124">-PassThru</span></span>
<span data-ttu-id="0957c-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="0957c-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0957c-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="0957c-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0957c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0957c-127">-ResourceGroupName</span></span>
<span data-ttu-id="0957c-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0957c-128">Resource Group Name</span></span>

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

### <span data-ttu-id="0957c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0957c-129">-ResourceId</span></span>
<span data-ttu-id="0957c-130">Идентификатор ресурса GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="0957c-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="0957c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0957c-131">-Confirm</span></span>
<span data-ttu-id="0957c-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0957c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0957c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0957c-133">-WhatIf</span></span>
<span data-ttu-id="0957c-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0957c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0957c-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0957c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0957c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0957c-136">CommonParameters</span></span>
<span data-ttu-id="0957c-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0957c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0957c-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0957c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0957c-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0957c-139">INPUTS</span></span>

### <span data-ttu-id="0957c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0957c-140">System.String</span></span>

### <span data-ttu-id="0957c-141">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="0957c-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="0957c-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0957c-142">OUTPUTS</span></span>

### <span data-ttu-id="0957c-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0957c-143">System.Boolean</span></span>

## <span data-ttu-id="0957c-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="0957c-144">NOTES</span></span>

## <span data-ttu-id="0957c-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0957c-145">RELATED LINKS</span></span>
