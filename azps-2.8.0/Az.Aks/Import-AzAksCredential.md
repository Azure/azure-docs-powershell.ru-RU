---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/import-azakscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
ms.openlocfilehash: bcc0a4f39b2c5578213aeb3ea5087ce1cc21cc4f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728207"
---
# <span data-ttu-id="26abe-101">Import-AzAksCredential</span><span class="sxs-lookup"><span data-stu-id="26abe-101">Import-AzAksCredential</span></span>

## <span data-ttu-id="26abe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26abe-102">SYNOPSIS</span></span>
<span data-ttu-id="26abe-103">Импорт и слияние конфигурации Kubectl для управляемого Kubernetes кластера.</span><span class="sxs-lookup"><span data-stu-id="26abe-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="26abe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26abe-104">SYNTAX</span></span>

### <span data-ttu-id="26abe-105">GroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="26abe-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26abe-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26abe-106">InputObjectParameterSet</span></span>
```
Import-AzAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26abe-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26abe-107">IdParameterSet</span></span>
```
Import-AzAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26abe-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26abe-108">DESCRIPTION</span></span>
<span data-ttu-id="26abe-109">Импорт и слияние конфигурации Kubectl для управляемого Kubernetes кластера.</span><span class="sxs-lookup"><span data-stu-id="26abe-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="26abe-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26abe-110">EXAMPLES</span></span>

### <span data-ttu-id="26abe-111">Импорт и слияние Kubectl конфигурации</span><span class="sxs-lookup"><span data-stu-id="26abe-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="26abe-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26abe-112">PARAMETERS</span></span>

### <span data-ttu-id="26abe-113">-Администратор</span><span class="sxs-lookup"><span data-stu-id="26abe-113">-Admin</span></span>
<span data-ttu-id="26abe-114">Получить clusterAdmin' kubectl config вместо значения по умолчанию "clusterUser".</span><span class="sxs-lookup"><span data-stu-id="26abe-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="26abe-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="26abe-115">-ConfigPath</span></span>
<span data-ttu-id="26abe-116">Файл конфигурации kubectl для создания или обновления.</span><span class="sxs-lookup"><span data-stu-id="26abe-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="26abe-117">Используйте "-", чтобы вывести YAML в stdout.</span><span class="sxs-lookup"><span data-stu-id="26abe-117">Use '-' to print YAML to stdout instead.</span></span>
<span data-ttu-id="26abe-118">По умолчанию:% Home%/.KUBE/config.</span><span class="sxs-lookup"><span data-stu-id="26abe-118">Default: %Home%/.kube/config.</span></span>

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

### <span data-ttu-id="26abe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26abe-119">-DefaultProfile</span></span>
<span data-ttu-id="26abe-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26abe-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26abe-121">-Force</span><span class="sxs-lookup"><span data-stu-id="26abe-121">-Force</span></span>
<span data-ttu-id="26abe-122">Импортировать конфигурацию Kubernetes, даже если она используется по умолчанию</span><span class="sxs-lookup"><span data-stu-id="26abe-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="26abe-123">-ID</span><span class="sxs-lookup"><span data-stu-id="26abe-123">-Id</span></span>
<span data-ttu-id="26abe-124">Идентификатор управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="26abe-124">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="26abe-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26abe-125">-InputObject</span></span>
<span data-ttu-id="26abe-126">Объект PSKubernetesCluster, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="26abe-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="26abe-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="26abe-127">-Name</span></span>
<span data-ttu-id="26abe-128">Имя управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="26abe-128">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="26abe-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26abe-129">-PassThru</span></span>
<span data-ttu-id="26abe-130">Возвращает значение истина, если импорт выполнен успешно</span><span class="sxs-lookup"><span data-stu-id="26abe-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="26abe-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26abe-131">-ResourceGroupName</span></span>
<span data-ttu-id="26abe-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="26abe-132">Resource group name</span></span>

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

### <span data-ttu-id="26abe-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26abe-133">-Confirm</span></span>
<span data-ttu-id="26abe-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="26abe-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26abe-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26abe-135">-WhatIf</span></span>
<span data-ttu-id="26abe-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="26abe-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26abe-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="26abe-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26abe-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26abe-138">CommonParameters</span></span>
<span data-ttu-id="26abe-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26abe-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26abe-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26abe-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26abe-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26abe-141">INPUTS</span></span>

### <span data-ttu-id="26abe-142">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="26abe-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="26abe-143">System. String</span><span class="sxs-lookup"><span data-stu-id="26abe-143">System.String</span></span>

## <span data-ttu-id="26abe-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26abe-144">OUTPUTS</span></span>

### <span data-ttu-id="26abe-145">System. String</span><span class="sxs-lookup"><span data-stu-id="26abe-145">System.String</span></span>

## <span data-ttu-id="26abe-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="26abe-146">NOTES</span></span>

## <span data-ttu-id="26abe-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26abe-147">RELATED LINKS</span></span>
