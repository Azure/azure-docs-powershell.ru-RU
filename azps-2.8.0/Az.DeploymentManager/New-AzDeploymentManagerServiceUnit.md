---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 3ae1aeb86e96bc3f37142e03c31cebbcf102ad3c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721129"
---
# <span data-ttu-id="257c6-101">New-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="257c6-101">New-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="257c6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="257c6-102">SYNOPSIS</span></span>
<span data-ttu-id="257c6-103">Создает модуль обслуживания для заданной топологии служб и служб.</span><span class="sxs-lookup"><span data-stu-id="257c6-103">Creates a service unit under the specified service and service topology.</span></span>

## <span data-ttu-id="257c6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="257c6-104">SYNTAX</span></span>

### <span data-ttu-id="257c6-105">ByTopologyAndServiceNames (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="257c6-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="257c6-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="257c6-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="257c6-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="257c6-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="257c6-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="257c6-108">ByServiceObject</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceObject] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="257c6-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="257c6-109">ByServiceResourceId</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="257c6-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="257c6-110">DESCRIPTION</span></span>
<span data-ttu-id="257c6-111">Командлет **New-AzDeploymentManagerServiceUnit** создает службу в рамках службы в топологии службы и возвращает объект, который представляет этот модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="257c6-111">The **New-AzDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="257c6-112">Укажите единицу обслуживания, указав ее имя, имя службы, топологию службы и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="257c6-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="257c6-113">Командлет возвращает объект ServiceUnit.</span><span class="sxs-lookup"><span data-stu-id="257c6-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="257c6-114">Вы можете локально изменить этот объект, а затем применить изменения к службе с помощью командлета Set-AzDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="257c6-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="257c6-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="257c6-115">EXAMPLES</span></span>

### <span data-ttu-id="257c6-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="257c6-116">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="257c6-117">Этот командлет создает новый модуль служб с именем ContosoService2Storage в ContosoResourceGroup в разделе Service ContosoService2 в топологии ContosoServiceTopology в главном регионе США.</span><span class="sxs-lookup"><span data-stu-id="257c6-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="257c6-118">Файлы шаблона и параметров определяются как относительные пути к источнику артефактов, на который ссылается топология службы ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="257c6-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="257c6-119">Ресурсы, определенные в этом шаблоне, развертываются в целевую группу ресурсов service2ResourceGroup, если для режима развертывания задано значение инкремент.</span><span class="sxs-lookup"><span data-stu-id="257c6-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="257c6-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="257c6-120">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="257c6-121">Этот командлет создает новый модуль служб с именем ContosoService2Storage в ContosoResourceGroup в разделе Service ContosoService2 в топологии ContosoServiceTopology в главном регионе США.</span><span class="sxs-lookup"><span data-stu-id="257c6-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="257c6-122">Ссылки на шаблон и параметры указаны в качестве идентификатора URI SAS как источника артефактов, не предоставленных в ContosoServiceTopology1 топологии служб.</span><span class="sxs-lookup"><span data-stu-id="257c6-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="257c6-123">Ресурсы, определенные в этом шаблоне, развертываются в целевую группу ресурсов, service2ResourceGroup с установленным режимом развертывания.</span><span class="sxs-lookup"><span data-stu-id="257c6-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="257c6-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="257c6-124">PARAMETERS</span></span>

