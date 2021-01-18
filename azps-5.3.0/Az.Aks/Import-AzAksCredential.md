---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/import-azakscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
ms.openlocfilehash: fe4e56e809dd2cda7c650e24b55ae3867a23a7b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506994"
---
# <span data-ttu-id="75dd5-101">Import-AzAksCredential</span><span class="sxs-lookup"><span data-stu-id="75dd5-101">Import-AzAksCredential</span></span>

## <span data-ttu-id="75dd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="75dd5-103">Импорт и слияние config Kubectl для управляемого кластера Куберсетей.</span><span class="sxs-lookup"><span data-stu-id="75dd5-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="75dd5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="75dd5-104">SYNTAX</span></span>

### <span data-ttu-id="75dd5-105">GroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75dd5-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75dd5-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75dd5-106">InputObjectParameterSet</span></span>
```
Import-AzAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75dd5-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75dd5-107">IdParameterSet</span></span>
```
Import-AzAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75dd5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75dd5-108">DESCRIPTION</span></span>
<span data-ttu-id="75dd5-109">Импорт и слияние config Kubectl для управляемого кластера Куберсетей.</span><span class="sxs-lookup"><span data-stu-id="75dd5-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="75dd5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="75dd5-110">EXAMPLES</span></span>

### <span data-ttu-id="75dd5-111">Импорт и слияние config Kubectl</span><span class="sxs-lookup"><span data-stu-id="75dd5-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="75dd5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75dd5-112">PARAMETERS</span></span>

### <span data-ttu-id="75dd5-113">-Администратор</span><span class="sxs-lookup"><span data-stu-id="75dd5-113">-Admin</span></span>
<span data-ttu-id="75dd5-114">Получите "clusterAdmin" kubectl config вместо "clusterUser" по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="75dd5-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="75dd5-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="75dd5-115">-ConfigPath</span></span>
<span data-ttu-id="75dd5-116">A kubectl config file to create or update.</span><span class="sxs-lookup"><span data-stu-id="75dd5-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="75dd5-117">Вместо этого используйте "-", чтобы напечатать YAML для распечатки.</span><span class="sxs-lookup"><span data-stu-id="75dd5-117">Use '-' to print YAML to stdout instead.</span></span>
<span data-ttu-id="75dd5-118">По умолчанию: %Home%/.kube/config.</span><span class="sxs-lookup"><span data-stu-id="75dd5-118">Default: %Home%/.kube/config.</span></span>

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

### <span data-ttu-id="75dd5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75dd5-119">-DefaultProfile</span></span>
<span data-ttu-id="75dd5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75dd5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75dd5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="75dd5-121">-Force</span></span>
<span data-ttu-id="75dd5-122">Импортировать config из Kubernetes, даже если он является стандартным</span><span class="sxs-lookup"><span data-stu-id="75dd5-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="75dd5-123">-Id</span><span class="sxs-lookup"><span data-stu-id="75dd5-123">-Id</span></span>
<span data-ttu-id="75dd5-124">ИД кластера управляемых кубарныхсетей</span><span class="sxs-lookup"><span data-stu-id="75dd5-124">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75dd5-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75dd5-125">-InputObject</span></span>
<span data-ttu-id="75dd5-126">Объект PSKubernetesCluster, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="75dd5-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75dd5-127">-Name</span><span class="sxs-lookup"><span data-stu-id="75dd5-127">-Name</span></span>
<span data-ttu-id="75dd5-128">Название кластера "Кубберсети"</span><span class="sxs-lookup"><span data-stu-id="75dd5-128">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75dd5-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75dd5-129">-PassThru</span></span>
<span data-ttu-id="75dd5-130">Возвращает "Истина" в случае успешного импорта.</span><span class="sxs-lookup"><span data-stu-id="75dd5-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="75dd5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75dd5-131">-ResourceGroupName</span></span>
<span data-ttu-id="75dd5-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="75dd5-132">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75dd5-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75dd5-133">-Confirm</span></span>
<span data-ttu-id="75dd5-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="75dd5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75dd5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75dd5-135">-WhatIf</span></span>
<span data-ttu-id="75dd5-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75dd5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75dd5-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="75dd5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75dd5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75dd5-138">CommonParameters</span></span>
<span data-ttu-id="75dd5-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75dd5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75dd5-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75dd5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75dd5-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75dd5-141">INPUTS</span></span>

### <span data-ttu-id="75dd5-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="75dd5-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="75dd5-143">System.String</span><span class="sxs-lookup"><span data-stu-id="75dd5-143">System.String</span></span>

## <span data-ttu-id="75dd5-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="75dd5-144">OUTPUTS</span></span>

### <span data-ttu-id="75dd5-145">System.String</span><span class="sxs-lookup"><span data-stu-id="75dd5-145">System.String</span></span>

## <span data-ttu-id="75dd5-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="75dd5-146">NOTES</span></span>

## <span data-ttu-id="75dd5-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75dd5-147">RELATED LINKS</span></span>
