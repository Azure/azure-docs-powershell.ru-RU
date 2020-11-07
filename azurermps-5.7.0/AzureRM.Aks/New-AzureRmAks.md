---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/new-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
ms.openlocfilehash: ed68271ae29c7af0219fa08d1c342b636d7d3fbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734500"
---
# <span data-ttu-id="b9b52-101">New-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="b9b52-101">New-AzureRmAks</span></span>

## <span data-ttu-id="b9b52-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9b52-102">SYNOPSIS</span></span>
<span data-ttu-id="b9b52-103">Создание нового управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="b9b52-103">Create a new managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9b52-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9b52-104">SYNTAX</span></span>

```
New-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-Force] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9b52-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9b52-105">DESCRIPTION</span></span>
<span data-ttu-id="b9b52-106">Создание нового управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="b9b52-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="b9b52-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9b52-107">EXAMPLES</span></span>

### <span data-ttu-id="b9b52-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b9b52-108">Example 1</span></span>
<span data-ttu-id="b9b52-109">Создание нового управляемого кластера Kubernetes с помощью параметров по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b9b52-109">Create a new managed Kubernetes cluster with default params</span></span>

```
PS C:\> New-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="b9b52-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9b52-110">PARAMETERS</span></span>

### <span data-ttu-id="b9b52-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="b9b52-111">-AdminUserName</span></span>
<span data-ttu-id="b9b52-112">Имя пользователя для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="b9b52-112">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b52-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9b52-113">-AsJob</span></span>
<span data-ttu-id="b9b52-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b9b52-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b52-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="b9b52-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="b9b52-116">Идентификатор клиента и секрет клиента, связанные с приложением или участником-службой AAD.</span><span class="sxs-lookup"><span data-stu-id="b9b52-116">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b52-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9b52-117">-DefaultProfile</span></span>
<span data-ttu-id="b9b52-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9b52-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b52-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="b9b52-119">-DnsNamePrefix</span></span>
<span data-ttu-id="b9b52-120">Префикс DNS-имени для кластера.</span><span class="sxs-lookup"><span data-stu-id="b9b52-120">The DNS name prefix for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b52-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b9b52-121">-Force</span></span>
<span data-ttu-id="b9b52-122">Создать кластер, даже если он уже существует</span><span class="sxs-lookup"><span data-stu-id="b9b52-122">Create cluster even if it already exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b52-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="b9b52-123">-KubernetesVersion</span></span>
<span data-ttu-id="b9b52-124">Версия Kubernetes, используемая для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="b9b52-124">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b52-125">-Location</span><span class="sxs-lookup"><span data-stu-id="b9b52-125">-Location</span></span>
<span data-ttu-id="b9b52-126">Расположение Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="b9b52-126">Azure location for the cluster.</span></span>
<span data-ttu-id="b9b52-127">По умолчанию — расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b9b52-127">Defaults to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b52-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b9b52-128">-Name</span></span>
<span data-ttu-id="b9b52-129">Имя управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="b9b52-129">Kubernetes managed cluster Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b52-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="b9b52-130">-NodeCount</span></span>
<span data-ttu-id="b9b52-131">Количество узлов, используемое по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="b9b52-131">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b52-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="b9b52-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="b9b52-133">Количество узлов, используемое по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="b9b52-133">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b52-134">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="b9b52-134">-NodeVmSize</span></span>
<span data-ttu-id="b9b52-135">Размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b9b52-135">The size of the Virtual Machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b52-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9b52-136">-ResourceGroupName</span></span>
<span data-ttu-id="b9b52-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b9b52-137">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b52-138">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="b9b52-138">-SshKeyValue</span></span>
<span data-ttu-id="b9b52-139">Значение файла ключа SSH или путь к файлу ключа.</span><span class="sxs-lookup"><span data-stu-id="b9b52-139">SSH key file value or key file path.</span></span>
<span data-ttu-id="b9b52-140">По умолчанию: {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="b9b52-140">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b52-141">-Тег</span><span class="sxs-lookup"><span data-stu-id="b9b52-141">-Tag</span></span>
<span data-ttu-id="b9b52-142">Теги, применяемые к ресурсу</span><span class="sxs-lookup"><span data-stu-id="b9b52-142">Tags to be applied to the resource</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b52-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9b52-143">-Confirm</span></span>
<span data-ttu-id="b9b52-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b9b52-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b52-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9b52-145">-WhatIf</span></span>
<span data-ttu-id="b9b52-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b9b52-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9b52-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b9b52-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b52-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9b52-148">CommonParameters</span></span>
<span data-ttu-id="b9b52-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9b52-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9b52-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9b52-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9b52-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9b52-151">INPUTS</span></span>

### <span data-ttu-id="b9b52-152">Ничего</span><span class="sxs-lookup"><span data-stu-id="b9b52-152">None</span></span>

## <span data-ttu-id="b9b52-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9b52-153">OUTPUTS</span></span>

### <span data-ttu-id="b9b52-154">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="b9b52-154">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="b9b52-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9b52-155">NOTES</span></span>

## <span data-ttu-id="b9b52-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9b52-156">RELATED LINKS</span></span>
