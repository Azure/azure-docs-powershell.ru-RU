---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: e927c01cf623a501f1583db1463dfa3abaf719be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730811"
---
# <span data-ttu-id="49247-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="49247-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="49247-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49247-102">SYNOPSIS</span></span>
<span data-ttu-id="49247-103">Вызывает отработку отказа географического восстановления и повторно конфигурирует псевдоним, чтобы он указывал на дополнительное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="49247-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="49247-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49247-104">SYNTAX</span></span>

### <span data-ttu-id="49247-105">GeoDRParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49247-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49247-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="49247-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49247-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49247-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49247-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49247-108">DESCRIPTION</span></span>
<span data-ttu-id="49247-109">Командлет **Set-AzEventHubGeoDRConfigurationFailOver** envokes отработки отказа в географическом процессе и повторно настройте его, чтобы он указывал на дополнительное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="49247-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="49247-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49247-110">EXAMPLES</span></span>

### <span data-ttu-id="49247-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="49247-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="49247-112">Вызывает отработку отказа для псевдонима "SampleDRCongifName", перестраивает и указывает на дополнительное пространство имен "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="49247-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="49247-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49247-113">PARAMETERS</span></span>

### <span data-ttu-id="49247-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49247-114">-DefaultProfile</span></span>
<span data-ttu-id="49247-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49247-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49247-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49247-116">-InputObject</span></span>
<span data-ttu-id="49247-117">Объект конфигурации GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="49247-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="49247-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="49247-118">-Name</span></span>
<span data-ttu-id="49247-119">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="49247-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="49247-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="49247-120">-Namespace</span></span>
<span data-ttu-id="49247-121">Имя пространства имен — дополнительное пространство имен</span><span class="sxs-lookup"><span data-stu-id="49247-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="49247-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49247-122">-PassThru</span></span>
<span data-ttu-id="49247-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="49247-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="49247-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="49247-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="49247-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49247-125">-ResourceGroupName</span></span>
<span data-ttu-id="49247-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="49247-126">Resource Group Name</span></span>

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

### <span data-ttu-id="49247-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49247-127">-ResourceId</span></span>
<span data-ttu-id="49247-128">Идентификатор ресурса GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="49247-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="49247-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49247-129">-Confirm</span></span>
<span data-ttu-id="49247-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="49247-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49247-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49247-131">-WhatIf</span></span>
<span data-ttu-id="49247-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="49247-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49247-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="49247-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49247-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49247-134">CommonParameters</span></span>
<span data-ttu-id="49247-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49247-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49247-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49247-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49247-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49247-137">INPUTS</span></span>

### <span data-ttu-id="49247-138">System. String</span><span class="sxs-lookup"><span data-stu-id="49247-138">System.String</span></span>

### <span data-ttu-id="49247-139">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="49247-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="49247-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49247-140">OUTPUTS</span></span>

### <span data-ttu-id="49247-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="49247-141">System.Boolean</span></span>

## <span data-ttu-id="49247-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="49247-142">NOTES</span></span>

## <span data-ttu-id="49247-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49247-143">RELATED LINKS</span></span>
