---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: e6ac8c2a47f7a8d11eb4f82d46be2047fd5ff47d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899753"
---
# <span data-ttu-id="e2d6c-101">New-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="e2d6c-101">New-AzMlWebService</span></span>

## <span data-ttu-id="e2d6c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="e2d6c-103">Создание новой веб-службы.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-103">Creates a new web service.</span></span>

## <span data-ttu-id="e2d6c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2d6c-104">SYNTAX</span></span>

### <span data-ttu-id="e2d6c-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="e2d6c-105">CreateFromFile</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2d6c-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="e2d6c-106">CreateFromInstance</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2d6c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2d6c-107">DESCRIPTION</span></span>
<span data-ttu-id="e2d6c-108">Создание веб-службы машинного обучения Azure в существующей группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="e2d6c-109">Если в группе ресурсов есть веб-служба с таким же именем, вызов выполняет операцию обновления, и существующая веб-служба перезаписывается.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="e2d6c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2d6c-110">EXAMPLES</span></span>

### <span data-ttu-id="e2d6c-111">Пример 1: создание новой службы из определения на основе JSON-файла</span><span class="sxs-lookup"><span data-stu-id="e2d6c-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="e2d6c-112">Создание новой веб-службы машинного обучения Azure с именем "mywebservicename" в группе "myresourcegroup" и в Южной Центральной области США в соответствии с определением, представленным в JSON-файле, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="e2d6c-113">Пример 2: создание новой службы из экземпляра объекта</span><span class="sxs-lookup"><span data-stu-id="e2d6c-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="e2d6c-114">Вы можете получить экземпляр объекта веб-службы для настройки перед публикацией как ресурс с помощью командлета Import-AzMlWebService.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="e2d6c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2d6c-115">PARAMETERS</span></span>

### <span data-ttu-id="e2d6c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2d6c-116">-DefaultProfile</span></span>
<span data-ttu-id="e2d6c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e2d6c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2d6c-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e2d6c-118">-DefinitionFile</span></span>
<span data-ttu-id="e2d6c-119">Specifes путь к файлу, содержащему определение формата JSON для веб-службы.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-119">Specifes the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="e2d6c-120">Последнюю спецификацию для определения веб-службы можно найти в спецификации Swagger ниже https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="e2d6c-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d6c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e2d6c-121">-Force</span></span>
<span data-ttu-id="e2d6c-122">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e2d6c-123">-Location</span><span class="sxs-lookup"><span data-stu-id="e2d6c-123">-Location</span></span>
<span data-ttu-id="e2d6c-124">Область веб-службы.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-124">The region of the web service.</span></span>
<span data-ttu-id="e2d6c-125">Введите регион центра обработки данных Azure, например "Западная часть США" или "Юго-Тихоокеанский регион".</span><span class="sxs-lookup"><span data-stu-id="e2d6c-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="e2d6c-126">Вы можете разместить веб-службу в любом регионе, поддерживающем ресурсы такого типа.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="e2d6c-127">Веб-служба не должна находиться в той же области, что и у подписки Azure, или в той же области, что и ее группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="e2d6c-128">Группы ресурсов могут содержать веб-службы из разных регионов.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="e2d6c-129">Чтобы определить, какие области поддерживают каждый тип ресурсов, используйте Get-AzResourceProvider с командлетом параметра ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-129">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="e2d6c-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e2d6c-130">-Name</span></span>
<span data-ttu-id="e2d6c-131">Имя веб-службы.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-131">The name for the web service.</span></span>
<span data-ttu-id="e2d6c-132">Имя должно быть уникальным в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="e2d6c-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="e2d6c-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="e2d6c-134">Определение новой веб-службы, содержащее все свойства, составляющие службу.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="e2d6c-135">Этот параметр является обязательным и представляет экземпляр класса Microsoft. Azure. Management. MachineLearning. WebService. WebService.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="e2d6c-136">Последнюю спецификацию для определения веб-службы можно найти в спецификации Swagger ниже https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="e2d6c-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d6c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2d6c-137">-ResourceGroupName</span></span>
<span data-ttu-id="e2d6c-138">Группа ресурсов, в которую нужно поместить веб-службу.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="e2d6c-139">Введите регион центра обработки данных Azure, например "Западная часть США" или "Юго-Тихоокеанский регион".</span><span class="sxs-lookup"><span data-stu-id="e2d6c-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="e2d6c-140">Вы можете разместить веб-службу в любом регионе, поддерживающем ресурсы такого типа.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="e2d6c-141">Веб-служба не должна находиться в той же области, что и у подписки Azure, или в той же области, что и ее группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="e2d6c-142">Группы ресурсов могут содержать веб-службы из разных регионов.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="e2d6c-143">Чтобы определить, какие области поддерживают каждый тип ресурсов, используйте Get-AzResourceProvider с командлетом параметра ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-143">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="e2d6c-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2d6c-144">-Confirm</span></span>
<span data-ttu-id="e2d6c-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2d6c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2d6c-146">-WhatIf</span></span>
<span data-ttu-id="e2d6c-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2d6c-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2d6c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2d6c-149">CommonParameters</span></span>
<span data-ttu-id="e2d6c-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2d6c-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2d6c-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2d6c-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2d6c-152">INPUTS</span></span>

### <span data-ttu-id="e2d6c-153">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="e2d6c-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2d6c-154">OUTPUTS</span></span>

### <span data-ttu-id="e2d6c-155">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="e2d6c-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="e2d6c-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2d6c-156">NOTES</span></span>
<span data-ttu-id="e2d6c-157">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="e2d6c-157">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e2d6c-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2d6c-158">RELATED LINKS</span></span>
