---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 4ee96fbe20fca3f0af1f0bb9604f178b912d0ea2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078283"
---
# <span data-ttu-id="4a772-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="4a772-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="4a772-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4a772-102">SYNOPSIS</span></span>
<span data-ttu-id="4a772-103">Вызывает отработку отказа географического восстановления и повторно конфигурирует псевдоним, чтобы он указывал на дополнительное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="4a772-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="4a772-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4a772-104">SYNTAX</span></span>

### <span data-ttu-id="4a772-105">GeoDRParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a772-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a772-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4a772-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a772-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a772-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a772-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a772-108">DESCRIPTION</span></span>
<span data-ttu-id="4a772-109">Командлет **Set-AzEventHubGeoDRConfigurationFailOver** вызывает отработку отказа в географическом процессе и повторно конфигурирует его, чтобы он указывал на дополнительное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="4a772-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="4a772-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4a772-110">EXAMPLES</span></span>

### <span data-ttu-id="4a772-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4a772-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="4a772-112">Вызывает отработку отказа для псевдонима "SampleDRConfigName", перестраивает и указывает на дополнительное пространство имен "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="4a772-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="4a772-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4a772-113">PARAMETERS</span></span>

### <span data-ttu-id="4a772-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a772-114">-DefaultProfile</span></span>
<span data-ttu-id="4a772-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a772-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a772-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a772-116">-InputObject</span></span>
<span data-ttu-id="4a772-117">Объект конфигурации GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="4a772-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="4a772-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4a772-118">-Name</span></span>
<span data-ttu-id="4a772-119">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="4a772-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="4a772-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4a772-120">-Namespace</span></span>
<span data-ttu-id="4a772-121">Имя пространства имен — дополнительное пространство имен</span><span class="sxs-lookup"><span data-stu-id="4a772-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="4a772-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a772-122">-PassThru</span></span>
<span data-ttu-id="4a772-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="4a772-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4a772-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4a772-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4a772-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a772-125">-ResourceGroupName</span></span>
<span data-ttu-id="4a772-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4a772-126">Resource Group Name</span></span>

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

### <span data-ttu-id="4a772-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a772-127">-ResourceId</span></span>
<span data-ttu-id="4a772-128">Идентификатор ресурса GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a772-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="4a772-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a772-129">-Confirm</span></span>
<span data-ttu-id="4a772-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4a772-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a772-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a772-131">-WhatIf</span></span>
<span data-ttu-id="4a772-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4a772-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a772-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4a772-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a772-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a772-134">CommonParameters</span></span>
<span data-ttu-id="4a772-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4a772-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a772-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a772-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a772-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4a772-137">INPUTS</span></span>

### <span data-ttu-id="4a772-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4a772-138">System.String</span></span>

### <span data-ttu-id="4a772-139">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="4a772-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="4a772-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a772-140">OUTPUTS</span></span>

### <span data-ttu-id="4a772-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4a772-141">System.Boolean</span></span>

## <span data-ttu-id="4a772-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="4a772-142">NOTES</span></span>

## <span data-ttu-id="4a772-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a772-143">RELATED LINKS</span></span>
