---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/set-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Set-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Set-AzureRmAks.md
ms.openlocfilehash: b5d3248c81507abf6092aa4354691975c4b4bc13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561288"
---
# <span data-ttu-id="13a43-101">Set-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="13a43-101">Set-AzureRmAks</span></span>

## <span data-ttu-id="13a43-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13a43-102">SYNOPSIS</span></span>
<span data-ttu-id="13a43-103">Обновите или создайте управляемый кластер Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="13a43-103">Update or create a managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13a43-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13a43-104">SYNTAX</span></span>

### <span data-ttu-id="13a43-105">defaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="13a43-105">defaultParameterSet (Default)</span></span>
```
Set-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13a43-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13a43-106">InputObjectParameterSet</span></span>
```
Set-AzureRmAks -InputObject <PSKubernetesCluster> [-Location <String>] [-AdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13a43-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="13a43-107">IdParameterSet</span></span>
```
Set-AzureRmAks [-Id] <String> [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13a43-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13a43-108">DESCRIPTION</span></span>
<span data-ttu-id="13a43-109">Обновите или создайте управляемый кластер Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="13a43-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="13a43-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13a43-110">EXAMPLES</span></span>

### <span data-ttu-id="13a43-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="13a43-111">Example 1</span></span>
```
PS C:\> Get-AzureRmAks -ResourceGroupName group -Name myCluster | Set-AzureRmAks -NodeCount 5
```

<span data-ttu-id="13a43-112">Установите количество узлов в кластере Kubernetes равным 5.</span><span class="sxs-lookup"><span data-stu-id="13a43-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="13a43-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13a43-113">PARAMETERS</span></span>

### <span data-ttu-id="13a43-114">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="13a43-114">-AdminUserName</span></span>
<span data-ttu-id="13a43-115">Имя пользователя для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="13a43-115">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="13a43-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13a43-116">-AsJob</span></span>
<span data-ttu-id="13a43-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="13a43-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13a43-118">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="13a43-118">-ClientIdAndSecret</span></span>
<span data-ttu-id="13a43-119">Идентификатор клиента и секрет клиента, связанные с приложением или участником-службой AAD.</span><span class="sxs-lookup"><span data-stu-id="13a43-119">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: defaultParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a43-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13a43-120">-DefaultProfile</span></span>
<span data-ttu-id="13a43-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13a43-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13a43-122">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="13a43-122">-DnsNamePrefix</span></span>
<span data-ttu-id="13a43-123">Префикс DNS-имени для кластера.</span><span class="sxs-lookup"><span data-stu-id="13a43-123">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="13a43-124">-ID</span><span class="sxs-lookup"><span data-stu-id="13a43-124">-Id</span></span>
<span data-ttu-id="13a43-125">Идентификатор управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="13a43-125">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="13a43-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13a43-126">-InputObject</span></span>
<span data-ttu-id="13a43-127">Объект PSKubernetesCluster, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="13a43-127">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="13a43-128">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="13a43-128">-KubernetesVersion</span></span>
<span data-ttu-id="13a43-129">Версия Kubernetes, используемая для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="13a43-129">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="13a43-130">-Location</span><span class="sxs-lookup"><span data-stu-id="13a43-130">-Location</span></span>
<span data-ttu-id="13a43-131">Расположение Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="13a43-131">Azure location for the cluster.</span></span>
<span data-ttu-id="13a43-132">По умолчанию — расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13a43-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="13a43-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13a43-133">-Name</span></span>
<span data-ttu-id="13a43-134">Имя управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="13a43-134">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a43-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="13a43-135">-NodeCount</span></span>
<span data-ttu-id="13a43-136">Количество узлов, используемое по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="13a43-136">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a43-137">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="13a43-137">-NodeOsDiskSize</span></span>
<span data-ttu-id="13a43-138">Количество узлов, используемое по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="13a43-138">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a43-139">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="13a43-139">-NodeVmSize</span></span>
<span data-ttu-id="13a43-140">Размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="13a43-140">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="13a43-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13a43-141">-ResourceGroupName</span></span>
<span data-ttu-id="13a43-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13a43-142">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a43-143">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="13a43-143">-SshKeyValue</span></span>
<span data-ttu-id="13a43-144">Значение файла ключа SSH или путь к файлу ключа.</span><span class="sxs-lookup"><span data-stu-id="13a43-144">SSH key file value or key file path.</span></span>
<span data-ttu-id="13a43-145">По умолчанию: {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="13a43-145">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a43-146">-Тег</span><span class="sxs-lookup"><span data-stu-id="13a43-146">-Tag</span></span>
<span data-ttu-id="13a43-147">Теги, применяемые к ресурсу</span><span class="sxs-lookup"><span data-stu-id="13a43-147">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="13a43-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13a43-148">-Confirm</span></span>
<span data-ttu-id="13a43-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="13a43-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13a43-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13a43-150">-WhatIf</span></span>
<span data-ttu-id="13a43-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="13a43-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13a43-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="13a43-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13a43-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a43-153">CommonParameters</span></span>
<span data-ttu-id="13a43-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13a43-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a43-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13a43-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a43-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13a43-156">INPUTS</span></span>

### <span data-ttu-id="13a43-157">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="13a43-157">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="13a43-158">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="13a43-158">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="13a43-159">System. String</span><span class="sxs-lookup"><span data-stu-id="13a43-159">System.String</span></span>

## <span data-ttu-id="13a43-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13a43-160">OUTPUTS</span></span>

### <span data-ttu-id="13a43-161">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="13a43-161">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="13a43-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="13a43-162">NOTES</span></span>

## <span data-ttu-id="13a43-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13a43-163">RELATED LINKS</span></span>
