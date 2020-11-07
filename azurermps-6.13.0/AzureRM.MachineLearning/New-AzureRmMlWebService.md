---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/new-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
ms.openlocfilehash: 23797a0137b8444e1e7db4d2256ced290ca919f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734360"
---
# <span data-ttu-id="5e178-101">New-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="5e178-101">New-AzureRmMlWebService</span></span>

## <span data-ttu-id="5e178-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e178-102">SYNOPSIS</span></span>
<span data-ttu-id="5e178-103">Создание новой веб-службы.</span><span class="sxs-lookup"><span data-stu-id="5e178-103">Creates a new web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e178-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e178-104">SYNTAX</span></span>

### <span data-ttu-id="5e178-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="5e178-105">CreateFromFile</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e178-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="5e178-106">CreateFromInstance</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e178-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e178-107">DESCRIPTION</span></span>
<span data-ttu-id="5e178-108">Создание веб-службы машинного обучения Azure в существующей группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5e178-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="5e178-109">Если в группе ресурсов есть веб-служба с таким же именем, вызов выполняет операцию обновления, и существующая веб-служба перезаписывается.</span><span class="sxs-lookup"><span data-stu-id="5e178-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="5e178-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e178-110">EXAMPLES</span></span>

### <span data-ttu-id="5e178-111">Пример 1: создание новой службы из определения на основе JSON-файла</span><span class="sxs-lookup"><span data-stu-id="5e178-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="5e178-112">Создание новой веб-службы машинного обучения Azure с именем "mywebservicename" в группе "myresourcegroup" и в Южной Центральной области США в соответствии с определением, представленным в JSON-файле, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="5e178-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="5e178-113">Пример 2: создание новой службы из экземпляра объекта</span><span class="sxs-lookup"><span data-stu-id="5e178-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="5e178-114">Вы можете получить экземпляр объекта веб-службы для настройки перед публикацией как ресурс с помощью командлета Import-AzureRmMlWebService.</span><span class="sxs-lookup"><span data-stu-id="5e178-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="5e178-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e178-115">PARAMETERS</span></span>

### <span data-ttu-id="5e178-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e178-116">-DefaultProfile</span></span>
<span data-ttu-id="5e178-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5e178-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e178-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="5e178-118">-DefinitionFile</span></span>
<span data-ttu-id="5e178-119">Specifes путь к файлу, содержащему определение формата JSON для веб-службы.</span><span class="sxs-lookup"><span data-stu-id="5e178-119">Specifes the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="5e178-120">Последнюю спецификацию для определения веб-службы можно найти в спецификации Swagger ниже https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="5e178-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

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

### <span data-ttu-id="5e178-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5e178-121">-Force</span></span>
<span data-ttu-id="5e178-122">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="5e178-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5e178-123">-Location</span><span class="sxs-lookup"><span data-stu-id="5e178-123">-Location</span></span>
<span data-ttu-id="5e178-124">Область веб-службы.</span><span class="sxs-lookup"><span data-stu-id="5e178-124">The region of the web service.</span></span>
<span data-ttu-id="5e178-125">Введите регион центра обработки данных Azure, например "Западная часть США" или "Юго-Тихоокеанский регион".</span><span class="sxs-lookup"><span data-stu-id="5e178-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="5e178-126">Вы можете разместить веб-службу в любом регионе, поддерживающем ресурсы такого типа.</span><span class="sxs-lookup"><span data-stu-id="5e178-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="5e178-127">Веб-служба не должна находиться в той же области, что и у подписки Azure, или в той же области, что и ее группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5e178-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="5e178-128">Группы ресурсов могут содержать веб-службы из разных регионов.</span><span class="sxs-lookup"><span data-stu-id="5e178-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="5e178-129">Чтобы определить, какие области поддерживают каждый тип ресурсов, используйте Get-AzureRmResourceProvider с командлетом параметра ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="5e178-129">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="5e178-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5e178-130">-Name</span></span>
<span data-ttu-id="5e178-131">Имя веб-службы.</span><span class="sxs-lookup"><span data-stu-id="5e178-131">The name for the web service.</span></span>
<span data-ttu-id="5e178-132">Имя должно быть уникальным в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5e178-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="5e178-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="5e178-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="5e178-134">Определение новой веб-службы, содержащее все свойства, составляющие службу.</span><span class="sxs-lookup"><span data-stu-id="5e178-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="5e178-135">Этот параметр является обязательным и представляет экземпляр класса Microsoft. Azure. Management. MachineLearning. WebService. WebService.</span><span class="sxs-lookup"><span data-stu-id="5e178-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="5e178-136">Последнюю спецификацию для определения веб-службы можно найти в спецификации Swagger ниже https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="5e178-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

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

### <span data-ttu-id="5e178-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e178-137">-ResourceGroupName</span></span>
<span data-ttu-id="5e178-138">Группа ресурсов, в которую нужно поместить веб-службу.</span><span class="sxs-lookup"><span data-stu-id="5e178-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="5e178-139">Введите регион центра обработки данных Azure, например "Западная часть США" или "Юго-Тихоокеанский регион".</span><span class="sxs-lookup"><span data-stu-id="5e178-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="5e178-140">Вы можете разместить веб-службу в любом регионе, поддерживающем ресурсы такого типа.</span><span class="sxs-lookup"><span data-stu-id="5e178-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="5e178-141">Веб-служба не должна находиться в той же области, что и у подписки Azure, или в той же области, что и ее группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5e178-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="5e178-142">Группы ресурсов могут содержать веб-службы из разных регионов.</span><span class="sxs-lookup"><span data-stu-id="5e178-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="5e178-143">Чтобы определить, какие области поддерживают каждый тип ресурсов, используйте Get-AzureRmResourceProvider с командлетом параметра ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="5e178-143">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="5e178-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e178-144">-Confirm</span></span>
<span data-ttu-id="5e178-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5e178-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e178-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e178-146">-WhatIf</span></span>
<span data-ttu-id="5e178-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5e178-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e178-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5e178-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e178-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e178-149">CommonParameters</span></span>
<span data-ttu-id="5e178-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e178-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e178-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e178-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e178-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e178-152">INPUTS</span></span>

### <span data-ttu-id="5e178-153">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="5e178-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="5e178-154">Параметры: NewWebServiceDefinition (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5e178-154">Parameters: NewWebServiceDefinition (ByValue)</span></span>

## <span data-ttu-id="5e178-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e178-155">OUTPUTS</span></span>

### <span data-ttu-id="5e178-156">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="5e178-156">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="5e178-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e178-157">NOTES</span></span>
<span data-ttu-id="5e178-158">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="5e178-158">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="5e178-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e178-159">RELATED LINKS</span></span>
