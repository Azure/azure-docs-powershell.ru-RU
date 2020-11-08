---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: e9f248575d0f5193a11c729384e674870b3de29c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066162"
---
# <span data-ttu-id="0f853-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0f853-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="0f853-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f853-102">SYNOPSIS</span></span>
<span data-ttu-id="0f853-103">Удаление приложения из кластера.</span><span class="sxs-lookup"><span data-stu-id="0f853-103">Remove an application from the cluster.</span></span> <span data-ttu-id="0f853-104">Это приведет к удалению всех служб в приложении.</span><span class="sxs-lookup"><span data-stu-id="0f853-104">This will remove all the services under the application.</span></span>

## <span data-ttu-id="0f853-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f853-105">SYNTAX</span></span>

### <span data-ttu-id="0f853-106">ByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0f853-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f853-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0f853-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f853-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0f853-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f853-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f853-109">DESCRIPTION</span></span>
<span data-ttu-id="0f853-110">Этот командлет удаляет приложение из кластера.</span><span class="sxs-lookup"><span data-stu-id="0f853-110">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="0f853-111">Это приведет к удалению всех служб, если таковые имеются, под ресурсом приложения.</span><span class="sxs-lookup"><span data-stu-id="0f853-111">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="0f853-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f853-112">EXAMPLES</span></span>

### <span data-ttu-id="0f853-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0f853-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="0f853-114">В этом примере удаляется приложение "testApp" в группе ресурсов "testRG" и кластере "testCluster".</span><span class="sxs-lookup"><span data-stu-id="0f853-114">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="0f853-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f853-115">PARAMETERS</span></span>

### <span data-ttu-id="0f853-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="0f853-116">-ClusterName</span></span>
<span data-ttu-id="0f853-117">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="0f853-117">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f853-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f853-118">-DefaultProfile</span></span>
<span data-ttu-id="0f853-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f853-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f853-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0f853-120">-Force</span></span>
<span data-ttu-id="0f853-121">Удалить без запроса.</span><span class="sxs-lookup"><span data-stu-id="0f853-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="0f853-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f853-122">-InputObject</span></span>
<span data-ttu-id="0f853-123">Ресурс приложения.</span><span class="sxs-lookup"><span data-stu-id="0f853-123">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f853-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f853-124">-Name</span></span>
<span data-ttu-id="0f853-125">Укажите имя приложения.</span><span class="sxs-lookup"><span data-stu-id="0f853-125">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f853-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f853-126">-PassThru</span></span>
<span data-ttu-id="0f853-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="0f853-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0f853-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f853-128">-ResourceGroupName</span></span>
<span data-ttu-id="0f853-129">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f853-129">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f853-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f853-130">-ResourceId</span></span>
<span data-ttu-id="0f853-131">ИД ресурса ARM приложения.</span><span class="sxs-lookup"><span data-stu-id="0f853-131">Arm ResourceId of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f853-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f853-132">-Confirm</span></span>
<span data-ttu-id="0f853-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0f853-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f853-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f853-134">-WhatIf</span></span>
<span data-ttu-id="0f853-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0f853-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f853-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0f853-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f853-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f853-137">CommonParameters</span></span>
<span data-ttu-id="0f853-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f853-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f853-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f853-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f853-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f853-140">INPUTS</span></span>

### <span data-ttu-id="0f853-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0f853-141">System.String</span></span>

### <span data-ttu-id="0f853-142">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="0f853-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="0f853-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f853-143">OUTPUTS</span></span>

### <span data-ttu-id="0f853-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0f853-144">System.Boolean</span></span>

## <span data-ttu-id="0f853-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f853-145">NOTES</span></span>

## <span data-ttu-id="0f853-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f853-146">RELATED LINKS</span></span>
