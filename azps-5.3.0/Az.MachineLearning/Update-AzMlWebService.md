---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
ms.openlocfilehash: a170d21a2301541f1346905ed701d477ecba4204
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425575"
---
# <span data-ttu-id="4e5a6-101">Update-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="4e5a6-101">Update-AzMlWebService</span></span>

## <span data-ttu-id="4e5a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e5a6-102">SYNOPSIS</span></span>
<span data-ttu-id="4e5a6-103">Обновляет свойства существующего ресурса веб-службы.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-103">Updates properties of an existing web service resource.</span></span>

## <span data-ttu-id="4e5a6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e5a6-104">SYNTAX</span></span>

### <span data-ttu-id="4e5a6-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="4e5a6-105">UpdateFromParameters</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e5a6-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="4e5a6-106">UpdateFromObject</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e5a6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e5a6-107">DESCRIPTION</span></span>
<span data-ttu-id="4e5a6-108">С Update-AzMlWebService можно обновить нестатические свойства веб-службы.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-108">The Update-AzMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="4e5a6-109">Этот cmdlet работает как исправление.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="4e5a6-110">Передать только свойства, которые нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="4e5a6-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e5a6-111">EXAMPLES</span></span>

### <span data-ttu-id="4e5a6-112">Пример 1. Аргументы выборочного обновления</span><span class="sxs-lookup"><span data-stu-id="4e5a6-112">Example 1: Selective update arguments</span></span>
```
Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="4e5a6-113">Здесь мы изменим описание, первичный ключ доступа и вметим сбор диагностики для всех трассировок во время работы веб-службы.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="4e5a6-114">Пример 2. Обновление на основе экземпляра веб-службы</span><span class="sxs-lookup"><span data-stu-id="4e5a6-114">Example 2: Update based on a web service instance</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="4e5a6-115">В этом примере сначала создается определение веб-службы, которое содержит только обновляемые поля, а затем вызывается Update-AzMlWebService, чтобы применить его с помощью параметра ServiceUpdates.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="4e5a6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e5a6-116">PARAMETERS</span></span>

### <span data-ttu-id="4e5a6-117">-Активы</span><span class="sxs-lookup"><span data-stu-id="4e5a6-117">-Assets</span></span>
<span data-ttu-id="4e5a6-118">Набор активов (например, модулей, наборов данных), которые составляют веб-службу.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5a6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e5a6-119">-DefaultProfile</span></span>
<span data-ttu-id="4e5a6-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4e5a6-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e5a6-121">-Description</span><span class="sxs-lookup"><span data-stu-id="4e5a6-121">-Description</span></span>
<span data-ttu-id="4e5a6-122">Новое значение описания веб-службы.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-122">The new value for the web service's description.</span></span>
<span data-ttu-id="4e5a6-123">Этот результат можно увидеть в схеме API-2016 для Swagger службы.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5a6-124">-Diagnostics</span><span class="sxs-lookup"><span data-stu-id="4e5a6-124">-Diagnostics</span></span>
<span data-ttu-id="4e5a6-125">Параметры, которые контролируют сбор диагностических трассировок для веб-службы.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.DiagnosticsConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5a6-126">-Force</span><span class="sxs-lookup"><span data-stu-id="4e5a6-126">-Force</span></span>
<span data-ttu-id="4e5a6-127">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4e5a6-128">-Input</span><span class="sxs-lookup"><span data-stu-id="4e5a6-128">-Input</span></span>
<span data-ttu-id="4e5a6-129">Определение входных данных веб-службы, предоставленное в качестве конструкции схемы Swagger.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5a6-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="4e5a6-130">-IsReadOnly</span></span>
<span data-ttu-id="4e5a6-131">Указывает, что эта веб-служба читается в браузере.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-131">Specifies that this web service is readonly.</span></span>
<span data-ttu-id="4e5a6-132">После этого веб-службу можно обновлять дольше, в том числе изменять значение этого свойства, и удалять ее можно только.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5a6-133">-Keys</span><span class="sxs-lookup"><span data-stu-id="4e5a6-133">-Keys</span></span>
<span data-ttu-id="4e5a6-134">Обновление одного или обоих ключей доступа, используемых для проверки подлинности звонков на API времени работы службы.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5a6-135">-Name</span><span class="sxs-lookup"><span data-stu-id="4e5a6-135">-Name</span></span>
<span data-ttu-id="4e5a6-136">Имя обновляемого ресурса веб-службы.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-136">The name of the web service resource to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5a6-137">-Output</span><span class="sxs-lookup"><span data-stu-id="4e5a6-137">-Output</span></span>
<span data-ttu-id="4e5a6-138">Определение выходных данных веб-службы, предоставленное в качестве конструкции схемы Swagger.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5a6-139">-Package</span><span class="sxs-lookup"><span data-stu-id="4e5a6-139">-Package</span></span>
<span data-ttu-id="4e5a6-140">Определение пакета графа, который определяет эту веб-службу.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.GraphPackage
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5a6-141">-Parameters</span><span class="sxs-lookup"><span data-stu-id="4e5a6-141">-Parameters</span></span>
<span data-ttu-id="4e5a6-142">Набор глобальных значений параметров, определенных для веб-службы, заданный как глобальное имя параметра — набор \> значений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="4e5a6-143">Если значение по умолчанию не задано, параметр считается требуемой.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5a6-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e5a6-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="4e5a6-145">Обновления для настройки конечной точки реального времени службы.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.RealtimeConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5a6-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e5a6-146">-ResourceGroupName</span></span>
<span data-ttu-id="4e5a6-147">Группа ресурсов, которая содержит обновляемую веб-службу.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-147">The resource group that contains the web service to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5a6-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="4e5a6-148">-ServiceUpdates</span></span>
<span data-ttu-id="4e5a6-149">Набор обновлений, которые нужно применять к веб-службе, предоставленной в качестве экземпляра определения веб-службы.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="4e5a6-150">Изменены только нестатические поля.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-150">Only non-static fields are modified.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: UpdateFromObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e5a6-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4e5a6-151">-StorageAccountKey</span></span>
<span data-ttu-id="4e5a6-152">Поворот ключа доступа для учетной записи хранения, связанной с веб-службой.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5a6-153">-Title</span><span class="sxs-lookup"><span data-stu-id="4e5a6-153">-Title</span></span>
<span data-ttu-id="4e5a6-154">Новое значение названия веб-службы.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-154">The new value for the web service's title.</span></span>
<span data-ttu-id="4e5a6-155">Этот результат можно увидеть в схеме API-2016 для Swagger службы.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e5a6-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e5a6-156">-Confirm</span></span>
<span data-ttu-id="4e5a6-157">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e5a6-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e5a6-158">-WhatIf</span></span>
<span data-ttu-id="4e5a6-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e5a6-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e5a6-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e5a6-161">CommonParameters</span></span>
<span data-ttu-id="4e5a6-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e5a6-163">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e5a6-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e5a6-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e5a6-164">INPUTS</span></span>

### <span data-ttu-id="4e5a6-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="4e5a6-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="4e5a6-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e5a6-166">OUTPUTS</span></span>

### <span data-ttu-id="4e5a6-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="4e5a6-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="4e5a6-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e5a6-168">NOTES</span></span>
<span data-ttu-id="4e5a6-169">Ключевые слова: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="4e5a6-169">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="4e5a6-170">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e5a6-170">RELATED LINKS</span></span>
