---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/update-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
ms.openlocfilehash: 5fb8c8f71366dd9fd0a2c6b12fc023c1ce3ccf9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567983"
---
# <span data-ttu-id="0981e-101">Update-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="0981e-101">Update-AzureRmMlWebService</span></span>

## <span data-ttu-id="0981e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0981e-102">SYNOPSIS</span></span>
<span data-ttu-id="0981e-103">Обновляет свойства существующего ресурса веб-службы.</span><span class="sxs-lookup"><span data-stu-id="0981e-103">Updates properties of an existing web service resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0981e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0981e-104">SYNTAX</span></span>

### <span data-ttu-id="0981e-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="0981e-105">UpdateFromParameters</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0981e-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="0981e-106">UpdateFromObject</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0981e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0981e-107">DESCRIPTION</span></span>
<span data-ttu-id="0981e-108">Командлет Update-AzureRmMlWebService позволяет обновлять нестатические свойства веб-службы.</span><span class="sxs-lookup"><span data-stu-id="0981e-108">The Update-AzureRmMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="0981e-109">Командлет работает как операция исправления.</span><span class="sxs-lookup"><span data-stu-id="0981e-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="0981e-110">Передача только тех свойств, которые вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="0981e-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="0981e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0981e-111">EXAMPLES</span></span>

### <span data-ttu-id="0981e-112">--------------------------Пример 1: аргументы выборочного обновления--------------------------</span><span class="sxs-lookup"><span data-stu-id="0981e-112">--------------------------  Example 1: Selective update arguments  --------------------------</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="0981e-113">Здесь мы изменим описание, основной ключ доступа и Активируй сбор диагностических сведений для всех трассировок во время выполнения для веб-службы.</span><span class="sxs-lookup"><span data-stu-id="0981e-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="0981e-114">--------------------------Пример 2: обновление на основе экземпляра веб-службы--------------------------</span><span class="sxs-lookup"><span data-stu-id="0981e-114">--------------------------  Example 2: Update based on a web service instance  --------------------------</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="0981e-115">В примере сначала создается определение веб-службы, которое включает только поля, которые нужно обновить, а затем вызывает Update-AzureRmMlWebService, чтобы применить их с помощью параметра ServiceUpdates.</span><span class="sxs-lookup"><span data-stu-id="0981e-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzureRmMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="0981e-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0981e-116">PARAMETERS</span></span>

### <span data-ttu-id="0981e-117">-Активы</span><span class="sxs-lookup"><span data-stu-id="0981e-117">-Assets</span></span>
<span data-ttu-id="0981e-118">Набор ресурсов (например, модулей, наборов данных), образующих веб-службу.</span><span class="sxs-lookup"><span data-stu-id="0981e-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: Hashtable
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0981e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0981e-119">-DefaultProfile</span></span>
<span data-ttu-id="0981e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0981e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0981e-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="0981e-121">-Description</span></span>
<span data-ttu-id="0981e-122">Новое значение для описания веб-службы.</span><span class="sxs-lookup"><span data-stu-id="0981e-122">The new value for the web service's description.</span></span>
<span data-ttu-id="0981e-123">Это видно в схеме API службы Swagger.</span><span class="sxs-lookup"><span data-stu-id="0981e-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0981e-124">-Диагностика</span><span class="sxs-lookup"><span data-stu-id="0981e-124">-Diagnostics</span></span>
<span data-ttu-id="0981e-125">Параметры, управляющие сбором трассировок диагностики для веб-службы.</span><span class="sxs-lookup"><span data-stu-id="0981e-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: DiagnosticsConfiguration
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0981e-126">-Force</span><span class="sxs-lookup"><span data-stu-id="0981e-126">-Force</span></span>
<span data-ttu-id="0981e-127">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="0981e-127">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0981e-128">-Input</span><span class="sxs-lookup"><span data-stu-id="0981e-128">-Input</span></span>
<span data-ttu-id="0981e-129">Определение входных данных веб-службы, предоставленных в качестве конструкции схемы Swagger.</span><span class="sxs-lookup"><span data-stu-id="0981e-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0981e-130">-ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0981e-130">-IsReadOnly</span></span>
<span data-ttu-id="0981e-131">Указывает, что эта веб-служба предназначена только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0981e-131">Specifies that this web serviceis readonly.</span></span>
<span data-ttu-id="0981e-132">После того как вы задали этот параметр, веб-службу можно будет обновлять, в том числе изменить значение этого свойства, и удалить ее.</span><span class="sxs-lookup"><span data-stu-id="0981e-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0981e-133">-Keys</span><span class="sxs-lookup"><span data-stu-id="0981e-133">-Keys</span></span>
<span data-ttu-id="0981e-134">Обновляет один или оба клавиши доступа, используемые для проверки подлинности вызовов API среды выполнения службы.</span><span class="sxs-lookup"><span data-stu-id="0981e-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: WebServiceKeys
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0981e-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0981e-135">-Name</span></span>
<span data-ttu-id="0981e-136">Имя ресурса веб-службы, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="0981e-136">The name of the web service resource to be updated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0981e-137">-Output</span><span class="sxs-lookup"><span data-stu-id="0981e-137">-Output</span></span>
<span data-ttu-id="0981e-138">Определение выходных данных веб-службы, которые представлены в виде конструкции схемы Swagger.</span><span class="sxs-lookup"><span data-stu-id="0981e-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0981e-139">-Package</span><span class="sxs-lookup"><span data-stu-id="0981e-139">-Package</span></span>
<span data-ttu-id="0981e-140">Определение пакета графа, определяющего эту веб-службу.</span><span class="sxs-lookup"><span data-stu-id="0981e-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: GraphPackage
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0981e-141">-Parameters</span><span class="sxs-lookup"><span data-stu-id="0981e-141">-Parameters</span></span>
<span data-ttu-id="0981e-142">Набор значений глобальных параметров, определенных для веб-службы, заданный в качестве имени глобального параметра — \> коллекция значений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0981e-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="0981e-143">Если значение по умолчанию не задано, параметр считается обязательным.</span><span class="sxs-lookup"><span data-stu-id="0981e-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: Hashtable
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0981e-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="0981e-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="0981e-145">Обновляет конфигурацию конечной точки реального времени службы.</span><span class="sxs-lookup"><span data-stu-id="0981e-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: RealtimeConfiguration
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0981e-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0981e-146">-ResourceGroupName</span></span>
<span data-ttu-id="0981e-147">Группа ресурсов, содержащая веб-службу, которую нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="0981e-147">The resource group that contains the web service to be updated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0981e-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="0981e-148">-ServiceUpdates</span></span>
<span data-ttu-id="0981e-149">Набор обновлений, которые необходимо применить к веб-службе, указанной в качестве экземпляра определения веб-службы.</span><span class="sxs-lookup"><span data-stu-id="0981e-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="0981e-150">Изменяются только поля, не являющиеся статическими.</span><span class="sxs-lookup"><span data-stu-id="0981e-150">Only non-static fields are modified.</span></span>

