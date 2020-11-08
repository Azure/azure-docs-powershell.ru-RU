---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/new-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
ms.openlocfilehash: 20daa8d14f77ca4563c072d58d1c2269235cb164
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078384"
---
# <span data-ttu-id="32d18-101">New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="32d18-101">New-AzContainerGroup</span></span>

## <span data-ttu-id="32d18-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32d18-102">SYNOPSIS</span></span>
<span data-ttu-id="32d18-103">Создание группы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="32d18-103">Creates a container group.</span></span>

## <span data-ttu-id="32d18-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32d18-104">SYNTAX</span></span>

### <span data-ttu-id="32d18-105">CreateContainerGroupBaseParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32d18-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-AssignIdentity] [-OsType <String>]
 [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32d18-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="32d18-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-AssignIdentity] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32d18-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span><span class="sxs-lookup"><span data-stu-id="32d18-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32d18-108">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="32d18-108">ExplicitIdentityParameterSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32d18-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32d18-109">DESCRIPTION</span></span>
<span data-ttu-id="32d18-110">Командлеты **New-AzContainerGroup** создают группу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="32d18-110">The **New-AzContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="32d18-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32d18-111">EXAMPLES</span></span>

### <span data-ttu-id="32d18-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32d18-112">Example 1</span></span>
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

<span data-ttu-id="32d18-113">Эти команды создают группу контейнеров с помощью последнего образа nginx и запрашивают общедоступный IP-адрес, открыв порт 8000.</span><span class="sxs-lookup"><span data-stu-id="32d18-113">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="32d18-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="32d18-114">Example 2</span></span>
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

<span data-ttu-id="32d18-115">Эти команды создают группу контейнеров и выполняют настраиваемый сценарий внутри контейнера.</span><span class="sxs-lookup"><span data-stu-id="32d18-115">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="32d18-116">Пример 3: создание группы контейнеров "выполнение в завершении".</span><span class="sxs-lookup"><span data-stu-id="32d18-116">Example 3: Creates a run-to-completion container group.</span></span>
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

<span data-ttu-id="32d18-117">Эти команды создают группу контейнеров, которая выполняет печать "Привет" и останавливается.</span><span class="sxs-lookup"><span data-stu-id="32d18-117">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="32d18-118">Пример 4: создание группы контейнеров с помощью изображения в реестре контейнера Azure</span><span class="sxs-lookup"><span data-stu-id="32d18-118">Example 4: Creates a container group using image in Azure Container Registry</span></span>
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

<span data-ttu-id="32d18-119">Эти команды создают группу контейнеров с помощью изображения nginx в реестре контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="32d18-119">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="32d18-120">Пример 5: создание группы контейнеров с помощью изображения в настраиваемом реестре изображений контейнера</span><span class="sxs-lookup"><span data-stu-id="32d18-120">Example 5: Creates a container group using image in custom container image registry</span></span>
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

<span data-ttu-id="32d18-121">Эти команды создают группу контейнеров с использованием настраиваемого изображения из настраиваемого реестра изображений контейнера.</span><span class="sxs-lookup"><span data-stu-id="32d18-121">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="32d18-122">Пример 6: создание группы контейнеров, которая монтирует файловый том Azure</span><span class="sxs-lookup"><span data-stu-id="32d18-122">Example 6: Creates a container group that mounts Azure File volume</span></span>
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

<span data-ttu-id="32d18-123">Эти команды создают группу контейнеров, которая монтирует указанную общую файловую службу Azure `/mnt/azfile` .</span><span class="sxs-lookup"><span data-stu-id="32d18-123">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

### <span data-ttu-id="32d18-124">Пример 7</span><span class="sxs-lookup"><span data-stu-id="32d18-124">Example 7</span></span>
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

<span data-ttu-id="32d18-125">Эти команды создают группу контейнеров с удостоверением системы с помощью последнего образа nginx и запрашивают общедоступный IP-адрес, открыв порт 8000.</span><span class="sxs-lookup"><span data-stu-id="32d18-125">This commands creates a container group with system assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="32d18-126">Пример 8</span><span class="sxs-lookup"><span data-stu-id="32d18-126">Example 8</span></span>
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

<span data-ttu-id="32d18-127">Эти команды создают группу контейнеров с назначенной системой и удостоверением пользователя с помощью последнего образа nginx и запрашивают общедоступный IP-адрес, открыв порт 8000.</span><span class="sxs-lookup"><span data-stu-id="32d18-127">This commands creates a container group with system assigned and user assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

## <span data-ttu-id="32d18-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32d18-128">PARAMETERS</span></span>

### <span data-ttu-id="32d18-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="32d18-129">-AssignIdentity</span></span>
<span data-ttu-id="32d18-130">Включить идентификационные данные, назначенные системой</span><span class="sxs-lookup"><span data-stu-id="32d18-130">Enable system assigned identity</span></span>

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

### <span data-ttu-id="32d18-131">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="32d18-131">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="32d18-132">Данные учетной записи хранения в общей папке Azure для подключения, где имя пользователя — это имя учетной записи хранения, а ключ — ключ учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="32d18-132">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

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

### <span data-ttu-id="32d18-133">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="32d18-133">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="32d18-134">Путь подключения к тому файла Azure.</span><span class="sxs-lookup"><span data-stu-id="32d18-134">The mount path for the Azure File volume.</span></span>

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

### <span data-ttu-id="32d18-135">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="32d18-135">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="32d18-136">Имя общей файловой службы Azure, которую нужно подключить.</span><span class="sxs-lookup"><span data-stu-id="32d18-136">The name of the Azure File share to mount.</span></span>

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

### <span data-ttu-id="32d18-137">-Command</span><span class="sxs-lookup"><span data-stu-id="32d18-137">-Command</span></span>
<span data-ttu-id="32d18-138">Команда, которую нужно выполнить в контейнере.</span><span class="sxs-lookup"><span data-stu-id="32d18-138">The command to run in the container.</span></span>

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

### <span data-ttu-id="32d18-139">-ЦП</span><span class="sxs-lookup"><span data-stu-id="32d18-139">-Cpu</span></span>
<span data-ttu-id="32d18-140">Требуемые ядра ЦП.</span><span class="sxs-lookup"><span data-stu-id="32d18-140">The required CPU cores.</span></span>
<span data-ttu-id="32d18-141">По умолчанию: 1</span><span class="sxs-lookup"><span data-stu-id="32d18-141">Default: 1</span></span>

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

### <span data-ttu-id="32d18-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32d18-142">-DefaultProfile</span></span>
<span data-ttu-id="32d18-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32d18-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32d18-144">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="32d18-144">-DnsNameLabel</span></span>
<span data-ttu-id="32d18-145">Метка имени DNS для IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="32d18-145">The DNS name label for the IP address.</span></span>

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

### <span data-ttu-id="32d18-146">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="32d18-146">-EnvironmentVariable</span></span>
<span data-ttu-id="32d18-147">Переменные среды контейнера.</span><span class="sxs-lookup"><span data-stu-id="32d18-147">The container environment variables.</span></span>

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

### <span data-ttu-id="32d18-148">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="32d18-148">-IdentityId</span></span>
<span data-ttu-id="32d18-149">Пользователи, которым назначены идентификаторы идентификаторов</span><span class="sxs-lookup"><span data-stu-id="32d18-149">The user assigned identity IDs</span></span>

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

### <span data-ttu-id="32d18-150">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="32d18-150">-IdentityType</span></span>
<span data-ttu-id="32d18-151">Тип управляемого удостоверения</span><span class="sxs-lookup"><span data-stu-id="32d18-151">The managed identity type</span></span>

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

### <span data-ttu-id="32d18-152">-Image</span><span class="sxs-lookup"><span data-stu-id="32d18-152">-Image</span></span>
<span data-ttu-id="32d18-153">Изображение контейнера.</span><span class="sxs-lookup"><span data-stu-id="32d18-153">The container image.</span></span>

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

### <span data-ttu-id="32d18-154">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="32d18-154">-IpAddressType</span></span>
<span data-ttu-id="32d18-155">Тип IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="32d18-155">The IP address type.</span></span>

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

### <span data-ttu-id="32d18-156">-Location</span><span class="sxs-lookup"><span data-stu-id="32d18-156">-Location</span></span>
<span data-ttu-id="32d18-157">Расположение группы контейнера.</span><span class="sxs-lookup"><span data-stu-id="32d18-157">The container group Location.</span></span>
<span data-ttu-id="32d18-158">По умолчанию — расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32d18-158">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="32d18-159">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="32d18-159">-MemoryInGB</span></span>
<span data-ttu-id="32d18-160">Требуемая память в ГБ.</span><span class="sxs-lookup"><span data-stu-id="32d18-160">The required memory in GB.</span></span>
<span data-ttu-id="32d18-161">По умолчанию: 1,5</span><span class="sxs-lookup"><span data-stu-id="32d18-161">Default: 1.5</span></span>

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

### <span data-ttu-id="32d18-162">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="32d18-162">-Name</span></span>
<span data-ttu-id="32d18-163">Имя группы контейнера.</span><span class="sxs-lookup"><span data-stu-id="32d18-163">The container group name.</span></span>

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

### <span data-ttu-id="32d18-164">-OsType</span><span class="sxs-lookup"><span data-stu-id="32d18-164">-OsType</span></span>
<span data-ttu-id="32d18-165">Тип ОС контейнера.</span><span class="sxs-lookup"><span data-stu-id="32d18-165">The container OS type.</span></span>
<span data-ttu-id="32d18-166">По умолчанию: Linux</span><span class="sxs-lookup"><span data-stu-id="32d18-166">Default: Linux</span></span>

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

### <span data-ttu-id="32d18-167">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="32d18-167">-Port</span></span>
<span data-ttu-id="32d18-168">Порт (-ы) для открытия.</span><span class="sxs-lookup"><span data-stu-id="32d18-168">The port(s) to open.</span></span> <span data-ttu-id="32d18-169">По умолчанию: [80]</span><span class="sxs-lookup"><span data-stu-id="32d18-169">Default: [80]</span></span>

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

### <span data-ttu-id="32d18-170">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="32d18-170">-RegistryCredential</span></span>
<span data-ttu-id="32d18-171">Учетные данные в реестре настраиваемого контейнера.</span><span class="sxs-lookup"><span data-stu-id="32d18-171">The custom container registry credential.</span></span>

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

### <span data-ttu-id="32d18-172">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="32d18-172">-RegistryServerDomain</span></span>
<span data-ttu-id="32d18-173">Сервер входа в реестр настраиваемого контейнера.</span><span class="sxs-lookup"><span data-stu-id="32d18-173">The custom container registry login server.</span></span>

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

### <span data-ttu-id="32d18-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32d18-174">-ResourceGroupName</span></span>
<span data-ttu-id="32d18-175">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32d18-175">The resource group name.</span></span>

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

### <span data-ttu-id="32d18-176">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="32d18-176">-RestartPolicy</span></span>
<span data-ttu-id="32d18-177">Политика перезапуска контейнера.</span><span class="sxs-lookup"><span data-stu-id="32d18-177">The container restart policy.</span></span> <span data-ttu-id="32d18-178">По умолчанию: всегда</span><span class="sxs-lookup"><span data-stu-id="32d18-178">Default: Always</span></span>

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

### <span data-ttu-id="32d18-179">-Тег</span><span class="sxs-lookup"><span data-stu-id="32d18-179">-Tag</span></span>
<span data-ttu-id="32d18-180">{{Fill описание тега}}</span><span class="sxs-lookup"><span data-stu-id="32d18-180">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="32d18-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32d18-181">-Confirm</span></span>
<span data-ttu-id="32d18-182">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="32d18-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32d18-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32d18-183">-WhatIf</span></span>
<span data-ttu-id="32d18-184">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="32d18-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32d18-185">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="32d18-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32d18-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32d18-186">CommonParameters</span></span>
<span data-ttu-id="32d18-187">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32d18-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32d18-188">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32d18-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32d18-189">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32d18-189">INPUTS</span></span>

### <span data-ttu-id="32d18-190">System. String</span><span class="sxs-lookup"><span data-stu-id="32d18-190">System.String</span></span>

### <span data-ttu-id="32d18-191">System. String []</span><span class="sxs-lookup"><span data-stu-id="32d18-191">System.String[]</span></span>

### <span data-ttu-id="32d18-192">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="32d18-192">System.Collections.Hashtable</span></span>

## <span data-ttu-id="32d18-193">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32d18-193">OUTPUTS</span></span>

### <span data-ttu-id="32d18-194">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="32d18-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="32d18-195">Пуск</span><span class="sxs-lookup"><span data-stu-id="32d18-195">NOTES</span></span>

## <span data-ttu-id="32d18-196">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32d18-196">RELATED LINKS</span></span>
