---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 60065541ecdd8439b67f4370bc1ef8bdc24119bc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517249"
---
# <span data-ttu-id="76fe6-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="76fe6-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="76fe6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76fe6-102">SYNOPSIS</span></span>
<span data-ttu-id="76fe6-103">Создайте новую версию типа приложения в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="76fe6-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="76fe6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="76fe6-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76fe6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76fe6-105">DESCRIPTION</span></span>
<span data-ttu-id="76fe6-106">Этот cmdlet создает новую версию приложения с пакетом, указанным в -PackageUrl. Он должен быть доступен через конечную точку REST диспетчера ресурсов Azure, используемую во время развертывания. Приложение было упаковано и запаковлено с расширением SFPKG.</span><span class="sxs-lookup"><span data-stu-id="76fe6-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="76fe6-107">Эта команда создает тип приложения, если он еще не существует.</span><span class="sxs-lookup"><span data-stu-id="76fe6-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="76fe6-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="76fe6-108">EXAMPLES</span></span>

### <span data-ttu-id="76fe6-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="76fe6-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="76fe6-110">В этом примере создается версия приложения "v1" в типе testAppType.</span><span class="sxs-lookup"><span data-stu-id="76fe6-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="76fe6-111">Версия манифеста приложения, содержалась в пакете, должна иметь ту же версию, что и в -Version.</span><span class="sxs-lookup"><span data-stu-id="76fe6-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="76fe6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76fe6-112">PARAMETERS</span></span>

### <span data-ttu-id="76fe6-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="76fe6-113">-ClusterName</span></span>
<span data-ttu-id="76fe6-114">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="76fe6-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="76fe6-115">-DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="76fe6-115">-DefaultParameter</span></span>
<span data-ttu-id="76fe6-116">Укажите значения по умолчанию для параметров приложения в качестве пар ключа и значения.</span><span class="sxs-lookup"><span data-stu-id="76fe6-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="76fe6-117">Эти параметры должны существовать в манифесте приложения.</span><span class="sxs-lookup"><span data-stu-id="76fe6-117">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="76fe6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76fe6-118">-DefaultProfile</span></span>
<span data-ttu-id="76fe6-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76fe6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76fe6-120">-Force</span><span class="sxs-lookup"><span data-stu-id="76fe6-120">-Force</span></span>
<span data-ttu-id="76fe6-121">Продолжить без запроса</span><span class="sxs-lookup"><span data-stu-id="76fe6-121">Continue without prompts</span></span>

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

### <span data-ttu-id="76fe6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="76fe6-122">-Name</span></span>
<span data-ttu-id="76fe6-123">Указание имени типа приложения</span><span class="sxs-lookup"><span data-stu-id="76fe6-123">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fe6-124">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="76fe6-124">-PackageUrl</span></span>
<span data-ttu-id="76fe6-125">Укажите URL-адрес SFPKG-файла пакета приложения</span><span class="sxs-lookup"><span data-stu-id="76fe6-125">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76fe6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76fe6-126">-ResourceGroupName</span></span>
<span data-ttu-id="76fe6-127">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76fe6-127">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="76fe6-128">-Версия</span><span class="sxs-lookup"><span data-stu-id="76fe6-128">-Version</span></span>
<span data-ttu-id="76fe6-129">Указание версии типа приложения</span><span class="sxs-lookup"><span data-stu-id="76fe6-129">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fe6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76fe6-130">-Confirm</span></span>
<span data-ttu-id="76fe6-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="76fe6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76fe6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76fe6-132">-WhatIf</span></span>
<span data-ttu-id="76fe6-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76fe6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76fe6-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="76fe6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76fe6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76fe6-135">CommonParameters</span></span>
<span data-ttu-id="76fe6-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76fe6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76fe6-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76fe6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76fe6-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76fe6-138">INPUTS</span></span>

### <span data-ttu-id="76fe6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="76fe6-139">System.String</span></span>

### <span data-ttu-id="76fe6-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="76fe6-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="76fe6-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="76fe6-141">OUTPUTS</span></span>

### <span data-ttu-id="76fe6-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="76fe6-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="76fe6-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="76fe6-143">NOTES</span></span>

## <span data-ttu-id="76fe6-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76fe6-144">RELATED LINKS</span></span>
