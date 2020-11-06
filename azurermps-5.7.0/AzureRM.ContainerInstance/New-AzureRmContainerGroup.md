---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/new-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 30635aa9bc1906c9e329e605327df1a2dfce5df4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559139"
---
# <span data-ttu-id="8fc95-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="8fc95-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="8fc95-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8fc95-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc95-103">Создание группы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="8fc95-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fc95-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8fc95-104">SYNTAX</span></span>

### <span data-ttu-id="8fc95-105">CreateContainerGroupBaseParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8fc95-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fc95-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="8fc95-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fc95-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fc95-107">DESCRIPTION</span></span>
<span data-ttu-id="8fc95-108">Командлеты **New-AzureRmContainerGroup** создают группу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="8fc95-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="8fc95-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8fc95-109">EXAMPLES</span></span>

### <span data-ttu-id="8fc95-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8fc95-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

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

<span data-ttu-id="8fc95-111">Эти команды создают группу контейнеров с помощью последнего образа nginx и запрашивают общедоступный IP-адрес, открыв порт 8000.</span><span class="sxs-lookup"><span data-stu-id="8fc95-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="8fc95-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8fc95-112">Example 2</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

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

<span data-ttu-id="8fc95-113">Эти команды создают группу контейнеров и выполняют настраиваемый сценарий внутри контейнера.</span><span class="sxs-lookup"><span data-stu-id="8fc95-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="8fc95-114">Пример 3: создание группы контейнеров "выполнение в завершении".</span><span class="sxs-lookup"><span data-stu-id="8fc95-114">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

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

<span data-ttu-id="8fc95-115">Эти команды создают группу контейнеров, которая выполняет печать "Привет" и останавливается.</span><span class="sxs-lookup"><span data-stu-id="8fc95-115">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="8fc95-116">Пример 4: создание группы контейнеров с помощью изображения в реестре контейнера Azure</span><span class="sxs-lookup"><span data-stu-id="8fc95-116">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

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

<span data-ttu-id="8fc95-117">Эти команды создают группу контейнеров с помощью изображения nginx в реестре контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="8fc95-117">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="8fc95-118">Пример 5: создание группы контейнеров с помощью изображения в настраиваемом реестре изображений контейнера</span><span class="sxs-lookup"><span data-stu-id="8fc95-118">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

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

<span data-ttu-id="8fc95-119">Эти команды создают группу контейнеров с использованием настраиваемого изображения из настраиваемого реестра изображений контейнера.</span><span class="sxs-lookup"><span data-stu-id="8fc95-119">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="8fc95-120">Пример 6: создание группы контейнеров, которая монтирует файловый том Azure</span><span class="sxs-lookup"><span data-stu-id="8fc95-120">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image alpine -AzureFileVolumeShareName myshare -AzureFileVolumeAccountKey $mycred -AzureFileVolumeMountPath /mnt/azfile

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

<span data-ttu-id="8fc95-121">Эти команды создают группу контейнеров, которая монтирует указанную общую файловую службу Azure `/mnt/azfile` .</span><span class="sxs-lookup"><span data-stu-id="8fc95-121">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

## <span data-ttu-id="8fc95-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8fc95-122">PARAMETERS</span></span>

### <span data-ttu-id="8fc95-123">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8fc95-123">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="8fc95-124">Данные учетной записи хранения в общей папке Azure для подключения, где имя пользователя — это имя учетной записи хранения, а ключ — ключ учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8fc95-124">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc95-125">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="8fc95-125">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="8fc95-126">Путь подключения к тому файла Azure.</span><span class="sxs-lookup"><span data-stu-id="8fc95-126">The mount path for the Azure File volume.</span></span>

