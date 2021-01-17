---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: 5295caae4ffa0138a1c81fd08a5614f6e636eb41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402996"
---
# <span data-ttu-id="22c5d-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="22c5d-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="22c5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22c5d-102">SYNOPSIS</span></span>
<span data-ttu-id="22c5d-103">Создайте новое приложение для создания структуры обслуживания в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="22c5d-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="22c5d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="22c5d-104">SYNTAX</span></span>

### <span data-ttu-id="22c5d-105">SkipAppTypeVersion (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="22c5d-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22c5d-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="22c5d-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22c5d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22c5d-107">DESCRIPTION</span></span>
<span data-ttu-id="22c5d-108">Этот cmdlet создает новое приложение для структуры обслуживания в соответствии с указанной группой ресурсов и кластером.</span><span class="sxs-lookup"><span data-stu-id="22c5d-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="22c5d-109">Параметр -PackageUrl можно использовать для создания версии типа. Если тип версии уже выходит, но его состояние имеет состояние "Сбой", будет выдан запрос на повторное создание версии типа.</span><span class="sxs-lookup"><span data-stu-id="22c5d-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="22c5d-110">Если процесс продолжится в состоянии "Сбой", команда остановит процесс и выкает исключение.</span><span class="sxs-lookup"><span data-stu-id="22c5d-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="22c5d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="22c5d-111">EXAMPLES</span></span>

### <span data-ttu-id="22c5d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="22c5d-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="22c5d-113">В этом примере приложение testApp создается в группе ресурсов testRG и кластере testCluster.</span><span class="sxs-lookup"><span data-stu-id="22c5d-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="22c5d-114">Тип приложения TestAppType версии v1 уже должен существовать в кластере, а параметры приложения должны быть определены в манифесте приложения. В противном случае сбой cmdlet не удастся.</span><span class="sxs-lookup"><span data-stu-id="22c5d-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="22c5d-115">Пример 2. Укажите -PackageUrl, чтобы создать версию типа приложения перед его созданием.</span><span class="sxs-lookup"><span data-stu-id="22c5d-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="22c5d-116">В этом примере создается тип приложения TestAppType версии v1, используя предоставленный URL-адрес пакета.</span><span class="sxs-lookup"><span data-stu-id="22c5d-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="22c5d-117">После этого создание приложения будет продолжаться как обычный процесс.</span><span class="sxs-lookup"><span data-stu-id="22c5d-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="22c5d-118">Если версия типа приложения уже выходит из приложения и ее подготовка имеет состояние "Сбой", пользователю будет предложено решить, захочет ли пользователь повторно создать ее.</span><span class="sxs-lookup"><span data-stu-id="22c5d-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="22c5d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22c5d-119">PARAMETERS</span></span>

### <span data-ttu-id="22c5d-120">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="22c5d-120">-ApplicationParameter</span></span>
<span data-ttu-id="22c5d-121">Укажите параметры приложения в качестве пар ключа и значения.</span><span class="sxs-lookup"><span data-stu-id="22c5d-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="22c5d-122">Эти параметры должны существовать в манифесте приложения.</span><span class="sxs-lookup"><span data-stu-id="22c5d-122">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="22c5d-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="22c5d-123">-ApplicationTypeName</span></span>
<span data-ttu-id="22c5d-124">Указание имени типа приложения</span><span class="sxs-lookup"><span data-stu-id="22c5d-124">Specify the name of the application type</span></span>

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

### <span data-ttu-id="22c5d-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="22c5d-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="22c5d-126">Указание версии типа приложения</span><span class="sxs-lookup"><span data-stu-id="22c5d-126">Specify the application type version</span></span>

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

### <span data-ttu-id="22c5d-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="22c5d-127">-ClusterName</span></span>
<span data-ttu-id="22c5d-128">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="22c5d-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="22c5d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22c5d-129">-DefaultProfile</span></span>
<span data-ttu-id="22c5d-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22c5d-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22c5d-131">-Force</span><span class="sxs-lookup"><span data-stu-id="22c5d-131">-Force</span></span>
<span data-ttu-id="22c5d-132">Продолжить без запроса</span><span class="sxs-lookup"><span data-stu-id="22c5d-132">Continue without prompts</span></span>

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

### <span data-ttu-id="22c5d-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="22c5d-133">-MaximumNodeCount</span></span>
<span data-ttu-id="22c5d-134">Указывает максимальное количество узлов, на которых нужно разместить приложение.</span><span class="sxs-lookup"><span data-stu-id="22c5d-134">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="22c5d-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="22c5d-135">-MinimumNodeCount</span></span>
<span data-ttu-id="22c5d-136">Указывает минимальное количество узлов, где "Сервисная ткань" будет резервировать мощность для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="22c5d-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="22c5d-137">-Name</span><span class="sxs-lookup"><span data-stu-id="22c5d-137">-Name</span></span>
<span data-ttu-id="22c5d-138">Укажите имя приложения</span><span class="sxs-lookup"><span data-stu-id="22c5d-138">Specify the name of the application</span></span>

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

### <span data-ttu-id="22c5d-139">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="22c5d-139">-PackageUrl</span></span>
<span data-ttu-id="22c5d-140">Укажите URL-адрес SFPKG-файла пакета приложения</span><span class="sxs-lookup"><span data-stu-id="22c5d-140">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="22c5d-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22c5d-141">-ResourceGroupName</span></span>
<span data-ttu-id="22c5d-142">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="22c5d-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="22c5d-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22c5d-143">-Confirm</span></span>
<span data-ttu-id="22c5d-144">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22c5d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22c5d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22c5d-145">-WhatIf</span></span>
<span data-ttu-id="22c5d-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22c5d-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22c5d-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="22c5d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22c5d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c5d-148">CommonParameters</span></span>
<span data-ttu-id="22c5d-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22c5d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c5d-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22c5d-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c5d-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22c5d-151">INPUTS</span></span>

### <span data-ttu-id="22c5d-152">System.String</span><span class="sxs-lookup"><span data-stu-id="22c5d-152">System.String</span></span>

### <span data-ttu-id="22c5d-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="22c5d-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="22c5d-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="22c5d-154">OUTPUTS</span></span>

### <span data-ttu-id="22c5d-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="22c5d-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="22c5d-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="22c5d-156">NOTES</span></span>

## <span data-ttu-id="22c5d-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22c5d-157">RELATED LINKS</span></span>
