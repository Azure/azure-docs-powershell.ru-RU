---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzContainerServiceConfig.md
ms.openlocfilehash: 4352edac7342bd421fb907295581aaa6bee8e8ef
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911478"
---
# <span data-ttu-id="45cab-101">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="45cab-101">New-AzContainerServiceConfig</span></span>

## <span data-ttu-id="45cab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45cab-102">SYNOPSIS</span></span>
<span data-ttu-id="45cab-103">Создает локальный объект конфигурации для службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="45cab-103">Creates a local configuration object for a container service.</span></span>

## <span data-ttu-id="45cab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45cab-104">SYNTAX</span></span>

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

## <span data-ttu-id="45cab-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45cab-105">DESCRIPTION</span></span>
<span data-ttu-id="45cab-106">Командлет **New-AzContainerServiceConfig** создает объект локальной конфигурации для службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="45cab-106">The **New-AzContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="45cab-107">Предоставьте этот объект командлету New-AzContainerService, чтобы создать службу контейнера.</span><span class="sxs-lookup"><span data-stu-id="45cab-107">Provide this object to the New-AzContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="45cab-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45cab-108">EXAMPLES</span></span>

### <span data-ttu-id="45cab-109">Пример 1: создание конфигурации службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="45cab-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="45cab-110">Эта команда создает контейнер и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="45cab-110">This command creates a container, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="45cab-111">Команда определяет различные параметры конфигурации службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="45cab-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="45cab-112">Команда передает объект конфигурации в командлет Add-AzContainerServiceAgentPoolProfile с помощью оператора Pipeline.</span><span class="sxs-lookup"><span data-stu-id="45cab-112">The command passes the configuration object to the Add-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="45cab-113">Этот командлет добавляет профиль пула агентов.</span><span class="sxs-lookup"><span data-stu-id="45cab-113">That cmdlet adds an agent pool profile.</span></span>

<span data-ttu-id="45cab-114">Укажите объект в $Container для параметра *ContainerService* **New-AzContainerService**.</span><span class="sxs-lookup"><span data-stu-id="45cab-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzContainerService**.</span></span>

## <span data-ttu-id="45cab-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45cab-115">PARAMETERS</span></span>

### <span data-ttu-id="45cab-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="45cab-116">-AdminUsername</span></span>
<span data-ttu-id="45cab-117">Указывает имя учетной записи администратора, которая будет использоваться для службы контейнеров на базе Linux.</span><span class="sxs-lookup"><span data-stu-id="45cab-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45cab-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="45cab-118">-AgentPoolProfile</span></span>
<span data-ttu-id="45cab-119">Указывает массив объектов профиля группы агента для службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="45cab-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="45cab-120">Добавьте профиль с помощью командлета Add-AzContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="45cab-120">Add a profile by using the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

```yaml
Type: ContainerServiceAgentPoolProfile[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45cab-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="45cab-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="45cab-122">Задает настраиваемую Orchestrator Profile.</span><span class="sxs-lookup"><span data-stu-id="45cab-122">Specifies the custom profile orchestrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45cab-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45cab-123">-DefaultProfile</span></span>
<span data-ttu-id="45cab-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45cab-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45cab-125">-Location</span><span class="sxs-lookup"><span data-stu-id="45cab-125">-Location</span></span>
<span data-ttu-id="45cab-126">Указывает расположение для создания службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="45cab-126">Specifies the location in which to create the container service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45cab-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="45cab-127">-MasterCount</span></span>
<span data-ttu-id="45cab-128">Задает количество создаваемых эталонных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="45cab-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45cab-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="45cab-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="45cab-130">Задает префикс DNS для основной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="45cab-130">Specifies the DNS prefix for the master virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45cab-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="45cab-131">-OrchestratorType</span></span>
<span data-ttu-id="45cab-132">Указывает тип Orchestrator для службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="45cab-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="45cab-133">Допустимые значения этого параметра: DCOS и Swarm.</span><span class="sxs-lookup"><span data-stu-id="45cab-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

```yaml
Type: ContainerServiceOrchestratorTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Swarm, DCOS, Custom, Kubernetes

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45cab-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="45cab-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="45cab-135">Указывает идентификатор клиента для профиля участника.</span><span class="sxs-lookup"><span data-stu-id="45cab-135">Specifies the principal profile client ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45cab-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="45cab-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="45cab-137">Указывает секретный профиль участника.</span><span class="sxs-lookup"><span data-stu-id="45cab-137">Specifies the principal profile secret.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45cab-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="45cab-138">-SshPublicKey</span></span>
<span data-ttu-id="45cab-139">Указывает открытый ключ SSH для службы контейнера на основе Linux.</span><span class="sxs-lookup"><span data-stu-id="45cab-139">Specifies the SSH public key for a Linux-based container service.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45cab-140">-Тег</span><span class="sxs-lookup"><span data-stu-id="45cab-140">-Tag</span></span>
<span data-ttu-id="45cab-141">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="45cab-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="45cab-142">Например:</span><span class="sxs-lookup"><span data-stu-id="45cab-142">For example:</span></span>

<span data-ttu-id="45cab-143">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="45cab-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45cab-144">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="45cab-144">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="45cab-145">Указывает, включает ли эта конфигурация диагностику для виртуальной машины службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="45cab-145">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45cab-146">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="45cab-146">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="45cab-147">Указывает пароль администратора для службы контейнеров, использующей операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="45cab-147">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45cab-148">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="45cab-148">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="45cab-149">Указывает имя пользователя администратора для службы контейнеров, использующей операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="45cab-149">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45cab-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45cab-150">-Confirm</span></span>
<span data-ttu-id="45cab-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="45cab-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45cab-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45cab-152">-WhatIf</span></span>
<span data-ttu-id="45cab-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="45cab-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45cab-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="45cab-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45cab-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45cab-155">CommonParameters</span></span>
<span data-ttu-id="45cab-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45cab-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45cab-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45cab-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45cab-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45cab-158">INPUTS</span></span>

### <span data-ttu-id="45cab-159">Ничего</span><span class="sxs-lookup"><span data-stu-id="45cab-159">None</span></span>
<span data-ttu-id="45cab-160">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="45cab-160">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="45cab-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45cab-161">OUTPUTS</span></span>

### <span data-ttu-id="45cab-162">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="45cab-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="45cab-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="45cab-163">NOTES</span></span>

## <span data-ttu-id="45cab-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45cab-164">RELATED LINKS</span></span>

[<span data-ttu-id="45cab-165">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="45cab-165">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="45cab-166">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="45cab-166">New-AzContainerService</span></span>](./New-AzContainerService.md)
