---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 1ad1e8220ed77a9206503adaf4f9924f95fe4f44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905282"
---
# <span data-ttu-id="ac388-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ac388-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="ac388-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac388-102">SYNOPSIS</span></span>
<span data-ttu-id="ac388-103">Удаление приложения из кластера.</span><span class="sxs-lookup"><span data-stu-id="ac388-103">Remove an application from the cluster.</span></span> <span data-ttu-id="ac388-104">Это приведет к удалению всех служб в приложении.</span><span class="sxs-lookup"><span data-stu-id="ac388-104">This will remove all the services under the application.</span></span>

## <span data-ttu-id="ac388-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac388-105">SYNTAX</span></span>

### <span data-ttu-id="ac388-106">ByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac388-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac388-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ac388-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac388-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ac388-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac388-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac388-109">DESCRIPTION</span></span>
<span data-ttu-id="ac388-110">Этот командлет удаляет приложение из кластера.</span><span class="sxs-lookup"><span data-stu-id="ac388-110">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="ac388-111">Это приведет к удалению всех служб, если таковые имеются, под ресурсом приложения.</span><span class="sxs-lookup"><span data-stu-id="ac388-111">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="ac388-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac388-112">EXAMPLES</span></span>

### <span data-ttu-id="ac388-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ac388-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="ac388-114">В этом примере удаляется приложение "testApp" в группе ресурсов "testRG" и кластере "testCluster".</span><span class="sxs-lookup"><span data-stu-id="ac388-114">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="ac388-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac388-115">PARAMETERS</span></span>

### <span data-ttu-id="ac388-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="ac388-116">-ClusterName</span></span>
<span data-ttu-id="ac388-117">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="ac388-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ac388-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac388-118">-DefaultProfile</span></span>
<span data-ttu-id="ac388-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac388-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac388-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ac388-120">-Force</span></span>
<span data-ttu-id="ac388-121">Удалить без запроса.</span><span class="sxs-lookup"><span data-stu-id="ac388-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="ac388-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac388-122">-InputObject</span></span>
<span data-ttu-id="ac388-123">Ресурс приложения.</span><span class="sxs-lookup"><span data-stu-id="ac388-123">The application resource.</span></span>

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

### <span data-ttu-id="ac388-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ac388-124">-Name</span></span>
<span data-ttu-id="ac388-125">Укажите имя приложения.</span><span class="sxs-lookup"><span data-stu-id="ac388-125">Specify the name of the application.</span></span>

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

### <span data-ttu-id="ac388-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac388-126">-PassThru</span></span>
<span data-ttu-id="ac388-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="ac388-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ac388-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac388-128">-ResourceGroupName</span></span>
<span data-ttu-id="ac388-129">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ac388-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ac388-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac388-130">-ResourceId</span></span>
<span data-ttu-id="ac388-131">ИД ресурса ARM приложения.</span><span class="sxs-lookup"><span data-stu-id="ac388-131">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="ac388-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac388-132">-Confirm</span></span>
<span data-ttu-id="ac388-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ac388-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac388-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac388-134">-WhatIf</span></span>
<span data-ttu-id="ac388-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ac388-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac388-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ac388-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac388-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac388-137">CommonParameters</span></span>
<span data-ttu-id="ac388-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac388-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac388-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac388-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac388-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac388-140">INPUTS</span></span>

### <span data-ttu-id="ac388-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ac388-141">System.String</span></span>

### <span data-ttu-id="ac388-142">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="ac388-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="ac388-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac388-143">OUTPUTS</span></span>

### <span data-ttu-id="ac388-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ac388-144">System.Boolean</span></span>

## <span data-ttu-id="ac388-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac388-145">NOTES</span></span>

## <span data-ttu-id="ac388-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac388-146">RELATED LINKS</span></span>
