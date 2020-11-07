---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
ms.openlocfilehash: e88f1d3ce684881d839574fe0b73f36b83e275f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735062"
---
# <span data-ttu-id="426e0-101">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="426e0-101">New-AzureRmContainerServiceConfig</span></span>

## <span data-ttu-id="426e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="426e0-102">SYNOPSIS</span></span>
<span data-ttu-id="426e0-103">Создает локальный объект конфигурации для службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="426e0-103">Creates a local configuration object for a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="426e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="426e0-104">SYNTAX</span></span>

```
New-AzureRmContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="426e0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="426e0-105">DESCRIPTION</span></span>
<span data-ttu-id="426e0-106">Командлет **New-AzureRmContainerServiceConfig** создает объект локальной конфигурации для службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="426e0-106">The **New-AzureRmContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="426e0-107">Предоставьте этот объект командлету New-AzureRmContainerService, чтобы создать службу контейнера.</span><span class="sxs-lookup"><span data-stu-id="426e0-107">Provide this object to the New-AzureRmContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="426e0-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="426e0-108">EXAMPLES</span></span>

### <span data-ttu-id="426e0-109">Пример 1: создание конфигурации службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="426e0-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="426e0-110">Эта команда создает контейнер и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="426e0-110">This command creates a container, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="426e0-111">Команда определяет различные параметры конфигурации службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="426e0-111">The command specifies various settings for the container service configuration.</span></span>
<span data-ttu-id="426e0-112">Команда передает объект конфигурации в командлет Add-AzureRmContainerServiceAgentPoolProfile с помощью оператора Pipeline.</span><span class="sxs-lookup"><span data-stu-id="426e0-112">The command passes the configuration object to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="426e0-113">Этот командлет добавляет профиль пула агентов.</span><span class="sxs-lookup"><span data-stu-id="426e0-113">That cmdlet adds an agent pool profile.</span></span>

<span data-ttu-id="426e0-114">Укажите объект в $Container для параметра *ContainerService* **New-AzureRmContainerService**.</span><span class="sxs-lookup"><span data-stu-id="426e0-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzureRmContainerService**.</span></span>

## <span data-ttu-id="426e0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="426e0-115">PARAMETERS</span></span>

### <span data-ttu-id="426e0-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="426e0-116">-AdminUsername</span></span>
<span data-ttu-id="426e0-117">Указывает имя учетной записи администратора, которая будет использоваться для службы контейнеров на базе Linux.</span><span class="sxs-lookup"><span data-stu-id="426e0-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="426e0-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="426e0-118">-AgentPoolProfile</span></span>
<span data-ttu-id="426e0-119">Указывает массив объектов профиля группы агента для службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="426e0-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="426e0-120">Добавьте профиль с помощью командлета Add-AzureRmContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="426e0-120">Add a profile by using the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="426e0-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="426e0-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="426e0-122">Задает настраиваемую Orchestrator Profile.</span><span class="sxs-lookup"><span data-stu-id="426e0-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="426e0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="426e0-123">-DefaultProfile</span></span>
<span data-ttu-id="426e0-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="426e0-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="426e0-125">-Location</span><span class="sxs-lookup"><span data-stu-id="426e0-125">-Location</span></span>
<span data-ttu-id="426e0-126">Указывает расположение для создания службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="426e0-126">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="426e0-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="426e0-127">-MasterCount</span></span>
<span data-ttu-id="426e0-128">Задает количество создаваемых эталонных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="426e0-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="426e0-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="426e0-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="426e0-130">Задает префикс DNS для основной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="426e0-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="426e0-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="426e0-131">-OrchestratorType</span></span>
<span data-ttu-id="426e0-132">Указывает тип Orchestrator для службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="426e0-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="426e0-133">Допустимые значения этого параметра: DCOS и Swarm.</span><span class="sxs-lookup"><span data-stu-id="426e0-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="426e0-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="426e0-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="426e0-135">Указывает идентификатор клиента для профиля участника.</span><span class="sxs-lookup"><span data-stu-id="426e0-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="426e0-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="426e0-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="426e0-137">Указывает секретный профиль участника.</span><span class="sxs-lookup"><span data-stu-id="426e0-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="426e0-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="426e0-138">-SshPublicKey</span></span>
<span data-ttu-id="426e0-139">Указывает открытый ключ SSH для службы контейнера на основе Linux.</span><span class="sxs-lookup"><span data-stu-id="426e0-139">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="426e0-140">-Тег</span><span class="sxs-lookup"><span data-stu-id="426e0-140">-Tag</span></span>
<span data-ttu-id="426e0-141">Указывает теги для службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="426e0-141">Specifies tags for the container service.</span></span>

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

### <span data-ttu-id="426e0-142">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="426e0-142">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="426e0-143">Указывает, включает ли эта конфигурация диагностику для виртуальной машины службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="426e0-143">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="426e0-144">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="426e0-144">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="426e0-145">Указывает пароль администратора для службы контейнеров, использующей операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="426e0-145">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="426e0-146">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="426e0-146">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="426e0-147">Указывает имя пользователя администратора для службы контейнеров, использующей операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="426e0-147">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="426e0-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="426e0-148">-Confirm</span></span>
<span data-ttu-id="426e0-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="426e0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="426e0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="426e0-150">-WhatIf</span></span>
<span data-ttu-id="426e0-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="426e0-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="426e0-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="426e0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="426e0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="426e0-153">CommonParameters</span></span>
<span data-ttu-id="426e0-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="426e0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="426e0-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="426e0-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="426e0-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="426e0-156">INPUTS</span></span>

## <span data-ttu-id="426e0-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="426e0-157">OUTPUTS</span></span>

## <span data-ttu-id="426e0-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="426e0-158">NOTES</span></span>

## <span data-ttu-id="426e0-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="426e0-159">RELATED LINKS</span></span>

[<span data-ttu-id="426e0-160">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="426e0-160">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="426e0-161">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="426e0-161">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)


