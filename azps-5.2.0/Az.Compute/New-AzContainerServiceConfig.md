---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
ms.openlocfilehash: a2d55c831860f5664f0f8f3dd5312368a9e5da4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403956"
---
# <span data-ttu-id="95267-101">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="95267-101">New-AzContainerServiceConfig</span></span>

## <span data-ttu-id="95267-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95267-102">SYNOPSIS</span></span>
<span data-ttu-id="95267-103">Создает объект локальной конфигурации для службы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="95267-103">Creates a local configuration object for a container service.</span></span>

## <span data-ttu-id="95267-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="95267-104">SYNTAX</span></span>

```
New-AzContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="95267-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95267-105">DESCRIPTION</span></span>
<span data-ttu-id="95267-106">**Из-за cmdlet New-AzContainerServiceConfig** создается объект локальной конфигурации для службы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="95267-106">The **New-AzContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="95267-107">Чтобы создать службу контейнера, New-AzContainerService этому объекту в New-AzContainerService.</span><span class="sxs-lookup"><span data-stu-id="95267-107">Provide this object to the New-AzContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="95267-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="95267-108">EXAMPLES</span></span>

### <span data-ttu-id="95267-109">Пример 1. Создание конфигурации службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="95267-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="95267-110">Эта команда создает контейнер, а затем сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="95267-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="95267-111">Команда определяет различные параметры конфигурации службы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="95267-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="95267-112">Команда передает объект конфигурации в командлет Add-AzContainerServiceAgentPoolProfile с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="95267-112">The command passes the configuration object to the Add-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="95267-113">Этот cmdlet добавляет профиль пула агентов.</span><span class="sxs-lookup"><span data-stu-id="95267-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="95267-114">Укажите объект в $Container *параметра ContainerService* **службы New-AzContainerService.**</span><span class="sxs-lookup"><span data-stu-id="95267-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzContainerService**.</span></span>

## <span data-ttu-id="95267-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95267-115">PARAMETERS</span></span>

### <span data-ttu-id="95267-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="95267-116">-AdminUsername</span></span>
<span data-ttu-id="95267-117">Указывает имя учетной записи администратора, используемой для службы контейнеров на базе Linux.</span><span class="sxs-lookup"><span data-stu-id="95267-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95267-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="95267-118">-AgentPoolProfile</span></span>
<span data-ttu-id="95267-119">Указывает массив объектов профиля пула агентов для службы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="95267-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="95267-120">Добавьте профиль с помощью Add-AzContainerServiceAgentPoolProfile управления.</span><span class="sxs-lookup"><span data-stu-id="95267-120">Add a profile by using the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95267-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="95267-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="95267-122">Указывает настраиваемый химятор профиля.</span><span class="sxs-lookup"><span data-stu-id="95267-122">Specifies the custom profile orchestrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95267-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95267-123">-DefaultProfile</span></span>
<span data-ttu-id="95267-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95267-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95267-125">-Location</span><span class="sxs-lookup"><span data-stu-id="95267-125">-Location</span></span>
<span data-ttu-id="95267-126">Определяет место, в котором нужно создать службу контейнера.</span><span class="sxs-lookup"><span data-stu-id="95267-126">Specifies the location in which to create the container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95267-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="95267-127">-MasterCount</span></span>
<span data-ttu-id="95267-128">Количество виртуальных машин, которые нужно создать.</span><span class="sxs-lookup"><span data-stu-id="95267-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95267-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="95267-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="95267-130">Указывает префикс DNS для этакого виртуального компьютера.</span><span class="sxs-lookup"><span data-stu-id="95267-130">Specifies the DNS prefix for the master virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95267-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="95267-131">-OrchestratorType</span></span>
<span data-ttu-id="95267-132">Определяет тип двектора для службы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="95267-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="95267-133">Допустимыми значениями для этого параметра являются DCOS и Swarm.</span><span class="sxs-lookup"><span data-stu-id="95267-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Swarm, DCOS, Custom, Kubernetes

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95267-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="95267-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="95267-135">Определяет ИД клиента основного профиля.</span><span class="sxs-lookup"><span data-stu-id="95267-135">Specifies the principal profile client ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95267-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="95267-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="95267-137">Указывает секрет основного профиля.</span><span class="sxs-lookup"><span data-stu-id="95267-137">Specifies the principal profile secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95267-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="95267-138">-SshPublicKey</span></span>
<span data-ttu-id="95267-139">Указывает общедоступный ключ SSH для службы контейнеров на базе Linux.</span><span class="sxs-lookup"><span data-stu-id="95267-139">Specifies the SSH public key for a Linux-based container service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95267-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="95267-140">-Tag</span></span>
<span data-ttu-id="95267-141">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="95267-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="95267-142">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="95267-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95267-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="95267-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="95267-144">Указывает, включает ли эта конфигурация диагностику для виртуальной машины службы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="95267-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95267-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="95267-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="95267-146">Указывает пароль администратора для службы контейнеров, использующей операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="95267-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95267-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="95267-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="95267-148">Указывает имя пользователя администратора для службы контейнеров, использующей операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="95267-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95267-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95267-149">-Confirm</span></span>
<span data-ttu-id="95267-150">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="95267-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95267-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95267-151">-WhatIf</span></span>
<span data-ttu-id="95267-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95267-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95267-153">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="95267-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95267-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95267-154">CommonParameters</span></span>
<span data-ttu-id="95267-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95267-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95267-156">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95267-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95267-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95267-157">INPUTS</span></span>

### <span data-ttu-id="95267-158">System.String</span><span class="sxs-lookup"><span data-stu-id="95267-158">System.String</span></span>

### <span data-ttu-id="95267-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="95267-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="95267-160">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="95267-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="95267-161">System.Int32</span><span class="sxs-lookup"><span data-stu-id="95267-161">System.Int32</span></span>

### <span data-ttu-id="95267-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span><span class="sxs-lookup"><span data-stu-id="95267-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="95267-163">System.String[]</span><span class="sxs-lookup"><span data-stu-id="95267-163">System.String[]</span></span>

### <span data-ttu-id="95267-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="95267-164">System.Boolean</span></span>

## <span data-ttu-id="95267-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="95267-165">OUTPUTS</span></span>

### <span data-ttu-id="95267-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="95267-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="95267-167">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="95267-167">NOTES</span></span>

## <span data-ttu-id="95267-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95267-168">RELATED LINKS</span></span>

[<span data-ttu-id="95267-169">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="95267-169">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="95267-170">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="95267-170">New-AzContainerService</span></span>](./New-AzContainerService.md)
