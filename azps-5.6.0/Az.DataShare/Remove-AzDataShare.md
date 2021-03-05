---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 8a46ecacae8df648ab6400cad25c3ca24b3ee3a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964728"
---
# <span data-ttu-id="a138a-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="a138a-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="a138a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a138a-102">SYNOPSIS</span></span>
<span data-ttu-id="a138a-103">Удаляет обойму данных.</span><span class="sxs-lookup"><span data-stu-id="a138a-103">Removes a data share.</span></span>

## <span data-ttu-id="a138a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a138a-104">SYNTAX</span></span>

### <span data-ttu-id="a138a-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a138a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a138a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a138a-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a138a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a138a-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a138a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a138a-108">DESCRIPTION</span></span>
<span data-ttu-id="a138a-109">Для удаления данных удаляется объем данных с его **cmdlet Remove-AzDataShare.**</span><span class="sxs-lookup"><span data-stu-id="a138a-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="a138a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a138a-110">EXAMPLES</span></span>

### <span data-ttu-id="a138a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a138a-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="a138a-112">Эти команды удаляют из Вики-ads учетной записи обмена данными Azure ресурс AdsShare с именем AdsShare.</span><span class="sxs-lookup"><span data-stu-id="a138a-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="a138a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a138a-113">PARAMETERS</span></span>

### <span data-ttu-id="a138a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a138a-114">-AccountName</span></span>
<span data-ttu-id="a138a-115">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="a138a-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a138a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a138a-116">-AsJob</span></span>
<span data-ttu-id="a138a-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="a138a-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="a138a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a138a-118">-DefaultProfile</span></span>
<span data-ttu-id="a138a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a138a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a138a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a138a-120">-InputObject</span></span>
<span data-ttu-id="a138a-121">Объект обмена данными Azure' 'тип yaml: наборы параметров PSDataShare: ByObjectParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="a138a-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="a138a-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="a138a-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a138a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a138a-123">-Name</span></span>
<span data-ttu-id="a138a-124">Имя обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="a138a-124">Azure data share name</span></span>

<span data-ttu-id="a138a-125">Yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="a138a-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="a138a-126">Обязательно: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="a138a-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a138a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a138a-127">-PassThru</span></span>
<span data-ttu-id="a138a-128">Возвращенный объект (если он указан).</span><span class="sxs-lookup"><span data-stu-id="a138a-128">Return object (if specified).</span></span>

<span data-ttu-id="a138a-129">Тип yaml: Наборы параметров SwitchParameter: (Все) псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="a138a-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="a138a-130">Обязательно: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="a138a-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="a138a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a138a-131">-ResourceGroupName</span></span>
<span data-ttu-id="a138a-132">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="a138a-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="a138a-133">Yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="a138a-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="a138a-134">Обязательно: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="a138a-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a138a-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a138a-135">-ResourceId</span></span>
<span data-ttu-id="a138a-136">ИД ресурса для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="a138a-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="a138a-137">Тип yaml: String Parameter Sets: ByResourceIdParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="a138a-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="a138a-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="a138a-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a138a-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a138a-139">-Confirm</span></span>
<span data-ttu-id="a138a-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a138a-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="a138a-141">Yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span><span class="sxs-lookup"><span data-stu-id="a138a-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="a138a-142">Обязательно: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="a138a-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="a138a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a138a-143">-WhatIf</span></span>
<span data-ttu-id="a138a-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a138a-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a138a-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a138a-145">The cmdlet is not run.</span></span>

<span data-ttu-id="a138a-146">Тип yaml: Наборы параметров SwitchParameter: (Все) Псевдонимы: wi</span><span class="sxs-lookup"><span data-stu-id="a138a-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="a138a-147">Обязательно: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="a138a-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="a138a-148">тип yaml: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDнаборы параметров ataShare: ByObjectParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="a138a-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="a138a-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="a138a-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="a138a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a138a-150">CommonParameters</span></span>
<span data-ttu-id="a138a-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a138a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a138a-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a138a-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a138a-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a138a-153">INPUTS</span></span>

### <span data-ttu-id="a138a-154">System.String</span><span class="sxs-lookup"><span data-stu-id="a138a-154">System.String</span></span>

### <span data-ttu-id="a138a-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="a138a-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="a138a-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a138a-156">OUTPUTS</span></span>

### <span data-ttu-id="a138a-157">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a138a-157">System.Boolean</span></span>

## <span data-ttu-id="a138a-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a138a-158">NOTES</span></span>

## <span data-ttu-id="a138a-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a138a-159">RELATED LINKS</span></span>
