---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 9a03dd861ee380b0ab01348e01091844240bfc04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242696"
---
# <span data-ttu-id="219c1-101">New-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="219c1-101">New-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="219c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="219c1-102">SYNOPSIS</span></span>
<span data-ttu-id="219c1-103">Создает единицу обслуживания в соответствии с указанной топологией службы и службы.</span><span class="sxs-lookup"><span data-stu-id="219c1-103">Creates a service unit under the specified service and service topology.</span></span>

## <span data-ttu-id="219c1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="219c1-104">SYNTAX</span></span>

### <span data-ttu-id="219c1-105">ByTopologyAndServiceNames (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="219c1-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="219c1-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="219c1-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="219c1-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="219c1-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="219c1-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="219c1-108">ByServiceObject</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceObject] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="219c1-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="219c1-109">ByServiceResourceId</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="219c1-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="219c1-110">DESCRIPTION</span></span>
<span data-ttu-id="219c1-111">**Cmdlet New-AzDeploymentManagerServiceUnit** создает службу для службы в топологии службы и возвращает объект, который представляет ее.</span><span class="sxs-lookup"><span data-stu-id="219c1-111">The **New-AzDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="219c1-112">Укажите единицу обслуживания по имени, названию службы, топологии службы и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="219c1-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="219c1-113">Этот cmdlet возвращает объект ServiceUnit.</span><span class="sxs-lookup"><span data-stu-id="219c1-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="219c1-114">Вы можете изменить этот объект локально, а затем применить изменения к службе с помощью Set-AzDeploymentManagerService-управления.</span><span class="sxs-lookup"><span data-stu-id="219c1-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="219c1-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="219c1-115">EXAMPLES</span></span>

### <span data-ttu-id="219c1-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="219c1-116">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="219c1-117">Этот cmdlet создает новый блок службы с именем ContosoService2Storage в contosoResourceGroup в службе ContosoService2 в топологии ContosoServiceTopology, расположенной в центральной части США.</span><span class="sxs-lookup"><span data-stu-id="219c1-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="219c1-118">Файлы шаблона и параметров определяются как относительные пути к источнику артефакта, на который ссылается топология ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="219c1-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="219c1-119">Ресурсы, определенные в этом шаблоне, должны быть развернуты в целевой группе ресурсов service2ResourceGroup, в режиме развертывания установлено значение "Приращение".</span><span class="sxs-lookup"><span data-stu-id="219c1-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="219c1-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="219c1-120">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="219c1-121">Этот cmdlet создает новый блок службы с именем ContosoService2Storage в contosoResourceGroup в службе ContosoService2 в топологии ContosoServiceTopology, расположенной в центральной части США.</span><span class="sxs-lookup"><span data-stu-id="219c1-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="219c1-122">Ссылки на шаблон и параметры uri в качестве источника ресурсов SAS не предоставляются в топологии ContosoServiceTopology1.</span><span class="sxs-lookup"><span data-stu-id="219c1-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="219c1-123">Ресурсы, определенные в этом шаблоне, будут развернуты в целевой группе ресурсов service2ResourceGroup в режиме развертывания Complete.</span><span class="sxs-lookup"><span data-stu-id="219c1-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="219c1-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="219c1-124">PARAMETERS</span></span>

### <span data-ttu-id="219c1-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="219c1-125">-AsJob</span></span>
<span data-ttu-id="219c1-126">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="219c1-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="219c1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="219c1-127">-DefaultProfile</span></span>
<span data-ttu-id="219c1-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="219c1-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="219c1-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="219c1-129">-DeploymentMode</span></span>
<span data-ttu-id="219c1-130">Режим развертывания, который используется при развертывании ресурсов в единицах обслуживания.</span><span class="sxs-lookup"><span data-stu-id="219c1-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="219c1-131">-Location</span><span class="sxs-lookup"><span data-stu-id="219c1-131">-Location</span></span>
<span data-ttu-id="219c1-132">Расположение ресурса единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="219c1-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="219c1-133">-Name</span><span class="sxs-lookup"><span data-stu-id="219c1-133">-Name</span></span>
<span data-ttu-id="219c1-134">Название единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="219c1-134">The name of the service unit.</span></span>

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

