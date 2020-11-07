---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/new-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
ms.openlocfilehash: f91b4f2afdb1c6aaf7cbac16f952a333d3d362b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733518"
---
# <span data-ttu-id="497d6-101">New-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="497d6-101">New-AzureRmAks</span></span>

## <span data-ttu-id="497d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="497d6-102">SYNOPSIS</span></span>
<span data-ttu-id="497d6-103">Создание нового управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="497d6-103">Create a new managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="497d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="497d6-104">SYNTAX</span></span>

```
New-AzureRmAks [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="497d6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="497d6-105">DESCRIPTION</span></span>

<span data-ttu-id="497d6-106">Создание нового управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="497d6-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="497d6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="497d6-107">EXAMPLES</span></span>

### <span data-ttu-id="497d6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="497d6-108">Example 1</span></span>

<span data-ttu-id="497d6-109">Создание нового управляемого кластера Kubernetes с помощью параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="497d6-109">Create a new managed Kubernetes cluster with default params.</span></span>

```
PS C:\> New-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="497d6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="497d6-110">PARAMETERS</span></span>

### <span data-ttu-id="497d6-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="497d6-111">-AdminUserName</span></span>
<span data-ttu-id="497d6-112">Имя пользователя для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="497d6-112">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="497d6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="497d6-113">-AsJob</span></span>
<span data-ttu-id="497d6-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="497d6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="497d6-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="497d6-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="497d6-116">Идентификатор клиента и секрет клиента, связанные с приложением или участником-службой AAD.</span><span class="sxs-lookup"><span data-stu-id="497d6-116">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="497d6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="497d6-117">-DefaultProfile</span></span>
<span data-ttu-id="497d6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="497d6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="497d6-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="497d6-119">-DnsNamePrefix</span></span>
<span data-ttu-id="497d6-120">Префикс DNS-имени для кластера.</span><span class="sxs-lookup"><span data-stu-id="497d6-120">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="497d6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="497d6-121">-Force</span></span>
<span data-ttu-id="497d6-122">Создать кластер, даже если он уже существует</span><span class="sxs-lookup"><span data-stu-id="497d6-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="497d6-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="497d6-123">-KubernetesVersion</span></span>
<span data-ttu-id="497d6-124">Версия Kubernetes, используемая для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="497d6-124">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="497d6-125">-Location</span><span class="sxs-lookup"><span data-stu-id="497d6-125">-Location</span></span>
<span data-ttu-id="497d6-126">Расположение Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="497d6-126">Azure location for the cluster.</span></span>
<span data-ttu-id="497d6-127">По умолчанию — расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="497d6-127">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="497d6-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="497d6-128">-Name</span></span>
<span data-ttu-id="497d6-129">Имя управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="497d6-129">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="497d6-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="497d6-130">-NodeCount</span></span>
<span data-ttu-id="497d6-131">Количество узлов, используемое по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="497d6-131">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="497d6-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="497d6-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="497d6-133">Размер диска операционной системы (ГБ) для каждого узла в пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="497d6-133">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="497d6-134">Минимум 30 ГБ.</span><span class="sxs-lookup"><span data-stu-id="497d6-134">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="497d6-135">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="497d6-135">-NodeVmSize</span></span>
<span data-ttu-id="497d6-136">Размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="497d6-136">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="497d6-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="497d6-137">-ResourceGroupName</span></span>
<span data-ttu-id="497d6-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="497d6-138">Resource Group Name.</span></span>

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

### <span data-ttu-id="497d6-139">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="497d6-139">-SshKeyValue</span></span>
<span data-ttu-id="497d6-140">Значение файла ключа SSH или путь к файлу ключа.</span><span class="sxs-lookup"><span data-stu-id="497d6-140">SSH key file value or key file path.</span></span>
<span data-ttu-id="497d6-141">По умолчанию: {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="497d6-141">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="497d6-142">-Тег</span><span class="sxs-lookup"><span data-stu-id="497d6-142">-Tag</span></span>
<span data-ttu-id="497d6-143">Теги, применяемые к ресурсу</span><span class="sxs-lookup"><span data-stu-id="497d6-143">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="497d6-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="497d6-144">-Confirm</span></span>
<span data-ttu-id="497d6-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="497d6-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="497d6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="497d6-146">-WhatIf</span></span>
<span data-ttu-id="497d6-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="497d6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="497d6-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="497d6-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="497d6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="497d6-149">CommonParameters</span></span>
<span data-ttu-id="497d6-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="497d6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="497d6-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="497d6-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="497d6-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="497d6-152">INPUTS</span></span>

### <span data-ttu-id="497d6-153">Ничего</span><span class="sxs-lookup"><span data-stu-id="497d6-153">None</span></span>

## <span data-ttu-id="497d6-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="497d6-154">OUTPUTS</span></span>

### <span data-ttu-id="497d6-155">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="497d6-155">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="497d6-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="497d6-156">NOTES</span></span>

## <span data-ttu-id="497d6-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="497d6-157">RELATED LINKS</span></span>
