---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
ms.openlocfilehash: 1de3cef0d14213a52873742f9bf878aaa545e8bf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728204"
---
# <span data-ttu-id="46136-101">New-AzAks</span><span class="sxs-lookup"><span data-stu-id="46136-101">New-AzAks</span></span>

## <span data-ttu-id="46136-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46136-102">SYNOPSIS</span></span>
<span data-ttu-id="46136-103">Создание нового управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="46136-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="46136-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46136-104">SYNTAX</span></span>

```
New-AzAks [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46136-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46136-105">DESCRIPTION</span></span>

<span data-ttu-id="46136-106">Создание нового управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="46136-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="46136-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46136-107">EXAMPLES</span></span>

### <span data-ttu-id="46136-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="46136-108">Example 1</span></span>

<span data-ttu-id="46136-109">Создание нового управляемого кластера Kubernetes с помощью параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46136-109">Create a new managed Kubernetes cluster with default params.</span></span>

```
PS C:\> New-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="46136-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46136-110">PARAMETERS</span></span>

### <span data-ttu-id="46136-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="46136-111">-AdminUserName</span></span>
<span data-ttu-id="46136-112">Имя пользователя для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="46136-112">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="46136-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46136-113">-AsJob</span></span>
<span data-ttu-id="46136-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="46136-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46136-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="46136-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="46136-116">Идентификатор клиента и секрет клиента, связанные с приложением или участником-службой AAD.</span><span class="sxs-lookup"><span data-stu-id="46136-116">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46136-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46136-117">-DefaultProfile</span></span>
<span data-ttu-id="46136-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46136-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46136-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="46136-119">-DnsNamePrefix</span></span>
<span data-ttu-id="46136-120">Префикс DNS-имени для кластера.</span><span class="sxs-lookup"><span data-stu-id="46136-120">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="46136-121">-Force</span><span class="sxs-lookup"><span data-stu-id="46136-121">-Force</span></span>
<span data-ttu-id="46136-122">Создать кластер, даже если он уже существует</span><span class="sxs-lookup"><span data-stu-id="46136-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="46136-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="46136-123">-KubernetesVersion</span></span>
<span data-ttu-id="46136-124">Версия Kubernetes, используемая для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="46136-124">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="46136-125">-Location</span><span class="sxs-lookup"><span data-stu-id="46136-125">-Location</span></span>
<span data-ttu-id="46136-126">Расположение Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="46136-126">Azure location for the cluster.</span></span>
<span data-ttu-id="46136-127">По умолчанию — расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46136-127">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="46136-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="46136-128">-Name</span></span>
<span data-ttu-id="46136-129">Имя управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="46136-129">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46136-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="46136-130">-NodeCount</span></span>
<span data-ttu-id="46136-131">Количество узлов, используемое по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="46136-131">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="46136-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="46136-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="46136-133">Размер диска операционной системы (ГБ) для каждого узла в пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="46136-133">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="46136-134">Минимум 30 ГБ.</span><span class="sxs-lookup"><span data-stu-id="46136-134">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="46136-135">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="46136-135">-NodeVmSize</span></span>
<span data-ttu-id="46136-136">Размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="46136-136">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="46136-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46136-137">-ResourceGroupName</span></span>
<span data-ttu-id="46136-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46136-138">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46136-139">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="46136-139">-SshKeyValue</span></span>
<span data-ttu-id="46136-140">Значение файла ключа SSH или путь к файлу ключа.</span><span class="sxs-lookup"><span data-stu-id="46136-140">SSH key file value or key file path.</span></span>
<span data-ttu-id="46136-141">По умолчанию: {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="46136-141">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="46136-142">-Тег</span><span class="sxs-lookup"><span data-stu-id="46136-142">-Tag</span></span>
<span data-ttu-id="46136-143">Теги, применяемые к ресурсу</span><span class="sxs-lookup"><span data-stu-id="46136-143">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="46136-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46136-144">-Confirm</span></span>
<span data-ttu-id="46136-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="46136-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46136-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46136-146">-WhatIf</span></span>
<span data-ttu-id="46136-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="46136-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46136-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="46136-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46136-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46136-149">CommonParameters</span></span>
<span data-ttu-id="46136-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46136-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46136-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46136-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46136-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46136-152">INPUTS</span></span>

### <span data-ttu-id="46136-153">Ничего</span><span class="sxs-lookup"><span data-stu-id="46136-153">None</span></span>

## <span data-ttu-id="46136-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46136-154">OUTPUTS</span></span>

### <span data-ttu-id="46136-155">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="46136-155">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="46136-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="46136-156">NOTES</span></span>

## <span data-ttu-id="46136-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46136-157">RELATED LINKS</span></span>
