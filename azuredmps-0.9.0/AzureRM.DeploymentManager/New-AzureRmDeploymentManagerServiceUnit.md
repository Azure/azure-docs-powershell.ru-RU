---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: e732463984088bbcb507eb55594f7de2114d25d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555319"
---
# <span data-ttu-id="ed645-101">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="ed645-101">New-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="ed645-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed645-102">SYNOPSIS</span></span>
<span data-ttu-id="ed645-103">Создает новый модуль обслуживания для службы в топологии службы.</span><span class="sxs-lookup"><span data-stu-id="ed645-103">Creates a new service unit under a service in a service topology.</span></span>

## <span data-ttu-id="ed645-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed645-104">SYNTAX</span></span>

### <span data-ttu-id="ed645-105">ByTopologyAndServiceNames (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed645-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed645-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="ed645-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopology] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed645-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="ed645-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed645-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="ed645-108">ByServiceObject</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-Service] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed645-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="ed645-109">ByServiceResourceId</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed645-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed645-110">DESCRIPTION</span></span>
<span data-ttu-id="ed645-111">Командлет **New-AzureRmDeploymentManagerServiceUnit** создает службу в рамках службы в топологии службы и возвращает объект, который представляет этот модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ed645-111">The **New-AzureRmDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="ed645-112">Укажите единицу обслуживания, указав ее имя, имя службы, топологию службы и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ed645-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="ed645-113">Командлет возвращает объект ServiceUnit.</span><span class="sxs-lookup"><span data-stu-id="ed645-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="ed645-114">Вы можете локально изменить этот объект, а затем применить изменения к службе с помощью командлета Set-AzureRmDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="ed645-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="ed645-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed645-115">EXAMPLES</span></span>

### <span data-ttu-id="ed645-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ed645-116">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="ed645-117">Этот командлет создает новый модуль служб с именем ContosoService2Storage в ContosoResourceGroup в разделе Service ContosoService2 в топологии ContosoServiceTopology в главном регионе США.</span><span class="sxs-lookup"><span data-stu-id="ed645-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="ed645-118">Файлы шаблона и параметров определяются как относительные пути к источнику артефактов, на который ссылается топология службы ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="ed645-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="ed645-119">Ресурсы, определенные в этом шаблоне, развертываются в целевую группу ресурсов service2ResourceGroup, если для режима развертывания задано значение инкремент.</span><span class="sxs-lookup"><span data-stu-id="ed645-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="ed645-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ed645-120">Example 2</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="ed645-121">Этот командлет создает новый модуль служб с именем ContosoService2Storage в ContosoResourceGroup в разделе Service ContosoService2 в топологии ContosoServiceTopology в главном регионе США.</span><span class="sxs-lookup"><span data-stu-id="ed645-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="ed645-122">Ссылки на шаблон и параметры указаны в качестве идентификатора URI SAS как источника артефактов, не предоставленных в ContosoServiceTopology1 топологии служб.</span><span class="sxs-lookup"><span data-stu-id="ed645-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="ed645-123">Ресурсы, определенные в этом шаблоне, развертываются в целевую группу ресурсов, service2ResourceGroup с установленным режимом развертывания.</span><span class="sxs-lookup"><span data-stu-id="ed645-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="ed645-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed645-124">PARAMETERS</span></span>

### <span data-ttu-id="ed645-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed645-125">-AsJob</span></span>
<span data-ttu-id="ed645-126">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ed645-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed645-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed645-127">-DefaultProfile</span></span>
<span data-ttu-id="ed645-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed645-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed645-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="ed645-129">-DeploymentMode</span></span>
<span data-ttu-id="ed645-130">Режим развертывания, который необходимо использовать при развертывании ресурсов в единицах обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ed645-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="ed645-131">-Location</span><span class="sxs-lookup"><span data-stu-id="ed645-131">-Location</span></span>
<span data-ttu-id="ed645-132">Расположение ресурса единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ed645-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="ed645-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ed645-133">-Name</span></span>
<span data-ttu-id="ed645-134">Название единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ed645-134">The name of the service unit.</span></span>

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

### <span data-ttu-id="ed645-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="ed645-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="ed645-136">Режим развертывания, который необходимо использовать при развертывании ресурсов в единицах обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ed645-136">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="ed645-137">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="ed645-137">-ParametersUri</span></span>
<span data-ttu-id="ed645-138">Режим развертывания, который необходимо использовать при развертывании ресурсов в единицах обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ed645-138">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="ed645-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed645-139">-ResourceGroupName</span></span>
<span data-ttu-id="ed645-140">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ed645-140">The resource group.</span></span>

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

### <span data-ttu-id="ed645-141">-Служба</span><span class="sxs-lookup"><span data-stu-id="ed645-141">-Service</span></span>
<span data-ttu-id="ed645-142">Объект обслуживания, для которого необходимо создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ed645-142">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="ed645-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ed645-143">-ServiceName</span></span>
<span data-ttu-id="ed645-144">Имя службы, частью которой является этот модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ed645-144">The name of the service this service unit is a part of.</span></span>

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

### <span data-ttu-id="ed645-145">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="ed645-145">-ServiceResourceId</span></span>
<span data-ttu-id="ed645-146">Идентификатор ресурса службы, в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ed645-146">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="ed645-147">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="ed645-147">-ServiceTopology</span></span>
<span data-ttu-id="ed645-148">Объект Topology (топология службы), в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ed645-148">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="ed645-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="ed645-149">-ServiceTopologyName</span></span>
<span data-ttu-id="ed645-150">Имя топологии службы, частью которой является этот модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ed645-150">The name of the serivce topology this service unit is a part of.</span></span>

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

### <span data-ttu-id="ed645-151">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="ed645-151">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="ed645-152">Идентификатор ресурса топологии служб, в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ed645-152">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="ed645-153">-Тег</span><span class="sxs-lookup"><span data-stu-id="ed645-153">-Tag</span></span>
<span data-ttu-id="ed645-154">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ed645-154">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="ed645-155">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ed645-155">-TargetResourceGroup</span></span>
<span data-ttu-id="ed645-156">Определяет расположение, в которое должны развертываться ресурсы в рамках сервисного модуля.</span><span class="sxs-lookup"><span data-stu-id="ed645-156">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="ed645-157">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="ed645-157">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="ed645-158">Режим развертывания, который необходимо использовать при развертывании ресурсов в единицах обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ed645-158">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="ed645-159">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="ed645-159">-TemplateUri</span></span>
<span data-ttu-id="ed645-160">Режим развертывания, который необходимо использовать при развертывании ресурсов в единицах обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ed645-160">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="ed645-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed645-161">-Confirm</span></span>
<span data-ttu-id="ed645-162">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ed645-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed645-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed645-163">-WhatIf</span></span>
<span data-ttu-id="ed645-164">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ed645-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed645-165">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ed645-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed645-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed645-166">CommonParameters</span></span>
<span data-ttu-id="ed645-167">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed645-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed645-168">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed645-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed645-169">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed645-169">INPUTS</span></span>

### <span data-ttu-id="ed645-170">Ничего</span><span class="sxs-lookup"><span data-stu-id="ed645-170">None</span></span>

## <span data-ttu-id="ed645-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed645-171">OUTPUTS</span></span>

### <span data-ttu-id="ed645-172">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="ed645-172">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="ed645-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed645-173">NOTES</span></span>

## <span data-ttu-id="ed645-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed645-174">RELATED LINKS</span></span>

[<span data-ttu-id="ed645-175">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="ed645-175">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Get-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="ed645-176">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="ed645-176">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="ed645-177">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="ed645-177">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)