```yaml
Type: WebService
Parameter Sets: UpdateFromObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0981e-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0981e-151">-StorageAccountKey</span></span>
<span data-ttu-id="0981e-152">Поворачивает клавишу доступа для учетной записи хранения, связанной с веб-службой.</span><span class="sxs-lookup"><span data-stu-id="0981e-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0981e-153">-Title</span><span class="sxs-lookup"><span data-stu-id="0981e-153">-Title</span></span>
<span data-ttu-id="0981e-154">Новое значение заголовка веб-службы.</span><span class="sxs-lookup"><span data-stu-id="0981e-154">The new value for the web service's title.</span></span>
<span data-ttu-id="0981e-155">Это видно в схеме API службы Swagger.</span><span class="sxs-lookup"><span data-stu-id="0981e-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0981e-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0981e-156">-Confirm</span></span>
<span data-ttu-id="0981e-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0981e-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0981e-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0981e-158">-WhatIf</span></span>
<span data-ttu-id="0981e-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0981e-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0981e-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0981e-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0981e-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0981e-161">CommonParameters</span></span>
<span data-ttu-id="0981e-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0981e-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0981e-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0981e-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0981e-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0981e-164">INPUTS</span></span>

### <span data-ttu-id="0981e-165">Вебслужба</span><span class="sxs-lookup"><span data-stu-id="0981e-165">WebService</span></span>
<span data-ttu-id="0981e-166">Параметр "ServiceUpdates" принимает значение типа WebService из конвейера.</span><span class="sxs-lookup"><span data-stu-id="0981e-166">Parameter 'ServiceUpdates' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="0981e-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0981e-167">OUTPUTS</span></span>

### <span data-ttu-id="0981e-168">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="0981e-168">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="0981e-169">Сводное описание веб-службы машинного обучения Azure.</span><span class="sxs-lookup"><span data-stu-id="0981e-169">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="0981e-170">Аналогично описанию, возвращаемому вызовом командлета Get-AzureRmMlWebService для существующей веб-службы.</span><span class="sxs-lookup"><span data-stu-id="0981e-170">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="0981e-171">Это описание не содержит конфиденциальные свойства, такие как учетные данные учетной записи хранения и клавиши доступа службы.</span><span class="sxs-lookup"><span data-stu-id="0981e-171">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="0981e-172">Пуск</span><span class="sxs-lookup"><span data-stu-id="0981e-172">NOTES</span></span>
<span data-ttu-id="0981e-173">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="0981e-173">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="0981e-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0981e-174">RELATED LINKS</span></span>

