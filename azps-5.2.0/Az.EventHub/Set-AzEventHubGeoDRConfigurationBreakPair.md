---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f343b92452a34a746d9ff09d5a519519aeaa7a6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392844"
---
# <span data-ttu-id="fd1b9-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="fd1b9-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="fd1b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd1b9-102">SYNOPSIS</span></span>
<span data-ttu-id="fd1b9-103">Эта операция отключает аварийное восстановление и останавливает репликацию изменений из основного в дополнительное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="fd1b9-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="fd1b9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fd1b9-104">SYNTAX</span></span>

### <span data-ttu-id="fd1b9-105">GeoDRParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fd1b9-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd1b9-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fd1b9-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd1b9-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd1b9-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd1b9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd1b9-108">DESCRIPTION</span></span>
<span data-ttu-id="fd1b9-109">Cmdlet **Set-AzEventHubGeoDRConfigurationBreakPair** отключает аварийное восстановление и останавливает репликацию изменений из основного в дополнительное пространство имен</span><span class="sxs-lookup"><span data-stu-id="fd1b9-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="fd1b9-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fd1b9-110">EXAMPLES</span></span>

### <span data-ttu-id="fd1b9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fd1b9-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="fd1b9-112">Эта операция отключает аварийное восстановление и останавливает репликацию изменений из основного в дополнительное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="fd1b9-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="fd1b9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd1b9-113">PARAMETERS</span></span>

### <span data-ttu-id="fd1b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd1b9-114">-DefaultProfile</span></span>
<span data-ttu-id="fd1b9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd1b9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd1b9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd1b9-116">-InputObject</span></span>
<span data-ttu-id="fd1b9-117">Объект конфигурации Eventhub GeoDR</span><span class="sxs-lookup"><span data-stu-id="fd1b9-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="fd1b9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fd1b9-118">-Name</span></span>
<span data-ttu-id="fd1b9-119">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="fd1b9-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="fd1b9-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fd1b9-120">-Namespace</span></span>
<span data-ttu-id="fd1b9-121">Namespace Name — Primary Namespace</span><span class="sxs-lookup"><span data-stu-id="fd1b9-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="fd1b9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd1b9-122">-PassThru</span></span>
<span data-ttu-id="fd1b9-123">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="fd1b9-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fd1b9-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="fd1b9-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fd1b9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd1b9-125">-ResourceGroupName</span></span>
<span data-ttu-id="fd1b9-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="fd1b9-126">Resource Group Name</span></span>

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

### <span data-ttu-id="fd1b9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd1b9-127">-ResourceId</span></span>
<span data-ttu-id="fd1b9-128">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="fd1b9-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="fd1b9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd1b9-129">-Confirm</span></span>
<span data-ttu-id="fd1b9-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd1b9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd1b9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd1b9-131">-WhatIf</span></span>
<span data-ttu-id="fd1b9-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd1b9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd1b9-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fd1b9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd1b9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd1b9-134">CommonParameters</span></span>
<span data-ttu-id="fd1b9-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd1b9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd1b9-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd1b9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd1b9-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd1b9-137">INPUTS</span></span>

### <span data-ttu-id="fd1b9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fd1b9-138">System.String</span></span>

### <span data-ttu-id="fd1b9-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="fd1b9-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="fd1b9-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fd1b9-140">OUTPUTS</span></span>

### <span data-ttu-id="fd1b9-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fd1b9-141">System.Boolean</span></span>

## <span data-ttu-id="fd1b9-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fd1b9-142">NOTES</span></span>

## <span data-ttu-id="fd1b9-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd1b9-143">RELATED LINKS</span></span>
