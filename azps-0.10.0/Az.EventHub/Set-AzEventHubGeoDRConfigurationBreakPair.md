---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: 76bb062105567303baac72f0b27f14f36bdb120d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910356"
---
# <span data-ttu-id="01aec-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="01aec-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="01aec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01aec-102">SYNOPSIS</span></span>
<span data-ttu-id="01aec-103">Эта операция отключает восстановление после аварии и останавливает репликацию изменений из основного в дополнительные пространства имен.</span><span class="sxs-lookup"><span data-stu-id="01aec-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="01aec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01aec-104">SYNTAX</span></span>

### <span data-ttu-id="01aec-105">GeoDRParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="01aec-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01aec-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="01aec-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01aec-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01aec-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01aec-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01aec-108">DESCRIPTION</span></span>
<span data-ttu-id="01aec-109">Командлет **Set-AzEventHubGeoDRConfigurationBreakPair** отключает аварийное восстановление и останавливает репликацию изменений из основного в дополнительные пространства имен.</span><span class="sxs-lookup"><span data-stu-id="01aec-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="01aec-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01aec-110">EXAMPLES</span></span>

### <span data-ttu-id="01aec-111">Образом</span><span class="sxs-lookup"><span data-stu-id="01aec-111">Example</span></span>
```
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="01aec-112">Эта операция отключает восстановление после аварии и останавливает репликацию изменений из основного в дополнительные пространства имен.</span><span class="sxs-lookup"><span data-stu-id="01aec-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="01aec-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01aec-113">PARAMETERS</span></span>

### <span data-ttu-id="01aec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01aec-114">-DefaultProfile</span></span>
<span data-ttu-id="01aec-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01aec-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01aec-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01aec-116">-InputObject</span></span>
<span data-ttu-id="01aec-117">Объект конфигурации GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="01aec-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="01aec-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="01aec-118">-Name</span></span>
<span data-ttu-id="01aec-119">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="01aec-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="01aec-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="01aec-120">-Namespace</span></span>
<span data-ttu-id="01aec-121">Имя пространства имен — основное пространство имен</span><span class="sxs-lookup"><span data-stu-id="01aec-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="01aec-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01aec-122">-PassThru</span></span>
<span data-ttu-id="01aec-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="01aec-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="01aec-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="01aec-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="01aec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01aec-125">-ResourceGroupName</span></span>
<span data-ttu-id="01aec-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="01aec-126">Resource Group Name</span></span>

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

### <span data-ttu-id="01aec-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01aec-127">-ResourceId</span></span>
<span data-ttu-id="01aec-128">Идентификатор ресурса GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="01aec-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="01aec-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01aec-129">-Confirm</span></span>
<span data-ttu-id="01aec-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="01aec-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01aec-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01aec-131">-WhatIf</span></span>
<span data-ttu-id="01aec-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="01aec-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01aec-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="01aec-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01aec-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01aec-134">CommonParameters</span></span>
<span data-ttu-id="01aec-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01aec-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01aec-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01aec-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01aec-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01aec-137">INPUTS</span></span>

### <span data-ttu-id="01aec-138">System. String</span><span class="sxs-lookup"><span data-stu-id="01aec-138">System.String</span></span>

### <span data-ttu-id="01aec-139">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="01aec-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="01aec-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01aec-140">OUTPUTS</span></span>

### <span data-ttu-id="01aec-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="01aec-141">System.Boolean</span></span>

## <span data-ttu-id="01aec-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="01aec-142">NOTES</span></span>

## <span data-ttu-id="01aec-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01aec-143">RELATED LINKS</span></span>
