---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 929ebdfb9cc38d5233027da75752f4c82c484536
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564935"
---
# <span data-ttu-id="09d5c-101">Remove-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="09d5c-101">Remove-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="09d5c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09d5c-102">SYNOPSIS</span></span>
<span data-ttu-id="09d5c-103">Удаление псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="09d5c-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09d5c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09d5c-104">SYNTAX</span></span>

### <span data-ttu-id="09d5c-105">GeoDRParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="09d5c-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09d5c-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="09d5c-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09d5c-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09d5c-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09d5c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09d5c-108">DESCRIPTION</span></span>
<span data-ttu-id="09d5c-109">Командлет **Remove-AzureRmEventHubGeoDRConfiguration** удаляет псевдоним (конфигурацию аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="09d5c-109">The **Remove-AzureRmEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="09d5c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09d5c-110">EXAMPLES</span></span>

### <span data-ttu-id="09d5c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="09d5c-111">Example 1</span></span>
```
PS C:\>Remove-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="09d5c-112">Удаление псевдонима (конфигурация аварийного восстановления)</span><span class="sxs-lookup"><span data-stu-id="09d5c-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="09d5c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09d5c-113">PARAMETERS</span></span>

### <span data-ttu-id="09d5c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09d5c-114">-AsJob</span></span>
<span data-ttu-id="09d5c-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="09d5c-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d5c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09d5c-116">-DefaultProfile</span></span>
<span data-ttu-id="09d5c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="09d5c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d5c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09d5c-118">-InputObject</span></span>
<span data-ttu-id="09d5c-119">Объект конфигурации GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="09d5c-119">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09d5c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="09d5c-120">-Name</span></span>
<span data-ttu-id="09d5c-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="09d5c-121">Alias (GeoDR)</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09d5c-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="09d5c-122">-Namespace</span></span>
<span data-ttu-id="09d5c-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="09d5c-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09d5c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09d5c-124">-PassThru</span></span>
<span data-ttu-id="09d5c-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="09d5c-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="09d5c-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="09d5c-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d5c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09d5c-127">-ResourceGroupName</span></span>
<span data-ttu-id="09d5c-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="09d5c-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09d5c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09d5c-129">-ResourceId</span></span>
<span data-ttu-id="09d5c-130">Идентификатор ресурса GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="09d5c-130">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09d5c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09d5c-131">-Confirm</span></span>
<span data-ttu-id="09d5c-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="09d5c-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d5c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09d5c-133">-WhatIf</span></span>
<span data-ttu-id="09d5c-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="09d5c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09d5c-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="09d5c-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d5c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09d5c-136">CommonParameters</span></span>
<span data-ttu-id="09d5c-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09d5c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="09d5c-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09d5c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09d5c-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09d5c-139">INPUTS</span></span>

### <span data-ttu-id="09d5c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="09d5c-140">System.String</span></span>
<span data-ttu-id="09d5c-141">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="09d5c-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="09d5c-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09d5c-142">OUTPUTS</span></span>

### <span data-ttu-id="09d5c-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="09d5c-143">System.Boolean</span></span>


## <span data-ttu-id="09d5c-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="09d5c-144">NOTES</span></span>

## <span data-ttu-id="09d5c-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09d5c-145">RELATED LINKS</span></span>
