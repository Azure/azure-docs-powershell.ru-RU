---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: e6dea50e3cb9933d9c6a8aa141f2df43be0b1a18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732734"
---
# <span data-ttu-id="a2e64-101">Set-AzureRmEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="a2e64-101">Set-AzureRmEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="a2e64-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2e64-102">SYNOPSIS</span></span>
<span data-ttu-id="a2e64-103">Эта операция отключает восстановление после аварии и останавливает репликацию изменений из основного в дополнительные пространства имен.</span><span class="sxs-lookup"><span data-stu-id="a2e64-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2e64-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2e64-104">SYNTAX</span></span>

### <span data-ttu-id="a2e64-105">GeoDRParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2e64-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2e64-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a2e64-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2e64-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2e64-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2e64-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2e64-108">DESCRIPTION</span></span>
<span data-ttu-id="a2e64-109">Командлет **Set-AzureRmEventHubGeoDRConfigurationBreakPair** отключает аварийное восстановление и останавливает репликацию изменений из основного в дополнительные пространства имен.</span><span class="sxs-lookup"><span data-stu-id="a2e64-109">The **Set-AzureRmEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="a2e64-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2e64-110">EXAMPLES</span></span>

### <span data-ttu-id="a2e64-111">Образом</span><span class="sxs-lookup"><span data-stu-id="a2e64-111">Example</span></span>
```
PS C:\> Set-AzureRmEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="a2e64-112">Эта операция отключает восстановление после аварии и останавливает репликацию изменений из основного в дополнительные пространства имен.</span><span class="sxs-lookup"><span data-stu-id="a2e64-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="a2e64-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2e64-113">PARAMETERS</span></span>

### <span data-ttu-id="a2e64-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2e64-114">-DefaultProfile</span></span>
<span data-ttu-id="a2e64-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2e64-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2e64-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2e64-116">-InputObject</span></span>
<span data-ttu-id="a2e64-117">Объект конфигурации GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="a2e64-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="a2e64-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a2e64-118">-Name</span></span>
<span data-ttu-id="a2e64-119">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="a2e64-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="a2e64-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a2e64-120">-Namespace</span></span>
<span data-ttu-id="a2e64-121">Имя пространства имен — основное пространство имен</span><span class="sxs-lookup"><span data-stu-id="a2e64-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="a2e64-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2e64-122">-PassThru</span></span>
<span data-ttu-id="a2e64-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="a2e64-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a2e64-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a2e64-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a2e64-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2e64-125">-ResourceGroupName</span></span>
<span data-ttu-id="a2e64-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a2e64-126">Resource Group Name</span></span>

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

### <span data-ttu-id="a2e64-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2e64-127">-ResourceId</span></span>
<span data-ttu-id="a2e64-128">Идентификатор ресурса GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="a2e64-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="a2e64-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2e64-129">-Confirm</span></span>
<span data-ttu-id="a2e64-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a2e64-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2e64-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2e64-131">-WhatIf</span></span>
<span data-ttu-id="a2e64-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a2e64-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2e64-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a2e64-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2e64-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2e64-134">CommonParameters</span></span>
<span data-ttu-id="a2e64-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2e64-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a2e64-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2e64-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2e64-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2e64-137">INPUTS</span></span>

### <span data-ttu-id="a2e64-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a2e64-138">System.String</span></span>
<span data-ttu-id="a2e64-139">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="a2e64-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="a2e64-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2e64-140">OUTPUTS</span></span>

### <span data-ttu-id="a2e64-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a2e64-141">System.Boolean</span></span>


## <span data-ttu-id="a2e64-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2e64-142">NOTES</span></span>

## <span data-ttu-id="a2e64-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2e64-143">RELATED LINKS</span></span>
