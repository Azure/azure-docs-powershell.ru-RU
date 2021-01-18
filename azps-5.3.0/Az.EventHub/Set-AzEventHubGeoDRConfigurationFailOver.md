---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 4ee96fbe20fca3f0af1f0bb9604f178b912d0ea2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504896"
---
# <span data-ttu-id="1460f-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="1460f-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="1460f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1460f-102">SYNOPSIS</span></span>
<span data-ttu-id="1460f-103">Вызывает отбой GEO DR и повторно настроит псевдоним, чтобы он указать на дополнительное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="1460f-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="1460f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1460f-104">SYNTAX</span></span>

### <span data-ttu-id="1460f-105">GeoDRParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1460f-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1460f-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1460f-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1460f-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1460f-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1460f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1460f-108">DESCRIPTION</span></span>
<span data-ttu-id="1460f-109">Cmdlet **Set-AzEventHubGeoDRConfigurationFailOver** вызывает отбой GEO DR и повторно настроен псевдоним, чтобы он ссылался на дополнительное пространство имен</span><span class="sxs-lookup"><span data-stu-id="1460f-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="1460f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1460f-110">EXAMPLES</span></span>

### <span data-ttu-id="1460f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1460f-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="1460f-112">Вызывает отрезок failover над псевдонимом SampleDRConfigName, перенаправляет его на дополнительное пространство имен "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="1460f-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="1460f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1460f-113">PARAMETERS</span></span>

### <span data-ttu-id="1460f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1460f-114">-DefaultProfile</span></span>
<span data-ttu-id="1460f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1460f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1460f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1460f-116">-InputObject</span></span>
<span data-ttu-id="1460f-117">Объект конфигурации Eventhub GeoDR</span><span class="sxs-lookup"><span data-stu-id="1460f-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="1460f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1460f-118">-Name</span></span>
<span data-ttu-id="1460f-119">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="1460f-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="1460f-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1460f-120">-Namespace</span></span>
<span data-ttu-id="1460f-121">Namespace Name ( Дополнительное пространство имен)</span><span class="sxs-lookup"><span data-stu-id="1460f-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="1460f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1460f-122">-PassThru</span></span>
<span data-ttu-id="1460f-123">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="1460f-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1460f-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1460f-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1460f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1460f-125">-ResourceGroupName</span></span>
<span data-ttu-id="1460f-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1460f-126">Resource Group Name</span></span>

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

### <span data-ttu-id="1460f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1460f-127">-ResourceId</span></span>
<span data-ttu-id="1460f-128">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="1460f-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="1460f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1460f-129">-Confirm</span></span>
<span data-ttu-id="1460f-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1460f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1460f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1460f-131">-WhatIf</span></span>
<span data-ttu-id="1460f-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1460f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1460f-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1460f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1460f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1460f-134">CommonParameters</span></span>
<span data-ttu-id="1460f-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1460f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1460f-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1460f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1460f-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1460f-137">INPUTS</span></span>

### <span data-ttu-id="1460f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1460f-138">System.String</span></span>

### <span data-ttu-id="1460f-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="1460f-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="1460f-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1460f-140">OUTPUTS</span></span>

### <span data-ttu-id="1460f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1460f-141">System.Boolean</span></span>

## <span data-ttu-id="1460f-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1460f-142">NOTES</span></span>

## <span data-ttu-id="1460f-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1460f-143">RELATED LINKS</span></span>
