---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 3e28b55a77ffb5f8d4ba95743e897628948d15f9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072870"
---
# <span data-ttu-id="58ebd-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="58ebd-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="58ebd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="58ebd-103">Удаляет сопоставление набора данных</span><span class="sxs-lookup"><span data-stu-id="58ebd-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="58ebd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58ebd-104">SYNTAX</span></span>

### <span data-ttu-id="58ebd-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="58ebd-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58ebd-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58ebd-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58ebd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58ebd-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58ebd-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58ebd-108">DESCRIPTION</span></span>
<span data-ttu-id="58ebd-109">Командлет **Remove-AzDataShareDataSetMapping** Удаляет сопоставления наборов данных.</span><span class="sxs-lookup"><span data-stu-id="58ebd-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="58ebd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58ebd-110">EXAMPLES</span></span>

### <span data-ttu-id="58ebd-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="58ebd-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="58ebd-112">Эти команды удаляют набор данных с именем DSM из sharesubscription WikiAds.</span><span class="sxs-lookup"><span data-stu-id="58ebd-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="58ebd-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58ebd-113">PARAMETERS</span></span>

### <span data-ttu-id="58ebd-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="58ebd-114">-AccountName</span></span>
<span data-ttu-id="58ebd-115">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="58ebd-115">Azure data share account name</span></span>

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

### <span data-ttu-id="58ebd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58ebd-116">-DefaultProfile</span></span>
<span data-ttu-id="58ebd-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58ebd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58ebd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58ebd-118">-InputObject</span></span>
<span data-ttu-id="58ebd-119">Объект сопоставления наборов данных Azure</span><span class="sxs-lookup"><span data-stu-id="58ebd-119">The azure data set mapping object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58ebd-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="58ebd-120">-Name</span></span>
<span data-ttu-id="58ebd-121">Имя сопоставления для наборов данных Azure</span><span class="sxs-lookup"><span data-stu-id="58ebd-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="58ebd-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58ebd-122">-PassThru</span></span>
<span data-ttu-id="58ebd-123">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="58ebd-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="58ebd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58ebd-124">-ResourceGroupName</span></span>
<span data-ttu-id="58ebd-125">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="58ebd-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="58ebd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58ebd-126">-ResourceId</span></span>
<span data-ttu-id="58ebd-127">Идентификатор ресурса для сопоставления набора данных Azure</span><span class="sxs-lookup"><span data-stu-id="58ebd-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="58ebd-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="58ebd-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="58ebd-129">Имя подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="58ebd-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="58ebd-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58ebd-130">-Confirm</span></span>
<span data-ttu-id="58ebd-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="58ebd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58ebd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58ebd-132">-WhatIf</span></span>
<span data-ttu-id="58ebd-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="58ebd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58ebd-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="58ebd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58ebd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ebd-135">CommonParameters</span></span>
<span data-ttu-id="58ebd-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58ebd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ebd-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58ebd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ebd-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58ebd-138">INPUTS</span></span>

### <span data-ttu-id="58ebd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="58ebd-139">System.String</span></span>

### <span data-ttu-id="58ebd-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="58ebd-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="58ebd-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58ebd-141">OUTPUTS</span></span>

### <span data-ttu-id="58ebd-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="58ebd-142">System.Boolean</span></span>

## <span data-ttu-id="58ebd-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="58ebd-143">NOTES</span></span>

## <span data-ttu-id="58ebd-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58ebd-144">RELATED LINKS</span></span>
