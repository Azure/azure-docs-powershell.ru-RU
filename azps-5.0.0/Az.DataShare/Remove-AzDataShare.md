---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312923"
---
# <span data-ttu-id="3b9dd-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="3b9dd-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="3b9dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b9dd-102">SYNOPSIS</span></span>
<span data-ttu-id="3b9dd-103">Удаление общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="3b9dd-103">Removes a data share.</span></span>

## <span data-ttu-id="3b9dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b9dd-104">SYNTAX</span></span>

### <span data-ttu-id="3b9dd-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3b9dd-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b9dd-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b9dd-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b9dd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b9dd-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b9dd-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b9dd-108">DESCRIPTION</span></span>
<span data-ttu-id="3b9dd-109">Командлет **Remove-AzDataShare** удаляет общий доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="3b9dd-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="3b9dd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b9dd-110">EXAMPLES</span></span>

### <span data-ttu-id="3b9dd-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3b9dd-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="3b9dd-112">Эта команда удаляет из учетной записи общего доступа к данным Azure общий доступ к данным с именем AdsShare из WikiAds.</span><span class="sxs-lookup"><span data-stu-id="3b9dd-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="3b9dd-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b9dd-113">PARAMETERS</span></span>

### <span data-ttu-id="3b9dd-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="3b9dd-114">-AccountName</span></span>
<span data-ttu-id="3b9dd-115">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="3b9dd-115">Azure data share account name</span></span>

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

### <span data-ttu-id="3b9dd-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b9dd-116">-AsJob</span></span>
<span data-ttu-id="3b9dd-117">{{Fill AsJob описание}}</span><span class="sxs-lookup"><span data-stu-id="3b9dd-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="3b9dd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b9dd-118">-DefaultProfile</span></span>
<span data-ttu-id="3b9dd-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b9dd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b9dd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b9dd-120">-InputObject</span></span>
<span data-ttu-id="3b9dd-121">Объект общего доступа к данным Azure "" YAML: PSDataShare наборы параметров: ByObjectParameterSet псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="3b9dd-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="3b9dd-122">Обязательно: true position (имя по умолчанию): None прием конвейерного ввода: истина (ByValue) сохранить подстановочные знаки: ложь</span><span class="sxs-lookup"><span data-stu-id="3b9dd-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="3b9dd-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3b9dd-123">-Name</span></span>
<span data-ttu-id="3b9dd-124">Имя общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="3b9dd-124">Azure data share name</span></span>

<span data-ttu-id="3b9dd-125">Тип YAML: наборы строковых параметров: ByFieldsParameterSet псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="3b9dd-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="3b9dd-126">Обязательно: true position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false</span><span class="sxs-lookup"><span data-stu-id="3b9dd-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="3b9dd-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b9dd-127">-PassThru</span></span>
<span data-ttu-id="3b9dd-128">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="3b9dd-128">Return object (if specified).</span></span>

<span data-ttu-id="3b9dd-129">Тип YAML: SwitchParameter наборы параметров: (все) псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="3b9dd-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="3b9dd-130">Обязательно: false position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false</span><span class="sxs-lookup"><span data-stu-id="3b9dd-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="3b9dd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b9dd-131">-ResourceGroupName</span></span>
<span data-ttu-id="3b9dd-132">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="3b9dd-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="3b9dd-133">Тип YAML: наборы строковых параметров: ByFieldsParameterSet псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="3b9dd-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="3b9dd-134">Обязательно: true position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false</span><span class="sxs-lookup"><span data-stu-id="3b9dd-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="3b9dd-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b9dd-135">-ResourceId</span></span>
<span data-ttu-id="3b9dd-136">Идентификатор ресурса общего ресурса данных Azure</span><span class="sxs-lookup"><span data-stu-id="3b9dd-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="3b9dd-137">Тип YAML: наборы строковых параметров: ByResourceIdParameterSet псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="3b9dd-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="3b9dd-138">Обязательно: true position (имя по умолчанию): None прием конвейерного ввода: истина (ByPropertyName) сохранить подстановочные знаки: ложь</span><span class="sxs-lookup"><span data-stu-id="3b9dd-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="3b9dd-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b9dd-139">-Confirm</span></span>
<span data-ttu-id="3b9dd-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3b9dd-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="3b9dd-141">Тип YAML: SwitchParameter наборы параметров: (все) псевдонимы: CF</span><span class="sxs-lookup"><span data-stu-id="3b9dd-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="3b9dd-142">Обязательно: false position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false</span><span class="sxs-lookup"><span data-stu-id="3b9dd-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="3b9dd-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b9dd-143">-WhatIf</span></span>
<span data-ttu-id="3b9dd-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3b9dd-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b9dd-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3b9dd-145">The cmdlet is not run.</span></span>

<span data-ttu-id="3b9dd-146">Тип YAML: SwitchParameter наборы параметров: (все) псевдонимы: Wi</span><span class="sxs-lookup"><span data-stu-id="3b9dd-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="3b9dd-147">Обязательно: false position (имя по умолчанию): None прием конвейерной передачи: false ввод подстановочных знаков: false</span><span class="sxs-lookup"><span data-stu-id="3b9dd-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="3b9dd-148">Тип YAML: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare наборы параметров: ByObjectParameterSet псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="3b9dd-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="3b9dd-149">Обязательно: true position (имя по умолчанию): None прием конвейерного ввода: истина (ByValue) сохранить подстановочные знаки: ложь</span><span class="sxs-lookup"><span data-stu-id="3b9dd-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="3b9dd-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b9dd-150">CommonParameters</span></span>
<span data-ttu-id="3b9dd-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b9dd-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b9dd-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b9dd-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b9dd-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b9dd-153">INPUTS</span></span>

### <span data-ttu-id="3b9dd-154">System. String</span><span class="sxs-lookup"><span data-stu-id="3b9dd-154">System.String</span></span>

### <span data-ttu-id="3b9dd-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="3b9dd-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="3b9dd-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b9dd-156">OUTPUTS</span></span>

### <span data-ttu-id="3b9dd-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3b9dd-157">System.Boolean</span></span>

## <span data-ttu-id="3b9dd-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b9dd-158">NOTES</span></span>

## <span data-ttu-id="3b9dd-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b9dd-159">RELATED LINKS</span></span>
