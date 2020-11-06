---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
ms.openlocfilehash: 51ebdbffcb88c1d43716170b236332741d05466f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566551"
---
# <span data-ttu-id="58487-101">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="58487-101">New-AzureRmContainerServiceConfig</span></span>

## <span data-ttu-id="58487-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58487-102">SYNOPSIS</span></span>
<span data-ttu-id="58487-103">Создает локальный объект конфигурации для службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="58487-103">Creates a local configuration object for a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58487-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58487-104">SYNTAX</span></span>

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

## <span data-ttu-id="58487-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58487-105">DESCRIPTION</span></span>
<span data-ttu-id="58487-106">Командлет **New-AzureRmContainerServiceConfig** создает объект локальной конфигурации для службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="58487-106">The **New-AzureRmContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="58487-107">Предоставьте этот объект командлету New-AzureRmContainerService, чтобы создать службу контейнера.</span><span class="sxs-lookup"><span data-stu-id="58487-107">Provide this object to the New-AzureRmContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="58487-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58487-108">EXAMPLES</span></span>

### <span data-ttu-id="58487-109">Пример 1: создание конфигурации службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="58487-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="58487-110">Эта команда создает контейнер и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="58487-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="58487-111">Команда определяет различные параметры конфигурации службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="58487-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="58487-112">Команда передает объект конфигурации в командлет Add-AzureRmContainerServiceAgentPoolProfile с помощью оператора Pipeline.</span><span class="sxs-lookup"><span data-stu-id="58487-112">The command passes the configuration object to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="58487-113">Этот командлет добавляет профиль пула агентов.</span><span class="sxs-lookup"><span data-stu-id="58487-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="58487-114">Укажите объект в $Container для параметра *ContainerService* **New-AzureRmContainerService**.</span><span class="sxs-lookup"><span data-stu-id="58487-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzureRmContainerService**.</span></span>

## <span data-ttu-id="58487-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58487-115">PARAMETERS</span></span>

### <span data-ttu-id="58487-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="58487-116">-AdminUsername</span></span>
<span data-ttu-id="58487-117">Указывает имя учетной записи администратора, которая будет использоваться для службы контейнеров на базе Linux.</span><span class="sxs-lookup"><span data-stu-id="58487-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="58487-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="58487-118">-AgentPoolProfile</span></span>
<span data-ttu-id="58487-119">Указывает массив объектов профиля группы агента для службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="58487-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="58487-120">Добавьте профиль с помощью командлета Add-AzureRmContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="58487-120">Add a profile by using the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="58487-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="58487-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="58487-122">Задает настраиваемую Orchestrator Profile.</span><span class="sxs-lookup"><span data-stu-id="58487-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="58487-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58487-123">-DefaultProfile</span></span>
<span data-ttu-id="58487-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58487-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58487-125">-Location</span><span class="sxs-lookup"><span data-stu-id="58487-125">-Location</span></span>
<span data-ttu-id="58487-126">Указывает расположение для создания службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="58487-126">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="58487-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="58487-127">-MasterCount</span></span>
<span data-ttu-id="58487-128">Задает количество создаваемых эталонных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="58487-128">Specifies the number of master virtual machines to create.</span></span>

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

### <span data-ttu-id="58487-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="58487-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="58487-130">Задает префикс DNS для основной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="58487-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="58487-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="58487-131">-OrchestratorType</span></span>
<span data-ttu-id="58487-132">Указывает тип Orchestrator для службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="58487-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="58487-133">Допустимые значения этого параметра: DCOS и Swarm.</span><span class="sxs-lookup"><span data-stu-id="58487-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="58487-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="58487-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="58487-135">Указывает идентификатор клиента для профиля участника.</span><span class="sxs-lookup"><span data-stu-id="58487-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="58487-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="58487-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="58487-137">Указывает секретный профиль участника.</span><span class="sxs-lookup"><span data-stu-id="58487-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="58487-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="58487-138">-SshPublicKey</span></span>
<span data-ttu-id="58487-139">Указывает открытый ключ SSH для службы контейнера на основе Linux.</span><span class="sxs-lookup"><span data-stu-id="58487-139">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="58487-140">-Тег</span><span class="sxs-lookup"><span data-stu-id="58487-140">-Tag</span></span>
<span data-ttu-id="58487-141">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="58487-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="58487-142">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="58487-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="58487-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="58487-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="58487-144">Указывает, включает ли эта конфигурация диагностику для виртуальной машины службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="58487-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="58487-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="58487-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="58487-146">Указывает пароль администратора для службы контейнеров, использующей операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="58487-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="58487-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="58487-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="58487-148">Указывает имя пользователя администратора для службы контейнеров, использующей операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="58487-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="58487-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58487-149">-Confirm</span></span>
<span data-ttu-id="58487-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="58487-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58487-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58487-151">-WhatIf</span></span>
<span data-ttu-id="58487-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="58487-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58487-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="58487-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58487-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58487-154">CommonParameters</span></span>
<span data-ttu-id="58487-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58487-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58487-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58487-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58487-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58487-157">INPUTS</span></span>

### <span data-ttu-id="58487-158">System. String</span><span class="sxs-lookup"><span data-stu-id="58487-158">System.String</span></span>

### <span data-ttu-id="58487-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="58487-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="58487-160">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. ContainerServiceOrchestratorTypes, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="58487-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="58487-161">System. Int32</span><span class="sxs-lookup"><span data-stu-id="58487-161">System.Int32</span></span>

### <span data-ttu-id="58487-162">Microsoft. Azure. Management. COMPUTE. Models. ContainerServiceAgentPoolProfile []</span><span class="sxs-lookup"><span data-stu-id="58487-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="58487-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="58487-163">System.String[]</span></span>

### <span data-ttu-id="58487-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="58487-164">System.Boolean</span></span>

## <span data-ttu-id="58487-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58487-165">OUTPUTS</span></span>

### <span data-ttu-id="58487-166">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="58487-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="58487-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="58487-167">NOTES</span></span>

## <span data-ttu-id="58487-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58487-168">RELATED LINKS</span></span>

[<span data-ttu-id="58487-169">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="58487-169">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="58487-170">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="58487-170">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)