```yaml
Type: String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc95-127">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="8fc95-127">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="8fc95-128">Имя общей файловой службы Azure, которую нужно подключить.</span><span class="sxs-lookup"><span data-stu-id="8fc95-128">The name of the Azure File share to mount.</span></span>

```yaml
Type: String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc95-129">-Command</span><span class="sxs-lookup"><span data-stu-id="8fc95-129">-Command</span></span>
<span data-ttu-id="8fc95-130">Команда, которую нужно выполнить в контейнере.</span><span class="sxs-lookup"><span data-stu-id="8fc95-130">The command to run in the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc95-131">-ЦП</span><span class="sxs-lookup"><span data-stu-id="8fc95-131">-Cpu</span></span>
<span data-ttu-id="8fc95-132">Требуемые ядра ЦП.</span><span class="sxs-lookup"><span data-stu-id="8fc95-132">The required CPU cores.</span></span>
<span data-ttu-id="8fc95-133">По умолчанию: 1</span><span class="sxs-lookup"><span data-stu-id="8fc95-133">Default: 1</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc95-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fc95-134">-DefaultProfile</span></span>
<span data-ttu-id="8fc95-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8fc95-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fc95-136">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="8fc95-136">-DnsNameLabel</span></span>
<span data-ttu-id="8fc95-137">Метка имени DNS для IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="8fc95-137">The DNS name label for the IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc95-138">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="8fc95-138">-EnvironmentVariable</span></span>
<span data-ttu-id="8fc95-139">Переменные среды контейнера.</span><span class="sxs-lookup"><span data-stu-id="8fc95-139">The container environment variables.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc95-140">-Image</span><span class="sxs-lookup"><span data-stu-id="8fc95-140">-Image</span></span>
<span data-ttu-id="8fc95-141">Изображение контейнера.</span><span class="sxs-lookup"><span data-stu-id="8fc95-141">The container image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc95-142">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="8fc95-142">-IpAddressType</span></span>
<span data-ttu-id="8fc95-143">Тип IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="8fc95-143">The IP address type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Public

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc95-144">-Location</span><span class="sxs-lookup"><span data-stu-id="8fc95-144">-Location</span></span>
<span data-ttu-id="8fc95-145">Расположение группы контейнера.</span><span class="sxs-lookup"><span data-stu-id="8fc95-145">The container group Location.</span></span>
<span data-ttu-id="8fc95-146">По умолчанию — расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8fc95-146">Default to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc95-147">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="8fc95-147">-MemoryInGB</span></span>
<span data-ttu-id="8fc95-148">Требуемая память в ГБ.</span><span class="sxs-lookup"><span data-stu-id="8fc95-148">The required memory in GB.</span></span>
<span data-ttu-id="8fc95-149">По умолчанию: 1,5</span><span class="sxs-lookup"><span data-stu-id="8fc95-149">Default: 1.5</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: Memory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc95-150">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8fc95-150">-Name</span></span>
<span data-ttu-id="8fc95-151">Имя группы контейнера.</span><span class="sxs-lookup"><span data-stu-id="8fc95-151">The container group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fc95-152">-OsType</span><span class="sxs-lookup"><span data-stu-id="8fc95-152">-OsType</span></span>
<span data-ttu-id="8fc95-153">Тип ОС контейнера.</span><span class="sxs-lookup"><span data-stu-id="8fc95-153">The container OS type.</span></span>
<span data-ttu-id="8fc95-154">По умолчанию: Linux</span><span class="sxs-lookup"><span data-stu-id="8fc95-154">Default: Linux</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Linux, Windows

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc95-155">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="8fc95-155">-Port</span></span>
<span data-ttu-id="8fc95-156">Порт (-ы) для открытия.</span><span class="sxs-lookup"><span data-stu-id="8fc95-156">The port(s) to open.</span></span> <span data-ttu-id="8fc95-157">По умолчанию: [80]</span><span class="sxs-lookup"><span data-stu-id="8fc95-157">Default: [80]</span></span>

```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc95-158">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="8fc95-158">-RegistryCredential</span></span>
<span data-ttu-id="8fc95-159">Учетные данные в реестре настраиваемого контейнера.</span><span class="sxs-lookup"><span data-stu-id="8fc95-159">The custom container registry credential.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc95-160">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="8fc95-160">-RegistryServerDomain</span></span>
<span data-ttu-id="8fc95-161">Сервер входа в реестр настраиваемого контейнера.</span><span class="sxs-lookup"><span data-stu-id="8fc95-161">The custom container registry login server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc95-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fc95-162">-ResourceGroupName</span></span>
<span data-ttu-id="8fc95-163">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8fc95-163">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fc95-164">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="8fc95-164">-RestartPolicy</span></span>
<span data-ttu-id="8fc95-165">Политика перезапуска контейнера.</span><span class="sxs-lookup"><span data-stu-id="8fc95-165">The container restart policy.</span></span> <span data-ttu-id="8fc95-166">По умолчанию: всегда</span><span class="sxs-lookup"><span data-stu-id="8fc95-166">Default: Always</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Always, Never, OnFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc95-167">-Тег</span><span class="sxs-lookup"><span data-stu-id="8fc95-167">-Tag</span></span>
<span data-ttu-id="8fc95-168">{{Fill описание тега}}</span><span class="sxs-lookup"><span data-stu-id="8fc95-168">{{Fill Tag Description}}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fc95-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8fc95-169">-Confirm</span></span>
<span data-ttu-id="8fc95-170">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8fc95-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fc95-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fc95-171">-WhatIf</span></span>
<span data-ttu-id="8fc95-172">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8fc95-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fc95-173">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8fc95-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fc95-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc95-174">CommonParameters</span></span>
<span data-ttu-id="8fc95-175">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8fc95-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc95-176">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fc95-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc95-177">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8fc95-177">INPUTS</span></span>

### <span data-ttu-id="8fc95-178">System. String</span><span class="sxs-lookup"><span data-stu-id="8fc95-178">System.String</span></span>
<span data-ttu-id="8fc95-179">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8fc95-179">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8fc95-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fc95-180">OUTPUTS</span></span>

### <span data-ttu-id="8fc95-181">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="8fc95-181">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="8fc95-182">Пуск</span><span class="sxs-lookup"><span data-stu-id="8fc95-182">NOTES</span></span>

## <span data-ttu-id="8fc95-183">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8fc95-183">RELATED LINKS</span></span>
