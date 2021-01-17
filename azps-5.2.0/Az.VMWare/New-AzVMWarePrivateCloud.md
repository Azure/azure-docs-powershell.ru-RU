---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
ms.openlocfilehash: 5dd91db9a8141bf9992da9eb364b00301036a898
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393023"
---
# <span data-ttu-id="cc163-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="cc163-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="cc163-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc163-102">SYNOPSIS</span></span>
<span data-ttu-id="cc163-103">Создание и обновление закрытого облака</span><span class="sxs-lookup"><span data-stu-id="cc163-103">Create or update a private cloud</span></span>

## <span data-ttu-id="cc163-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cc163-104">SYNTAX</span></span>

```
New-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cc163-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc163-105">DESCRIPTION</span></span>
<span data-ttu-id="cc163-106">Создание и обновление закрытого облака</span><span class="sxs-lookup"><span data-stu-id="cc163-106">Create or update a private cloud</span></span>

## <span data-ttu-id="cc163-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cc163-107">EXAMPLES</span></span>

### <span data-ttu-id="cc163-108">Пример 1. Создание закрытого облака</span><span class="sxs-lookup"><span data-stu-id="cc163-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="cc163-109">Создание закрытого облака</span><span class="sxs-lookup"><span data-stu-id="cc163-109">Create private cloud</span></span>

## <span data-ttu-id="cc163-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc163-110">PARAMETERS</span></span>

### <span data-ttu-id="cc163-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc163-111">-AsJob</span></span>
<span data-ttu-id="cc163-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="cc163-112">Run the command as a job</span></span>

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

### <span data-ttu-id="cc163-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc163-113">-DefaultProfile</span></span>
<span data-ttu-id="cc163-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc163-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc163-115">-Internet</span><span class="sxs-lookup"><span data-stu-id="cc163-115">-Internet</span></span>
<span data-ttu-id="cc163-116">Подключение к Интернету включено или отключено</span><span class="sxs-lookup"><span data-stu-id="cc163-116">Connectivity to internet is enabled or disabled</span></span>

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

### <span data-ttu-id="cc163-117">-Location</span><span class="sxs-lookup"><span data-stu-id="cc163-117">-Location</span></span>
<span data-ttu-id="cc163-118">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="cc163-118">Resource location</span></span>

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

### <span data-ttu-id="cc163-119">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="cc163-119">-ManagementClusterSize</span></span>
<span data-ttu-id="cc163-120">Размер кластера</span><span class="sxs-lookup"><span data-stu-id="cc163-120">The cluster size</span></span>

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

### <span data-ttu-id="cc163-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cc163-121">-Name</span></span>
<span data-ttu-id="cc163-122">Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="cc163-122">Name of the private cloud</span></span>

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

### <span data-ttu-id="cc163-123">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="cc163-123">-NetworkBlock</span></span>
<span data-ttu-id="cc163-124">Блок адресов должен быть уникальным для всей сети VNet в вашей подписке, а также локально.</span><span class="sxs-lookup"><span data-stu-id="cc163-124">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="cc163-125">Убедитесь, что формат CIDR соответствует формату A.B.C.D/X, где A,B,C,D находятся от 0 до 255, а X — от 0 до 22</span><span class="sxs-lookup"><span data-stu-id="cc163-125">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="cc163-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cc163-126">-NoWait</span></span>
<span data-ttu-id="cc163-127">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="cc163-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cc163-128">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="cc163-128">-NsxtPassword</span></span>
<span data-ttu-id="cc163-129">При желании можно установить пароль диспетчера NSX-T при создания закрытого облака.</span><span class="sxs-lookup"><span data-stu-id="cc163-129">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="cc163-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc163-130">-ResourceGroupName</span></span>
<span data-ttu-id="cc163-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc163-131">The name of the resource group.</span></span>
<span data-ttu-id="cc163-132">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="cc163-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cc163-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="cc163-133">-Sku</span></span>
<span data-ttu-id="cc163-134">Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="cc163-134">The name of the SKU.</span></span>

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

### <span data-ttu-id="cc163-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc163-135">-SubscriptionId</span></span>
<span data-ttu-id="cc163-136">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="cc163-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cc163-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="cc163-137">-Tag</span></span>
<span data-ttu-id="cc163-138">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="cc163-138">Resource tags</span></span>

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

### <span data-ttu-id="cc163-139">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="cc163-139">-VcenterPassword</span></span>
<span data-ttu-id="cc163-140">При желании можно установить пароль администратора vCenter при создания закрытого облака.</span><span class="sxs-lookup"><span data-stu-id="cc163-140">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="cc163-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc163-141">-Confirm</span></span>
<span data-ttu-id="cc163-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc163-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc163-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc163-143">-WhatIf</span></span>
<span data-ttu-id="cc163-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc163-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc163-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cc163-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc163-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc163-146">CommonParameters</span></span>
<span data-ttu-id="cc163-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc163-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc163-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc163-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc163-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc163-149">INPUTS</span></span>

## <span data-ttu-id="cc163-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cc163-150">OUTPUTS</span></span>

### <span data-ttu-id="cc163-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="cc163-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="cc163-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cc163-152">NOTES</span></span>

<span data-ttu-id="cc163-153">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cc163-153">ALIASES</span></span>

## <span data-ttu-id="cc163-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc163-154">RELATED LINKS</span></span>

