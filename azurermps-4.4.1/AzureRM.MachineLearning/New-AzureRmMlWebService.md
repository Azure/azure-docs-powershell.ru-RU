---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
ms.openlocfilehash: 1fe6476836622445337ea0b4741b361504a57302
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569355"
---
# <span data-ttu-id="1843e-101">New-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="1843e-101">New-AzureRmMlWebService</span></span>

## <span data-ttu-id="1843e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1843e-102">SYNOPSIS</span></span>
<span data-ttu-id="1843e-103">Создание новой веб-службы.</span><span class="sxs-lookup"><span data-stu-id="1843e-103">Creates a new web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1843e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1843e-104">SYNTAX</span></span>

### <span data-ttu-id="1843e-105">Создание новой веб-службы Azure ML из файла JSON Definiton.</span><span class="sxs-lookup"><span data-stu-id="1843e-105">Create a new Azure ML webservice from a JSON definiton file.</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1843e-106">Создание новой веб-службы Azure ML из определения экземпляра WebService.</span><span class="sxs-lookup"><span data-stu-id="1843e-106">Create a new Azure ML webservice from a WebService instance definition.</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1843e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1843e-107">DESCRIPTION</span></span>
<span data-ttu-id="1843e-108">Создание веб-службы машинного обучения Azure в существующей группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1843e-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="1843e-109">Если в группе ресурсов есть веб-служба с таким же именем, вызов выполняет операцию обновления, и существующая веб-служба перезаписывается.</span><span class="sxs-lookup"><span data-stu-id="1843e-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="1843e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1843e-110">EXAMPLES</span></span>

### <span data-ttu-id="1843e-111">--------------------------Пример 1: создание новой службы из определения на основе JSON-файла--------------------------</span><span class="sxs-lookup"><span data-stu-id="1843e-111">--------------------------  Example 1: Create a new service from a Json file based definition  --------------------------</span></span>
<span data-ttu-id="1843e-112">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="1843e-112">@{paragraph=PS C:\\\>}</span></span>





```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="1843e-113">Создание новой веб-службы машинного обучения Azure с именем "mywebservicename" в группе "myresourcegroup" и в Южной Центральной области США в соответствии с определением, представленным в JSON-файле, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="1843e-113">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="1843e-114">--------------------------Пример 2: создание новой службы из экземпляра объекта--------------------------</span><span class="sxs-lookup"><span data-stu-id="1843e-114">--------------------------  Example 2: Create a new service from an object instance  --------------------------</span></span>
<span data-ttu-id="1843e-115">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="1843e-115">@{paragraph=PS C:\\\>}</span></span>





```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="1843e-116">Вы можете получить экземпляр объекта веб-службы для настройки перед публикацией как ресурс с помощью командлета Import-AzureRmMlWebService.</span><span class="sxs-lookup"><span data-stu-id="1843e-116">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="1843e-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1843e-117">PARAMETERS</span></span>

