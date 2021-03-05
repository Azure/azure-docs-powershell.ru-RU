---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
ms.openlocfilehash: 8cdc8e49a78c4f2c2bfb88d42fe710ad783df97f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988644"
---
# <span data-ttu-id="0b330-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="0b330-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="0b330-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b330-102">SYNOPSIS</span></span>
<span data-ttu-id="0b330-103">Создание и обновление закрытого облака</span><span class="sxs-lookup"><span data-stu-id="0b330-103">Create or update a private cloud</span></span>

## <span data-ttu-id="0b330-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0b330-104">SYNTAX</span></span>

```
New-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>] [-AcceptEULA]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0b330-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b330-105">DESCRIPTION</span></span>
<span data-ttu-id="0b330-106">Создание и обновление закрытого облака</span><span class="sxs-lookup"><span data-stu-id="0b330-106">Create or update a private cloud</span></span>

## <span data-ttu-id="0b330-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0b330-107">EXAMPLES</span></span>

### <span data-ttu-id="0b330-108">Пример 1. Создание закрытого облака</span><span class="sxs-lookup"><span data-stu-id="0b330-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="0b330-109">Создание закрытого облака</span><span class="sxs-lookup"><span data-stu-id="0b330-109">Create private cloud</span></span>

## <span data-ttu-id="0b330-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b330-110">PARAMETERS</span></span>

### <span data-ttu-id="0b330-111">-AcceptEULA</span><span class="sxs-lookup"><span data-stu-id="0b330-111">-AcceptEULA</span></span>
<span data-ttu-id="0b330-112">Примите условия соглашения EULA о AVS, юридический термин будет всплывать, если этот параметр не предоставлен</span><span class="sxs-lookup"><span data-stu-id="0b330-112">Accept EULA of AVS, legal term will pop up without this parameter provided</span></span>

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

### <span data-ttu-id="0b330-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b330-113">-AsJob</span></span>
<span data-ttu-id="0b330-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="0b330-114">Run the command as a job</span></span>

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

### <span data-ttu-id="0b330-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b330-115">-DefaultProfile</span></span>
<span data-ttu-id="0b330-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0b330-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b330-117">-Интернет</span><span class="sxs-lookup"><span data-stu-id="0b330-117">-Internet</span></span>
<span data-ttu-id="0b330-118">Подключение к Интернету включено или отключено</span><span class="sxs-lookup"><span data-stu-id="0b330-118">Connectivity to internet is enabled or disabled</span></span>

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

### <span data-ttu-id="0b330-119">-Location</span><span class="sxs-lookup"><span data-stu-id="0b330-119">-Location</span></span>
<span data-ttu-id="0b330-120">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="0b330-120">Resource location</span></span>

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

### <span data-ttu-id="0b330-121">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="0b330-121">-ManagementClusterSize</span></span>
<span data-ttu-id="0b330-122">Размер кластера</span><span class="sxs-lookup"><span data-stu-id="0b330-122">The cluster size</span></span>

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

### <span data-ttu-id="0b330-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0b330-123">-Name</span></span>
<span data-ttu-id="0b330-124">Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="0b330-124">Name of the private cloud</span></span>

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

### <span data-ttu-id="0b330-125">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="0b330-125">-NetworkBlock</span></span>
<span data-ttu-id="0b330-126">Блок адресов должен быть уникальным как для VNet, так и для локальной службы.</span><span class="sxs-lookup"><span data-stu-id="0b330-126">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="0b330-127">Убедитесь, что формат CIDR соответствует формату (A.B.C.D/X), где A,B,C,D находятся от 0 до 255, а X — от 0 до 22</span><span class="sxs-lookup"><span data-stu-id="0b330-127">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="0b330-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0b330-128">-NoWait</span></span>
<span data-ttu-id="0b330-129">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="0b330-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0b330-130">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="0b330-130">-NsxtPassword</span></span>
<span data-ttu-id="0b330-131">При желании можно установить пароль диспетчера NSX-T при создания закрытого облака.</span><span class="sxs-lookup"><span data-stu-id="0b330-131">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="0b330-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b330-132">-ResourceGroupName</span></span>
<span data-ttu-id="0b330-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b330-133">The name of the resource group.</span></span>
<span data-ttu-id="0b330-134">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="0b330-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0b330-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="0b330-135">-Sku</span></span>
<span data-ttu-id="0b330-136">Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="0b330-136">The name of the SKU.</span></span>

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

### <span data-ttu-id="0b330-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b330-137">-SubscriptionId</span></span>
<span data-ttu-id="0b330-138">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="0b330-138">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0b330-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b330-139">-Tag</span></span>
<span data-ttu-id="0b330-140">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="0b330-140">Resource tags</span></span>

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

### <span data-ttu-id="0b330-141">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="0b330-141">-VcenterPassword</span></span>
<span data-ttu-id="0b330-142">При желании можно установить пароль администратора vCenter при создания закрытого облака.</span><span class="sxs-lookup"><span data-stu-id="0b330-142">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="0b330-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b330-143">-Confirm</span></span>
<span data-ttu-id="0b330-144">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0b330-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b330-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b330-145">-WhatIf</span></span>
<span data-ttu-id="0b330-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b330-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b330-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0b330-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b330-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b330-148">CommonParameters</span></span>
<span data-ttu-id="0b330-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b330-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b330-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b330-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b330-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b330-151">INPUTS</span></span>

## <span data-ttu-id="0b330-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0b330-152">OUTPUTS</span></span>

### <span data-ttu-id="0b330-153">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="0b330-153">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="0b330-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0b330-154">NOTES</span></span>

<span data-ttu-id="0b330-155">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0b330-155">ALIASES</span></span>

## <span data-ttu-id="0b330-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b330-156">RELATED LINKS</span></span>

