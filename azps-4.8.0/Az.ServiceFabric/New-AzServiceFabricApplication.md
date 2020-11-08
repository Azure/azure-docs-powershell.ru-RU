---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: 5295caae4ffa0138a1c81fd08a5614f6e636eb41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078725"
---
# <span data-ttu-id="737dd-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="737dd-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="737dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="737dd-102">SYNOPSIS</span></span>
<span data-ttu-id="737dd-103">Создание нового приложения фабрики служб в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="737dd-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="737dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="737dd-104">SYNTAX</span></span>

### <span data-ttu-id="737dd-105">SkipAppTypeVersion (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="737dd-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="737dd-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="737dd-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="737dd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="737dd-107">DESCRIPTION</span></span>
<span data-ttu-id="737dd-108">Этот командлет создает новое приложение фабрики служб в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="737dd-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="737dd-109">Параметр-PackageUrl можно использовать для создания версии Type, если версия типа уже выходит из нее, но в состоянии "сбой" Этот командлет выдаст запрос о том, требуется ли пользователю повторно создать версию типа.</span><span class="sxs-lookup"><span data-stu-id="737dd-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="737dd-110">Если он продолжает работу в состоянии "не пройден", команда прекратит процесс и создаст исключение.</span><span class="sxs-lookup"><span data-stu-id="737dd-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="737dd-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="737dd-111">EXAMPLES</span></span>

### <span data-ttu-id="737dd-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="737dd-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="737dd-113">В этом примере создается приложение "testApp" в группе ресурсов "testRG" и кластере "testCluster".</span><span class="sxs-lookup"><span data-stu-id="737dd-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="737dd-114">Тип приложения "TestAppType" версии "v1" уже должен существовать в кластере, а параметры приложения должны быть заданы в манифесте приложения, в противном случае командлет завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="737dd-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="737dd-115">Пример 2: укажите-PackageUrl, чтобы создать версию типа приложения перед созданием приложения.</span><span class="sxs-lookup"><span data-stu-id="737dd-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="737dd-116">В этом примере создается тип приложения "TestAppType" Version "v1" с помощью указанного URL-адреса пакета.</span><span class="sxs-lookup"><span data-stu-id="737dd-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="737dd-117">После этого она продолжит обычную процедуру для создания приложения.</span><span class="sxs-lookup"><span data-stu-id="737dd-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="737dd-118">Если версия типа приложения уже закрыта, а состояние подготовки — in "Failed", это предложит решить, требуется ли пользователю повторно создать версию типа.</span><span class="sxs-lookup"><span data-stu-id="737dd-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="737dd-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="737dd-119">PARAMETERS</span></span>

### <span data-ttu-id="737dd-120">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="737dd-120">-ApplicationParameter</span></span>
<span data-ttu-id="737dd-121">Укажите параметры приложения в виде пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="737dd-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="737dd-122">Эти параметры должны существовать в манифесте приложения.</span><span class="sxs-lookup"><span data-stu-id="737dd-122">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="737dd-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="737dd-123">-ApplicationTypeName</span></span>
<span data-ttu-id="737dd-124">Укажите имя типа приложения.</span><span class="sxs-lookup"><span data-stu-id="737dd-124">Specify the name of the application type</span></span>

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

### <span data-ttu-id="737dd-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="737dd-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="737dd-126">Указание версии типа приложения</span><span class="sxs-lookup"><span data-stu-id="737dd-126">Specify the application type version</span></span>

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

### <span data-ttu-id="737dd-127">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="737dd-127">-ClusterName</span></span>
<span data-ttu-id="737dd-128">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="737dd-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="737dd-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="737dd-129">-DefaultProfile</span></span>
<span data-ttu-id="737dd-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="737dd-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="737dd-131">-Force</span><span class="sxs-lookup"><span data-stu-id="737dd-131">-Force</span></span>
<span data-ttu-id="737dd-132">Продолжение без запросов</span><span class="sxs-lookup"><span data-stu-id="737dd-132">Continue without prompts</span></span>

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

### <span data-ttu-id="737dd-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="737dd-133">-MaximumNodeCount</span></span>
<span data-ttu-id="737dd-134">Указывает максимальное количество узлов, на которое нужно поместить приложение.</span><span class="sxs-lookup"><span data-stu-id="737dd-134">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737dd-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="737dd-135">-MinimumNodeCount</span></span>
<span data-ttu-id="737dd-136">Указывает минимальное количество узлов, на которое зарезервирована емкость для этого приложения в структуре обслуживания</span><span class="sxs-lookup"><span data-stu-id="737dd-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737dd-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="737dd-137">-Name</span></span>
<span data-ttu-id="737dd-138">Указание имени приложения</span><span class="sxs-lookup"><span data-stu-id="737dd-138">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737dd-139">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="737dd-139">-PackageUrl</span></span>
<span data-ttu-id="737dd-140">Укажите URL-адрес файла sfpkg пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="737dd-140">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAppTypeVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737dd-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="737dd-141">-ResourceGroupName</span></span>
<span data-ttu-id="737dd-142">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="737dd-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="737dd-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="737dd-143">-Confirm</span></span>
<span data-ttu-id="737dd-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="737dd-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="737dd-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="737dd-145">-WhatIf</span></span>
<span data-ttu-id="737dd-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="737dd-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="737dd-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="737dd-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="737dd-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737dd-148">CommonParameters</span></span>
<span data-ttu-id="737dd-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="737dd-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737dd-150">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="737dd-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737dd-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="737dd-151">INPUTS</span></span>

### <span data-ttu-id="737dd-152">System. String</span><span class="sxs-lookup"><span data-stu-id="737dd-152">System.String</span></span>

### <span data-ttu-id="737dd-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="737dd-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="737dd-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="737dd-154">OUTPUTS</span></span>

### <span data-ttu-id="737dd-155">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="737dd-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="737dd-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="737dd-156">NOTES</span></span>

## <span data-ttu-id="737dd-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="737dd-157">RELATED LINKS</span></span>
