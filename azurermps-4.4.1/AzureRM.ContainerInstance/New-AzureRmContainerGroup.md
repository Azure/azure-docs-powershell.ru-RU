---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 63c54c5f1bb17af82e353b70e757bf91b1208958
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567664"
---
# <span data-ttu-id="09f99-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="09f99-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="09f99-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09f99-102">SYNOPSIS</span></span>
<span data-ttu-id="09f99-103">Создание группы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="09f99-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09f99-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09f99-104">SYNTAX</span></span>

### <span data-ttu-id="09f99-105">CreateContainerGroupBaseParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="09f99-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09f99-106">CreateContainerGroupWithRegistryParamSet</span><span class="sxs-lookup"><span data-stu-id="09f99-106">CreateContainerGroupWithRegistryParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>]
 -RegistryCredential <PSCredential> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09f99-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09f99-107">DESCRIPTION</span></span>
<span data-ttu-id="09f99-108">Командлеты **New-AzureRmContainerGroup** создают группу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="09f99-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="09f99-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09f99-109">EXAMPLES</span></span>

### <span data-ttu-id="09f99-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="09f99-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port 8000

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
```

<span data-ttu-id="09f99-111">Эти команды создают группу контейнеров с помощью последнего образа nginx и запрашивают общедоступный IP-адрес, открыв порт 8000.</span><span class="sxs-lookup"><span data-stu-id="09f99-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="09f99-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="09f99-112">Example 2</span></span>
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
```

<span data-ttu-id="09f99-113">Эти команды создают группу контейнеров и выполняют настраиваемый сценарий внутри контейнера.</span><span class="sxs-lookup"><span data-stu-id="09f99-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="09f99-114">Пример 3: создание группы контейнеров с помощью изображения в реестре контейнера Azure</span><span class="sxs-lookup"><span data-stu-id="09f99-114">Example 3: Creates a container group using image in Azure Container Registry</span></span>
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
```

<span data-ttu-id="09f99-115">Эти команды создают группу контейнеров с помощью изображения nginx в реестре контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="09f99-115">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="09f99-116">Пример 4: создание группы контейнеров с помощью изображения в настраиваемом реестре изображений контейнера</span><span class="sxs-lookup"><span data-stu-id="09f99-116">Example 4: Creates a container group using image in custom container image registry</span></span>
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
```

<span data-ttu-id="09f99-117">Эти команды создают группу контейнеров с использованием настраиваемого изображения из настраиваемого реестра изображений контейнера.</span><span class="sxs-lookup"><span data-stu-id="09f99-117">This commands creates a container group using a custom image from a custom container image registry.</span></span>

## <span data-ttu-id="09f99-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09f99-118">PARAMETERS</span></span>

### <span data-ttu-id="09f99-119">-Command</span><span class="sxs-lookup"><span data-stu-id="09f99-119">-Command</span></span>
<span data-ttu-id="09f99-120">Команда, которую нужно выполнить в контейнере.</span><span class="sxs-lookup"><span data-stu-id="09f99-120">The command to run in the container.</span></span>

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

### <span data-ttu-id="09f99-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09f99-121">-Confirm</span></span>
<span data-ttu-id="09f99-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="09f99-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09f99-123">-ЦП</span><span class="sxs-lookup"><span data-stu-id="09f99-123">-Cpu</span></span>
<span data-ttu-id="09f99-124">Требуемые ядра ЦП.</span><span class="sxs-lookup"><span data-stu-id="09f99-124">The required CPU cores.</span></span>
<span data-ttu-id="09f99-125">По умолчанию: 1</span><span class="sxs-lookup"><span data-stu-id="09f99-125">Default: 1</span></span>

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

### <span data-ttu-id="09f99-126">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="09f99-126">-EnvironmentVariable</span></span>
<span data-ttu-id="09f99-127">Переменные среды контейнера.</span><span class="sxs-lookup"><span data-stu-id="09f99-127">The container environment variables.</span></span>

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

### <span data-ttu-id="09f99-128">-Image</span><span class="sxs-lookup"><span data-stu-id="09f99-128">-Image</span></span>
<span data-ttu-id="09f99-129">Изображение контейнера.</span><span class="sxs-lookup"><span data-stu-id="09f99-129">The container image.</span></span>

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

