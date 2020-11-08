---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
ms.openlocfilehash: 5dd91db9a8141bf9992da9eb364b00301036a898
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243437"
---
# <span data-ttu-id="65205-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="65205-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="65205-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="65205-102">SYNOPSIS</span></span>
<span data-ttu-id="65205-103">Создание и обновление частного облака</span><span class="sxs-lookup"><span data-stu-id="65205-103">Create or update a private cloud</span></span>

## <span data-ttu-id="65205-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="65205-104">SYNTAX</span></span>

```
New-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="65205-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65205-105">DESCRIPTION</span></span>
<span data-ttu-id="65205-106">Создание и обновление частного облака</span><span class="sxs-lookup"><span data-stu-id="65205-106">Create or update a private cloud</span></span>

## <span data-ttu-id="65205-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="65205-107">EXAMPLES</span></span>

### <span data-ttu-id="65205-108">Пример 1: создание частного облака</span><span class="sxs-lookup"><span data-stu-id="65205-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="65205-109">Создание частного облака</span><span class="sxs-lookup"><span data-stu-id="65205-109">Create private cloud</span></span>

## <span data-ttu-id="65205-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="65205-110">PARAMETERS</span></span>

### <span data-ttu-id="65205-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65205-111">-AsJob</span></span>
<span data-ttu-id="65205-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="65205-112">Run the command as a job</span></span>

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

### <span data-ttu-id="65205-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65205-113">-DefaultProfile</span></span>
<span data-ttu-id="65205-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65205-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65205-115">-Интернет</span><span class="sxs-lookup"><span data-stu-id="65205-115">-Internet</span></span>
<span data-ttu-id="65205-116">Возможность подключения к Интернету включена или отключена</span><span class="sxs-lookup"><span data-stu-id="65205-116">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65205-117">-Location</span><span class="sxs-lookup"><span data-stu-id="65205-117">-Location</span></span>
<span data-ttu-id="65205-118">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="65205-118">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65205-119">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="65205-119">-ManagementClusterSize</span></span>
<span data-ttu-id="65205-120">Размер кластера</span><span class="sxs-lookup"><span data-stu-id="65205-120">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65205-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="65205-121">-Name</span></span>
<span data-ttu-id="65205-122">Имя частного облака</span><span class="sxs-lookup"><span data-stu-id="65205-122">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65205-123">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="65205-123">-NetworkBlock</span></span>
<span data-ttu-id="65205-124">Блок адресов должен быть уникальным в рамках виртуальной сети в рамках подписки, а также локально.</span><span class="sxs-lookup"><span data-stu-id="65205-124">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="65205-125">Убедитесь, что формат CIDR соответствует (A. B. C. D/X), где A, B, C, D — от 0 до 255, а X — между 0 и 22.</span><span class="sxs-lookup"><span data-stu-id="65205-125">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65205-126">-Wait</span><span class="sxs-lookup"><span data-stu-id="65205-126">-NoWait</span></span>
<span data-ttu-id="65205-127">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="65205-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="65205-128">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="65205-128">-NsxtPassword</span></span>
<span data-ttu-id="65205-129">При необходимости установите пароль в диспетчере NSX-T, когда вы создаете частное облако</span><span class="sxs-lookup"><span data-stu-id="65205-129">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="65205-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65205-130">-ResourceGroupName</span></span>
<span data-ttu-id="65205-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="65205-131">The name of the resource group.</span></span>
<span data-ttu-id="65205-132">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="65205-132">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65205-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="65205-133">-Sku</span></span>
<span data-ttu-id="65205-134">Название SKU.</span><span class="sxs-lookup"><span data-stu-id="65205-134">The name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65205-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65205-135">-SubscriptionId</span></span>
<span data-ttu-id="65205-136">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="65205-136">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65205-137">-Тег</span><span class="sxs-lookup"><span data-stu-id="65205-137">-Tag</span></span>
<span data-ttu-id="65205-138">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="65205-138">Resource tags</span></span>

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

### <span data-ttu-id="65205-139">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="65205-139">-VcenterPassword</span></span>
<span data-ttu-id="65205-140">При необходимости задайте пароль администратора vCenter при создании частного облака.</span><span class="sxs-lookup"><span data-stu-id="65205-140">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="65205-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65205-141">-Confirm</span></span>
<span data-ttu-id="65205-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="65205-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65205-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65205-143">-WhatIf</span></span>
<span data-ttu-id="65205-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="65205-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65205-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="65205-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65205-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65205-146">CommonParameters</span></span>
<span data-ttu-id="65205-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="65205-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65205-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65205-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65205-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="65205-149">INPUTS</span></span>

## <span data-ttu-id="65205-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="65205-150">OUTPUTS</span></span>

### <span data-ttu-id="65205-151">Microsoft. Azure. PowerShell. командлеты. VMWare. Models. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="65205-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="65205-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="65205-152">NOTES</span></span>

<span data-ttu-id="65205-153">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="65205-153">ALIASES</span></span>

## <span data-ttu-id="65205-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65205-154">RELATED LINKS</span></span>

