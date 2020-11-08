---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: a9e9f5fdc71250acb2496c8eaaf1677461e9cd07
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072874"
---
# <span data-ttu-id="8f1f8-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="8f1f8-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="8f1f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f1f8-102">SYNOPSIS</span></span>
<span data-ttu-id="8f1f8-103">Удаление общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="8f1f8-103">Removes a data share.</span></span>

## <span data-ttu-id="8f1f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f1f8-104">SYNTAX</span></span>

### <span data-ttu-id="8f1f8-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8f1f8-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f1f8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f1f8-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f1f8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f1f8-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f1f8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f1f8-108">DESCRIPTION</span></span>
<span data-ttu-id="8f1f8-109">Командлет **Remove-AzDataShare** удаляет общий доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="8f1f8-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="8f1f8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f1f8-110">EXAMPLES</span></span>

### <span data-ttu-id="8f1f8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8f1f8-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="8f1f8-112">Эта команда удаляет из учетной записи общего доступа к данным Azure общий доступ к данным с именем AdsShare из WikiAds.</span><span class="sxs-lookup"><span data-stu-id="8f1f8-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="8f1f8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f1f8-113">PARAMETERS</span></span>

### <span data-ttu-id="8f1f8-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="8f1f8-114">-AccountName</span></span>
<span data-ttu-id="8f1f8-115">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="8f1f8-115">Azure data share account name</span></span>

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

### <span data-ttu-id="8f1f8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f1f8-116">-AsJob</span></span>
<span data-ttu-id="8f1f8-117">{{Fill AsJob описание}}</span><span class="sxs-lookup"><span data-stu-id="8f1f8-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="8f1f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f1f8-118">-DefaultProfile</span></span>
<span data-ttu-id="8f1f8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f1f8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f1f8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f1f8-120">-InputObject</span></span>
<span data-ttu-id="8f1f8-121">Объект общего доступа к данным Azure "" YAML: PSDataShare наборы параметров: ByObjectParameterSet псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="8f1f8-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="8f1f8-122">Обязательно: true position (имя по умолчанию): None прием конвейерного ввода: истина (ByValue) сохранить подстановочные знаки: ложь</span><span class="sxs-lookup"><span data-stu-id="8f1f8-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>


### <span data-ttu-id="8f1f8-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8f1f8-123">-Name</span></span>
<span data-ttu-id="8f1f8-124">Имя общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="8f1f8-124">Azure data share name</span></span>

<span data-ttu-id="8f1f8-125">Тип YAML: наборы строковых параметров: ByFieldsParameterSet псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="8f1f8-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="8f1f8-126">Обязательно: true position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false</span><span class="sxs-lookup"><span data-stu-id="8f1f8-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="8f1f8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f1f8-127">-PassThru</span></span>
<span data-ttu-id="8f1f8-128">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="8f1f8-128">Return object (if specified).</span></span>

<span data-ttu-id="8f1f8-129">Тип YAML: SwitchParameter наборы параметров: (все) псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="8f1f8-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="8f1f8-130">Обязательно: false position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false</span><span class="sxs-lookup"><span data-stu-id="8f1f8-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="8f1f8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f1f8-131">-ResourceGroupName</span></span>
<span data-ttu-id="8f1f8-132">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="8f1f8-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="8f1f8-133">Тип YAML: наборы строковых параметров: ByFieldsParameterSet псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="8f1f8-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="8f1f8-134">Обязательно: true position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false</span><span class="sxs-lookup"><span data-stu-id="8f1f8-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="8f1f8-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f1f8-135">-ResourceId</span></span>
<span data-ttu-id="8f1f8-136">Идентификатор ресурса общего ресурса данных Azure</span><span class="sxs-lookup"><span data-stu-id="8f1f8-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="8f1f8-137">Тип YAML: наборы строковых параметров: ByResourceIdParameterSet псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="8f1f8-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="8f1f8-138">Обязательно: true position (имя по умолчанию): None прием конвейерного ввода: истина (ByPropertyName) сохранить подстановочные знаки: ложь</span><span class="sxs-lookup"><span data-stu-id="8f1f8-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>


### <span data-ttu-id="8f1f8-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f1f8-139">-Confirm</span></span>
<span data-ttu-id="8f1f8-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8f1f8-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="8f1f8-141">Тип YAML: SwitchParameter наборы параметров: (все) псевдонимы: CF</span><span class="sxs-lookup"><span data-stu-id="8f1f8-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="8f1f8-142">Обязательно: false position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false</span><span class="sxs-lookup"><span data-stu-id="8f1f8-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="8f1f8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f1f8-143">-WhatIf</span></span>
<span data-ttu-id="8f1f8-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8f1f8-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f1f8-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8f1f8-145">The cmdlet is not run.</span></span>

<span data-ttu-id="8f1f8-146">Тип YAML: SwitchParameter наборы параметров: (все) псевдонимы: Wi</span><span class="sxs-lookup"><span data-stu-id="8f1f8-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="8f1f8-147">Обязательно: false position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false</span><span class="sxs-lookup"><span data-stu-id="8f1f8-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>
```

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

### <span data-ttu-id="8f1f8-148">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8f1f8-148">-Name</span></span>
<span data-ttu-id="8f1f8-149">Имя общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="8f1f8-149">Azure data share name</span></span>

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

### <span data-ttu-id="8f1f8-150">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f1f8-150">-PassThru</span></span>
<span data-ttu-id="8f1f8-151">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="8f1f8-151">Return object (if specified).</span></span>

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

### <span data-ttu-id="8f1f8-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f1f8-152">-ResourceGroupName</span></span>
<span data-ttu-id="8f1f8-153">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="8f1f8-153">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="8f1f8-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f1f8-154">-ResourceId</span></span>
<span data-ttu-id="8f1f8-155">Идентификатор ресурса общего ресурса данных Azure</span><span class="sxs-lookup"><span data-stu-id="8f1f8-155">The resource id of the Azure data share</span></span>

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

### <span data-ttu-id="8f1f8-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f1f8-156">-Confirm</span></span>
<span data-ttu-id="8f1f8-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8f1f8-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f1f8-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f1f8-158">-WhatIf</span></span>
<span data-ttu-id="8f1f8-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8f1f8-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f1f8-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8f1f8-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f1f8-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f1f8-161">CommonParameters</span></span>
<span data-ttu-id="8f1f8-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f1f8-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f1f8-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f1f8-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f1f8-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f1f8-164">INPUTS</span></span>

### <span data-ttu-id="8f1f8-165">System. String</span><span class="sxs-lookup"><span data-stu-id="8f1f8-165">System.String</span></span>

### <span data-ttu-id="8f1f8-166">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="8f1f8-166">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="8f1f8-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f1f8-167">OUTPUTS</span></span>

### <span data-ttu-id="8f1f8-168">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8f1f8-168">System.Boolean</span></span>

## <span data-ttu-id="8f1f8-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f1f8-169">NOTES</span></span>

## <span data-ttu-id="8f1f8-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f1f8-170">RELATED LINKS</span></span>
