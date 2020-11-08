---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 60065541ecdd8439b67f4370bc1ef8bdc24119bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247533"
---
# <span data-ttu-id="ac088-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ac088-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="ac088-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac088-102">SYNOPSIS</span></span>
<span data-ttu-id="ac088-103">Создать новую версию типа приложения в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="ac088-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="ac088-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac088-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac088-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac088-105">DESCRIPTION</span></span>
<span data-ttu-id="ac088-106">Этот командлет создает новую версию типа приложения с помощью пакета, заданного в параметре-PackageUrl, это должно быть доступно через конечную точку RESTFUL для диспетчера ресурсов Azure, которая может использоваться при развертывании, а также в том случае, если приложение было упаковано и сжато с помощью Extension. sfpkg.</span><span class="sxs-lookup"><span data-stu-id="ac088-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="ac088-107">Эта команда создаст тип приложения, если он еще не существует.</span><span class="sxs-lookup"><span data-stu-id="ac088-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="ac088-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac088-108">EXAMPLES</span></span>

### <span data-ttu-id="ac088-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ac088-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="ac088-110">В этом примере создается версия типа приложения "v1" в разделе Type "testAppType".</span><span class="sxs-lookup"><span data-stu-id="ac088-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="ac088-111">Версия манифеста приложения, содержащегося в пакете, должна иметь ту же версию, что и указанная в версии.</span><span class="sxs-lookup"><span data-stu-id="ac088-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="ac088-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac088-112">PARAMETERS</span></span>

### <span data-ttu-id="ac088-113">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="ac088-113">-ClusterName</span></span>
<span data-ttu-id="ac088-114">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="ac088-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ac088-115">-DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="ac088-115">-DefaultParameter</span></span>
<span data-ttu-id="ac088-116">Укажите значения по умолчанию для параметров приложения в виде пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="ac088-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="ac088-117">Эти параметры должны существовать в манифесте приложения.</span><span class="sxs-lookup"><span data-stu-id="ac088-117">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="ac088-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac088-118">-DefaultProfile</span></span>
<span data-ttu-id="ac088-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac088-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac088-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ac088-120">-Force</span></span>
<span data-ttu-id="ac088-121">Продолжение без запросов</span><span class="sxs-lookup"><span data-stu-id="ac088-121">Continue without prompts</span></span>

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

### <span data-ttu-id="ac088-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ac088-122">-Name</span></span>
<span data-ttu-id="ac088-123">Укажите имя типа приложения.</span><span class="sxs-lookup"><span data-stu-id="ac088-123">Specify the name of the application type</span></span>

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

### <span data-ttu-id="ac088-124">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="ac088-124">-PackageUrl</span></span>
<span data-ttu-id="ac088-125">Укажите URL-адрес файла sfpkg пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="ac088-125">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="ac088-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac088-126">-ResourceGroupName</span></span>
<span data-ttu-id="ac088-127">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ac088-127">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ac088-128">-Version</span><span class="sxs-lookup"><span data-stu-id="ac088-128">-Version</span></span>
<span data-ttu-id="ac088-129">Указание версии типа приложения</span><span class="sxs-lookup"><span data-stu-id="ac088-129">Specify the application type version</span></span>

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

### <span data-ttu-id="ac088-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac088-130">-Confirm</span></span>
<span data-ttu-id="ac088-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ac088-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac088-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac088-132">-WhatIf</span></span>
<span data-ttu-id="ac088-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ac088-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac088-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ac088-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac088-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac088-135">CommonParameters</span></span>
<span data-ttu-id="ac088-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac088-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac088-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac088-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac088-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac088-138">INPUTS</span></span>

### <span data-ttu-id="ac088-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ac088-139">System.String</span></span>

### <span data-ttu-id="ac088-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ac088-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ac088-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac088-141">OUTPUTS</span></span>

### <span data-ttu-id="ac088-142">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ac088-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="ac088-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac088-143">NOTES</span></span>

## <span data-ttu-id="ac088-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac088-144">RELATED LINKS</span></span>