### <span data-ttu-id="219c1-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="219c1-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="219c1-136">Путь к файлу параметров относительно источника артефакта.</span><span class="sxs-lookup"><span data-stu-id="219c1-136">The path to the parameters file relative to the artifact source.</span></span>
<span data-ttu-id="219c1-137">Требует ссылку на источник артефактов в службе(Topology).</span><span class="sxs-lookup"><span data-stu-id="219c1-137">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="219c1-138">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="219c1-138">-ParametersUri</span></span>
<span data-ttu-id="219c1-139">Uri SAS в файле параметров.</span><span class="sxs-lookup"><span data-stu-id="219c1-139">The SAS Uri to the parameters file.</span></span>
<span data-ttu-id="219c1-140">Если ссылка на артефактSourceId указана в параметрах ServiceTopology, укажите относительный путь с помощью ParametersArtifactSourceRelativePath.</span><span class="sxs-lookup"><span data-stu-id="219c1-140">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using ParametersArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="219c1-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="219c1-141">-ResourceGroupName</span></span>
<span data-ttu-id="219c1-142">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="219c1-142">The resource group.</span></span>

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

### <span data-ttu-id="219c1-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="219c1-143">-ServiceName</span></span>
<span data-ttu-id="219c1-144">Название службы, в состав которого входит данный блок обслуживания.</span><span class="sxs-lookup"><span data-stu-id="219c1-144">The name of the service this service unit is a part of.</span></span>

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

### <span data-ttu-id="219c1-145">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="219c1-145">-ServiceObject</span></span>
<span data-ttu-id="219c1-146">Объект-служба, в котором нужно создать единицу обслуживания.</span><span class="sxs-lookup"><span data-stu-id="219c1-146">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="219c1-147">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="219c1-147">-ServiceResourceId</span></span>
<span data-ttu-id="219c1-148">Идентификатор ресурса службы, в котором нужно создать единицу обслуживания.</span><span class="sxs-lookup"><span data-stu-id="219c1-148">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="219c1-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="219c1-149">-ServiceTopologyName</span></span>
<span data-ttu-id="219c1-150">Имя топологии службы, частью которого является этот блок службы.</span><span class="sxs-lookup"><span data-stu-id="219c1-150">The name of the service topology this service unit is a part of.</span></span>

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

### <span data-ttu-id="219c1-151">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="219c1-151">-ServiceTopologyObject</span></span>
<span data-ttu-id="219c1-152">Объект топологии службы, в котором нужно создать единицу обслуживания.</span><span class="sxs-lookup"><span data-stu-id="219c1-152">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="219c1-153">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="219c1-153">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="219c1-154">Идентификатор ресурса топологии службы, в котором нужно создать единицу обслуживания.</span><span class="sxs-lookup"><span data-stu-id="219c1-154">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="219c1-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="219c1-155">-Tag</span></span>
<span data-ttu-id="219c1-156">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="219c1-156">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="219c1-157">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="219c1-157">-TargetResourceGroup</span></span>
<span data-ttu-id="219c1-158">Определяет место, в котором будут развернуты ресурсы из блока обслуживания.</span><span class="sxs-lookup"><span data-stu-id="219c1-158">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="219c1-159">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="219c1-159">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="219c1-160">Путь к файлу шаблона относительно источника артефакта.</span><span class="sxs-lookup"><span data-stu-id="219c1-160">The path to the template file relative to the artifact source.</span></span>
<span data-ttu-id="219c1-161">Требует ссылку на источник артефактов в службе(Topology).</span><span class="sxs-lookup"><span data-stu-id="219c1-161">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="219c1-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="219c1-162">-TemplateUri</span></span>
<span data-ttu-id="219c1-163">Uri SAS в файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="219c1-163">The SAS Uri to the template file.</span></span>
<span data-ttu-id="219c1-164">Если ссылка на артефактSourceId была указана в окне ServiceTopology, укажите относительный путь с помощью TemplateArtifactSourceRelativePath.</span><span class="sxs-lookup"><span data-stu-id="219c1-164">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using TemplateArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="219c1-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="219c1-165">-Confirm</span></span>
<span data-ttu-id="219c1-166">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="219c1-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="219c1-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="219c1-167">-WhatIf</span></span>
<span data-ttu-id="219c1-168">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="219c1-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="219c1-169">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="219c1-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="219c1-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="219c1-170">CommonParameters</span></span>
<span data-ttu-id="219c1-171">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="219c1-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="219c1-172">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="219c1-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="219c1-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="219c1-173">INPUTS</span></span>

### <span data-ttu-id="219c1-174">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="219c1-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="219c1-175">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="219c1-175">OUTPUTS</span></span>

### <span data-ttu-id="219c1-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="219c1-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="219c1-177">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="219c1-177">NOTES</span></span>

## <span data-ttu-id="219c1-178">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="219c1-178">RELATED LINKS</span></span>
