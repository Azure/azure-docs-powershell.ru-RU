---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/new-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
ms.openlocfilehash: 20daa8d14f77ca4563c072d58d1c2269235cb164
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415252"
---
# <span data-ttu-id="acbb0-101">New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="acbb0-101">New-AzContainerGroup</span></span>

## <span data-ttu-id="acbb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acbb0-102">SYNOPSIS</span></span>
<span data-ttu-id="acbb0-103">Создает группу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="acbb0-103">Creates a container group.</span></span>

## <span data-ttu-id="acbb0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="acbb0-104">SYNTAX</span></span>

### <span data-ttu-id="acbb0-105">CreateContainerGroupBaseParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="acbb0-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-AssignIdentity] [-OsType <String>]
 [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acbb0-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="acbb0-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-AssignIdentity] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acbb0-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span><span class="sxs-lookup"><span data-stu-id="acbb0-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acbb0-108">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="acbb0-108">ExplicitIdentityParameterSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acbb0-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="acbb0-109">DESCRIPTION</span></span>
<span data-ttu-id="acbb0-110">Для этого создается группа контейнеров с новыми рабочими группами **AzContainerGroup.**</span><span class="sxs-lookup"><span data-stu-id="acbb0-110">The **New-AzContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="acbb0-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="acbb0-111">EXAMPLES</span></span>

### <span data-ttu-id="acbb0-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="acbb0-112">Example 1</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="acbb0-113">Эта команда создает группу контейнеров с использованием нового изображения nginx и запрашивает общедоступный IP-адрес с открытием порта 8000.</span><span class="sxs-lookup"><span data-stu-id="acbb0-113">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="acbb0-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="acbb0-114">Example 2</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="acbb0-115">Эта команда создает группу контейнеров и выполняет настраиваемый сценарий внутри контейнера.</span><span class="sxs-lookup"><span data-stu-id="acbb0-115">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="acbb0-116">Пример 3. Создает группу контейнеров для выполнения выполнения.</span><span class="sxs-lookup"><span data-stu-id="acbb0-116">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="acbb0-117">Эта команда создает группу контейнеров, которая печатает "привет" и остановки.</span><span class="sxs-lookup"><span data-stu-id="acbb0-117">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="acbb0-118">Пример 4. Создание группы контейнеров с помощью изображения в Azure Container Registry</span><span class="sxs-lookup"><span data-stu-id="acbb0-118">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myacr}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="acbb0-119">Эти команды создают группу контейнеров с использованием nginx-изображения в azure Container Registry.</span><span class="sxs-lookup"><span data-stu-id="acbb0-119">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="acbb0-120">Пример 5. Создание группы контейнеров с помощью изображения в настраиваемом реестре изображений контейнера</span><span class="sxs-lookup"><span data-stu-id="acbb0-120">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="acbb0-121">Эта команда создает группу контейнеров с использованием настраиваемой картинки из настраиваемой реестра изображений контейнера.</span><span class="sxs-lookup"><span data-stu-id="acbb0-121">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="acbb0-122">Пример 6. Создание группы контейнеров для установки громкости файлов Azure</span><span class="sxs-lookup"><span data-stu-id="acbb0-122">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name mycontainer -Image alpine -AzureFileVolumeShareName myshare -AzureFileVolumeAccountCredential $mycred -AzureFileVolumeMountPath /mnt/azfile

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  : {AzureFile}
State                    : Running
Events                   : {}
```

<span data-ttu-id="acbb0-123">Эти команды создают группу контейнеров, в которую будет вметься предоставленная папка файлов `/mnt/azfile` Azure.</span><span class="sxs-lookup"><span data-stu-id="acbb0-123">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

### <span data-ttu-id="acbb0-124">Пример 7</span><span class="sxs-lookup"><span data-stu-id="acbb0-124">Example 7</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -AssignIdentity

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="acbb0-125">Эта команда создает группу контейнеров с системой, назначенной удостоверением, используя последнее изображение nginx, и запрашивает общедоступный IP-адрес с открытием порта 8000.</span><span class="sxs-lookup"><span data-stu-id="acbb0-125">This commands creates a container group with system assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="acbb0-126">Пример 8</span><span class="sxs-lookup"><span data-stu-id="acbb0-126">Example 8</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -IdentityType SystemAssignedUserAssigned -IdentityId /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<UserIdentityName>

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="acbb0-127">Эти команды создают группу контейнеров с системой и удостоверениями, которые назначены пользователю с использованием последних nginx-изображений, и запрашивает общедоступный IP-адрес с открытием порта 8000.</span><span class="sxs-lookup"><span data-stu-id="acbb0-127">This commands creates a container group with system assigned and user assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

## <span data-ttu-id="acbb0-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acbb0-128">PARAMETERS</span></span>

### <span data-ttu-id="acbb0-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="acbb0-129">-AssignIdentity</span></span>
<span data-ttu-id="acbb0-130">Включить системные удостоверения</span><span class="sxs-lookup"><span data-stu-id="acbb0-130">Enable system assigned identity</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateContainerGroupBaseParamSet, CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbb0-131">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="acbb0-131">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="acbb0-132">Учетные данные учетной записи хранения в папке файлов Azure, чтобы у пользователя было имя учетной записи хранения, а ключом является ключ учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="acbb0-132">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbb0-133">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="acbb0-133">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="acbb0-134">Путь к файлу Azure.</span><span class="sxs-lookup"><span data-stu-id="acbb0-134">The mount path for the Azure File volume.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbb0-135">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="acbb0-135">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="acbb0-136">Имя файла Azure, который нужно установить.</span><span class="sxs-lookup"><span data-stu-id="acbb0-136">The name of the Azure File share to mount.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbb0-137">-Command</span><span class="sxs-lookup"><span data-stu-id="acbb0-137">-Command</span></span>
<span data-ttu-id="acbb0-138">Команда для запуска в контейнере.</span><span class="sxs-lookup"><span data-stu-id="acbb0-138">The command to run in the container.</span></span>

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

### <span data-ttu-id="acbb0-139">-CPU</span><span class="sxs-lookup"><span data-stu-id="acbb0-139">-Cpu</span></span>
<span data-ttu-id="acbb0-140">Необходимые ядро ЦП.</span><span class="sxs-lookup"><span data-stu-id="acbb0-140">The required CPU cores.</span></span>
<span data-ttu-id="acbb0-141">По умолчанию: 1</span><span class="sxs-lookup"><span data-stu-id="acbb0-141">Default: 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbb0-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acbb0-142">-DefaultProfile</span></span>
<span data-ttu-id="acbb0-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="acbb0-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acbb0-144">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="acbb0-144">-DnsNameLabel</span></span>
<span data-ttu-id="acbb0-145">Метка имени DNS для IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="acbb0-145">The DNS name label for the IP address.</span></span>

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

### <span data-ttu-id="acbb0-146">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="acbb0-146">-EnvironmentVariable</span></span>
<span data-ttu-id="acbb0-147">Переменные среды контейнера.</span><span class="sxs-lookup"><span data-stu-id="acbb0-147">The container environment variables.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbb0-148">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="acbb0-148">-IdentityId</span></span>
<span data-ttu-id="acbb0-149">Идентификаторы, присвоенные пользователю</span><span class="sxs-lookup"><span data-stu-id="acbb0-149">The user assigned identity IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acbb0-150">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="acbb0-150">-IdentityType</span></span>
<span data-ttu-id="acbb0-151">Управляемый тип удостоверений</span><span class="sxs-lookup"><span data-stu-id="acbb0-151">The managed identity type</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerInstance.Models.ResourceIdentityType
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet, ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbb0-152">-Image</span><span class="sxs-lookup"><span data-stu-id="acbb0-152">-Image</span></span>
<span data-ttu-id="acbb0-153">Изображение контейнера.</span><span class="sxs-lookup"><span data-stu-id="acbb0-153">The container image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbb0-154">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="acbb0-154">-IpAddressType</span></span>
<span data-ttu-id="acbb0-155">Тип IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="acbb0-155">The IP address type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Public

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbb0-156">-Location</span><span class="sxs-lookup"><span data-stu-id="acbb0-156">-Location</span></span>
<span data-ttu-id="acbb0-157">Группа контейнеров "Расположение".</span><span class="sxs-lookup"><span data-stu-id="acbb0-157">The container group Location.</span></span>
<span data-ttu-id="acbb0-158">Расположение группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="acbb0-158">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="acbb0-159">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="acbb0-159">-MemoryInGB</span></span>
<span data-ttu-id="acbb0-160">Необходимая память в ГБ.</span><span class="sxs-lookup"><span data-stu-id="acbb0-160">The required memory in GB.</span></span>
<span data-ttu-id="acbb0-161">Значение по умолчанию: 1,5</span><span class="sxs-lookup"><span data-stu-id="acbb0-161">Default: 1.5</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases: Memory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbb0-162">-Name</span><span class="sxs-lookup"><span data-stu-id="acbb0-162">-Name</span></span>
<span data-ttu-id="acbb0-163">Имя группы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="acbb0-163">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acbb0-164">-OsType</span><span class="sxs-lookup"><span data-stu-id="acbb0-164">-OsType</span></span>
<span data-ttu-id="acbb0-165">Тип ОС контейнера.</span><span class="sxs-lookup"><span data-stu-id="acbb0-165">The container OS type.</span></span>
<span data-ttu-id="acbb0-166">По умолчанию: Linux</span><span class="sxs-lookup"><span data-stu-id="acbb0-166">Default: Linux</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Linux, Windows

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbb0-167">-Port</span><span class="sxs-lookup"><span data-stu-id="acbb0-167">-Port</span></span>
<span data-ttu-id="acbb0-168">Порты, которые нужно открыть.</span><span class="sxs-lookup"><span data-stu-id="acbb0-168">The port(s) to open.</span></span> <span data-ttu-id="acbb0-169">Значение по умолчанию: [80]</span><span class="sxs-lookup"><span data-stu-id="acbb0-169">Default: [80]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbb0-170">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="acbb0-170">-RegistryCredential</span></span>
<span data-ttu-id="acbb0-171">Учетные данные настраиваемой контейнерной учетной записи реестра.</span><span class="sxs-lookup"><span data-stu-id="acbb0-171">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbb0-172">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="acbb0-172">-RegistryServerDomain</span></span>
<span data-ttu-id="acbb0-173">Настраиваемый сервер входа в реестр контейнеров.</span><span class="sxs-lookup"><span data-stu-id="acbb0-173">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbb0-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acbb0-174">-ResourceGroupName</span></span>
<span data-ttu-id="acbb0-175">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="acbb0-175">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acbb0-176">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="acbb0-176">-RestartPolicy</span></span>
<span data-ttu-id="acbb0-177">Политика перезапуска контейнера.</span><span class="sxs-lookup"><span data-stu-id="acbb0-177">The container restart policy.</span></span> <span data-ttu-id="acbb0-178">По умолчанию: всегда</span><span class="sxs-lookup"><span data-stu-id="acbb0-178">Default: Always</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Always, Never, OnFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbb0-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="acbb0-179">-Tag</span></span>
<span data-ttu-id="acbb0-180">{{Fill Tag Description}}</span><span class="sxs-lookup"><span data-stu-id="acbb0-180">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="acbb0-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acbb0-181">-Confirm</span></span>
<span data-ttu-id="acbb0-182">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="acbb0-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acbb0-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acbb0-183">-WhatIf</span></span>
<span data-ttu-id="acbb0-184">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acbb0-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acbb0-185">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="acbb0-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acbb0-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acbb0-186">CommonParameters</span></span>
<span data-ttu-id="acbb0-187">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acbb0-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acbb0-188">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acbb0-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acbb0-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="acbb0-189">INPUTS</span></span>

### <span data-ttu-id="acbb0-190">System.String</span><span class="sxs-lookup"><span data-stu-id="acbb0-190">System.String</span></span>

### <span data-ttu-id="acbb0-191">System.String[]</span><span class="sxs-lookup"><span data-stu-id="acbb0-191">System.String[]</span></span>

### <span data-ttu-id="acbb0-192">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="acbb0-192">System.Collections.Hashtable</span></span>

## <span data-ttu-id="acbb0-193">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="acbb0-193">OUTPUTS</span></span>

### <span data-ttu-id="acbb0-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="acbb0-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="acbb0-195">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="acbb0-195">NOTES</span></span>

## <span data-ttu-id="acbb0-196">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="acbb0-196">RELATED LINKS</span></span>
