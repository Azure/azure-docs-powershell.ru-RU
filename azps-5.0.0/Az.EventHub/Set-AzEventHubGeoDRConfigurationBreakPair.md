---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f343b92452a34a746d9ff09d5a519519aeaa7a6c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247437"
---
# <span data-ttu-id="c1e62-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="c1e62-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="c1e62-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1e62-102">SYNOPSIS</span></span>
<span data-ttu-id="c1e62-103">Эта операция отключает восстановление после аварии и останавливает репликацию изменений из основного в дополнительные пространства имен.</span><span class="sxs-lookup"><span data-stu-id="c1e62-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="c1e62-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1e62-104">SYNTAX</span></span>

### <span data-ttu-id="c1e62-105">GeoDRParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c1e62-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1e62-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c1e62-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1e62-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1e62-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1e62-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1e62-108">DESCRIPTION</span></span>
<span data-ttu-id="c1e62-109">Командлет **Set-AzEventHubGeoDRConfigurationBreakPair** отключает аварийное восстановление и останавливает репликацию изменений из основного в дополнительные пространства имен.</span><span class="sxs-lookup"><span data-stu-id="c1e62-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="c1e62-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1e62-110">EXAMPLES</span></span>

### <span data-ttu-id="c1e62-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c1e62-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="c1e62-112">Эта операция отключает восстановление после аварии и останавливает репликацию изменений из основного в дополнительные пространства имен.</span><span class="sxs-lookup"><span data-stu-id="c1e62-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="c1e62-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1e62-113">PARAMETERS</span></span>

### <span data-ttu-id="c1e62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1e62-114">-DefaultProfile</span></span>
<span data-ttu-id="c1e62-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1e62-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1e62-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1e62-116">-InputObject</span></span>
<span data-ttu-id="c1e62-117">Объект конфигурации GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="c1e62-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="c1e62-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c1e62-118">-Name</span></span>
<span data-ttu-id="c1e62-119">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="c1e62-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="c1e62-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c1e62-120">-Namespace</span></span>
<span data-ttu-id="c1e62-121">Имя пространства имен — основное пространство имен</span><span class="sxs-lookup"><span data-stu-id="c1e62-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="c1e62-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1e62-122">-PassThru</span></span>
<span data-ttu-id="c1e62-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="c1e62-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c1e62-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c1e62-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c1e62-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1e62-125">-ResourceGroupName</span></span>
<span data-ttu-id="c1e62-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c1e62-126">Resource Group Name</span></span>

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

### <span data-ttu-id="c1e62-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1e62-127">-ResourceId</span></span>
<span data-ttu-id="c1e62-128">Идентификатор ресурса GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1e62-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="c1e62-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1e62-129">-Confirm</span></span>
<span data-ttu-id="c1e62-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c1e62-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1e62-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1e62-131">-WhatIf</span></span>
<span data-ttu-id="c1e62-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c1e62-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1e62-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c1e62-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1e62-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1e62-134">CommonParameters</span></span>
<span data-ttu-id="c1e62-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1e62-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1e62-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1e62-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1e62-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1e62-137">INPUTS</span></span>

### <span data-ttu-id="c1e62-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c1e62-138">System.String</span></span>

### <span data-ttu-id="c1e62-139">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c1e62-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="c1e62-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1e62-140">OUTPUTS</span></span>

### <span data-ttu-id="c1e62-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1e62-141">System.Boolean</span></span>

## <span data-ttu-id="c1e62-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1e62-142">NOTES</span></span>

## <span data-ttu-id="c1e62-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1e62-143">RELATED LINKS</span></span>