### <span data-ttu-id="09f99-130">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="09f99-130">-IpAddressType</span></span>
<span data-ttu-id="09f99-131">Тип IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="09f99-131">The IP address type.</span></span>

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

### <span data-ttu-id="09f99-132">-Location</span><span class="sxs-lookup"><span data-stu-id="09f99-132">-Location</span></span>
<span data-ttu-id="09f99-133">Расположение группы контейнера.</span><span class="sxs-lookup"><span data-stu-id="09f99-133">The container group Location.</span></span>
<span data-ttu-id="09f99-134">По умолчанию — расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="09f99-134">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="09f99-135">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="09f99-135">-MemoryInGB</span></span>
<span data-ttu-id="09f99-136">Требуемая память в ГБ.</span><span class="sxs-lookup"><span data-stu-id="09f99-136">The required memory in GB.</span></span>
<span data-ttu-id="09f99-137">По умолчанию: 1,5</span><span class="sxs-lookup"><span data-stu-id="09f99-137">Default: 1.5</span></span>

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

### <span data-ttu-id="09f99-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="09f99-138">-Name</span></span>
<span data-ttu-id="09f99-139">Имя группы контейнера.</span><span class="sxs-lookup"><span data-stu-id="09f99-139">The container group name.</span></span>

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

### <span data-ttu-id="09f99-140">-OsType</span><span class="sxs-lookup"><span data-stu-id="09f99-140">-OsType</span></span>
<span data-ttu-id="09f99-141">Тип ОС контейнера.</span><span class="sxs-lookup"><span data-stu-id="09f99-141">The container OS type.</span></span>
<span data-ttu-id="09f99-142">По умолчанию: Linux</span><span class="sxs-lookup"><span data-stu-id="09f99-142">Default: Linux</span></span>

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

### <span data-ttu-id="09f99-143">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="09f99-143">-Port</span></span>
<span data-ttu-id="09f99-144">Открываемый порт.</span><span class="sxs-lookup"><span data-stu-id="09f99-144">The port to open.</span></span>
<span data-ttu-id="09f99-145">По умолчанию: 80</span><span class="sxs-lookup"><span data-stu-id="09f99-145">Default: 80</span></span>

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

### <span data-ttu-id="09f99-146">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="09f99-146">-RegistryCredential</span></span>
<span data-ttu-id="09f99-147">Учетные данные в реестре настраиваемого контейнера.</span><span class="sxs-lookup"><span data-stu-id="09f99-147">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f99-148">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="09f99-148">-RegistryServerDomain</span></span>
<span data-ttu-id="09f99-149">Сервер входа в реестр настраиваемого контейнера.</span><span class="sxs-lookup"><span data-stu-id="09f99-149">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f99-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09f99-150">-ResourceGroupName</span></span>
<span data-ttu-id="09f99-151">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="09f99-151">The resource group name.</span></span>

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

### <span data-ttu-id="09f99-152">-Тег</span><span class="sxs-lookup"><span data-stu-id="09f99-152">-Tag</span></span>
<span data-ttu-id="09f99-153">{{Fill описание тега}}</span><span class="sxs-lookup"><span data-stu-id="09f99-153">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="09f99-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09f99-154">-WhatIf</span></span>
<span data-ttu-id="09f99-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="09f99-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09f99-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="09f99-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09f99-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f99-157">-DefaultProfile</span></span>
<span data-ttu-id="09f99-158">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="09f99-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09f99-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f99-159">CommonParameters</span></span>
<span data-ttu-id="09f99-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09f99-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f99-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09f99-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f99-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09f99-162">INPUTS</span></span>

### <span data-ttu-id="09f99-163">System. String</span><span class="sxs-lookup"><span data-stu-id="09f99-163">System.String</span></span>
<span data-ttu-id="09f99-164">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="09f99-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="09f99-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09f99-165">OUTPUTS</span></span>

### <span data-ttu-id="09f99-166">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="09f99-166">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="09f99-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="09f99-167">NOTES</span></span>

## <span data-ttu-id="09f99-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09f99-168">RELATED LINKS</span></span>