### <span data-ttu-id="257c6-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="257c6-125">-AsJob</span></span>
<span data-ttu-id="257c6-126">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="257c6-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="257c6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="257c6-127">-DefaultProfile</span></span>
<span data-ttu-id="257c6-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="257c6-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="257c6-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="257c6-129">-DeploymentMode</span></span>
<span data-ttu-id="257c6-130">Режим развертывания, который необходимо использовать при развертывании ресурсов в единицах обслуживания.</span><span class="sxs-lookup"><span data-stu-id="257c6-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257c6-131">-Location</span><span class="sxs-lookup"><span data-stu-id="257c6-131">-Location</span></span>
<span data-ttu-id="257c6-132">Расположение ресурса единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="257c6-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="257c6-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="257c6-133">-Name</span></span>
<span data-ttu-id="257c6-134">Название единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="257c6-134">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257c6-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="257c6-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="257c6-136">Путь к файлу параметров относительно источника артефакта.</span><span class="sxs-lookup"><span data-stu-id="257c6-136">The path to the parameters file relative to the artifact source.</span></span>
<span data-ttu-id="257c6-137">Требуется ссылка на ArtifactSource в ServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="257c6-137">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257c6-138">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="257c6-138">-ParametersUri</span></span>
<span data-ttu-id="257c6-139">Универсальный код ресурса (URI) SAS в файл параметров.</span><span class="sxs-lookup"><span data-stu-id="257c6-139">The SAS Uri to the parameters file.</span></span>
<span data-ttu-id="257c6-140">Если ссылка на ArtifactSourceId указана в ServiceTopology, укажите относительный путь с помощью ParametersArtifactSourceRelativePath.</span><span class="sxs-lookup"><span data-stu-id="257c6-140">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using ParametersArtifactSourceRelativePath.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257c6-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="257c6-141">-ResourceGroupName</span></span>
<span data-ttu-id="257c6-142">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="257c6-142">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257c6-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="257c6-143">-ServiceName</span></span>
<span data-ttu-id="257c6-144">Имя службы, частью которой является этот модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="257c6-144">The name of the service this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257c6-145">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="257c6-145">-ServiceObject</span></span>
<span data-ttu-id="257c6-146">Объект обслуживания, для которого необходимо создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="257c6-146">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257c6-147">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="257c6-147">-ServiceResourceId</span></span>
<span data-ttu-id="257c6-148">Идентификатор ресурса службы, в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="257c6-148">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257c6-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="257c6-149">-ServiceTopologyName</span></span>
<span data-ttu-id="257c6-150">Имя топологии службы, частью которой является этот модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="257c6-150">The name of the service topology this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257c6-151">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="257c6-151">-ServiceTopologyObject</span></span>
<span data-ttu-id="257c6-152">Объект Topology (топология службы), в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="257c6-152">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257c6-153">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="257c6-153">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="257c6-154">Идентификатор ресурса топологии служб, в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="257c6-154">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257c6-155">-Тег</span><span class="sxs-lookup"><span data-stu-id="257c6-155">-Tag</span></span>
<span data-ttu-id="257c6-156">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="257c6-156">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="257c6-157">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="257c6-157">-TargetResourceGroup</span></span>
<span data-ttu-id="257c6-158">Определяет расположение, в которое должны развертываться ресурсы в рамках сервисного модуля.</span><span class="sxs-lookup"><span data-stu-id="257c6-158">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="257c6-159">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="257c6-159">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="257c6-160">Путь к файлу шаблона по отношению к источнику артефакта.</span><span class="sxs-lookup"><span data-stu-id="257c6-160">The path to the template file relative to the artifact source.</span></span>
<span data-ttu-id="257c6-161">Требуется ссылка на ArtifactSource в ServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="257c6-161">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257c6-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="257c6-162">-TemplateUri</span></span>
<span data-ttu-id="257c6-163">Универсальный код ресурса (URI) SAS в файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="257c6-163">The SAS Uri to the template file.</span></span>
<span data-ttu-id="257c6-164">Если ссылка на ArtifactSourceId указана в ServiceTopology, укажите относительный путь с помощью TemplateArtifactSourceRelativePath.</span><span class="sxs-lookup"><span data-stu-id="257c6-164">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using TemplateArtifactSourceRelativePath.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257c6-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="257c6-165">-Confirm</span></span>
<span data-ttu-id="257c6-166">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="257c6-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="257c6-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="257c6-167">-WhatIf</span></span>
<span data-ttu-id="257c6-168">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="257c6-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="257c6-169">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="257c6-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="257c6-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="257c6-170">CommonParameters</span></span>
<span data-ttu-id="257c6-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="257c6-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="257c6-172">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="257c6-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="257c6-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="257c6-173">INPUTS</span></span>

### <span data-ttu-id="257c6-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="257c6-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="257c6-175">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="257c6-175">OUTPUTS</span></span>

### <span data-ttu-id="257c6-176">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="257c6-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="257c6-177">Пуск</span><span class="sxs-lookup"><span data-stu-id="257c6-177">NOTES</span></span>

## <span data-ttu-id="257c6-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="257c6-178">RELATED LINKS</span></span>
