---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 16b212a0c5549f74b56e8c80be8d949a025ecb24
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312908"
---
# <span data-ttu-id="0efee-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="0efee-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="0efee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0efee-102">SYNOPSIS</span></span>
<span data-ttu-id="0efee-103">Удаляет сопоставление набора данных</span><span class="sxs-lookup"><span data-stu-id="0efee-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="0efee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0efee-104">SYNTAX</span></span>

### <span data-ttu-id="0efee-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0efee-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0efee-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0efee-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0efee-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0efee-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0efee-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0efee-108">DESCRIPTION</span></span>
<span data-ttu-id="0efee-109">Командлет **Remove-AzDataShareDataSetMapping** Удаляет сопоставления наборов данных.</span><span class="sxs-lookup"><span data-stu-id="0efee-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="0efee-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0efee-110">EXAMPLES</span></span>

### <span data-ttu-id="0efee-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0efee-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="0efee-112">Эти команды удаляют набор данных с именем DSM из sharesubscription WikiAds.</span><span class="sxs-lookup"><span data-stu-id="0efee-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="0efee-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0efee-113">PARAMETERS</span></span>

### <span data-ttu-id="0efee-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="0efee-114">-AccountName</span></span>
<span data-ttu-id="0efee-115">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="0efee-115">Azure data share account name</span></span>

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

### <span data-ttu-id="0efee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0efee-116">-DefaultProfile</span></span>
<span data-ttu-id="0efee-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0efee-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0efee-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0efee-118">-InputObject</span></span>
<span data-ttu-id="0efee-119">Объект сопоставления наборов данных Azure</span><span class="sxs-lookup"><span data-stu-id="0efee-119">The azure data set mapping object</span></span>


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

### <span data-ttu-id="0efee-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0efee-120">-Name</span></span>
<span data-ttu-id="0efee-121">Имя сопоставления для наборов данных Azure</span><span class="sxs-lookup"><span data-stu-id="0efee-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="0efee-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0efee-122">-PassThru</span></span>
<span data-ttu-id="0efee-123">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="0efee-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="0efee-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0efee-124">-ResourceGroupName</span></span>
<span data-ttu-id="0efee-125">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="0efee-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="0efee-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0efee-126">-ResourceId</span></span>
<span data-ttu-id="0efee-127">Идентификатор ресурса для сопоставления набора данных Azure</span><span class="sxs-lookup"><span data-stu-id="0efee-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="0efee-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="0efee-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="0efee-129">Имя подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="0efee-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="0efee-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0efee-130">-Confirm</span></span>
<span data-ttu-id="0efee-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0efee-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0efee-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0efee-132">-WhatIf</span></span>
<span data-ttu-id="0efee-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0efee-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0efee-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0efee-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0efee-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0efee-135">CommonParameters</span></span>
<span data-ttu-id="0efee-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0efee-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0efee-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0efee-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0efee-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0efee-138">INPUTS</span></span>

### <span data-ttu-id="0efee-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0efee-139">System.String</span></span>

### <span data-ttu-id="0efee-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="0efee-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="0efee-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0efee-141">OUTPUTS</span></span>

### <span data-ttu-id="0efee-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0efee-142">System.Boolean</span></span>

## <span data-ttu-id="0efee-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="0efee-143">NOTES</span></span>

## <span data-ttu-id="0efee-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0efee-144">RELATED LINKS</span></span>
