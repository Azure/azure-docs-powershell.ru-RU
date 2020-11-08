---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
ms.openlocfilehash: a2d55c831860f5664f0f8f3dd5312368a9e5da4d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065947"
---
# <span data-ttu-id="fd8ce-101">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="fd8ce-101">New-AzContainerServiceConfig</span></span>

## <span data-ttu-id="fd8ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd8ce-102">SYNOPSIS</span></span>
<span data-ttu-id="fd8ce-103">Создает локальный объект конфигурации для службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-103">Creates a local configuration object for a container service.</span></span>

## <span data-ttu-id="fd8ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd8ce-104">SYNTAX</span></span>

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

## <span data-ttu-id="fd8ce-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd8ce-105">DESCRIPTION</span></span>
<span data-ttu-id="fd8ce-106">Командлет **New-AzContainerServiceConfig** создает объект локальной конфигурации для службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-106">The **New-AzContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="fd8ce-107">Предоставьте этот объект командлету New-AzContainerService, чтобы создать службу контейнера.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-107">Provide this object to the New-AzContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="fd8ce-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd8ce-108">EXAMPLES</span></span>

### <span data-ttu-id="fd8ce-109">Пример 1: создание конфигурации службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="fd8ce-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="fd8ce-110">Эта команда создает контейнер и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="fd8ce-111">Команда определяет различные параметры конфигурации службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="fd8ce-112">Команда передает объект конфигурации в командлет Add-AzContainerServiceAgentPoolProfile с помощью оператора Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-112">The command passes the configuration object to the Add-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="fd8ce-113">Этот командлет добавляет профиль пула агентов.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="fd8ce-114">Укажите объект в $Container для параметра *ContainerService* **New-AzContainerService**.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzContainerService**.</span></span>

## <span data-ttu-id="fd8ce-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd8ce-115">PARAMETERS</span></span>

### <span data-ttu-id="fd8ce-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="fd8ce-116">-AdminUsername</span></span>
<span data-ttu-id="fd8ce-117">Указывает имя учетной записи администратора, которая будет использоваться для службы контейнеров на базе Linux.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="fd8ce-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="fd8ce-118">-AgentPoolProfile</span></span>
<span data-ttu-id="fd8ce-119">Указывает массив объектов профиля группы агента для службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="fd8ce-120">Добавьте профиль с помощью командлета Add-AzContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-120">Add a profile by using the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="fd8ce-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="fd8ce-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="fd8ce-122">Задает настраиваемую Orchestrator Profile.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="fd8ce-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd8ce-123">-DefaultProfile</span></span>
<span data-ttu-id="fd8ce-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd8ce-125">-Location</span><span class="sxs-lookup"><span data-stu-id="fd8ce-125">-Location</span></span>
<span data-ttu-id="fd8ce-126">Указывает расположение для создания службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-126">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="fd8ce-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="fd8ce-127">-MasterCount</span></span>
<span data-ttu-id="fd8ce-128">Задает количество создаваемых эталонных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-128">Specifies the number of master virtual machines to create.</span></span>

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

### <span data-ttu-id="fd8ce-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="fd8ce-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="fd8ce-130">Задает префикс DNS для основной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="fd8ce-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="fd8ce-131">-OrchestratorType</span></span>
<span data-ttu-id="fd8ce-132">Указывает тип Orchestrator для службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="fd8ce-133">Допустимые значения этого параметра: DCOS и Swarm.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="fd8ce-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="fd8ce-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="fd8ce-135">Указывает идентификатор клиента для профиля участника.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="fd8ce-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="fd8ce-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="fd8ce-137">Указывает секретный профиль участника.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="fd8ce-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="fd8ce-138">-SshPublicKey</span></span>
<span data-ttu-id="fd8ce-139">Указывает открытый ключ SSH для службы контейнера на основе Linux.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-139">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="fd8ce-140">-Тег</span><span class="sxs-lookup"><span data-stu-id="fd8ce-140">-Tag</span></span>
<span data-ttu-id="fd8ce-141">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fd8ce-142">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="fd8ce-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fd8ce-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="fd8ce-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="fd8ce-144">Указывает, включает ли эта конфигурация диагностику для виртуальной машины службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="fd8ce-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="fd8ce-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="fd8ce-146">Указывает пароль администратора для службы контейнеров, использующей операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="fd8ce-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="fd8ce-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="fd8ce-148">Указывает имя пользователя администратора для службы контейнеров, использующей операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="fd8ce-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd8ce-149">-Confirm</span></span>
<span data-ttu-id="fd8ce-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd8ce-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd8ce-151">-WhatIf</span></span>
<span data-ttu-id="fd8ce-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd8ce-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd8ce-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd8ce-154">CommonParameters</span></span>
<span data-ttu-id="fd8ce-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd8ce-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd8ce-156">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd8ce-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd8ce-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd8ce-157">INPUTS</span></span>

### <span data-ttu-id="fd8ce-158">System. String</span><span class="sxs-lookup"><span data-stu-id="fd8ce-158">System.String</span></span>

### <span data-ttu-id="fd8ce-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fd8ce-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fd8ce-160">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. ContainerServiceOrchestratorTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="fd8ce-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="fd8ce-161">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fd8ce-161">System.Int32</span></span>

### <span data-ttu-id="fd8ce-162">Microsoft. Azure. Management. COMPUTE. Models. ContainerServiceAgentPoolProfile []</span><span class="sxs-lookup"><span data-stu-id="fd8ce-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="fd8ce-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="fd8ce-163">System.String[]</span></span>

### <span data-ttu-id="fd8ce-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd8ce-164">System.Boolean</span></span>

## <span data-ttu-id="fd8ce-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd8ce-165">OUTPUTS</span></span>

### <span data-ttu-id="fd8ce-166">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="fd8ce-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="fd8ce-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd8ce-167">NOTES</span></span>

## <span data-ttu-id="fd8ce-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd8ce-168">RELATED LINKS</span></span>

[<span data-ttu-id="fd8ce-169">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="fd8ce-169">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="fd8ce-170">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="fd8ce-170">New-AzContainerService</span></span>](./New-AzContainerService.md)
