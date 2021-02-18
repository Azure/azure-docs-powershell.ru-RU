---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/set-azadvisorConfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
ms.openlocfilehash: bfd1677fa46a749b73206b02bb6585c4a529637f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224481"
---
# <span data-ttu-id="90a09-101">Set-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="90a09-101">Set-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="90a09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90a09-102">SYNOPSIS</span></span>
<span data-ttu-id="90a09-103">Обновляет или создает конфигурацию помощника Azure.</span><span class="sxs-lookup"><span data-stu-id="90a09-103">Updates or creates the Azure Advisor Configuration.</span></span>

## <span data-ttu-id="90a09-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="90a09-104">SYNTAX</span></span>

### <span data-ttu-id="90a09-105">InputObjectRgExcludeParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="90a09-105">InputObjectRgExcludeParameterSet (Default)</span></span>
```
Set-AzAdvisorConfiguration [-Exclude] [[-ResourceGroupName] <String>]
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90a09-106">InputObjectLowCpuExcludeParameterSet</span><span class="sxs-lookup"><span data-stu-id="90a09-106">InputObjectLowCpuExcludeParameterSet</span></span> 
```
Set-AzAdvisorConfiguration [-Exclude] [-LowCpuThreshold] <Int32>
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90a09-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90a09-107">DESCRIPTION</span></span>
<span data-ttu-id="90a09-108">Используется для обновления конфигурации помощника Azure.</span><span class="sxs-lookup"><span data-stu-id="90a09-108">Used to update the configuration of the Azure Advisor.</span></span> <span data-ttu-id="90a09-109">Имеются два типа конфигурации: конфигурация уровня подписки и настройка на уровне группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90a09-109">Two types of Configuration are present: Subscription level configuration and ResourceGroup level configuration.</span></span> 

<span data-ttu-id="90a09-110">Конфигурация на уровне подписки: для этого типа подписки может быть только одна конфигурация.</span><span class="sxs-lookup"><span data-stu-id="90a09-110">Subscription level configuration: There can be only one Configuration for this type for a subscription.</span></span> <span data-ttu-id="90a09-111">С помощью этого cmdlet можно обновлять свойства LowCpuThreshold и Exclude.</span><span class="sxs-lookup"><span data-stu-id="90a09-111">LowCpuThreshold and Exclude properties can be updated using this cmdlet.</span></span>
<span data-ttu-id="90a09-112">Конфигурация уровня resourceGroup: для каждой группы ресурсов может быть только одна конфигурация.</span><span class="sxs-lookup"><span data-stu-id="90a09-112">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup.</span></span> <span data-ttu-id="90a09-113">С помощью этого cmdlet можно обновить только свойство Exclude.</span><span class="sxs-lookup"><span data-stu-id="90a09-113">Only Exclude property can be updated using this cmdlet.</span></span>

## <span data-ttu-id="90a09-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="90a09-114">EXAMPLES</span></span>

###  <span data-ttu-id="90a09-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="90a09-115">Example 1</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 10
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 10

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="90a09-116">Обновляет конфигурацию (lowCpuThreshold) для конфигурации уровня подписки.</span><span class="sxs-lookup"><span data-stu-id="90a09-116">Updates the configuration(lowCpuThreshold) for subscription level Configuration.</span></span>

### <span data-ttu-id="90a09-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="90a09-117">Example 2</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 15 -Exclude 
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : 15

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="90a09-118">Обновляет конфигурацию (lowCpuThreshold, exclude) для конфигурации уровня подписки и исключает ее из генерации рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="90a09-118">Updates the configuration(lowCpuThreshold, exclude) for subscription level Configuration and excludes from the recommendation generation.</span></span>

### <span data-ttu-id="90a09-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="90a09-119">Example 3</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -ResourceGroupName resourceGroupName1 -Exclude

Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}-resourceGroupName1
Name       : {user_subscription}-resourceGroupName1
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : null

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="90a09-120">Обновляет конфигурацию (исключаемую) для resourceGroupName1, чтобы исключить ее в генерации рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="90a09-120">Updates the configuration(exclude) for resourceGroupName1 to be excluded in the recommendation generation.</span></span>

### <span data-ttu-id="90a09-121">Пример 4</span><span class="sxs-lookup"><span data-stu-id="90a09-121">Example 4</span></span>
```powershell
PS C:\> Get-AzAdvisorConfiguration | Set-AzAdvisorConfiguration -LowCpuThreshold 20
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 20

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="90a09-122">Обновляет конфигурацию заданной рекомендации, передаемой из конвейера.</span><span class="sxs-lookup"><span data-stu-id="90a09-122">Updates the configuration for the given recommendation passed on from the pipeline.</span></span>

## <span data-ttu-id="90a09-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90a09-123">PARAMETERS</span></span>

### <span data-ttu-id="90a09-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90a09-124">-Confirm</span></span>
<span data-ttu-id="90a09-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90a09-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90a09-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a09-126">-DefaultProfile</span></span>
<span data-ttu-id="90a09-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90a09-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90a09-128">-Exclude</span><span class="sxs-lookup"><span data-stu-id="90a09-128">-Exclude</span></span>
<span data-ttu-id="90a09-129">Исключить из генерации рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="90a09-129">Exclude from the recommendation generation.</span></span> <span data-ttu-id="90a09-130">Если не указано свойство exclude, будет задано свойство "Ложь".</span><span class="sxs-lookup"><span data-stu-id="90a09-130">If not specified exclude property will be set to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a09-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90a09-131">-InputObject</span></span>
<span data-ttu-id="90a09-132">Объект Powershell типа PsAzureAdvisorConfigurationData, Get-AzAdvisorConfiguration звонка.</span><span class="sxs-lookup"><span data-stu-id="90a09-132">The powershell object type PsAzureAdvisorConfigurationData returned by Get-AzAdvisorConfiguration call.</span></span>

```yaml
Type: PsAzureAdvisorConfigurationData
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90a09-133">-LowCpuThreshold</span><span class="sxs-lookup"><span data-stu-id="90a09-133">-LowCpuThreshold</span></span>
<span data-ttu-id="90a09-134">Значение для порогового значения низкого ЦП.</span><span class="sxs-lookup"><span data-stu-id="90a09-134">Value for Low Cpu threshold.</span></span>

```yaml
Type: Int32
Parameter Sets: InputObjectLowCpuExcludeParameterSet
Aliases:
Accepted values: 0, 5, 10, 15, 20

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a09-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90a09-135">-ResourceGroupName</span></span>
<span data-ttu-id="90a09-136">Имя группы ресурсов для конфигурации.</span><span class="sxs-lookup"><span data-stu-id="90a09-136">Resource Group name for the configuration.</span></span>

```yaml
Type: String
Parameter Sets: InputObjectRgExcludeParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a09-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90a09-137">-WhatIf</span></span>
<span data-ttu-id="90a09-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90a09-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90a09-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="90a09-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90a09-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a09-140">CommonParameters</span></span>
<span data-ttu-id="90a09-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90a09-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="90a09-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90a09-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a09-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90a09-143">INPUTS</span></span>

### <span data-ttu-id="90a09-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="90a09-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="90a09-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="90a09-145">OUTPUTS</span></span>

### <span data-ttu-id="90a09-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="90a09-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="90a09-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="90a09-147">NOTES</span></span>

## <span data-ttu-id="90a09-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90a09-148">RELATED LINKS</span></span>