### <span data-ttu-id="1843e-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="1843e-118">-DefinitionFile</span></span>
<span data-ttu-id="1843e-119">Specifes путь к файлу, содержащему определение формата JSON для веб-службы.</span><span class="sxs-lookup"><span data-stu-id="1843e-119">Specifes the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="1843e-120">Последнюю спецификацию для определения веб-службы можно найти в спецификации Swagger ниже https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="1843e-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: System.String
Parameter Sets: Create a new Azure ML webservice from a JSON definiton file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1843e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1843e-121">-Force</span></span>
<span data-ttu-id="1843e-122">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="1843e-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1843e-123">-Location</span><span class="sxs-lookup"><span data-stu-id="1843e-123">-Location</span></span>
<span data-ttu-id="1843e-124">Область веб-службы.</span><span class="sxs-lookup"><span data-stu-id="1843e-124">The region of the web service.</span></span>
<span data-ttu-id="1843e-125">Введите регион центра обработки данных Azure, например "Западная часть США" или "Юго-Тихоокеанский регион".</span><span class="sxs-lookup"><span data-stu-id="1843e-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="1843e-126">Вы можете разместить веб-службу в любом регионе, поддерживающем ресурсы такого типа.</span><span class="sxs-lookup"><span data-stu-id="1843e-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="1843e-127">Веб-служба не должна находиться в той же области, что и у подписки Azure, или в той же области, что и ее группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1843e-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="1843e-128">Группы ресурсов могут содержать веб-службы из разных регионов.</span><span class="sxs-lookup"><span data-stu-id="1843e-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="1843e-129">Чтобы определить, какие области поддерживают каждый тип ресурсов, используйте Get-AzureRmResourceProvider с командлетом параметра ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="1843e-129">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="1843e-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1843e-130">-Name</span></span>
<span data-ttu-id="1843e-131">Имя веб-службы.</span><span class="sxs-lookup"><span data-stu-id="1843e-131">The name for the web service.</span></span>
<span data-ttu-id="1843e-132">Имя должно быть уникальным в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1843e-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="1843e-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="1843e-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="1843e-134">Определение новой веб-службы, содержащее все свойства, составляющие службу.</span><span class="sxs-lookup"><span data-stu-id="1843e-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="1843e-135">Этот параметр является обязательным и представляет экземпляр класса Microsoft. Azure. Management. MachineLearning. WebService. WebService.</span><span class="sxs-lookup"><span data-stu-id="1843e-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="1843e-136">Последнюю спецификацию для определения веб-службы можно найти в спецификации Swagger ниже https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="1843e-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Create a new Azure ML webservice from a WebService instance definition.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1843e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1843e-137">-ResourceGroupName</span></span>
<span data-ttu-id="1843e-138">Группа ресурсов, в которую нужно поместить веб-службу.</span><span class="sxs-lookup"><span data-stu-id="1843e-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="1843e-139">Введите регион центра обработки данных Azure, например "Западная часть США" или "Юго-Тихоокеанский регион".</span><span class="sxs-lookup"><span data-stu-id="1843e-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="1843e-140">Вы можете разместить веб-службу в любом регионе, поддерживающем ресурсы такого типа.</span><span class="sxs-lookup"><span data-stu-id="1843e-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="1843e-141">Веб-служба не должна находиться в той же области, что и у подписки Azure, или в той же области, что и ее группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1843e-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="1843e-142">Группы ресурсов могут содержать веб-службы из разных регионов.</span><span class="sxs-lookup"><span data-stu-id="1843e-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="1843e-143">Чтобы определить, какие области поддерживают каждый тип ресурсов, используйте Get-AzureRmResourceProvider с командлетом параметра ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="1843e-143">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="1843e-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1843e-144">-Confirm</span></span>
<span data-ttu-id="1843e-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1843e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1843e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1843e-146">-WhatIf</span></span>
<span data-ttu-id="1843e-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1843e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1843e-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1843e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1843e-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1843e-149">-DefaultProfile</span></span>
<span data-ttu-id="1843e-150">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1843e-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1843e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1843e-151">CommonParameters</span></span>
<span data-ttu-id="1843e-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1843e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1843e-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1843e-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1843e-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1843e-154">INPUTS</span></span>

### <span data-ttu-id="1843e-155">Вебслужба</span><span class="sxs-lookup"><span data-stu-id="1843e-155">WebService</span></span>
<span data-ttu-id="1843e-156">Параметр "NewWebServiceDefinition" принимает значение типа WebService из конвейера.</span><span class="sxs-lookup"><span data-stu-id="1843e-156">Parameter 'NewWebServiceDefinition' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="1843e-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1843e-157">OUTPUTS</span></span>

### <span data-ttu-id="1843e-158">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="1843e-158">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="1843e-159">Сводное описание веб-службы машинного обучения Azure.</span><span class="sxs-lookup"><span data-stu-id="1843e-159">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="1843e-160">Аналогично описанию, возвращаемому вызовом командлета Get-AzureRmMlWebService для существующей веб-службы.</span><span class="sxs-lookup"><span data-stu-id="1843e-160">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="1843e-161">Это описание не содержит конфиденциальные свойства, такие как учетные данные учетной записи хранения и клавиши доступа службы.</span><span class="sxs-lookup"><span data-stu-id="1843e-161">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="1843e-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="1843e-162">NOTES</span></span>
<span data-ttu-id="1843e-163">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="1843e-163">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="1843e-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1843e-164">RELATED LINKS</span></span>

