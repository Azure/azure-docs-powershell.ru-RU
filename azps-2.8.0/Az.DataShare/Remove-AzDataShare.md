---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: b16e5a9ff2c6e5a898baf56cf237676665bc12c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721170"
---
# <span data-ttu-id="5fd38-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="5fd38-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="5fd38-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5fd38-102">SYNOPSIS</span></span>
<span data-ttu-id="5fd38-103">Удаление общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="5fd38-103">Removes a data share.</span></span>

## <span data-ttu-id="5fd38-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5fd38-104">SYNTAX</span></span>

### <span data-ttu-id="5fd38-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5fd38-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fd38-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fd38-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fd38-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fd38-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fd38-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fd38-108">DESCRIPTION</span></span>
<span data-ttu-id="5fd38-109">Командлет **Remove-AzDataShare** удаляет общий доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="5fd38-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="5fd38-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5fd38-110">EXAMPLES</span></span>

### <span data-ttu-id="5fd38-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5fd38-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="5fd38-112">Эта команда удаляет из учетной записи общего доступа к данным Azure общий доступ к данным с именем AdsShare из WikiAds.</span><span class="sxs-lookup"><span data-stu-id="5fd38-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="5fd38-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5fd38-113">PARAMETERS</span></span>

### <span data-ttu-id="5fd38-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="5fd38-114">-AccountName</span></span>
<span data-ttu-id="5fd38-115">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="5fd38-115">Azure data share account name</span></span>

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

### <span data-ttu-id="5fd38-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fd38-116">-AsJob</span></span>
<span data-ttu-id="5fd38-117">{{Fill AsJob описание}}</span><span class="sxs-lookup"><span data-stu-id="5fd38-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="5fd38-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fd38-118">-DefaultProfile</span></span>
<span data-ttu-id="5fd38-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5fd38-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fd38-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fd38-120">-InputObject</span></span>
<span data-ttu-id="5fd38-121">Объект общего доступа к данным Azure "" YAML: PSDataShare наборы параметров: ByObjectParameterSet псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="5fd38-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="5fd38-122">Обязательно: true position (имя по умолчанию): None прием конвейерного ввода: истина (ByValue) сохранить подстановочные знаки: ложь</span><span class="sxs-lookup"><span data-stu-id="5fd38-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>


### <span data-ttu-id="5fd38-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5fd38-123">-Name</span></span>
<span data-ttu-id="5fd38-124">Имя общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="5fd38-124">Azure data share name</span></span>

<span data-ttu-id="5fd38-125">Тип YAML: наборы строковых параметров: ByFieldsParameterSet псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="5fd38-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="5fd38-126">Обязательно: true position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false</span><span class="sxs-lookup"><span data-stu-id="5fd38-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="5fd38-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5fd38-127">-PassThru</span></span>
<span data-ttu-id="5fd38-128">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="5fd38-128">Return object (if specified).</span></span>

<span data-ttu-id="5fd38-129">Тип YAML: SwitchParameter наборы параметров: (все) псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="5fd38-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="5fd38-130">Обязательно: false position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false</span><span class="sxs-lookup"><span data-stu-id="5fd38-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="5fd38-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fd38-131">-ResourceGroupName</span></span>
<span data-ttu-id="5fd38-132">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="5fd38-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="5fd38-133">Тип YAML: наборы строковых параметров: ByFieldsParameterSet псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="5fd38-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="5fd38-134">Обязательно: true position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false</span><span class="sxs-lookup"><span data-stu-id="5fd38-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="5fd38-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fd38-135">-ResourceId</span></span>
<span data-ttu-id="5fd38-136">Идентификатор ресурса общего ресурса данных Azure</span><span class="sxs-lookup"><span data-stu-id="5fd38-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="5fd38-137">Тип YAML: наборы строковых параметров: ByResourceIdParameterSet псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="5fd38-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="5fd38-138">Обязательно: true position (имя по умолчанию): None прием конвейерного ввода: истина (ByPropertyName) сохранить подстановочные знаки: ложь</span><span class="sxs-lookup"><span data-stu-id="5fd38-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>


### <span data-ttu-id="5fd38-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fd38-139">-Confirm</span></span>
<span data-ttu-id="5fd38-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5fd38-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="5fd38-141">Тип YAML: SwitchParameter наборы параметров: (все) псевдонимы: CF</span><span class="sxs-lookup"><span data-stu-id="5fd38-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="5fd38-142">Обязательно: false position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false</span><span class="sxs-lookup"><span data-stu-id="5fd38-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="5fd38-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fd38-143">-WhatIf</span></span>
<span data-ttu-id="5fd38-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5fd38-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fd38-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5fd38-145">The cmdlet is not run.</span></span>

<span data-ttu-id="5fd38-146">Тип YAML: SwitchParameter наборы параметров: (все) псевдонимы: Wi</span><span class="sxs-lookup"><span data-stu-id="5fd38-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="5fd38-147">Обязательно: false position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false</span><span class="sxs-lookup"><span data-stu-id="5fd38-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>
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

### <span data-ttu-id="5fd38-148">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5fd38-148">-Name</span></span>
<span data-ttu-id="5fd38-149">Имя общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="5fd38-149">Azure data share name</span></span>

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

### <span data-ttu-id="5fd38-150">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5fd38-150">-PassThru</span></span>
<span data-ttu-id="5fd38-151">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="5fd38-151">Return object (if specified).</span></span>

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

### <span data-ttu-id="5fd38-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fd38-152">-ResourceGroupName</span></span>
<span data-ttu-id="5fd38-153">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="5fd38-153">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="5fd38-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fd38-154">-ResourceId</span></span>
<span data-ttu-id="5fd38-155">Идентификатор ресурса общего ресурса данных Azure</span><span class="sxs-lookup"><span data-stu-id="5fd38-155">The resource id of the Azure data share</span></span>

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

### <span data-ttu-id="5fd38-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fd38-156">-Confirm</span></span>
<span data-ttu-id="5fd38-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5fd38-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fd38-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fd38-158">-WhatIf</span></span>
<span data-ttu-id="5fd38-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5fd38-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5fd38-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5fd38-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fd38-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd38-161">CommonParameters</span></span>
<span data-ttu-id="5fd38-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5fd38-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fd38-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fd38-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd38-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5fd38-164">INPUTS</span></span>

### <span data-ttu-id="5fd38-165">System. String</span><span class="sxs-lookup"><span data-stu-id="5fd38-165">System.String</span></span>

### <span data-ttu-id="5fd38-166">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="5fd38-166">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="5fd38-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fd38-167">OUTPUTS</span></span>

### <span data-ttu-id="5fd38-168">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5fd38-168">System.Boolean</span></span>

## <span data-ttu-id="5fd38-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="5fd38-169">NOTES</span></span>

## <span data-ttu-id="5fd38-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5fd38-170">RELATED LINKS</span></span>
