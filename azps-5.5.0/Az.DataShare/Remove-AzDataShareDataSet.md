---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: c3d5105fc3b43a3f6b7ff8b45c5ba8236fed656b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228644"
---
# <span data-ttu-id="60dea-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="60dea-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="60dea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60dea-102">SYNOPSIS</span></span>
<span data-ttu-id="60dea-103">Удаление сопоставления для наборов данных</span><span class="sxs-lookup"><span data-stu-id="60dea-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="60dea-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="60dea-104">SYNTAX</span></span>

### <span data-ttu-id="60dea-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="60dea-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60dea-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60dea-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60dea-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60dea-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60dea-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60dea-108">DESCRIPTION</span></span>
<span data-ttu-id="60dea-109">Для удаления набор данных удаляется набор данных **стевого-azDataShareDataSet.**</span><span class="sxs-lookup"><span data-stu-id="60dea-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="60dea-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="60dea-110">EXAMPLES</span></span>

### <span data-ttu-id="60dea-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="60dea-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="60dea-112">Эти команды удаляют набор данных с именем DS из share WikiAds.</span><span class="sxs-lookup"><span data-stu-id="60dea-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="60dea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60dea-113">PARAMETERS</span></span>

### <span data-ttu-id="60dea-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="60dea-114">-AccountName</span></span>
<span data-ttu-id="60dea-115">Имя учетной записи для обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="60dea-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="60dea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60dea-116">-DefaultProfile</span></span>
<span data-ttu-id="60dea-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60dea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60dea-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60dea-118">-InputObject</span></span>
<span data-ttu-id="60dea-119">Объект набора данных Azure.</span><span class="sxs-lookup"><span data-stu-id="60dea-119">The azure data set object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60dea-120">-Name</span><span class="sxs-lookup"><span data-stu-id="60dea-120">-Name</span></span>
<span data-ttu-id="60dea-121">Имя набора данных Azure.</span><span class="sxs-lookup"><span data-stu-id="60dea-121">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60dea-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60dea-122">-PassThru</span></span>
<span data-ttu-id="60dea-123">Возвращенный объект (если он указан).</span><span class="sxs-lookup"><span data-stu-id="60dea-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="60dea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60dea-124">-ResourceGroupName</span></span>
<span data-ttu-id="60dea-125">Имя группы ресурсов учетной записи azure data share.</span><span class="sxs-lookup"><span data-stu-id="60dea-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="60dea-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60dea-126">-ResourceId</span></span>
<span data-ttu-id="60dea-127">ИД ресурса для набора данных Azure.</span><span class="sxs-lookup"><span data-stu-id="60dea-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="60dea-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="60dea-128">-ShareName</span></span>
<span data-ttu-id="60dea-129">Имя обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="60dea-129">Azure data share name.</span></span>

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

### <span data-ttu-id="60dea-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60dea-130">-Confirm</span></span>
<span data-ttu-id="60dea-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="60dea-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60dea-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60dea-132">-WhatIf</span></span>
<span data-ttu-id="60dea-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60dea-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60dea-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="60dea-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60dea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60dea-135">CommonParameters</span></span>
<span data-ttu-id="60dea-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60dea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60dea-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60dea-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60dea-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60dea-138">INPUTS</span></span>

### <span data-ttu-id="60dea-139">System.String</span><span class="sxs-lookup"><span data-stu-id="60dea-139">System.String</span></span>

### <span data-ttu-id="60dea-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="60dea-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="60dea-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="60dea-141">OUTPUTS</span></span>

### <span data-ttu-id="60dea-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="60dea-142">System.Boolean</span></span>

## <span data-ttu-id="60dea-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="60dea-143">NOTES</span></span>

## <span data-ttu-id="60dea-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60dea-144">RELATED LINKS</span></span>
