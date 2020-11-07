---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: 122d5118761e3a4b7a400b4bc73daa29d218c4ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721166"
---
# <span data-ttu-id="5796b-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="5796b-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="5796b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5796b-102">SYNOPSIS</span></span>
<span data-ttu-id="5796b-103">Удаляет сопоставление набора данных</span><span class="sxs-lookup"><span data-stu-id="5796b-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="5796b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5796b-104">SYNTAX</span></span>

### <span data-ttu-id="5796b-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5796b-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5796b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5796b-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5796b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5796b-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5796b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5796b-108">DESCRIPTION</span></span>
<span data-ttu-id="5796b-109">Командлет **Remove-AzDataShareDataSet** удаляет набор данных.</span><span class="sxs-lookup"><span data-stu-id="5796b-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="5796b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5796b-110">EXAMPLES</span></span>

### <span data-ttu-id="5796b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5796b-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="5796b-112">Эта команда удаляет набор данных с именем DS из WikiAds доступа.</span><span class="sxs-lookup"><span data-stu-id="5796b-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="5796b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5796b-113">PARAMETERS</span></span>

### <span data-ttu-id="5796b-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="5796b-114">-AccountName</span></span>
<span data-ttu-id="5796b-115">Имя учетной записи для предоставления доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="5796b-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="5796b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5796b-116">-DefaultProfile</span></span>
<span data-ttu-id="5796b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5796b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5796b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5796b-118">-InputObject</span></span>
<span data-ttu-id="5796b-119">Объект Set данных Azure.</span><span class="sxs-lookup"><span data-stu-id="5796b-119">The azure data set object.</span></span>


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

### <span data-ttu-id="5796b-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5796b-120">-Name</span></span>
<span data-ttu-id="5796b-121">Имя Set данных Azure.</span><span class="sxs-lookup"><span data-stu-id="5796b-121">Azure data set name.</span></span>

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

### <span data-ttu-id="5796b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5796b-122">-PassThru</span></span>
<span data-ttu-id="5796b-123">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="5796b-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="5796b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5796b-124">-ResourceGroupName</span></span>
<span data-ttu-id="5796b-125">Имя группы ресурсов для учетной записи общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="5796b-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="5796b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5796b-126">-ResourceId</span></span>
<span data-ttu-id="5796b-127">Идентификатор ресурса для набора данных Azure.</span><span class="sxs-lookup"><span data-stu-id="5796b-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="5796b-128">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="5796b-128">-ShareName</span></span>
<span data-ttu-id="5796b-129">Имя общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="5796b-129">Azure data share name.</span></span>

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

### <span data-ttu-id="5796b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5796b-130">-Confirm</span></span>
<span data-ttu-id="5796b-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5796b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5796b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5796b-132">-WhatIf</span></span>
<span data-ttu-id="5796b-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5796b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5796b-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5796b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5796b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5796b-135">CommonParameters</span></span>
<span data-ttu-id="5796b-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5796b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5796b-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5796b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5796b-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5796b-138">INPUTS</span></span>

### <span data-ttu-id="5796b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5796b-139">System.String</span></span>

### <span data-ttu-id="5796b-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="5796b-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="5796b-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5796b-141">OUTPUTS</span></span>

### <span data-ttu-id="5796b-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5796b-142">System.Boolean</span></span>

## <span data-ttu-id="5796b-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="5796b-143">NOTES</span></span>

## <span data-ttu-id="5796b-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5796b-144">RELATED LINKS</span></span>
